---
tags: project/tesis
---
Para poder cerrar el problema de [[Reynolds-Averaged Navier Stokes (RANS)]] se debem tener ecuaciones que modelen el [[tensor de esfuerzos de Reynolds]] únicamente con valores medios de velocidad y presión.

>[!tip] La [[hipótesis de Boussinesq]] implica una relación lineal entre las componentes del [[tensor de esfuerzos de Reynolds]] y la [[tasa de deformación media]] con una [[viscosidad turbulenta]].
>Se tiene entonces $\nu_t$ en analogía con la viscosidad molecular.

Los modelos para obtener la [[viscosidad turbulenta]] pueden ser algebráicos, de una ecuación o de 2 ecuaciones, siendo estos últimos los completos.
Las 2 ecuaciones que se emplean son:
* una para la [[energía cinética turbulenta (k)]] y otra relacionada con la escala de longitud de turbulencia. Para esta última se tienen varios modelos entre ellos:
	* [[longitud de mezcla (l)]]
	* [[tasa de disipación de energía turbulenta (epsilon)]] 
	* [[tasa de disipación de energía turbulenta en energía térmica (omega)]]

>[!done] Modelo k-epsilon estándar
>![[modelo k-epsilon estándar]]

>[!done] [[modelo k-epsilon realizable]]
>![[modelo k-epsilon realizable]]

>[!done] Modelo k-espilon Wind
>![[modelo k-epsilon wind]]

>[!done] Modelo k-epsilon-fp
>![[modelo k-epsilon-fp]]