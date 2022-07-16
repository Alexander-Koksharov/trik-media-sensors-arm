Preparations
============

This projects depends on trik-libcodecengine-client that is already installed
into the TRIK SDK. Unfortunately, the corresponding pkgconfig file is broken.

For your convenience there is an 'almost' fixed libcodecengine-client.pc file
located in the very same directory as this README. The only thing left for
you to do is to replace "\<YOUR TI DEPOT LOCATION\>" with the correct location
of your TI tools.

N.B.: the series of /../../.. in the beginning of variable `tidepot` must be
left as is! For example, if you put the TI bundle into the
`home/user/work/trik/from_jake/ti_tools_repo.git-bundle`
folder, the variable should look like:
`tidepot=/../../../../../../../../home/lich/work/trik/from_jake/ti_tools_repo.git-bundle`

The exact amount of '..' is not important, it should be at least 5.

Copy your libcodecengine-client.pc file into SDK:
`cp libcodecengine-client.pc /opt/trik-sdk/sysroots/arm926ejse-oe-linux-gnueabi/usr/lib/pkgconfig/libcodecengine-client.pc`

Build
=====

The project is split into two parts: `ov7670` and `webcam`.

To build the project just issue a standard sequence of commands in both
`ov7670` and `webcam` folders:
```
mkdir build
cd build
../configure --host=arm-oe-linux-gnueabi
make -j4
make install DESTDIR=`pwd`/target
```
