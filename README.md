# Learning OpenGL
> Learning OpenGL cause I'm bored.

## Links
- [OpenGL](https://learnopengl.com/)
- [C++](https://www.learncpp.com/)

## Setting up OpenGL with VScode
1. Get the GLFW precompiled binaries from [here](https://www.glfw.org/download.html).
2. Download GLAD from [here](https://glad.dav1d.de/). Steps below: 
   - Set the language to C/C++ and specification to OpenGL.
   - In API section set gl version to 3.3 or above.
   - Set profile to core and leave extensions empty.
   - Tick the *Generate a loader* option and click on *Generate*.
3. Also download a C/C++ compiler and install a C/C++ extension in VScode.
4. Create a workspace and run a simple cpp program, which would create a .vscode folder with tasks.json file.
5. Open tasks.json replace "args" with: 
    ```
    "args": [
                "-g",
                "-std=c++17",
                "-I${workspaceFolder}/include",
                "-L${workspaceFolder}/lib",
                "${workspaceFolder}/src/\\*.cpp",
                "${workspaceFolder}/src/glad.c",
                "-lglfw3dll",
                "-o",
                "${workspaceFolder}/main.exe"
            ],
    ```
6. Unzip and move the GLFW and GLAD files, your workspace would look something like this:
    ![Final Workspace](./final%20workspace.PNG)