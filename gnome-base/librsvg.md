# gnome-base/librsvg

### introspection
Pass the `--enable-introspection` option to the configure script. Generate GIR metadata `Rsvg-2.0.gir` file and generate a typelib from it during a build time to provide dynamic bindings support for languages other than C.

It is safe to disable this flag.

### tools
Pass the `--with-gtk3` option to the configure script. Build and install the `rsvg-view-3` tool - a simple GTK+ 3 application that can be used to view an SVG file.

The flag can be safely disabled.

### vala
Prepare environment for the configure script to find an appropriate version of vala files. Pass the `--enable-vala` option to the configure script. Generate the `librsvg-2.0.vapi` Vala bindings file during a build time using the GObject Introspection.

It is safe to disable this flag.
