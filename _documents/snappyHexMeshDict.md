---
tags:
  - resource/openfoam
  - project/tesis
fecha: 2023-09-06
---
diccionario para [[snappyHexMesh]] de [[openfoam]]
[Guia de las distintas partes](https://www.cfdsupport.com/openfoam-training-by-cfd-support/node126.html)
- dividido en 5 secciones
	- geometry
		- definición de entidades de geometría que se van a usar para mallar
		- se puede usar un atchivo .stl  o una entidad geométrica predefinida (box, sphere, etc)
			- el archivo .stl tiene que estar en la carpeta `constant/triSurface/`
		- para definir box se define un min y un max, que son las esquinas de la caja. los generalizo como `xib_j` con `i` la dirección y `j=0`para el mín y `j=1` para el max, para referenciarlos en el [[includeSettings]].
		- 
	- castellatedMeshControls
		- definición del refinado
		- 
	- snapControls
		- definicón de snapping y parametros avanzados
	- addLayersControls
		- definicón de mallado de borde
	- meshQualityControls
		- definición de metricas de calidad de la malla