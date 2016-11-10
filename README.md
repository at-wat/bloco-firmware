# bloco-firmware
Spun out project from at-wat/yp-spur

## build
```
$ autoreconf -vfi
$ mkdir build
$ cd build
$ ../configure
$ make
```

## dependencies
* SH-2 cross compiler
```
$ cd /tmp
$ wget https://openspur.org/tools/sh-elf-4.7.1.i686.tar.bz2
$ tar xjfv sh-elf-4.7.1.i686.tar.bz2
$ sudo mv sh-elf /usr/local/
$ echo "export PATH=$PATH:/usr/local/sh-elf/bin" >> ~/.bashrc
$ exit
```
