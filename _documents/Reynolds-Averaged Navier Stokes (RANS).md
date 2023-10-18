---
tags: project/tesis
---
Se utilizan las **medias temporales** para describir la turbulencia, de esta forma:
$$u=\overline{u} + u'$$
Aplicandolo a las [[ecuaciones de Navier Stokes]] y se termina representando al efecto de los vórtices sobre el flujo media como $\overline{{u_i}'\; {u_j}'}$, al cual se lo conoce como el [[tensor de esfuerzos de Reynolds]].
	En analogía con el tensor de esfuerzos, se puede considerar al [[tensor de esfuerzos de Reynolds]] como al conformado por una parte de presión isotrópica llamada presión turbulenta, y otra parte fuera de la diagonal considerada como una viscosidad turbulenta efectiva.
>[!warning] El problema de este método es que crea términos adicionales sin tener ecuaciones adicionales, por lo que se tiene un sistema de ecuaciones incompleto. Para poder cerrar el problema se deben utilizar [[modelos de turbulencia]]

>[!success] Como las mediciones obtenidas en el [[mastil meteorológico]] son un promedio diezminutal, se utiliza este método para la simulación de [[aerogeneradores]].
