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

Wait ... I just discovered http://levskaya.github.io/polyhedronisme/
That does most of what I had in mind, and more.
It uses a typed recipe instead of a more GUI input approach, but that's ok.
However, it doesn't seem to implement gyro correctly ... e.g. a gyrated cube (recipe "gC") doesn't look the same in polyHédronisme as it does at https://en.wikipedia.org/wiki/Conway_polyhedron_notation#/media/File:Pentagonalicositetrahedronccw.jpg
In fact, in polyHédronisme it doesn't even look like the faces are planar.
And trying to reproduce Hart's sculpture [Roads Untaken](http://www.georgehart.com/sculpture/roads-untaken.html), [using recipe "eptI"](http://fennetic.tumblr.com/post/72960263404/roads-untaken-by-george-hart-the-shape-is-an),
we don't get anything like his sculpture.
Is this just a problem with the 'g' operator, that could be fixed with a pull request? I guess I can create a bug report for it and see if anything happens. Maybe there's some misunderstanding on my part, or an intrinsic limitation that Hart glossed over?
