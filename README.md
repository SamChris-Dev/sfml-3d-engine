# **3D Graphics Engine (OpenGL/C++)**

<p align="center">
  <img src="assets/game_engine.png" alt="Game Preview" width="500" />
</p>

A modular, Object-Oriented 3D game engine built from the ground up using C++, OpenGL, FreeGLUT, and GLM. This project implements a full graphics pipeline including hierarchical modeling, custom camera controls, the Phong lighting model, and 2D texture mapping.

## **Project Structure**

* **`src/`** - Contains all the C++ source and header files, including the core Engine and GameObject classes.
* **`assets/`** - Stores assets and resources like textures (e.g., `brickjpg.jpg`).
* **`include/`** - External dependencies and header libraries, including `stb_image.h` and GLM.
* **`.vscode/`** - VS Code configuration files for compiling and debugging the project.

## **Key Features**

### Architecture
* **OOP Singleton Engine:** Wraps procedural GLUT C-callbacks into a clean C++ class.
* **Hierarchical Transform System:** Base *GameObject* class managing local space (Translation -> Rotation -> Scale).
* **Vertex Array Rendering:** High-performance drawing using *glDrawArrays* and *glDrawElements.*

### Graphics Pipeline
* **Phong Lighting Model:** Real-time calculation of Ambient, Diffuse, and Specular light components.
* **Shading Modes:** Support for both Flat and Smooth (Gouraud) shading algorithms.
* **Texture Mapping:** 2D bitmap application with *stb\_image*, supporting various filtering and wrapping modes.
* **Projection Systems:** Instant switching between Perspective (field of view) and Orthographic (parallel) views.

### Observer \& Interaction
* **Custom Camera:** Observer class utilizing *lookAt* logic for 3D navigation.
* **Input Mapping:** Integration of standard ASCII keys and Special Arrow keys for player movement.

## **Technical Stack**
* **Graphics API:** OpenGL (Compatibility Profile).
* **Windowing/Events:** FreeGLUT.
* **Mathematics:** GLM (OpenGL Mathematics).
* **Image Loading:** stb\_image header-only library.

## **How to Build and Run**

This project is configured to compile and run seamlessly in **Visual Studio Code** using the MinGW `g++` compiler on Windows.

1. Ensure you have a MinGW-w64 `g++` compiler installed.
2. Download the **GLM** headers and **FreeGLUT** headers and place them in `include/glm/` and `include/GL/` respectively, as these third-party dependencies are excluded from the repository to save space.
3. Open the project folder in Visual Studio Code.
4. Install the official Microsoft **C/C++** extension if you haven't already.
5. Press **F5** (or `Run > Start Debugging`). VS Code will automatically compile the source files using the settings defined in `.vscode/tasks.json` and launch the application.
6. The executable is built into the `build/Debug/` directory. *(Note: `freeglut.dll` must be present in the repository root for the executable to run correctly).*
