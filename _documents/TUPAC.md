---
tags:
  - project/tesis
---

### iniciar
```shell
ssh jteich@h1.tupac.gob.ar
```

#### entrar en carpeta via Nautilus
``` shell
nautilus sftp://jteich@h1.tupac.gob.ar/nfs/home/jteich &
```

#### iniciar openfoam
```shell
cd openfoam-nix/
enable_nix
nix develop
source openfoam-OpenFOAM-v2212/etc/bashrc
```

#### correr caso en openfoam
```shell
sbatch slurm-Case
squeue #--> para ver la cola
```

#### cancelar un trabajo
```shell
scancel [nro de trabajo]
```

#### copiar
``` shell
# se usa el comando:
scp -r

# la dirección en TUPAC se escribe:
jteich@h1.tupac.gob.ar:jteich-2212/....
```