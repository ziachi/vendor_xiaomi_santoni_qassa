# vendor_xiaomi_santoni_qassa

Proprietary vendor blobs for the Xiaomi Redmi 4X (santoni), Qualcomm MSM8937.

## Branch `qassa-ubuntu`

This branch targets the **Headless Ubuntu 22.04 (santoni)** project — the
Ubuntu userspace that boots on top of the prebuilt Luuvy-C.4.0 kernel.

It is based on `10.0` and carries no blob changes of its own. It exists so the
device tree can pin a stable vendor branch instead of tracking `10.0` directly.

## Clone path

The repository root contains a single `santoni/` directory, so clone it one
level above the device directory:

```bash
git clone -b qassa-ubuntu https://github.com/ziachi/vendor_xiaomi_santoni_qassa vendor/xiaomi
```

That yields `vendor/xiaomi/santoni/santoni-vendor.mk`, which is the path
`lunch` expects. Cloning into `vendor/xiaomi/santoni` instead produces a
doubled `vendor/xiaomi/santoni/santoni/` and `lunch` fails with
`"vendor/xiaomi/santoni/santoni-vendor.mk" does not exist`.

## Related repos

| Repo | Branch | Path |
|------|--------|------|
| [santoni_qassa_ubuntu](https://github.com/ziachi/santoni_qassa_ubuntu) | `main` | `device/xiaomi/santoni` |
| [kernel_xiaomi_msm8937_qassa](https://github.com/ziachi/kernel_xiaomi_msm8937_qassa) | `qassa-ubuntu` | `kernel/xiaomi/msm8937` |
