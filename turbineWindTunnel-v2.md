---
tags:
  - project/tesis
  - resource/openfoam
---
# turbineWindTunnel-v2
> - incorpora tener más de un actuador en 1 problema
> - incorpora tener más de un problema en 1 carpeta
> - incorpora python script que pueda armar los archivos del problema a partir de un archivo de configuración base

- input files
	- [[initialSetup.py]]
	- [[initialSetupPreSetted.py]]
	- [[initialSettings.py]]
- setup files outputted from input files 
	- [[fvOptions]]
	- [[includeSettings]]
	- [[problemReadme]]
	- [[problemSettings]]
	- [[snappyHexMeshDict]]
	- [[topoSetDict]]
- output folders/files
	- problem1Files/
		- *contiene todos los setup files para correr el problem1, obtenidos a partir de los input files*
	- problem1/
		- *contiene el output del problema1 corrido*
		- problemMesh/
			- *contiene el mallado del problema*
			- apartir de este directorio, se copian sus archivos al directorio caseRunned/ y se corren sucesivamente los casos de cada problema
		- caseRunned/
			- *es el directorio donde se corren propiamente dicho los casos. Al final la simulación completa, contiene los archivos del último caso corrido*
			- a partir de este directorio se exportan los datos relevantes para luego post procesar a files_Uinf*Uinf*\_TI*TI*/
		- files_Uinf*Uinf*\_TI*TI*/
			- *contiene los datos para luego post procesar de cada corrida del problema, según su velocidad de entrada y su intensidad turbulenta*
			- *contiene el includeSettings del caso, y los logs relevantes de las aplicaciones de openfoam*
		- problemReadme1
			- *README con la info básica del problema y sus casos para poder identificar rápidamente qué se corrió en el problema*