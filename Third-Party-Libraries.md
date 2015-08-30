# Thrid-party libraries used in Windows prebuilt binaries

## Botan
You can download pre-compiled `botan` libraries linked in Windows builds [here] (http://file.librehat.com/botan/). Note: they're statically linked. The filename indicates build information.

## Qt
For Windows builds, self-compiled statically linked Qt libraries are used. Because they're directly compiled from Qt source without any source modifications, you can compile it yourself using Qt's source code.

## libQtShadowsocks
See my [libQtShadowsocks](https://github.com/librehat/libQtShadowsocks) project.

## zbar
Pre-compiled statically linked libraries are provided in `3rdparty` directory. You can get my modified source code [here](http://file.librehat.com/).

## qrencode
You can download the source code from [their website](https://fukuchi.org/works/qrencode/) and compile it yourself. The compiling process based on MSYS/MinGW is listed below.

```
tar xf qrencode-3.4.4.tar.gz
cd qrencode-3.4.4
mkdir build && cd build
../configure --prefix=$HOME/qrencode --enable-static=yes --enable-shared=no --disable-rpath --disable-sdltest --with-tools=no
make -j4
make install
```