# Celestial Uprising &nbsp; [![bluebuild build badge](https://github.com/celestial-uprising/framework/actions/workflows/build.yml/badge.svg)](https://github.com/celestial-uprising/framework/actions/workflows/build.yml)

*Celestial Uprising's* Lalamatine *is proudly built for all, by lesbidoodles and their coven of magical rabbits*

## Spins

- *virt / headless / headless-nv / mini / mini-nv / muse / muse-nv / dev / dev-nv / gg / gg-nv / unholy / unholy-nv*

## Installation

To rebase an existing **atomic**/**ucore**/**ublue** installation to the latest build:

- First rebase to the unsigned image:

  ```bash
  sudo rpm-ostree rebase ostree-unverified-registry:ghcr.io/celestial-uprising/${IMAGE_NAME}:latest && sudo systemctl reboot
  ```
- Then rebase to the signed image:

  ```bash
  sudo rpm-ostree rebase ostree-image-signed:docker://ghcr.io/celestial-uprising/${IMAGE_NAME}:latest && sudo systemctl reboot
  ```

## Verification

These images are signed with [Sigstore](https://www.sigstore.dev/)'s [cosign](https://github.com/sigstore/cosign). You can verify the signature by downloading the `cosign.pub` file from this repo and running the following command:

```bash
cosign verify --key cosign.pub ghcr.io/celestial-uprising/framework
```
