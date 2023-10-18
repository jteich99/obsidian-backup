---
tags:
  - project/tesis
---

# Actuador Discal Analytical
- primer desarrollo por [[sorensen-2020]], validado en [[sorensen-andersen-2020]]
 - expresiones analiticas determinan la distribución radial tanto para las componentes normales como tangenciales de la fuerza del aspa
 - Suposiciones
	 - el disco del rotor es sujeto a circulación constante corregida por los efectos de punta (tip) y raiz (root)
 - para un cierto tamaño de turbina, solo requiere de los coeficientes de potencia y de empuje como una función de la relación entre velocidad de la punta
 - al realizarse los cálculos de forma local, el modelo permite tener distribuciones no uniformes de velocidad sobre el rotor.

### Funcionamiento
1. cuando [[Uref]] no se encuentra determinada y se debe estimar, se determina la velocidad promedio sobre el rotor [[<Ud>]] y se calcula la de referencia como $$U_{ref}=\frac{2\;<U_d>}{1+\sqrt{1-C_T}}$$ como $C_T$ depende de $U_{ref}$, está cuenta se realiza de forma iterativa.
2. Se calcula la relación tip velocidad (tip speed ratio) $\lambda$ $$\lambda=\frac{\omega\;R}{U_{ref}}$$
3. como este modelo requiere las [[tip and root correction]]($\mathcal{F}_{tip}$ y $\mathcal{F}_{root}$), por lo que se calcula la circulación de referencia adimensional $q_0$ $$q_0=\frac{\sqrt{16\lambda^2{a_2}^2+8a_1C_T}-4\lambda a_2}{4a_1}$$siendo $a_1$ y $a_2$ el resultado de integrar $\mathcal{F}_{tip}$ y $\mathcal{F}_{root}$ en el aspa: $$a_1=\int_0^l \frac{{\mathcal{F}_{root}}^2{\mathcal{F}_{tip}}^2}{x} dx$$$$a_2=\int_0^l \mathcal{F}_{root}\mathcal{F}_{tip} x dx$$
4. Se calcula las fuerzas normales y tangenciales para cada nodo $i$ como: $$\Delta F_{n,i}=\rho\;q_0\;\frac{\mathcal{F}_{root}\mathcal{F}_{tip}}{x} \left( \lambda x + \frac{1}{2} q_0 \frac{\mathcal{F}_{root}\mathcal{F}_{tip}}{x} \right) {U_{\infty}}^2$$$$\Delta F_{\theta,i}=\rho\;q_0\;\frac{\mathcal{F}_{root}\mathcal{F}_{tip}}{x} \left( \lambda x + \frac{1}{2} q_0 \frac{\mathcal{F}_{root}\mathcal{F}_{tip}}{x} \right) {U_{\infty}}^2$$ siendo $U_\infty$ la velocidad aguas arriba sin perturbaciones definida con la velocidad local en el nodo ($U_{d,i}$) como: $$U_{\infty}=\frac{2U_{d,i}}{1+\sqrt{1-C_T}}$$
- [ ] [[Diferencia entre Uref, U_inf, <U_d>? no termino de entender cuales son "reales" y cuales son "auxiliares de cálculo"]] --> [[00-Dudas]] #duda 

