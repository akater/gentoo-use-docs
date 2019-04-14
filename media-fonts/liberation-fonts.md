# media-fonts/liberation-fonts

### fontforge
Use the Fontforge to build fonts from source instead of using prebuilt ones.

This flag should normally be disabled.

### X
Generate and install various files needed by the X Server to properly handle the font: `fonts.dir` - list of fonts in the directory and files they are stored in, `fonts.scale` - list of scalable fonts in the directory, `encodings.dir` - list of known encodings and the files they are stored in.

This flag should be enable if there is a need to use the font for the X Server.
