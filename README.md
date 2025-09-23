# NeuroSim

NeuroSim is a C++ OpenGL-based 3D rendering and simulation engine. It demonstrates modern rendering techniques including shadow mapping, multiple light types, material systems, and model loading using Assimp. The project is modular, with clear separation between window management, rendering, lighting, and model handling.

## Features

- **OpenGL Rendering**: Uses modern OpenGL (via GLEW and GLFW) for 3D graphics.
- **Lighting System**: Supports directional, point, and spot lights, each with shadow mapping.
- **Material System**: Easily assign different material properties to objects.
- **Model Loading**: Loads 3D models using the Assimp library. -- Update model loading to load from UI and make it as import and some default models for basic rendering.
- **Texture Mapping**: Supports multiple textures per model.
- **Camera Controls**: Fly-through camera with keyboard and mouse input.
- **Shader Management**: Modular shader class for easy GLSL management.
- **Shadow Mapping**: Directional and omnidirectional shadow mapping for realistic lighting.

## Project Structure

- `NeuroSim.cpp` - Main application entry point and render loop.
- `Shader.h/cpp` - Shader management, uniform handling, and light setup.
- `Model.h/cpp` - Model loading and rendering using Assimp.
- `Mesh.h/cpp` - Mesh abstraction for vertex/index buffers.
- `Texture.h/cpp` - Texture loading and binding.
- `Window.h/cpp` - Window and OpenGL context management.
- `DirectionalLight.h/cpp`, `PointLight.h/cpp`, `SpotLight.h/cpp` - Lighting classes.
- `Material.h/cpp` - Material property management.

## Dependencies

- [GLEW](http://glew.sourceforge.net/) (OpenGL Extension Wrangler)
- [GLFW](https://www.glfw.org/) (OpenGL window/context/input)
- [GLM](https://glm.g-truc.net/) (OpenGL Mathematics)
- [Assimp](https://www.assimp.org/) (Asset Import Library)
- [stb_image](https://github.com/nothings/stb) (Image loading)

## Building

1. **Clone the repository** and open the solution in Visual Studio 2022.
2. **Configure dependencies**:
   - Make sure the include and library directories for GLEW, GLFW, GLM, and Assimp are set in your project properties.
   - Link against the 64-bit versions of GLEW and GLFW if building for x64.
   - If you are using a Visual studio 2022 and please change the build from x64 to x86 then this should not give any glm or gl errors
3. **Build the solution**.

## Running

- Place your shader files in the `Shaders/` directory.
- Place your textures in the `Textures/` directory.
- Place your models in the `Models/` directory.
- Run the built executable. Use keyboard and mouse to control the camera.

## Controls

- **W/A/S/D**: Move camera
- **Mouse**: Look around
- **L**: Toggle spotlight

## Notes

- Ensure all required assets (shaders, textures, models) are present in their respective folders.
- If you encounter linker errors, verify that you are linking the correct architecture (x64 vs x86) for all libraries.

## License

This project is for educational and demonstration purposes.
This further will be taken to simulation engine once the physics engine is up

---
