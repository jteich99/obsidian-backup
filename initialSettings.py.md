---
tags:
  - project/tesis
---
> archivo leído por [[initialSetupPreSetted.py]] para generar los archivos del problema

### archivo base:
```python
"""
----------------------------------------
created by Juan Ignacio Teich
facultad de Ingeniería, UBA
jteich@fi.uba.ar
----------------------------------------
"""

# THIS FILE CONTAINS ALL THE VARIABLES NEEDED FOR RUNNING initalSettingsPreSetted.py

#---TOTAL PROBLEMS TO SETUP AND INITIAL NUMBER OF PROBLEM
totalProblems=
problemN1=

#---NODES AND CORES
nodes=
cores=

#---FOR EACH PROBLEM THE FOLLOWING BLOCK MUST BE COMPLETED. IMPORTANT TO CHANGE NUMBERS IN VARIABLES DEFINITION
#--- PROBLEM 1 ---------------------------------------------
#ACTUATOR DIAMETER
D1=

#DOMAIN SIZE IN DIAMETERS
Dx1=
Dy1=
Dz1=

#CELLS PER DIAMETER
c_D1=

#BOUNDARY CONDITION.
#   MUST BE SLIP OR ABL
BC1=""

#HEIGHT OF ACTUATOR NACELLE (GONDOLA EN ESPAÑOL)
#ONLY MATTERS IN ABL CONDITION
H1=

#AMOUNT OF ACTUATORS
amountActuators1=
#---SETUP OF ACTUATORS--------------------------------
#---ACTUATOR N1-------
#ACTUATOR TYPE SELECTION
#NUMBERED ij, WITH i=PROBLEM NUMBER AND j=ACTUATOR NUMBER
#TYPES SUPPORTED:
#   - actuationDiskRingsV11_calib_Source
actuatorType11=''

#x POSITION OF THE ACTUATOR IN DIAMETERS
x_act11=
#---------------------

#IF MORE THAN 1 ACTUATOR IS USED IN THE PROBLEM, THE FOLLOWING BLOCK HAS TO BE USED PER ACTUATOR N > 1
#IF ONLY 1 ACTUATOR DELETE
#---ACTUATOR N2-------
#ACTUATOR TYPE SELECTION
#NUMBERED ij, WITH i=PROBLEM NUMBER AND j=ACTUATOR NUMBER
#TYPES SUPPORTED:
#   - actuationDiskRingsV11_calib_Source
actuatorType12=''

#x AND y POSITION OF ACTUATOR IN DIAMETERS, RELATIVE TO ACTUATOR 1
x_act12=
y_act12=
#---------------------
#-----------------------------------------------------

#VELOCITY SETUP. IF MULTIPLE VELOCITIES IN PROBLEM, varU=on
varU1= '' #on/off
#IF off COMPLETE ALL VARIABLES EQUAL (ONLY Uinf WILL BE USED)
Uinf1=
Umin1=
Umax1=
Ustep1=

#TURBULENT INTESITY SETUP. IF MULTIPLE TI IN PROBLEM, varTI=on
varTI1= '' #on/off
#IF off COMPLETE ALL VARIABLES EQUAL (ONLY TI WILL BE USED)
TI1=
TImin1=
TImax1=
TIstep1=

#⨪----------------------------------------------------------
```
