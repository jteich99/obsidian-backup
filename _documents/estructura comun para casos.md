---
tags:
  - project/tesis
---
>[! hot]+ Consideraciones
> - que no se corra un python en el ./Allrun, para poder mandarlo a [[TUPAC]] con el python ya corrido
> - armar parte de postProcess para grafico de colores con [[paraview]] en modo guardar script
> - hacer que Cp y Ct se levanten de una tabla con Uref
> - el post procesado lo hago en mi computadora y no en TUPAC

>[! warning]+ Estructura
1. carpeta `baseProblem` 

- script dentro del baseProblem, que en función de la Uinf complete Cp y Ct en el `includeSettings`
	- un append al `includeSettings` generado previamente
	- también tiene que append la Uinf e IT
		- para poder configurarlo en modo steps
	 - el script en bash exporta la Uinf e IT y un script de python calcula Cp, Ct, parametros turbulentos, apendea Uinf e IT, etc...


