# mate-ocrshot
(MATE) Copy &amp; paste text from videos &amp; photos by screenshotting

## Description
Simple bash script that allows you to copy-and-paste text via Optical Character Recognition

IMO, this is useful for copying-and-pasting text from videos or photos, as well as from Google Docs et al services which go through great lengths to prevent ctrl+c ctrl+v

Also IMO, it's most useful when tied to a quick&easy keyboard shortcut

## Usage
After calling 'ocrshot', your cursor will be used to select an area of your screen to screenshot

After this screenshot is taken, it's run through Tesseract to read the text inside it

And that text, finally, is copied to your clipboard (ctrl+v to paste)


Calling 'ocrshot -i' will do the same thing but also invert the colors of the screenshot before pushing it to Tesseract. The -i option is best if you use a dark theme (a dark background with light text should be inverted to a light background with dark text for Tesseract)


## Depends on
 - mate-screenshot (Mate desktop) [If using something else, just replace the "mate-screenshot -a -c" in the shell script with whatever is equivalent for you]

 - xclip

 - tesseract

 - imagemagick [If running ocrshot -i]
