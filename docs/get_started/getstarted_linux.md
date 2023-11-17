---
    hide:
        - navigation
---

# Linux / MacOS


## 1. Prerequisite

You will need to download and install a few tools.

 - [CMake](https://cmake.org/download/){:target="_blank"}
 - [Git](https://git-scm.com/){:target="_blank"}
 - Any IDE, for example [VS Code](https://code.visualstudio.com/){:target="_blank"}

## 2. Get examples

To get started, you should clone the Ultimaille examples. Open a terminal and type the following command:

`git clone https://github.com/ultimaille/ultimaille-examples.git`

## 3. Build and run examples

In the `ultimaille-examples` directory type the following command:

`cmake -B build && cd build && make -j && examples/create_tri_mesh && graphite tri_mesh.geogram`

This command will: 

 - generate MakeFiles for your platform
 - build the `ultimaille-examples`
 - run example `create_tri_mesh`
 - open the result in graphite (don't forget to add graphite to your PATH)

That's it, you should see a simple triangular surface displayed in the Graphite viewer.

## What does the example do ?

### Git / CMake

 - Git clone is used to copy ultimaille-examples in your local computer
 - CMake configure the environment, it downloads Ultimaille library, Graphite viewer and put them at the right place in the `build` directory
 - CMake then generate Visual Studio solution and projects, which will then be used for compilation


### Code

 - The code use Ultimaille library to create a triangle surface composed by 5 points and 3 facets (3 triangles) and write the mesh in a file named `tri_mesh.geogram`
 - Then, system is called to execute Graphite viewer - which was previously automatically downloaded and unzip by CMake in the `build` directory of `ultimaille-examples` - and open the generated mesh.

!!!note 
    You can find an in-depth description of the examples in the How to section.

## What's next

Edit `create_tri_mesh.cpp` using [How to ?](../how_to/index.md) pages to experiment other features.