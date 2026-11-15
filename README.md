# Vendor — Xiaomi Redmi 4X (santoni)

Vendor proprietary blobs for keepQASSA Sisu (Android 10) on Xiaomi Redmi 4X (santoni).

## Branch `qassa-ubuntu`

This branch targets the **Headless Ubuntu 22.04 (santoni)** project — the
Ubuntu userspace that boots on top of the prebuilt Luuvy-C.4.0 kernel.

It is based on `10.0` and carries no blob changes of its own. It exists so the
device tree can pin a stable vendor branch instead of tracking `10.0` directly.

## Structure

```
vendor/xiaomi/santoni/
├── Android.bp            # Soong build rules for vendor libs
├── Android.mk            # Make build rules
├── BoardConfigVendor.mk  # Board-level vendor config
├── santoni-vendor.mk     # Product-level vendor packages
└── proprietary/          # Vendor binary blobs
    ├── vendor/           # /vendor partition files
    └── system/           # /system partition vendor files
```

## Usage

Clone this repo directly into `vendor/xiaomi/santoni`:

```bash
git clone -b qassa-ubuntu https://github.com/ziachi/vendor_xiaomi_santoni_qassa.git \
    vendor/xiaomi/santoni
```

Include in device tree `device.mk`:

```makefile
$(call inherit-product, vendor/xiaomi/santoni/santoni-vendor.mk)
```

## Notes

- Blobs extracted from Xiaomi Redmi 4X stock firmware
- Dolby (MotoDolbyV3) removed — vanilla audio stack only

## Related Repos

| Repo | Branch | Path |
|------|--------|------|
| [santoni_qassa_ubuntu](https://github.com/ziachi/santoni_qassa_ubuntu) | `main` | `device/xiaomi/santoni` |
| [kernel_xiaomi_msm8937_qassa](https://github.com/ziachi/kernel_xiaomi_msm8937_qassa) | `qassa-ubuntu` | `kernel/xiaomi/msm8937` |

## Maintainer

**[@kalomakan](https://t.me/kalomakan) / [ziachi](https://github.com/ziachi)**
