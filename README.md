## StatixOS prebuilt kernel repository for Nokia 8 (2017, Repartitioned)

## How to use?

Clone this repository in ```device/nokia/NLA-kernel```.

Drop all of these flags in BoardConfig (this is an example):

```
BOARD_KERNEL_IMAGE_NAME := Image.gz-dtb

TARGET_KERNEL_CLANG_COMPILE := true
TARGET_KERNEL_CONFIG := lineageos_NLA_defconfig
TARGET_KERNEL_SOURCE := kernel/nokia/msm8998
TARGET_KERNEL_VERSION := 4.4
```

Add this in device makefile:

```
# Kernel
PRODUCT_COPY_FILES += \
    device/nokia/NLA-kernel/kernel:kernel
```
