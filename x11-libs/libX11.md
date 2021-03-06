# x11-libs/libX11

### doc
Pass the `--with-xmlto` and the `--enable-specs` options to the configure script. Generate and install an additional documentation into a `/usr/share/doc/libX11-<VERSION>` directory.

This flag can be safely disabled.

### ipv6
Pass the `--enable-ipv6` option to the configure script. Define an `IPv6` macro used by system include files to enable IPv6 transport protocol support for X Input Method client-server model.

This flag should be enabled if there is a need to connect to IM server over the network using an IPv6 protocol. It is mainly useful for complex languages, e.g. Japanese.

### static-libs
Remove a `-Wl,-Bdirect` option from a `CFLAGS`, `CPPFLAGS`, `CXXFLAGS`, `CCASFLAGS`, `FFLAGS`, `FCFLAGS` and an `LDFLAGS` variables and a `-Bdirect` option from a `LDFLAGS` variable for a duration of a build. Build and install a statically linked `libX11` and `libX11-xcb` libraries.

It is recommended to disable the flag, unless there is an explicit need for the static libraries.

### test
Execute a `make check` command once the main build is completed. Run a test suite provided with a source code. This will extend a build time.

This flag should normally be disabled as it is mainly useful for the Gentoo team, testers and developers.
