# Nextcloud Office Desktop Editors – Releases

This repository hosts the release binaries of **Nextcloud Office Desktop Editors**,
the Nextcloud-branded build of the [Euro-Office Desktop Editors](https://github.com/Euro-Office/DesktopEditors).

It contains no source code. Releases are published automatically by the CI of
[Euro-Office/DesktopEditors](https://github.com/Euro-Office/DesktopEditors) whenever a version tag is pushed there.

## Download

Get the latest version from the [Releases page](https://github.com/nextcloud-releases/Office-DesktopEditors/releases).

| Platform | Packages |
|----------|----------|
| Linux    | `.deb`, `.rpm` |
| Windows  | installer `.exe` / `.msi` |
| macOS    | `.dmg` (Apple Silicon and Intel), signed and notarized |

Releases tagged `-N` (e.g. `v9.3.4-1`) are stable. All other tags
(beta, rc, dev) are marked as pre-releases.

### Package repositories (Linux)

Stable releases are also available through our APT and DNF repositories:

**Debian / Ubuntu**

```sh
sudo install -d -m 0755 /etc/apt/keyrings
sudo curl -fsSL https://download.nextcloud.com/office/repo/nextcloud-office.asc \
  -o /etc/apt/keyrings/nextcloud-office.asc
echo "deb [signed-by=/etc/apt/keyrings/nextcloud-office.asc] https://download.nextcloud.com/office/repo/deb stable main" \
  | sudo tee /etc/apt/sources.list.d/nextcloud-office.list
sudo apt update
sudo apt install nextcloud-office-desktopeditors
```

**Fedora / RHEL / openSUSE-compatible DNF systems**

```sh
sudo tee /etc/yum.repos.d/nextcloud-office.repo <<'EOF'
[nextcloud-office]
name=Nextcloud Office
baseurl=https://download.nextcloud.com/office/repo/rpm/stable/$basearch
enabled=1
gpgcheck=1
repo_gpgcheck=1
gpgkey=https://download.nextcloud.com/office/repo/nextcloud-office.asc
EOF
sudo dnf install nextcloud-office-desktopeditors
```

Packages are available for `x86_64` and `aarch64`.

## Reporting issues

Please do not open issues here. Report bugs and feature requests in the
[Euro-Office/DesktopEditors](https://github.com/Euro-Office/DesktopEditors/issues) repository.

## License

See the [source repository](https://github.com/Euro-Office/DesktopEditors) for license information.