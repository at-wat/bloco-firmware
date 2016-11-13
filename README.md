# bloco-firmware
B-Loco motor controller board firmware for YP-Spur. (B-Loco has been almost obsolete.)

This project was split from YP-Spur.

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

* SH-2 programmer
```
$ wget https://openspur.org/tools/sh7045writer-1.0.3.tar.gz
$ tar xzfv sh7045writer-1.0.3.tar.gz
$ cd sh7045writer-1.0.3
$ ./configure
$ make
$ sudo make install
```

## program

1. Connect board by using RS-232c port
2. Set board into boot mode (short boot jumper)
3. Write new firmware
```
    $ cd (ypspur build directory)
    $ sh7045writer --port=/dev/ttyUSB0 target-sh/sh-vel.mot
```
