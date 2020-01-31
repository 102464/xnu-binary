# xnu_binary
#### Compiled binary of Apple XNU ARM Kernel. QEMU boot supported.

Based on darwin-on-arm's xnu kernel.<br>
Compiled using my [build script](https://gitee.com/pxesrv/xnu-buildscript)
## File description
+ mach_kernel.DEBUG.armpba8: DEBUG version of kernel file for RealView
+ mach_kernel.DEVELOPMENT.armpba8: DEVELOPMENT version of kernel file for RealView
+ mach_kernel.RELEASE.armpba8: RELEASE version of kernel file for RealView
+ uImage_xnu_DEBUG_RealView: DEBUG version of kernel image for RealView, can boot on qemu
+ uImage_xnu_DEVELOPMENT_RealView: DEVELOPMENT version of kernel image for RealView, can boot on qemu
+ uImage_xnu_RELEASE_RealView: RELEASE version of kernel image for RealView, can boot on qemu
## Booting on QEMU
qemu-system-arm -machine realview-pb-a8 -m 512 -kernel uImage_xnu_DEBUG_RealView -append "rd=md0 debug=0x16e serial=3 -v symbolicate_panics=1" -serial stdio
## Image preview
![Image Preview](https://gitee.com/pxesrv/xnu-binary/raw/master/XNU.PNG)
