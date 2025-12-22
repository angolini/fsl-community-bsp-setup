# fsl-community-bsp-setup


This repository contains the setup scripts and configuration files to help you get started with the Freescale Community BSP for Yocto Project.

```
$ mkdir -p ~/yocto
$ cd ~/yocto
$ git clone https://git.openembedded.org/bitbake

$ ./bitbake/bin/bitbake-setup \
   --setting default top-dir-prefix ~/yocto/fslc \
   --setting default top-dir-name ~/yocto/fslc/master \
   init https://raw.githubusercontent.com/angolini/fsl-community-bsp-setup/refs/heads/master/fsl-community-bsp.conf.json

```

One option is to use a `--non-interactive` flag to avoid prompts and specify the desired distribution and machine directly in the command line, for example:

```
./bitbake/bin/bitbake-setup \
   --setting default top-dir-prefix ~/yocto/fslc \
   --setting default top-dir-name ~/yocto/fslc/master \
   init \
   --non-interactive https://raw.githubusercontent.com/angolini/fsl-community-bsp-setup/refs/heads/master/fsl-community-bsp.conf.json \
   fslc-framebuffer distro/fslc-framebuffer machine/imx8mm-lpddr4-evk
```

This will result in a directory structure similar to the following:

```

$ tree -L 4
.
├── bitbake
(...)
└── fslc
    └── master
        ├── fslc-framebuffer-master
        │   ├── build
        │   ├── config
        │   └── layers
        └── site.conf

```


To run builds, source the environment using
    . ~/yocto/fslc/master/fslc-framebuffer-master/build/init-build-env
