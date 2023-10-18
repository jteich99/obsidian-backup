---
tags:
  - project/tesis
---

 - primera introducción en [[sorensen-myken-1992]] y [[sorensen-kock-1995]]
 - requiere de mucha información del perfil de las aspas de la turbina, los cuales no suelen ser provistos por los fabricantes

#### Funcionamiento
 1. se debe obtener el régimen de operación general de la turbina, el cuál está relacionado con la velocidad de referencia [[Uref]]
 2. Sabiendo [[Uref]], se obtienen Theta_p y omega de las características de la turbina
 3. Cuándo no se tiene la velocidad de referencia [[Uref]], se tienen 2 opciones
	 1. aplicar un controlador del torque que fije la velocidad de la turbina
	 2. una tabla de calibración con la relazción entre la velocidad sobre el disco [[<Ud>]] y [[Uref]]
 4. Determinado el régimen de operación, se determina [[Urel]] $$U_{rel}=\sqrt{{U_n}^2+(U_{\theta}-\omega\cdot r})^2$$donde $U_n$ es la velocidad local normal y $U_{\theta}$ es la velocidad tangencial local. 
	 El angulo entre [[Urel]] y el plano del rotor se calcula como $$\Phi=\arctan\left[{\frac{U_n}{U_{theta}-\omega\cdot r}}\right]$$
 5. El ángulo local de ataque se determina como $\alpha=\Phi-\beta$ , donde $\beta$ es la suma entre el ángulo del flujo $\Theta_p$ y el "twist" del ala en la posición local radial $r$.
 6. Se determinan las fuerzas por unidad de area como $$\Delta F_L=\frac{1}{2}\rho{U_{rel}}^2\frac{B\;c}{2\pi\;r} \mathcal{F}_{tip} C_L e_L$$ $$\Delta F_D=\frac{1}{2}\rho{U_{rel}}^2\frac{B\;c}{2\pi\;r} \mathcal{F}_{tip} C_D e_D$$ donde $e_L$ y $e_D$ son los vectores unitarios de lift y drag, $B$ es el número de aspas (3) y $\mathcal{F}_{tip}$ y $\mathcal{F}_{root}$ son las [[tip and root correction]].
 7. Las componentes normales y tangenciales por unidad de área se obtienen como $$\Delta F_n=\Delta F_L\; \cos\Phi + \Delta F_D\; \sin\Phi$$ $$\Delta F_\theta=\Delta F_L\; \sin\Phi - \Delta F_D\; \cos\Phi$$
 