## qemu-user-static ##

Link:	 [qemu-bsd-user repository](https://github.com/qemu-bsd-user/qemu-bsd-user)  

Contact: Emulation Team <emulation@FreeBSD.org>  

emulators/qemu-user-static enables user-mode emulation of other architectures
with the QEMU emulator.  User-mode emulation is the mechanism used by poudriere
to cross-build ports for other architectures.  qemu-user-static is currently
used by the official package building infrastructure to provide packages for
armv6, armv7, mips, and mips64.

Since the previous quarter, the qemu-bsd-user part of the qemu-user-static
project has undergone reorganization.  The repository hosting the bsd-user work
branch has moved to an independant account not tied to any single maintainer,
and emulation@FreeBSD.org has taken maintainership of the ports.

emulators/qemu-user-static-devel has been created as a preview of the port with
local modifications rebased forward to QEMU 3.1, as opposed to QEMU 2.11.  This
is a part of a larger effort to get FreeBSD's local modifications rebased up to
modern QEMU and eventually merged back into mainline.  Testing is both welcome
and appreciated of this new port, and please send any feedback to
emulation@FreeBSD.org.

Future plans are to continue the rebase forward to modern-day QEMU, and
deprecate the emulators/qemu-sbruno master port in favor of a single port that
builds and installs qemu-user-static binaries.  Users requiring full-system
emulation with QEMU should consider using emulators/qemu instead.
