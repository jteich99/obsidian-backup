---
tags:
  - resource/openfoam
---
[[postProcessing]]
La estructura que estoy usando es:
```c++
surfaces
{
    type            surfaces;
    libs            (sampling);
    writeControl    writeTime;

    surfaceFormat   vtk;
    fields          (mag(U));

    // interpolationScheme cellPoint;  //<- default

    surfaces
    {
        zNormal
        {
            type            cuttingPlane;
            planeType       pointAndNormal;
            pointAndNormalDict
            {
                point   (0 0 450);
                normal  (0 0 1);
            }
            interpolate     true;
        }
    }
}
```
Links:
- [PPT de Chalmers University](https://www.tfd.chalmers.se/~hani/kurser/OS_CFD_2020/lectureNotes/05_someUtilitiesAndFunctionObjects.pdf)
- [Guía de uso de openfoam.com](https://doc.openfoam.com/2306/tools/post-processing/function-objects/sampling/surfaces/)
- 