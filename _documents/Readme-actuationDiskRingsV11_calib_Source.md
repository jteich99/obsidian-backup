---
tags:
  - resource/openfoam
  - project/tesis
---

*Created by Juan Ignacio Teich*
*Facultad de Ingeniería, UBA*
jteich@fi.uba.ar
## functionality
### workflow
1. run **[[initialSetup.py]]** and establish problem variables. Creates files *[[includeSettings]]* and *[[problemSettings]]*
2. run **[[RunFull.sh]]**. It works in the following way:
    1. run **[[RunFullMesh.sh]]**.
        1. source *[[problemSettings]]* and create dir *problem$problemNumber*
        2. create dir *[[problemMesh]]*
        3. copy from baseProblem dir all files
        4. establish BC, copying the corresponding 0 directory
        5. run **[[AllrunMeshParallel]]**
            1. run *blockMesh*
            2. run *decomposePar*
            3. run *snappyHexMesh*
            4. run *reconstructParMesh* & *reconstructPar*
            5. check mesh
        6. remove *processor\** folders
    2. run **[[RunFullCase.sh]]**
        1. source *[[problemSettings]]* and make dir *caseRunned* (in this dir the cases will be run, and then exported)
        2. check if multiple velocities are used. If yes --> enter for, if not go on.
        3. check if multiple turbulent intensities are used. If yes --> enter for, if not go on.
        4. run **[[RunCase.sh]]**
            1. clean *caseRunned* dir and copy *problemMesh* dir contents to *caseRunned*
            2. export variables for python to READ
            3. run python3 script **[[calculatedSetup.py]]**
            3. clean logs
            4. run **[[AllrunCaseParallel]]**
                1. run *decomposePar*
                2. run *topoSet*
                3. run *application*
                4. run *reconstructParMesh* & *reconstructPar*
                5. remove *processor\** folders
            5. run *postProcess* utility
            6. make dir with name according to $Uinf and $TI and copy logs and postProcess files
            7. rename postProcess files to have Uinf, TI and cells per diameter in their name

## files
### initalSetup.py
 - asks the user for the problem conditions and creates files **includeSettings** and **problemSettings**

### baseProblem/includeSettings
  - created by **initialSetup.py**
  - completed by **calculatedSetup.py**
  - read by **openfoam** dictionaries

### problemSettings
  - created by **initialSetup.py**
  - read by **RunFullMesh.sh**, **RunFullCase.sh**, **calculatedSetup**
  - contains the variables needed outside of openfoam
   - problemNumber, BoundaryCond, Umin, Umax, Ustep, TImin, TImax, TIstep
   - nodes, cores

## folders
### baseProblem
 - folder with baseProblem files, from which Run*\*.sh grabs files and creates problem* directory
#### 0.org.ABL/
  - folder with initial conditions if logarithmic profile is chosen as border condition

#### 0.org.SLIP/
  - folder with initial conditions if uniform profile is chosen as border condition
