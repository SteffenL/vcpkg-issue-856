## Building

### Dependencies

```
git submodule update --init
pushd external\vcpkg
powershell -ExecutionPolicy Bypass -File .\scripts\bootstrap.ps1
.\vcpkg.exe install qt5
popd
```

### Main application

```
mkdir build
cd build
cmake -G "Visual Studio 15 2017" -DCMAKE_TOOLCHAIN_FILE=external/vcpkg/scripts/buildsystems/vcpkg.cmake ..
cmake --build .
```
