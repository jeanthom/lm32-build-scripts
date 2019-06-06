# LM32 Build Scripts

Used to build a cross compiling toolchain for lm32 and LiteX/MiSoC development.

## Instructions

I use a GP1-L instance from [Scaleway](https://www.scaleway.com) (32 vCPUs, 128GB RAM, x86_64) running Ubuntu Xenial (16.04). You should be able to do the same on any other cloud provider or on a local computer (although I highly recommend running it at least in a VM). If you're using cheaper instances with lower vCPU count, you'll need to tweak the build script (`-j` parameter on the make command).

```
screen # in case you loose connection to your instance
wget https://raw.githubusercontent.com/jeanthom/lm32-build-scripts/master/build-lm32-toolchain.sh
chmod +x build-lm32-toolchain.sh
./build-lm32-toolchain.sh
```

At the end of the build process you should be greeted with a `lm32-toolchain.tar.gz` tarball in the `/opt` folder.
