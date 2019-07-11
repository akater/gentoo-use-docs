# sys-fs/e2fsprogs

### cron
Pass the `--with-cron-dir=/etc/cron.d` option to the configure script. Install the cron job that periodically runs `e2scrub` tool on all LVM volumes that are formatted in ext2, ext3 or ext4 filesystem to perform online filesystem check and either mark them as clean and update last checked timestamp or mark them for subsequent check during next mount.

This flag can be enabled if there is a need to perform automatic filesystem check.

### fuse
Pass the `--enable-fuse2fs` option to the configure script. Build and install `fuse2fs` tool for userspace handling of ext2/3/4 filesystems. This is mostly useful for non-Linux UNIX-like OSes that don't have a native EXT filesystem support but have a FUSE support.

It is recommended to disable this flag because native Kernel ext4 handling is way more efficient than FUSE.

### nls
Pass the `--enable-nls` option to the configure script. Use gettext to translate various program messages, e.g. help texts and interactive prompts.

This flag can be safely disabled unless there is a need to display messeages in languages other than English.

### static-libs
Install statically linked libraries `*.a` (aka library archives) into the target system. If disabled these libraries will be removed from build tree before installation.

It is safe to disable the flag unless there is an explicit need for statically linked libraries, e.g. for development purposes.
