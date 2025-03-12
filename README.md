# Draft: Measuring Network Performance in libp2p Applications

![CC0 1.0 Universal](https://img.shields.io/badge/license-CC0%201.0%20Universal-blue.svg)

## Introduction

The libp2p protocol serves as a core networking layer for decentralized systems such as IPFS, Filecoin and Ethereum. It supports a range of transports including TCP, QUIC, and WebRTC, each optimized for different use cases. While this versatility enhances resilience and adaptability, it also complicates the evaluation of performance, particularly when integrating VPN tunneling and overlay technologies designed for security and censorship resistance ([OpenVPN](https://github.com/OpenVPN/openvpn), [Wireguard](https://www.wireguard.com/), [Tor](https://github.com/thetorproject), [I2P](https://github.com/i2p/i2p.i2p), [lokinet](https://github.com/oxen-io/lokinet), [Nym](https://github.com/nymtech), [Sentinel](https://github.com/sentinel-official), [Mysterium](https://github.com/mysteriumnetwork/node), [Orchid](https://github.com/OrchidTechnologies/orchid), [HOPR](https://github.com/hoprnet/hoprnet), etc).

Similarly, tunnels and overlays operate across various layers of the network stack, each imposing distinct constraints and performance implications affecting connectivity, latency, bandwidth utilization, and peer discovery in different ways, further increasing the complexity of network behavior analysis.

This draft provides a hands-on approach to assessing how libp2p applications perform in different network conditions, with a particular focus on how they operate over VPNs.

## Methodology

### Synthetic Traffic

Since P2P applications are resource-intensive and involve multiple parallel connections with uncontrolled peers discovered dynamically, direct performance measurement of them would be too complex.

We propose synthetic testing instead using purpose-built scripts that emulate both ends of the interactions, reproducing traffic patterns as close to live applications as possible.

To ensure realism, these scripts are created by analyzing live application traffic and identifying key behavioral patterns. The goal is to replicate observed traffic characteristics while minimizing complexity for easier measurement, debugging, and evaluation.


## Authors

* Kirill Varlamov - Technical Lead, Researcher at OnGrid since 2017, ex Networking Engineer at Cisco (SP Core and Edge, Cloud). Master's Degree, MIEE.
* Dmitry Stryukovsky - Metrology Engineer, Python/Golang Developer, Science Advisor, Technical Reviewer. PhD Studies/Postgrad at MIPT.
* Dmitry Suldin - DevOps, ChainOps, Automation Engineer, Python Developer, Data Analyst.

## License

Feel free to use, remix, and share this work. It's licensed under [CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/).