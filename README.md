# Giuroll-Desync-Detector
Interfaces with Giruoll to display whether the game is desynced or not.

# Build
Requires CMake, git and the Visual Studio Compiler (MSVC).
Both git and CMake must be in the PATH environment variable.

All commands are to be run in `x86 Native Tools Command Prompt for VS 20XX`, unless stated otherwise.

## Initialization
1. Change directory to desired location. In this example it will be `C:\Users\_Kookie\SokuProjects`.

```cd C:\Users\_Kookie\SokuProjects```

2. Clone the repo and initialize.
```
git clone https://github.com/kookie2332/Giuroll-Desync-Detector.git
cd Giuroll-Desync-Detector
git submodule init
git submodule update
mkdir build
cd build
cmake .. -G "NMake Makefiles" -DCMAKE_BUILD_TYPE=Debug
```
To build in Release, replace `-DCMAKE_BUILD_TYPE=Debug` with `-DCMAKE_BUILD_TYPE=Release`.

## Compiling
1. Go to the build directory (if you did the previous step you're already inside)

```cd C:\Users\_Kookie\SokuProjects\Giuroll-Desync-Detector\build```

2. Invoke the compiler by running 

```cmake --build . --target giuroll_desync_detector```

3. The file `giuroll_desync_detector.dll` will appear inside the build folder.
4. To test the mod, you can add 

```Giuroll_Desync_Detector=C:/Users/_Kookie/SokuProjects/Giuroll-Desync-Detector/build/giuroll_desync_detector.dll``` 

on a new line in your `SWRSToys.ini` file.
