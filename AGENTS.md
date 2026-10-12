# AGENTS.md - device/xiaomi/mi7150-mainline

Agents must read this file before touching anything in this repository.

Part of the mainline repository set. Map of all repos: `vendor/mainline/docs/REPOSITORIES.md`.

Family tree for Xiaomi SM7150 devices (`davinci_mainline`). Layer:
`mainline/common` -> `mainline/qcom-common` -> this tree -> device
directory.

## Read first

| Task | Read |
|------|------|
| Anything about bringup, kernel, boot, init, SELinux | `device/mainline/common/docs/README.md` |
| Commits, style, review | `hardware/mainline/common/docs/` |
| Qualcomm layers | `device/mainline/qcom-common/docs/NEW_DEVICE.md` |

## Hard rules

- No Android build, flashing or test without asking the human first
  (`hardware/mainline/common/docs/WORKFLOW.md`).
- Do not search from the AOSP tree root; use precise directories.
- Keep device specific values here. Things that apply to more devices
  belong in the common trees (ask first).
- Do not copy the shared kernel patch table into the README; link to
  `device/mainline/common/docs/KERNEL_PATCHES.md`.
- Do not add firmware or proprietary files.
