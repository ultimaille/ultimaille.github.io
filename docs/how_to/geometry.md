# Work on geometry of primitives

We call primitives the elements that make up a mesh, such as facets, cells and lines (for a polyline). To give a few examples, in a triangular surface mesh, all facets will be triangles, in a quadrangular surface mesh, quads, and in a hexahedral volume mesh, hexahedrons.

Extracting the geometry of primitives provides access to functions for calculating some of their properties, such as the **normal** or **area** of a triangular facet.

Example of an extraction of the geometry of a tri facet:
```cpp 
{%
   include-markdown "https://raw.githubusercontent.com/ultimaille/ultimaille-examples/master/examples/primitive_geometry.cpp"
   start="// --- TRI ---"
   end="// --- END TRI ---"
   dedent=true
   comments=false
%}
```

Example of an extraction of the geometry of a quad facet:
```cpp 
{%
   include-markdown "https://raw.githubusercontent.com/ultimaille/ultimaille-examples/master/examples/primitive_geometry.cpp"
   start="// --- QUAD ---"
   end="// --- END QUAD ---"
   dedent=true
   comments=false
%}
```

Example of an extraction of the geometry of a hex cell:
```cpp 
{%
   include-markdown "https://raw.githubusercontent.com/ultimaille/ultimaille-examples/master/examples/primitive_geometry.cpp"
   start="// --- HEX ---"
   end="// --- END HEX ---"
   dedent=true
   comments=false
%}
```