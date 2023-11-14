# Load / Save a mesh

## Load & Save

A mesh can be opened by using the generic function `read_by_extension` and writed using `write_by_extension`:

```cpp
{%
   include-markdown "https://raw.githubusercontent.com/ultimaille/ultimaille-examples/master/examples/open_save_mesh.cpp"
   start="// --- ? ---"
   end="// --- ? ---"
   dedent=true
   comments=false
%}
```

[Source code here](https://github.com/ultimaille/ultimaille-examples/blob/master/examples/open_save_mesh.cpp)

!!!note
    If the file fails to open, the user will be notified by an error message, for example when you try to open a non-existent file:
    Failed to open /home/tex/Projects/ultimaille-examples/build/examples/assets/unavailable_catorus.geogram

!!!warning

    If the mesh type you're trying to open is not consistent with the mesh type supplied as a parameter, you won't get any errors, but only the vertices will be loaded. For example, you're trying to load a tri surface mesh into a `Quads` structure.


## Supported file types

Ultimaille currently support reading and writing into the following file formats:

 - `.geogram` (graphite)
 - `.mesh`
 - `.vtk`
 - `.xyz`
 - `.obj`