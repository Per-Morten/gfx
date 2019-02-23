# GFX
GFX is a collection of tools developed for the course IMT2531 Graphics Programming at NTNU Gjøvik.
The tool intends to help the students in debugging their graphics applications.

## Logging utilities
GFX contains simple utilities for logging messages to terminal and also outputs information about which file, line, and function a message comes from, including its category (DEBUG, INFO, WARNING, ERROR).
Additionally, a wrapper macro for error checking of each OpenGL call is supplied, allowing the students to get feedback on where they made an erroneous call quickly.

## Introspection tools
GFX also contains some simple introspection tools, allowing students to inspect the contents of their buffers, vertex array objects, and shaders at runtime
in an in-application GUI (implemented using the excellent [Dear ImGui](https://github.com/ocornut/imgui)). Through this GUI students can also modify uniform variables in their shaders (as long as these uniforms are overridden elsewhere in the code).
The introspection tool is not written with performance in mind, but rather to put as few restrictions on the students' architectures as possible, and to allow the tools to be used in an easy plug an play manner.
A demo of the visualization tools can be seen in the animation below.
# TODO: Insert Animation

## Documentation & This Repo
GFX is header only (except for the dependency on Dear ImGui), and the main documentation is located within the header file.
I do not maintain these tools at this repository, but rather the university's internal gitlab server, this repository only acts as a mirror for the gfx header. However, if anyone wants to use these tools, and want specific functionality or finds any issues with it, you are more than welcome to report it here.
Hopefully, the documentation within gfx.h is self-explanatory, at the moment it depends on Dear ImGui and GLEW. However, I am looking into ways to allow students to use other function loaders if they so desire. Additionally, using the introspection tool requires support for OpenGL 4.1.
