
updated archlinuxarm kernel for the samsung xe303 chromebook aka snow, aka daisy

unlike the stock arch kernel for this device it has a fixed cmdline
and does not use a boot script or u-boot settings.

all that is required from u-boot is to load the kernel and bootm it.

## issues:

- boot up lag during xor profiling

- irq related kernel panic when opening ttySAC3

- doesn't power off, same is in 3.4

- startx doesn't allow fbdev/odroid to become drm master, but lxdm works

## known to work:

- xf86-video-fbdev

- xf86-video-armsoc-odroid tries to set an incorrect hdmi mode if
  monitor is not 720p/1080p

- wifi

- usb storage/input

