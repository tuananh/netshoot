[![Build action](https://github.com/tuananh/netshoot/actions/workflows/release.yaml/badge.svg)](https://github.com/tuananh/netshoot/actions/workflows/release.yaml)

# netshoot

Using [melange](https://github.com/chainguard-dev/melange) and [apko](https://github.com/chainguard-dev/apko) to build a Wolfi-based netshoot image, a port of [nicolaka/netshoot](https://github.com/nicolaka/netshoot).

Right now, we built lots of the packages here but eventually, I want to get them all in Wolfi.

- 1st PR: [ctop, dhcping, grpcurl, iperf, iperf3, libnet, libmnl, libpcap & libssh](https://github.com/wolfi-dev/os/pull/742)
- 2nd PR: [libnl3, fping, ethtool, iftop and tcpdump](https://github.com/wolfi-dev/os/pull/749)
- 3rd PR: [socat](https://github.com/wolfi-dev/os/pull/720)
- 4nd PR: [ipvsadm,ldns, and bird](https://github.com/wolfi-dev/os/pull/838)

List of tools available in this image

```
- bash
- bind-tools
- bird
- busybox
- calicoctl
- ctop
- curl
- dhcping
- drill
- ethtool
- file
- fping
- git
- grpcurl
- iftop
- iperf
- iperf3
- ipvsadm
- jq
- ldns
- netcat-openbsd
- nmap-nping
- nmap-scripts
- nmap
- openssh
- openssl
- py3.11-pip
- python-3.11
- socat
- speedtest-cli
- strace
- swaks
- tcpdump
- tcptraceroute
- vim
- websocat
```

## Usage

For example usage, see the [original project's README here](https://github.com/nicolaka/netshoot#readme).

## Signing

This image is signed with [cosign](https://github.com/sigstore/cosign). To verify, download cosign and run

```sh
cosign verify ghcr.io/tuananh/netshoot:latest --certificate-oidc-issuer https://token.actions.githubusercontent.com --certificate-identity https://github.com/tuananh/netshoot/.github/workflows/release.yaml@refs/heads/main
```

Output

```
Verification for ghcr.io/tuananh/netshoot:latest --
The following checks were performed on each of these signatures:
  - The cosign claims were validated
  - Existence of the claims in the transparency log was verified offline
  - The code-signing certificate was verified using trusted certificate authority certificates
```
## License

MIT License

Copyright (c) 2023 Tuan Anh Tran <me@tuananh.org>

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
