# DNS over CoAP and application/dns+cbor projects

## DNS Servers and Stub Resolvers to Extend with DoC

This provides a non-exhaustive list of existing DNS servers and (stub) resolvers that have potential
to be extended with [DNS over CoAP][DoC] and the [application/dns+cbor] message format.

### DNS Servers

- Source: https://en.wikipedia.org/wiki/Comparison_of_DNS_server_software#Feature_matrix
	- Prerequisite: Free Software and DoH support

(🟨 = WIP, ⬜ = Not Implemented, ✅ = Implemented)

Software | Developer | Language | License | Repo Link | [DoH] | [DoC] | [DNS+CBOR][application/dns+cbor]
----------: | :--: | :-: | :-: | :-------------------- | :-: | :-: | :-:
BIND | [ISC](https://isc.org/) | C | Apache-2.0 | https://gitlab.isc.org/isc-projects/bind9/ | ✅ | ⬜ | ⬜
CoreDNS | [CNCF](https://cncf.io/) | Go | Apache-2.0 | https://github.com/coredns/coredns | ✅ | ⬜ | ⬜
Knot Resolver | [CZ.NIC](https://nic.cz/) | C/Lua | GPL-3.0 | https://gitlab.nic.cz/knot/knot-resolver | ✅ | ⬜ | ⬜
PowerDNS | [PowerDNS](https://powerdns.com/) | C++ | GPL-2.0 | https://github.com/PowerDNS/pdns | ✅ | ⬜ | ⬜
Technitium DNS Server | [Technitium](https://technitium.com/) | C# | GPL-3.0 | https://github.com/TechnitiumSoftware/DnsServer | ✅ | ⬜ | ⬜
Unbound | [NLnet Labs](https://nlnetlabs.nl/) | C | BSD-3 | https://github.com/NLnetLabs/unbound | ✅ | 🟨 | ⬜

### Libraries and (stub) resolvers

(🟨 = WIP, ⬜ = Not Implemented, ✅ = Implemented)

Software | Developer | Language | License | Repo Link | [DoH] | [DoC] | [DNS+CBOR][application/dns+cbor]
----------: | :--: | :-: | :-: | :-------------------- | :-: | :-: | :-:
c-ares | [c-ares](https://c-ares.org/) | C | MIT | https://github.com/c-ares/c-ares | ⬜ [^1] | ⬜ | ⬜
Chromium | [Google](https://google.com) | C++ | BSD-3 | https://chromium.googlesource.com/chromium/ | ✅ | ⬜ | ⬜
curl | [curl](https://curl.se/) | C | curl (MIT/BSD-like) | https://github.com/curl/curl |  ✅ | ⬜ | ⬜
dig | [ISC](https://isc.org/) | C | Apache-2.0 | https://gitlab.isc.org/isc-projects/bind9/ | ✅ | ⬜ | ⬜
dnspython | [rthalley](https://github.com/rthalley) | Python | ISCL | https://github.com/rthalley/dnspython |  ✅ | ⬜ | ⬜
Firefox | [Mozilla](mozilla.org) | JavaScript | MPL-2 | https://searchfox.org/mozilla-central/source/browser/components/doh |  ✅ | ⬜ | ⬜

[DoH]: https://datatracker.ietf.org/doc/rfc8484/
[DoC]: https://datatracker.ietf.org/doc/draft-ietf-core-dns-over-coap/
[application/dns+cbor]: https://datatracker.ietf.org/doc/draft-lenders-dns-cbor/
[^1]: https://github.com/c-ares/c-ares/issues/612
