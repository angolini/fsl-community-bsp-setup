# fsl-community-bsp-setup


This repository contains the setup scripts and configuration files to help you get started with the Freescale Community BSP for Yocto Project.

```
$ git clone https://git.openembedded.org/bitbake

$ ./bitbake/bin/bitbake-setup \
   --setting default top-dir-prefix ~/yocto/fslc \
   --setting default top-dir-name ~/yocto/fslc/master \
   init ~/yocto/setup-layers.conf.json

```
