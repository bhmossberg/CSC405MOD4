# CSC405 Module 4 — Textbook Example Programs

Example code from Gordon, V. S., & Clevenger, J. (2021). Computer graphics programming in OpenGL with Java (3rd ed.). Mercury Learning and Information. Used for coursework study.

Official companion files were downloaded from the author’s page,
[Computer Graphics Programming in OpenGL with Java, 3rd Edition](https://athena.ecs.csus.edu/~gordonvs/textJ3E.html)
(`J3E_CompanionFiles.zip`). Each program folder is self-contained:
its `.java` sources, `.glsl` shaders, utility classes (`Utils.java`,
`Sphere.java`, `Torus.java`, `ImportedModel.java` as needed), and any
textures or models that program loads are copied into that folder.

**Assigned reading:** Chapter 3 (entire); Chapter 4, Sections 4.1–4.5.

## Programs in this module

### Program3_1 — Building Transformation Matrices in GLSL

- **Section:** 3.10 GLSL Functions for Building Matrix Transforms
- **Source:** transcribed from the book listing (no official companion folder).
- **Note:** The official companion has no Chapter 3 program folder. Program 3.1 is a set of GLSL helper functions (buildTranslate, buildRotateX/Y/Z, buildScale), not a standalone Java application. transforms.glsl was transcribed from the book listing. Also assigned in Module 5 (Section 3.10).

### Program4_1 — Plain Red Cube (plus companion variants)

- **Section:** 4.5 Our First 3D Program — A 3D Cube (variants also illustrate 4.3 interpolation)
- **Official folder:** `Chapter_04_graphicsData/Prog4_1_cube`
- **Note:** Official companion includes four variants under Prog4_1_cube. This module includes (1) plainRedCube — the Program 4.1 listing in Section 4.5; (2) interpolatedColors — per-vertex colors, which Section 4.3 discusses and which matches the colored-cube idea used in the Module 4 assignment; (3) tumbling — a time-rotated cube, the starting point the Module 4 assignment describes. The fourth variant (multipleCubes) belongs to Section 4.6 and is in Module 3, not here.

## Assigned sections without a numbered program

- Sections 4.1–4.4 (buffers, uniforms, interpolation, model-view and perspective matrices) are demonstrated inside Program 4.1 rather than as their own numbered programs.

## Compile and run

These programs use the official companion layout: Java sources and shaders live in a `code/` package (`package code;`), and textures or `.obj` models sit in the program folder (the working directory when you run). Shaders are loaded with paths such as `code/vertShader.glsl`.

You need **JDK 11**, **JOGL 2.4** (`jogl-all.jar`, `gluegen-rt.jar`, plus the native jars for your OS), and **JOML 1.10** (`joml-1.10.0.jar`) on the classpath. The textbook’s Appendix A (Windows) and Appendix B (macOS) cover installation. On Linux, put the jars in a `lib` directory (or any folder you prefer) and run the following from a program folder, for example `Program2_5`:

```bash
# Adjust these paths to where you keep the jars
CP="lib/jogl-all.jar:lib/jogl-all-natives-linux-amd64.jar:lib/gluegen-rt.jar:lib/gluegen-rt-natives-linux-amd64.jar:lib/joml-1.10.0.jar"

# Compile (from the program folder that contains the code/ directory)
javac -cp "$CP" code/*.java

# Run (also from that program folder, so shader and texture paths resolve)
java -cp "$CP:." \
  --add-exports java.base/java.lang=ALL-UNNAMED \
  --add-exports java.desktop/sun.awt=ALL-UNNAMED \
  --add-exports java.desktop/sun.java2d=ALL-UNNAMED \
  -Dsun.java2d.d3d=false -Dsun.java2d.uiScale=1 \
  code.Code
```

On Windows, use `;` instead of `:` in the classpath, and the official `compile.bat` / `run.bat` in each folder assume the JOGL and JOML jars are already on your global `CLASSPATH` (as the book’s setup appendix describes):

```bat
javac code/Code.java
java --add-exports java.base/java.lang=ALL-UNNAMED --add-exports java.desktop/sun.awt=ALL-UNNAMED --add-exports java.desktop/sun.java2d=ALL-UNNAMED -Dsun.java2d.d3d=false -Dsun.java2d.uiScale=1 code.Code
```

Programs that open a window need a display; compiling does not.


This `textbook-examples` folder contains **21** files.
