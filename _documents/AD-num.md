---
tags:
  - project/tesis
---

 - desarrollado en [[navarro-tesis-2019]]
 - se desarrollan 2 tablas precalibradas para una amplia gama de condiciones de operación, para luego utilizar en el cálculo local de las fuerzas del rotor.

### Funcionamiento
 - en la publicación original, las fuerzas normales y tangenciales por unidad de área sin correción por tip y root se calculan como $$\Delta F_{n,i}' = \frac{1}{2} \rho C_T {U_\infty}^2$$ $$\Delta F_{\theta,i}' = \frac{\rho C_P {U_\infty}^3}{2\omega\;r}$$donde $U_\infty$ es la velocidad aguas arriba, que para casos con velocidad uniforme cumple que $U_\infty=U_{ref}$
 - para aplicar las [[tip and root correction]], pero mantener el empuje y potencia totales, se calculan las fuerzas normales y tangenciales por unidad de area escaladas de la siguiente manera: $$\Delta F_{n,i}=b_1\mathcal{F}_{tip}\mathcal{F}_{root}\Delta F_{n,i}'$$$$\Delta F_{\theta,i}=b_2\mathcal{F}_{tip}\mathcal{F}_{root}\Delta F_{\theta,i}'$$donde: $$b_1=\frac{\sum_i F_{n,i}'}{\sum_i F_{n,i}' \mathcal{F}_{tip} \mathcal{F}_{root}}$$ $$b_2=\frac{\sum_i F_{\theta,i}'}{\sum_i F_{\theta,i}' \mathcal{F}_{tip} \mathcal{F}_{root}}$$
 - Cuando no se conoce [[Uref]] (define $C_P$, $C_T$ y $\omega$), se debe estimar a partir de la velocidad promedio sobre el disco [[<Ud>]].
	 - Se realiza un proceso de calibración, donde la turbina se enfrenta a distintos casos de velocidad uniforme. Esto permite hacer una tabla relacionando [[Uref]] y [[<Ud>]], y definiendo los respectivos $C_T$ y $C_P$.
		 - Se corre la simulación a $U_\infty$=[[Uref]], imponiendo las fuerzas $\Delta F_{n,i}$ y $\Delta F_{\theta,i}$ , y se obtiene [[<Ud>]].
	 - Luego para configuración de [[Uref]] se obtiene la relación entre $U_{d,i}$ y $\Delta F_{n,i}$ y $\Delta F_{\theta,i}$ 
		 - Seteando una cierta [[Uref]], se aplican distintas $U_\infty$, dando como resultado $U_{d,i}$, $\Delta F_{n,i}$ y $\Delta F_{\theta,i}$ para cada posición discreta radial $r_i$

- [ ] [[Como se hace para aplicar las fuerzas? Y como hago para extraerlas?]] --> [[00-Dudas]] #duda 