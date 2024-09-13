# linux-firmware-amd-ipu-staging-patch
Patch for [linux-firmware](https://gitlab.com/kernel-firmware/linux-firmware) that merges [amd-ipu-staging](https://gitlab.freedesktop.org/drm/firmware/-/tree/amd-ipu-staging) for use in the [linux-firmware-amd-staging-um5606-git AUR package](https://aur.archlinux.org/packages/linux-firmware-amd-staging-um5606-git)

How the patch is made:

1. Go into `main` branch of https://gitlab.com/kernel-firmware/linux-firmware
2. Add `drm` remote: https://gitlab.com/kernel-firmware/drm-firmware
3. `git merge drm/amd-ipu-staging`
4. Manually clean up `WHENCE` file, add and commit
5. `git log -p --reverse --binary --pretty=email --stat -m --first-parent origin/main..HEAD > amd-ipu-staging.patch`
