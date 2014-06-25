Earth Gears
===========

Something of a failed experiment. It works - it's just very difficult
to grab the spherical shape and turn the gears. I don't recommend
printing this for that reason. However, I think it's a good example of
turning your own models into gears with the excellent parts this is
derived from.

TODO: Upgrade the model to use [eccentric gears](http://www.thingiverse.com/thing:6499) so they extend out of the sphere when rotated, making them easier to grab.

The license is [CC BY-SA 3.0](http://creativecommons.org/licenses/by-sa/3.0/).


Instructions
------------

Make sure you have Tony Buser's pins - thingiverse.com/thing:10288
Greg Frost's involute gear library should be included with OpenSCAD.

The STL files take a long time to generate, because of all the
polygons. I modified the Screwless Heart Gear .scad file to accept
command line parameters telling OpenSCAD what part to generate. This
could be automated in a Makefile. To generate, I run:

    openscad -D part=X -o earthgears_X.stl earthgears.scad

where X is 1-8 for the 8 gears. For the center and pins, I run:

    openscad -D part=9 -o earthgears_center.stl earthgears.scad
    openscad -D part=10 -o earthgears_pins.stl earthgears.scad

If you want to generate a complete STL for visualization purposes, run:

    openscad -D part=11 -o earthgears_complete.stl earthgears.scad

Note these can take a LONG time to generate, and consume lots of ram
if the mesh is too big. If you have a multicore processor and ram to
spare, you can run more than one job at a time.
