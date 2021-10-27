# GhostScript-issue
I just make a sample image using paint.exe on Windows.
Then I convert it to a PDF with Imagemagick:

```convert input.png input.pdf```

Then I try to resize the PDF using Ghostscript:

```gs -o output.pdf -sDEVICE=pdfwrite -sPAPERSIZE=a4 -dFIXEDMEDIA -dPDFFitPage -dCompatibilityLevel=1.4 input.pdf```

But as you can see, it somehow rotates my PDF!! I don't understand why, I've tried this on a lot of PDF's and PDF books as well, they all rotate.

My GS version:
$ gs --version

9.53.3

My IM version:
$ convert --version

Version: ImageMagick 7.0.10-27 Q16 x86_64 2021-02-07 https://imagemagick.org
Copyright: © 1999-2020 ImageMagick Studio LLC
License: https://imagemagick.org/script/license.php
Features: Cipher DPC HDRI OpenMP(4.5)
Delegates (built-in): bzlib cairo djvu fftw fontconfig fpx freetype gslib gvc jbig jng jp2 jpeg lcms lqr lzma pangocairo png ps raqm raw rsvg tiff webp x xml zlib

I'm using Cygwin and MinTTY to run all these commands on Windows.
But just for testing, I ran the GS command on a Linux Virtual Machine (linuxmint-20.2-mate-64bit).
sx@sx-vm:~/Documents$ gs --version
9.50

And the PDF was still rotated.
Sometimes the PDF's rotate 90 degrees and sometimes they rotate 180 degrees!!
