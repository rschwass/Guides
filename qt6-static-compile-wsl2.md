## Get the correct files

```
git clone https://github.com/qt/qt5.git qt6
cd qt6
git checkout 6.2.4
./init-repository
```
```
sudo apt-get update
sudo apt-get install build-essential python3 bison flex gperf libnss3-dev \
libx11-dev libxext-dev libxcomposite-dev libxrender-dev libxrandr-dev \
libxcb1-dev libx11-xcb-dev libxcb-glx0-dev libxcb-keysyms1-dev \
libxcb-image0-dev libxcb-shm0-dev libxcb-icccm4-dev libxcb-sync-dev \
libxcb-xfixes0-dev libxcb-shape0-dev libxcb-randr0-dev libxcb-util-dev \
libxcb-xinerama0-dev libxkbcommon-dev libxkbcommon-x11-dev libatspi2.0-dev \
libdrm-dev libgbm-dev libegl1-mesa-dev libgles2-mesa-dev libopus-dev \
libminizip-dev libjsoncpp-dev libprotobuf-dev protobuf-compiler cmake\
clang-14 lldb-14 lld-14 libclang-14-dev llvm-14-dev

```

```
./configure -opensource -confirm-license -static -nomake tests -nomake examples \
    -skip qt3d -skip qt5compat -skip qtquick3d -skip qtwayland -skip qtquickcontrols \
    -skip qtquickcontrols2 -skip qtmultimedia -skip qtsensors -skip qtlocation \
    -skip qtnetworkauth -skip qtpositioning -skip qtdatavis3d -skip qtserialbus \
    -skip qtserialport -skip qtcharts -skip qtvirtualkeyboard -skip qtremoteobjects \
    -skip qtbluetooth -DQT_BUILD_EXAMPLES=OFF -DLLVM_INSTALL_DIR=/usr/lib/llvm-14 \
    -prefix /path/to/install/location
```

```
export PATH=/opt/qt6/bin:$PATH
export CMAKE_PREFIX_PATH=/opt/qt6/lib/cmake
cd qtwebengine
/opt/qt6/bin/qt-configure-module .

```

