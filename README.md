makefader_perl
==============

## Create an fader image animation.

        This is just a really simple script that allows quick and easy generation of images that may be used for horizontal or vertical faders in other applications, such as Audio Unit or VST plugins. We're currently using it for generating the faders to be used in our upcoming sampler sound library for Native Instruments Kontakt.</p>

It's a perl script, and it's using the ImageMagick PerlMagick library as well as the actual ImageMagick command line interface. So, it requires that you have ImageMagick and the Image::Magick.pm module for perl installed.

Once this is set up, add execution permissions to the script file, and run it like this:

```
makefader.pl inputfile outputfile stepcount direction width_or_height
```

where:

*inputfile: button source filename (this is the moving part of the fader. It should reside on your computer)
*outputfile: destination filename. Folders in path are required to exist
*stepcount: granularity of the fader movement
*direction: horizontal or vertical
*size: desired width (for horizontal fader) or height (for vertical fader) in pixel

The script will now generate an image file according to outputfile. The generated image will consist of stepcount images appended below each other with the inputfile moving a small step across the canvas, a little more for each iteration. Try it out, and you'll see :)
