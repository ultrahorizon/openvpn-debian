# UH VPN Server Core

- This is a fork of [OpenVPN (Debian)](https://salsa.debian.org/debian/openvpn) - a secure tunneling daemon.
- This fork contains modifications to OpenVPN that assist with evading detection in DPI censored networks.
- This repository is a direct representation of the openvpn package available from the [Ultra Horizon PPA](https://launchpad.net/~ultrahorizon/+archive/ubuntu/ppa).

### Install via apt

```bash
sudo add-apt-repository ppa:ultrahorizon/ppa
sudo apt-get update
sudo apt-get install openvpn
```

### Build & Install Locally

Ensure the following build tools are installed:
`autoconf`, `automake` and `libtool`

Ensure the following library dependencies are met:
`openssl`, `libssl-dev`, `liblz4-1`, `liblz4-dev`, `liblzo2-2`, `liblzo2-dev`, `libpam0g`, `libpam0g-dev`

Build OpenVPN:
```bash
autoreconf -vi
./configure
make
make install
```

Check Installation:
```bash
make check
```

**It is crucial that `make check` is executed in order to verify that the underlying cryptographic operations of OpenVPN are sound.**

### Contributions

To make contributions:

1. Fork the repo
2. Make changes to your local repo
3. Create a PR back to the master branch of this repo for review.

