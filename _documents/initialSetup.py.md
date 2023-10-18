---
tags:
  - project/tesis
---
> script de [[python]] para armar los archivos base para cada problema a correr en [[openfoam]]

# version 3 --> [[turbineWindTunnel-v3]]


# version 2 --> [[turbineWindTunnel-v2]]
[[initalSetup-canva.canvas|initalSetup-canva]]
 - toma archvios base para armar el fvOptions, topoSetDict y snappyHexMeshDict para cada problema
	 - copia de la carpeta fvOptions.file/ los contenidos del archivo del actuador (según que tipo se elija) y se copia al fvOptions
 - 

# version 1
### outline
1. preguntar si se quiere cambiar el archivo includeSettings
2. determinar cant de nodos y de procesadores
3. determinar nro de problema
4. determinar diametro y tamaño del dominio
5. determinar esquinas del mallado
6. determinar mallado (celdas por diametro)
7. ubicar en x la turbina
8. determinar condicion de borde de entrada
	1. poner un gradiente de mallado en z si se elije ABL
	2. determinar la altura del aactuador
9. armar puntos para la box de la estela --> snappy
10. armar puntos esquina para la box del actuadora --> topoSet
11. determinar velocidad (con o sin step)
12. determinar varias variables del fvOptions
13. determinar centro del disco
14. determinar TI