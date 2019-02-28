# ZXing C++ Port

ZXing is great at reading barcodes and QR codes. It is a library and has two console programs. Portable to Linux, Windows and MacOS. If you want a GUI, there's an example that comes with Qt.'

    ./build/Release/zxing-cv.exe
    ./build/Release/zxing.exe

## Building using CMake

    mkdir build
    cd build
	cmake .. -A x64 -DCMAKE_PREFIX_PATH=/code/opencv/build  

Linux 

    make 
	
Windows
	
	msbuild zxing.sln /property:Configuration=Release [Windows]

Or, load into VisualStudio. Built with VS 2017.

Switch between build modes by specifying:

    -DCMAKE_BUILD_TYPE=Debug or
    -DCMAKE_BUILD_TYPE=Release

## OpenCV integration

When build on a system where opencv is installed the open cv bridge classes and executable will be built too.

## History

This project forked from [ZXing-cpp](https://github.com/glassechidna/zxing-cpp) because it seems it is no longer maintained there.

[![Build Status](https://travis-ci.org/glassechidna/zxing-cpp.svg?branch=master)](https://travis-ci.org/glassechidna/zxing-cpp)

[ZXing](https://github.com/zxing/zxing) is/was a Java library.

At some point a complete C++ port/rewrite was created and maintained in the official [ZXing](https://github.com/zxing/zxing) repo. However, at the time of writing the C++ port is no longer maintained and has been removed from the official ZXing repo.

The original ZXing-cpp project was forked from the [last ZXing commit](https://github.com/zxing/zxing/commit/00f6340) to contain the C++ project, with the following exceptions

 * scons (Python) build system has been deleted.
 * Deleted black box tests, because they refer to a large test data in ZXing repo.
 * Added appropriate copyright/licensing details (based on those in the ZXing repo).
 * Updated README.md

Removal of build systems was done to minimise maintenance burden.

If tests and XCode projects (other than those produced automatically be CMake) are desired, then another repo should be created and this repo referenced as a submodule. 

-0-