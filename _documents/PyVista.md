---
tags:
  - resource/openfoam
  - project/tesis
---

 - Codigo para plottear .vtl visto en 2D en [[python]]
```python
import pyvista as pv

filename='zNormal.vtp'

mesh = pv.PolyData(filename)
#cpos = mesh.plot()
p = pv.Plotter()
#p.camera_position = [(0,0,900),(0, 0, 450),(0,0,1)]
p.add_mesh(mesh, scalars='U')
p.view_xy()
#p.show()
p.save_graphic('grafico.pdf')
```