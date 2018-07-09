# app-arch/libarchive

### acl
Pass the `--enable-acl` option to the configure script. Provide an ability to store ACL permissions on files and directories that are compressed into an archive and an ability to extract them back from an archive for supported formats.

It is recommended to toggle this flag system-wide. Disabling this flag on ACL-enabled systems will lead to ACL permissions being lost after an archiving or unarchaving operations.

### bzip2
Pass the `--with-bz2lib` option to the configure script. Enable support for compressing and decompressing archives in BZip2 format.

This flag can be safely disabled.

### e2fsprogs
Export the `ac_cv_header_ext2fs_ext2_fs_h=yes` (`no` when disabled) variable for the configure script. See [Gentoo Bug 354923](https://bugs.gentoo.org/354923) for details.

This flag can be disabled to avoid dependency on `e2fsprogs`.

### expat
Pass the `--with-expat` option to the configure script. When disabled, pass `--with-xml2` option instead. An XML library is used by expat for XAR archives (eXtensible ARchive format) compression and decompression.

This flag can be safely disabled.

### iconv
Pass the `--with-iconv` option to the configure script. Enable a character set conversion support between filenames in an archive and a filesystem.

It is recommended to enable this flag. Disabling it might lead to corrupted filenames to be extracted from archives created using a different character set.

### libressl
Use a LibreSSL library instead of an OpenSSL one.

This flag should only be toggled system-wide, because only one of an OpenSSL or a LibreSSL library can be installed at the same time.

### lz4
Pass the `--with-lz4` option to the configure script. Provide an ability to compress and decompress archives in LZ4 format using a `liblz4` library.

It is safe to disable this flag.

### lzma
Pass the `--with-lzma` option to the configure script. Provide an ability to compress and decompress archives in XZ format using a `liblzma` library.

This flag can be safely disabled.

### lzo
Pass the `--with-lzo2` option to the configure script. Provide an ability to compress and decompress archives in LZO format using liblzo2.

It is safe to disable the flag.

### nettle
Pass the `--with-nettle` option to the configure script. Use a `libnettle` instead of a `libcrypto` to handle encrypted archives of supported formats, e.g. RAR, 7-Zip, ZIP.

This flag can be safely disabled.

### static-libs
Pass the `--enable-static` option to the configure script. Build and install statically linked version of a `libarchive` library.

The flag should normally be disabled unless there is an explicit need to use static library, e.g. for development purposes.

### threads
This flag doesn't change anything in the library itself. It makes sure that all dependencies are thread safe.

This flag can be disabled if there is no need to use the library in threaded applications.

### xattr
Pass the `--enable-xattr` option to the configure script. Provide an ability to store and subsequently restore extended file attributes while creating and extracting archives for supported formats.

It is recommended to toggle this flag system-wide. Disabling this flag when it is enabled for other packages might and will result in losing XATTRs while handling archives.

### zlib
Pass the `--with-zlib` option to the configure script. Provide an ability to create and extract Gzip archives using a `libz` library.

This flag can be safely disabled.