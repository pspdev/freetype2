# FreeType2 for PSP

Requirements (from README.git):

 - automake 1.10.1 or higher
 - libtool 2.2.4 or higher
 - autoconf 2.62 or higher

build procedure:

```shell
./autogen.sh
LDFLAGS="-L$(psp-config --pspsdk-path)/lib" LIBS="-lc -lpspuser" \
  ./configure --host psp --prefix=$(psp-config --psp-prefix)
make
make install
```
