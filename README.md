# DNS over CoAP and application/dns+cbor projects

## DNS Servers and Stub Resolvers to Extend with DoC

This provides a non-exhaustive list of existing DNS servers and (stub) resolvers that have potential
to be extended with [DNS over CoAP][DoC] and the [application/dns+cbor] message format.

### DNS Servers

- Source: https://en.wikipedia.org/wiki/Comparison_of_DNS_server_software#Feature_matrix
	- Prerequisite: Free Software and DoH support

( :yellow_square: = WIP, :white_large_square: = Not Implemented, :white_check_mark: = Implemented)

Software | Developer | Language | License | Repo Link | [DoH] | [DoC] | [DNS+CBOR][application/dns+cbor]
----------: | :--: | :-: | :-: | :-------------------- | :-: | :-: | :-:
BIND | [ISC](https://isc.org/) | C | Apache-2.0 | https://gitlab.isc.org/isc-projects/bind9/ | :white_check_mark: | :white_large_square: | :white_large_square:
CoreDNS | [CNCF](https://cncf.io/) | Go | Apache-2.0 | https://github.com/coredns/coredns | :white_check_mark: | :white_large_square: | :white_large_square:
Knot Resolver | [CZ.NIC](https://nic.cz/) | C/Lua | GPL-3.0 | https://gitlab.nic.cz/knot/knot-resolver | :white_check_mark: | :white_large_square: | :white_large_square:
PowerDNS | [PowerDNS](https://powerdns.com/) | C++ | GPL-2.0 | https://github.com/PowerDNS/pdns | :white_check_mark: | :white_large_square: | :white_large_square:
Technitium DNS Server | [Technitium](https://technitium.com/) | C# | GPL-3.0 | https://github.com/TechnitiumSoftware/DnsServer | :white_check_mark: | :white_large_square: | :white_large_square:
Unbound | [NLnet Labs](https://nlnetlabs.nl/) | C | BSD-3 | https://github.com/NLnetLabs/unbound | :white_check_mark: | :yellow_square: | :white_large_square:

### Libraries and (stub) resolvers

( :yellow_square: = WIP, :white_large_square: = Not Implemented, :white_check_mark: = Implemented)

Software | Developer | Language | License | Repo Link | [DoH] | [DoC] | [DNS+CBOR][application/dns+cbor]
----------: | :--: | :-: | :-: | :-------------------- | :-: | :-: | :-:
c-ares | [c-ares](https://c-ares.org/) | C | MIT | https://github.com/c-ares/c-ares | :white_large_square: [^1] | :white_large_square: | :white_large_square:
Chromium | [Google](https://google.com) | C++ | BSD-3 | https://chromium.googlesource.com/chromium/ | :white_check_mark: | :white_large_square: | :white_large_square:
curl | [curl](https://curl.se/) | C | curl (MIT/BSD-like) | https://github.com/curl/curl |  :white_check_mark: | :white_large_square: | :white_large_square:
dig | [ISC](https://isc.org/) | C | Apache-2.0 | https://gitlab.isc.org/isc-projects/bind9/ | :white_check_mark: | :white_large_square: | :white_large_square:
dnspython | [rthalley](https://github.com/rthalley) | Python | ISCL | https://github.com/rthalley/dnspython |  :white_check_mark: | :white_large_square: | :white_large_square:[^2]
Firefox | [Mozilla](mozilla.org) | JavaScript | MPL-2 | https://searchfox.org/mozilla-central/source/browser/components/doh |  :white_check_mark: | :white_large_square: | :white_large_square:

[DoH]: https://datatracker.ietf.org/doc/rfc8484/
[DoC]: https://datatracker.ietf.org/doc/draft-ietf-core-dns-over-coap/
[application/dns+cbor]: https://datatracker.ietf.org/doc/draft-lenders-dns-cbor/
[^1]: https://github.com/c-ares/c-ares/issues/612
[^2]: Monkey-patched version for [`dns.query.https()`](https://dnspython.readthedocs.io/en/latest/query.html#https) by @miri64 exists. Please ask via martine.lenders@tu-dresden.de for the source.
