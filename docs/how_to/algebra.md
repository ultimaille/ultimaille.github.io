# Use algebra

Ultimaille provides a few classes and functions for basic linear algebra.

## Vectors

In ultimaille you can define vectors of arbitrary length, but the most commonly used are 2D, 3D and 4D vectors. For this reason, ultimaille has predefined the following vector types: 

| Name | Number of dimensions |
| --- | --- |
| `vec2` | 2 |
| `vec3` | 3 |
| `vec4` | 4 |
| `vec<n>` | n |

You can perform basic operations on vectors:

| Name | Operation | Computation |
| --- | --- | --- |
| Addition | $$\vec{v} + \vec{u} $$ | $$ (v_1 + u_1, ..., v_n + u_n) $$ |
| Subtraction | $$\vec{v} - \vec{u} $$ | $$ (v_1 - u_1, ..., v_n - u_n) $$ |
| Dot product | $$\vec{v} \cdot \vec{u} $$ | $$ \sum_{i=1}^{n}  v_i * u_i $$ |

Only on `vec2` and `vec3`:

| Name | Operation | Computation |
| --- | --- | --- |
| Square norm | $$ \lVert v \rVert^2 $$ | $$ (v_x * v_x + v_y * v_y + ...) $$ |
| norm (length) | $$ \lVert v \rVert $$ | $$ \sqrt{(v_x * v_x + v_y * v_y + ...)} $$ |
| normalize | $$ \frac{\vec{v}}{\lVert v \rVert} $$ | $$ (\frac{v_x}{\lVert v \rVert}, \frac{v_y}{\lVert v \rVert}, ...) $$ |

### 2D Vector example

```cpp
{%
   include-markdown "https://raw.githubusercontent.com/ultimaille/ultimaille-examples/master/examples/algebra.cpp"
   start="// --- 2D VECTORS ---"
   end="// --- 3D VECTORS ---"
   dedent=true
   comments=false
%}
```

### 3D Vector example

```cpp
{%
   include-markdown "https://raw.githubusercontent.com/ultimaille/ultimaille-examples/master/examples/algebra.cpp"
   start="// --- 3D VECTORS ---"
   end="// --- 2x2 MAT ---"
   dedent=true
   comments=false
%}
```

## Matrices

[Coming soon]