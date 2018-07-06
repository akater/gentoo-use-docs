# sys-fs/cryptsetup
### gcrypt
Pull a [dev-libs/libgcrypt](../dev-libs/libgcrypt.md) package as a dependency. Pass the `--with-crypto_backend=gcrypt` option to the configure script. Use a libgcrypt library as an encryption and a decryption backend. A Libgcrypt built with threads can't be used while statically linking (`static` flag, see [Gentoo bug #496612](https://bugs.gentoo.org/496612)).

This flag should normally be disabled because gcrypt performs very slow (even slower than Kernel) according to benchmarks.

### kernel
Pass the `--with-crypto_backend=kernel` option to the configure script. Use Kernel routines as a cryptographic backend. This backend is very slow according to various benchmarks and usually is not recommended.

This flag should be disabled unless the target system is an embedded system and provides no userspace cryptographic libraries.

### libressl
This flag only works if an `openssl` flag is also enabled. Pass the `--with-crypto_backend=libressl` option to the configure script. Use a LibreSSL library instead of an OpenSSL as a backend for an encryption and a decryption operations. It's performance is

This flag should only ever be toggled system-wide, because a LibreSSL and an OpenSSL libraries can't be installed at the same time.

### nettle
Pass the `--with-crypto_backend=nettle` option to the configure script. Use a Nettle library as a backend for an encryption and a decryption operations. This is a fastest backend according to benchmarks. It does not support `whirlpool` hash function.

It is recommended to enable this flag due to performance benefits it brings.

### nls
Pass the `--enable-nls` option to the configure script. Enable localization support using gettext and install translation files.

This flag should be enabled if there is a need to display cryptsetup error messages or help texts in languages other than English, otherwise it is safe to disable.

### openssl
Pass the `--with-crypto_backend=openssl` option to the configure script. Use OpenSSL library as a backend for an encryption and a decryption operations.

This flag should be enabled if there is no desire to use `nettle` or there is a need to use `whirlpool` hash function.

OpenSSL performs around 20% to 40% slower than Nettle according to benchmarks.

### pwquality
Pass the `--enable-pwquality` option to the configure script. Enable a decryption passphrase complexity/quality checking using pwquality library.

It is safe to disable this flag but it can be used to improve passphrase security.

### python
Python support is disabled in the build by default using the `--disable-python` option. Enabling this flag will build and install a Python `cryptsetup` module for every supported target.

It is safe to disable this flag, unless there is a need to run Python scripts that require cryptsetup features.

### reencrypt
Pass the `--enable-cryptsetup-reencrypt` option to the configure script. Build and install a `cryptsetup-reencrypt` tool for offline LUKS device re-encryption (change encryption parameters which otherwise require full on-disk data change).

It is safe to disable this flag unless there is a need to re-encrypt LUKS devices.

### static
Pass the `--enable-static-cryptsetup` option to the configure script. Build and install statically linked binaries, e.g. a `cryptsetup`, a `veritysetup` and etc.

This flag should normally be disabled unless there is an explicit need for static binaries.

### static-libs
Pass the `--enable-static` option to the configure script. Build and install a statically linked `libcryptsetup` library.

This flag should be normally disabled unless there is an explicit requirement for a static library.

### udev
Pass the `--enable-udev` option to the configure script. Use a `libdevmapper`'s udev synchronisation to prevent DM and UDEV getting out of sync and leading to e.g. inaccessible device nodes.

It is recommended do enable this flag.

### urandom
When disabled pass the `--enable-dev-random` option to the configure script. A `/dev/random` will be used for cryptographically secure random number generation. When enabled - use a `/dev/urandom` instead.

This flag should normally be disabled unless the target system has a limited entropy, e.g. on an embedded hardware. Enabling this flag reduces an encryption security.