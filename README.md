# zenvara-platform/apt

Official APT repository for Zenvara command-line tools, signed with the
`Zenvara Package Signing <packages@zenvara.ai>` GPG key
(fingerprint `8AB9A1A98BAF97FDCFBCCB66714C0C3ED9A43DC3`).

## Install

```sh
curl -fsSL https://zenvara-platform.github.io/apt/gpg.key | sudo gpg --dearmor -o /usr/share/keyrings/zenvara.gpg
echo "deb [signed-by=/usr/share/keyrings/zenvara.gpg] https://zenvara-platform.github.io/apt stable main" | sudo tee /etc/apt/sources.list.d/zenvara.list
sudo apt update
sudo apt install zen
```

## Packages

| Package | Description |
|---|---|
| `zen` | The Zenvara CLI — installs, runs, and operates a Zenvara instance. |

## Scope

This repository only serves the **current stable release** of each package — a
deliberate simplification (see the [zen release pipeline](https://github.com/zenvara-platform/cli-source)
docs) rather than a full versioned Debian archive. Historical versions remain
available as `.deb` downloads on each package's GitHub Releases page.

Published by the [zen release pipeline](https://github.com/zenvara-platform/cli);
do not edit `pool/`, `dists/`, or `gpg.key` by hand.
