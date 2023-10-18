---
tags:
  - resource/python
---
> lo que quiero es que si tengo que definir una variable x y quiero que sea igual a la variable x_i con el i variando según un for, que vaya igualando x=x_1, x=x_2 a medida que se avanza en el loop

si tengo la variable `i` que define a qué variable leer:
```python
i=1
x1=100
#quiero que x=x1
x=globals()['x%s' % i]
```

si el nombre depende de varias variables:
```python
i=1, j=2
x12=100
#quiero x=x12
x=globals()['x%s' % i + '%s' % j]
```