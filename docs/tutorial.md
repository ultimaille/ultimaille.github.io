# Tutorial

## 1 - Generalities

### What is a mesh

### Graphite

A mesh can be visualized in a number of tools, such as meshlab. For our part, we use [Graphite](https://github.com/BrunoLevy/GraphiteThree), a lightweight yet powerful viewer that can display meshes in a variety of formats, including the geogram format.

The geogram format is interesting because it allows you to handle different types of surface or volumetric meshes and associate data with them, which we call attributes. Graphite is able to display attributes in a pleasant way.

We recommend you to download and install graphite by following the instructions on [Graphite repository](https://github.com/BrunoLevy/GraphiteThree).

For our part, we will use graphite throughout this tutorial to visualize our results. Below an overwiew of Graphite:

![Graphite screenshot](assets/graphite_screenshot.png "Graphite")

### Common practices

In this tutorial, in the interests of greater clarity, we declare the ultimaille namespace at the top of the cpp file. We encourage you to do the same with your own projects.

```cpp
using namespace UM;
```

Although unusual, for the sake of readability, we'll be using a python case as naming convention. For example:

```cpp
void my_function(int my_var) {
    ...
}
```

## 2 - Get started

### Open a surface mesh

A mesh can be opened by using the generic function `read_by_extension`:

```cpp
#include <ultimaille/all.h>

using namespace UM;

int main(int argc, char** argv) {

    // Declare a mesh with triangle surface
    Triangle& m;
    // Loading tri.geogram mesh into m
    read_by_extension("tri.geogram", m);

    std::cout 
        << "n vertices: " << m.nverts() 
        << ", n facets: " << m.nfacets() 
        << ", n corners: " << m.ncorners() << std::endl;

    return 0;
}
```

!!!warning

    If the mesh type you're trying to open is not consistent with the mesh type supplied as a parameter, you won't get any errors, but only the vertices will be loaded. For example, you're trying to load a tri surface mesh into a `Quads` structure.

### Save a mesh

A mesh can be saved by using the generic function `write_by_extension`:

```cpp
#include <ultimaille/all.h>

using namespace UM;

int main(int argc, char** argv) {

    // Declare a mesh with triangle surface
    Triangle& m;
    // Loading tri.geogram mesh into m
    read_by_extension("tri.geogram", m);

    std::cout 
        << "n vertices: " << m.nverts() 
        << ", n facets: " << m.nfacets() 
        << ", n corners: " << m.ncorners() << std::endl;

    // Save mesh
    write_by_extension(path + "/res/catorus.obj", m);

    return 0;
}
```

### Supported file types

Ultimaille currently support reading and writing into the following file formats:

 - `.geogram` (graphite)
 - `.mesh`
 - `.vtk`
 - `.xyz`
 - `.obj`