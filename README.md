# iDSK

## Description
iDSK is a tool to edit DSK (Amstrad CPC disk images) files from the command
line. You can add and remove files from your image, but also list BASIC and
DAMS source files (which are usually in a tokenized format, not plain ASCII).

iDSK can add and remove AMSDOS headers as needed.

## **Building iDSK**

### **from Source**
Before compiling iDSK, ensure you have the following installed:

#### **Linux (Ubuntu/Debian)**
```bash
sudo apt update && sudo apt install -y cmake make g++ git

# Clone the repository
git clone https://github.com/cpcsdk/idsk.git
cd idsk

# Create a build directory
mkdir build && cd build

# Run CMake to configure the build
cmake ..

# Compile the project
cmake --build .
```

#### **macOS**
```bash
# Assuming Homebrew is installed see https://brew.sh

# May require that you install XCode first
# xcode-select --install

brew install cmake make 

git clone https://github.com/cpcsdk/idsk.git
cd idsk

# Create a build directory
mkdir build && cd build

# Run CMake to configure the build
cmake ..

# Compile the project
cmake --build .
```

#### **Windows**
```powershell
# Requires CMake (https://cmake.org/download/) and Visual Studio 2022
# (or the Build Tools for Visual Studio) with the "Desktop development with C++" workload

git clone https://github.com/cpcsdk/idsk.git
cd idsk

# Run CMake to configure the build
cmake -S . -B build -G "Visual Studio 17 2022" -A x64

# Compile the project (output: build\Release\iDSK.exe)
cmake --build build --config Release
```

#### **Docker Image**

See https://github.com/cpcsdk/docker-amstrad-crossdev