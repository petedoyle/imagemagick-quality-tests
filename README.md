# ImageMagick Quality Tests
This is a quick and dirty test to get a feel for file size vs. image quality for JPEG files (as output by ImageMagick 6..6.7-9).

The goal was to figure out how Google Plus has such nice images with decent file sizes.  Findings:

* Google Plus uses a quality setting of ~80 (I had been using the ImageMagick default of 92 which led to very large files.  ~4x the size of q80 but with very little difference in quality).
* Google Plus strips EXIF and color profiles on all but the largest (2048px on the longest edge) sizes.  This can lead to a ~30KB size reduction per image.

