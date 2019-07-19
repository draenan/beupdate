# beupdate - Automate freebsd-update in ZFS Boot Environments

This utility automated the use of `freebsd-update` for binary or source-based
patching in a ZFS Boot Environment.  It was created to provide the update
functionality contained in `manageBE` after I switched to `beadm`.

It was dependent on a ZFS Root file system layout where all file systems were
children of the root file system.  FreeBSD 10 changed this; The root file
system was isolated by itself, with the other ZFS file systems like "/usr"
created as direct children of the root pool and mounted off directories inside
the root file system.  I switched to this particular layout in January 2015 in
preparation for an eventual update from FreeBSD 9.3 to 10.3 that happened in
May 2016, so this script became obsolete.

