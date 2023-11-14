---
    hide:
        - navigation
---

# Getting started



## From scratch

The easiest way to create a project from scratch that use ultimaille is to copy, clone or fork [ultimaille-hello](https://github.com/ultimaille/ultimaille-hello) blank project.


Good for:

 - A basis for a project from scratch


## With examples

Another way to get started is to clone the Ultimaille examples [ultimaille-example](https://github.com/ultimaille/ultimaille-examples) to test, modify and study them.
All examples are presented in the tutorial.

Good for:

 - Study ultimaille
 - Adapt an existing example
 - Follow the tutorial


## Graphite viewer

A mesh can be visualized in a number of tools, such as meshlab. For our part, we use [Graphite](https://github.com/BrunoLevy/GraphiteThree), a lightweight yet powerful viewer that can display meshes in a variety of formats, including the geogram format.

The geogram format is interesting because it allows you to handle different types of surface or volumetric meshes and associate data with them, which we call attributes. Graphite is able to display attributes in a pleasant way.

We recommend you to download and install graphite by following the instructions on [Graphite repository](https://github.com/BrunoLevy/GraphiteThree).

For our part, we will use graphite throughout this tutorial to visualize our results. Below an overview of Graphite:

![Graphite screenshot](assets/graphite_screenshot.png "Graphite")

## Common practices

In tutorial, in the interests of greater clarity, we declare the ultimaille namespace at the top of the cpp file. We encourage you to do the same with your own projects.

```cpp
using namespace UM;
```

Although unusual, for the sake of readability, we'll be using a python case as naming convention. For example:

```cpp
void my_function(int my_var) {
    ...
}
```
____
Next: [How to ?](how_to/index.md)