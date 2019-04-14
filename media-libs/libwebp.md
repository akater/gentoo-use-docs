# media-libs/libwebp

### experimental
Pass the `--enable-experimental` option to the configure script. Enable some experimental features, including delta palettization compression mode - fastest way to decode photographic images, however it won't work for images with alpha channel and might produce some artefacts, and JPEG's YUVj natural colorspace that is currenly only used for comparison purposes.

It is safe to disable the flag.

### gif
Pass the `--enable-gif` option to the configure script. Build and install a `gif2web` tool that converts a GIF image to a WebP image.

This flag can be safely disabled.

### jpeg
Pass the `--enable-jpeg` option to the configure script. Provide an ability to compress JPEG images into the WebP format using the `cwebp` tool.

It is safe to disable the flag.

### neon
Pass the `--enable-neon` option to the configure script. Use the optimized assembly code that utilizes NEON SIMD instruction set on supported ARM platforms to accelerate encoding and decoding procedures, including colorspace conversion, chroma strong-filtering, quantization, histogram collection, etc.

This flag should be enabled on ARM platforms that support NEON SIMD instructions.

### opengl
Pass the `--enable-gl` option to the configure script. Build and install the `vwebp` tool to decompresses a WebP file and display it in a window using the OpenGL API.

It is safe to disable the flag.

### png
Pass the `--enable-png` option to the configure script. Enable support to decompress WebP images into the PNG format using the `dwebp` tool and to compress PNG images into the WebP format using the `cwebp` tool.

It is safe to dsiable the flag.

### static-libs
Pass the `--enable-static` option to the configure script. Build and install statically linked versions of the `libwebp`, `libwebpdecoder`, `libwebpmux` and the `libwebpdemux` libraries.

This flag should only be enabled if there is an explicit need for the static libraries.

### swap-16bit-csp
Pass the `--enable-swap-16bit-csp` option to the configure script. Enable byte swap for 16-bit colorspaces to convert between big endian and little endian byte order.

This flag should normally be disabled, at least on x86 architecture, but should be enabled for (rare) big-endian platforms.

### tiff
Pass the `--enable-tiff` option to the configure script. Provide an ability to compress TIFF images into the WebP format using the `cwebp` tool.

It is safe to disable the flag.
