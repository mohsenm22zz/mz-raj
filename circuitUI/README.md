# Circuit Simulator C++ Core

This directory contains the C++ core of the circuit simulator that is used by the C# WPF UI.

## Building the C++ Project

### Prerequisites
- CMake 3.10 or higher
- A C++ compiler with C++17 support (Visual Studio, GCC, Clang)

### Building on Windows

1. Run the build script:
   ```
   build.bat
   ```

   This will:
   - Create a `build` directory
   - Generate Visual Studio project files
   - Build the project in Release configuration
   - Copy the resulting `CircuitSimulator.dll` to the main directory

### Building manually with CMake

1. Create a build directory:
   ```
   mkdir build
   cd build
   ```

2. Generate build files:
   ```
   cmake .. -G "Visual Studio 17 2022"
   ```
   
   Replace "Visual Studio 17 2022" with your preferred generator.

3. Build the project:
   ```
   cmake --build . --config Release
   ```

4. Copy the resulting DLL:
   ```
   copy bin\Release\CircuitSimulator.dll ..
   ```

### Project Structure

- `include/` - Header files
- `src/` - Source files
- `CMakeLists.txt` - CMake build configuration
- `build/` - Build directory (created during build process)
- `CircuitSimulator.dll` - The compiled DLL used by the C# application

## Components

The circuit simulator includes implementations for:
- Resistors
- Capacitors
- Inductors
- Diodes (normal and Zener)
- Voltage sources (DC and AC)
- Current sources

## Analysis Types

The simulator supports:
- DC Operating Point Analysis
- Transient Analysis
- AC Sweep Analysis
- Phase Sweep Analysis