# Vendor — Xiaomi Redmi 4X (santoni)

Vendor proprietary blobs for keepQASSA Sisu (Android 10) on Xiaomi Redmi 4X (santoni).

## Structure

```
vendor/xiaomi/santoni/
└── santoni/
    ├── Android.bp          # Soong build rules for vendor libs
    ├── Android.mk          # Make build rules
    ├── BoardConfigVendor.mk # Board-level vendor config
    ├── santoni-vendor.mk   # Product-level vendor packages
    └── proprietary/        # Vendor binary blobs
        ├── vendor/         # /vendor partition files
        └── system/         # /system partition vendor files
```

## Usage

Include in device tree `device.mk`:

```makefile
$(call inherit-product, vendor/xiaomi/santoni/santoni/santoni-vendor.mk)
```

## Notes

- Blobs extracted from Xiaomi Redmi 4X stock firmware
- Dolby (MotoDolbyV3) removed — vanilla audio stack only

## Related Repos

| Repo | Branch | Description |
|------|--------|-------------|
| [device_xiaomi_santoni_qassa](https://github.com/ziachi/device_xiaomi_santoni_qassa/tree/qassa-dev) | `qassa-dev` | Device tree |
| [kernel_xiaomi_msm8937_qassa](https://github.com/ziachi/kernel_xiaomi_msm8937_qassa/tree/10) | `10` | Kernel source |

## Maintainer

**[@kalomakan](https://t.me/kalomakan) / [ziachi](https://github.com/ziachi)**
