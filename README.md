# Android device tree for Xiaomi devices with SM7150 SoC running mainline kernel

## Notes

- Some ALSA UCM profiles in `ucm2/conf.d/sm8250` are NOT installed due to incompatibility with the build system; Please install these to the device manually. Otherwise, audio will not work, and may even lead to ADSP crash.

## Before flashing the Android build

1. Erase dtbo partition: `fastboot erase dtbo`
2. Flash the appropriate U-Boot build from [here](https://github.com/sm7150-mainline/u-boot/releases) to boot partition.

## Additional repositories required to build

| Path | Source |
|------|--------|
| kernel/mainline/sm7150-mainline | https://github.com/sm7150-mainline/linux (branch: `v7.2`) |
| vendor/xiaomi/davinci | https://wiki.lineageos.org/devices/davinci/build/variant1/#extract-proprietary-blobs |

## Patches

Apply the shared patches listed in
`device/mainline/common/docs/KERNEL_PATCHES.md`.

This includes the Android platform patch for booting on v7.2+ kernels
and the `MEMFD_ASHMEM_SHIM` Kconfig edit. There are no device specific patches.
