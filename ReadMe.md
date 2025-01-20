# OpenGL Project Template

This project is a template for learning OpenGL in a Windows environment. It includes a CMake configuration, GLAD for loading OpenGL functions, and GLFW for creating windows and handling input.

## Project Structure
OpenGL_Project_Template/  
├── code/  
│   └── main.cpp  #*write your code here*  
├── Debug/  
│   └──glfw3.dll #*the dll library of GLFW*  
├── include/  
│    ├── glad/  
│    │    └── glad.c  
│    │    └── glad.h  
│    ├── GLFW/  #*this directory contains the source code of GLFW*  
│    └──KHR  
├── CMakeLists.txt  
├── license  
└── README.md


## Prerequisites

- CMake 3.10 or higher
- A C++ compiler (e.g., MSVC, GCC)
- Git (optional, for cloning repositories)
- Visual Studio or MinGW (for building GLFW)

## Setup

1. **Clone the repository:**

   ```sh
   git clone https://github.com/yourusername/OpenGL_Project_Template.git
   cd OpenGL_Project_Template
   ``` 
2. **Add CMake to your system PATH:**

    Ensure that CMake is installed and added to your system PATH. You can download CMake from [cmake.org](https://cmake.org/download/).
3. **update submodule**
    ```sh
    git submodule init
    git submodule update
    ```
    
## Building the Project
### 1.build GLFW

#### 2.Create a build directory and run CMake:
```sh
# in project's root directory
cmake .
```
#### 2.Build the project
```sh
# in project's root directory
cmake --build .
```
#### 3.Running the project
After building, you can run your exectuable by
```sh
./Debug/OpenGLProject.exe
```
## License

This project **except contents in /include directory** is licensed under the WTFPL License - see the [license](./license) file for details.