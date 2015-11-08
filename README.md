# Polyhedron operations workshop

## Status: Still in initial development

The idea here is a web-based (convex) polyhedron lab - a place to perform operations and transformations,
like truncation, cantellation, and subdivision, on polyhedra and see the results.

First, the lab allows you to load well-known polyhedra (Platonic, Archimedean, Johnson) as starting points.
They are loaded not only into graphics-oriented meshes for interactive display, but also into a richer
topological data structure that facilitates analysis and modification without breaking consistency.

Then, you can globally apply selected tools to the current polyhedron, such as truncation (hopefully
offering a variety of different strategies), rectification, cantellation, snub, subdivision, project
to sphere.

At each point you can view the results in real time, rotate them, and maybe check statistics about
the resulting polyhedron. You can undo an operation and try another in its place, or you can
apply successive operations to the results of previous ones.

Finally, the results of experimentation can be exported in a couple of useful formats for use with other
software, whether for graphical display (triangulated mesh) or more abstract computational geometry
(VRML maybe).

My motivation is to produce logistically sound, and aesthetically pleasing, topologically-spherical graphs 
for games that are traditionally planar, like [slitherlink puzzles](http://krazydad.com/slitherlink/variety.php).
But I discovered, en route to that, a need for a web-based tool for experimenting with operations on
polyhedra. There are some already, and [some of them are far more extensive](https://en.wikipedia.org/wiki/TopMod)
than what I hope to do here,
but most of them I found were either Java applets (and therefore difficult to run in modern browsers), desktop apps
(with attendant cross-platform issues), not free, limited to a single operation, or some combination of those.

This app is built on Lee Stemkowski's examples, http://stemkoski.github.io/Three.js/Topology-Data.html and
http://stemkoski.github.io/Three.js/Polyhedra.html. Those apps contain base polyhedron data, conversion of that data
to Three.js meshes for display, and topological data structures for understanding Three.js geometries.
