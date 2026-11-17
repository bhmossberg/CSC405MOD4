# CSC405MOD4

**CSC405 Computer Graphics, CSU Global (Winter 2026, Session A). Module 4: Geometric Objects and Transformations**

OpenGL Java colored cube.

## Enabling Objectives

By the end of this module, you will be able to:

1. Characterize geometric objects.
2. Describe three-dimensional primitives.
3. Create coordinate systems and frames.
4. Describe matrix and vector types.
5. Apply the computer science view.

## Readings

**Required**

- Gordon, V. S., & Clevenger, J. (2021). Computer graphics programming in OpenGL with Java (3rd ed.). Mercury Learning.
  - Chapter 3: Mathematical Foundations
  - Chapter 4
    - Section 4.1: Buffers and Vertex Attributes
    - Section 4.2: Uniform Variables
    - Section 4.3: Interpolation
    - Section 4.4: Model-View and Perspective Matrices
    - Section 4.5: Our First 3D Program - A 3D Cube

**Recommended**

- JOML Project. (2024). JOML - Java OpenGL math library. https://github.com/JOML-CI/JOML
- Scratchapixel.com. (n.d.). http://Scratchapixel.com

## Assignment: Module 4: Critical Thinking

Colored Cube (100 Points)

Read Chapter 3 (“Mathematical Foundations”) and Chapter 4, Sections 4.1–4.5 of Gordon & Clevenger (2021). Be sure you understand how vertices, vertex buffer objects, uniform variables, model-view and perspective matrices, and shaders work together to produce a 3D rendering.

Using Java with JOGL and JOML, create a program that produces a colored cube. Your vertex shader should handle the vertex positions and apply the combined model-view–projection transformation. Your fragment shader should output the per-vertex color (interpolated across the cube faces). Use the code in Section 4.5 (“Our First 3D Program—A 3D Cube”) as a starting point, then extend it so that the cube is rotated each frame by a time-dependent angle (animating around a chosen axis).

Inside your render loop, apply transformations, update uniform values, and issue draw calls. Ensure the depth test is enabled so that the cube’s faces occlude correctly.

Document the steps you took to create the colored cube. Explain the role of the VBO, uniform matrices, and the shader stages in achieving the final result. Reflect on what changed compared to your Module 2 program. The documentation should be approximately 3 paragraphs.


### Submission Guidelines

Your Java source files and GLSL shader files.

A screenshot of the working colored cube.

A Word document with your documentation and reflection.

Your paper must be formatted according to APA guidelines in the CSU Global Writing Center (available in the left-hand navigation panel).

Refer to the rubric below for more details about how you will be graded for this assignment.

