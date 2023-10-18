---
tags:
  - resource/python
---
>lo que busco es que un script de python lea un archivo y tome del mismo las variables que necesita.

#### importar todas las variables tal cual en el archivo fuente
 - el archivo "fuente" tiene que se run archivo .py, por ejemplo file.py
 ```python
 from file import *
```
- y ya se tienen todas las variables importadas nombradas de la misma manera que en file.py

#### importar algunas variables del archivo fuente
 ```python
 from file import var1, var2, ...
```

#### importar el archivo e ir llamando las variables
```python
import file
# supongamos que queremos printear a la variable var1 del archivo file.py
print(file.var1)
```