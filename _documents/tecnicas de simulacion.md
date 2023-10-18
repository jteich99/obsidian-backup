---
tags: project/tesis
---
Las técnicas de simulación se dividen en [[modelos analíticos]] y simulación de la dinámica de fluidos computacional (CFD).
>Los métodos CFD resuelven las [[ecuaciones de Navier Stokes]] de los fluidos, utilizanod un modelo para representar la interacción aerodinámica con el aerogenerador.
>Los métodos analíticos **no** resuelven la física del problema.

Se tienen 2 enfoques inicialmente para la técnica CFD:
* representando explicitamente la geomtría de las aspas en el mallado: [[full-rotor]]
* utilizando un enfoque simplificado, en el que se reemplaza el rotor por las fuerzas equivalentes aplicadas sobre el viento entrante, mediante [[actuadores]]. Se tiene:
	![[actuador lineal]]
	![[actuador de superficie]]
	![[actuador discal]]
Para [[flujos uniformes]] las diferencias entre [[full-rotor]] y [[actuador discal]] en estela lejana son bajas y no justifican el [[costo computacional]].

![[Contornos de vorticidad para full-rotor, actuador lineal y actuador discal.png]]
