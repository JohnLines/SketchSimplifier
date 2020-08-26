# SketchSimplifier
Sketch simplifier macro for FreeCAD

This macro is used to simplfy drawings imported from PDFs via

1. Import PDF (usually of an architectural or technical drawing) into Inkscape, and save as plain SVG
1. Edit (e.g. with geany) the generated SVG file and scale according to the original document - for example if it said 1:20 then multiply the numbers in the height and width by the scale factor,
1. Import SVG into FreeCAD
1. Manually remove unneeded Path Objects (in Path Workbench)
1. Select all Path Objects and use the Draft2Sketch tool to convert them to path objects, and press delete to get rid of the path objects.

At this point you will have a document with many sketches, but the straight lines in the sketches will be B-Splines

This macro finds all the sketch objects in the active document composed of Bsplines of degree 1 (straight lines) and creates new objects  with LineSegments and adds the simplified sketch objects to the SimplifiedSketches group
