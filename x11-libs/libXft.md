# x11-libs/libXft

### doc
Man pages are automatically installed with the library, so when this flag enabled no extra actions are taken. If the flag is disabled, then manual pages will be removed from the build before installing the package.

It is safe to disable the flag, because manual pages only contain development related information.

### static-libs
Remove a `-Wl,-Bdirect` option from a `CFLAGS`, `CPPFLAGS`, `CXXFLAGS`, `CCASFLAGS`, `FFLAGS`, `FCFLAGS` and an `LDFLAGS` variables and a `-Bdirect` option from a `LDFLAGS` variable for a duration of the build. Build and install a statically linked version of a `libXft` library.

This flag should only be enabled if there is an explicit need for the static library.
