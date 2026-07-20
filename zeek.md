# Zeek Network Security Monitor

Zeek is a powerful, open-source network security monitoring framework that passively analyzes network traffic and transforms it into structured, high-level logs and events for security analysis.<br>
It's widely used by SOC teams, research institutions, and enterprises  for intrusion detection, network forensics, and traffic analysis at scale. The framework is noted for its deep protocol-aware parsing via the Spicy parser-generator, its flexible scripting layer for custom detection logic, and its long-standing production use in real-world threat-hunting pipelines.

<a href="https://github.com/zeek/zeek">Github Repo</a>

## My Contributions
* <a href="https://github.com/zeek/zeek/pull/5601">PR 5601</a> | <a href="https://github.com/zeek/zeek/issues/4361">Issue 4361</a> : Forwarded LDAP SASL authentication payloads (NTLM/Kerberos) to their respective child analyzers by extracting raw credential bytes from `ASN.1`-wrapped `SaslCredentials` in the Spicy parser, enabling automatic extraction of usernames, hostnames, and domain info from LDAP authentication traffic.

* <a href="https://github.com/zeek/zeek/pull/5669">PR 5669</a> | <a href="https://github.com/zeek/zeek/issues/4766">Issue 4766</a> : Designed and implemented a dedicated `SyslogTCP` Spicy analyzer supporting [RFC 6587](https://datatracker.ietf.org/doc/html/rfc6587) framing, handling both `OctetCounting` (reusing the UDP `Syslog::Message` parser via explicit length prefixes) and `NonTransparent` (delimiter-based) modes over long-lived TCP streams, with pcap-based integration tests covering interleaved framing.
