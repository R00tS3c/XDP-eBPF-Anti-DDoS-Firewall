# XDP-eBPF-Anti-DDoS-Firewall
An advanced XDP/eBPF-based security system for protecting game servers, VPN services, and network applications.

🛡️ About

This project is a high-performance anti-DDoS firewall built on XDP/eBPF technology.
It is designed to stop DDoS attacks at the network interface level, before packets even reach the Linux network stack.

The system uses behavior-based filters, advanced traffic analysis, and heuristic detection of abnormal patterns rather than relying on static signatures.
Its goal is to provide safe, fast, and efficient protection without depending on sensitive protocol internals.

🔥 Key Features

✔ XDP/eBPF Firewall at the NIC Level

Filters packets very early in the network stack

Minimal CPU overhead

Ultra-low latency

✔ Behavior-Based Legitimate Traffic Detection

Recognizes normal traffic patterns based on:

Packet size ranges

Data entropy

Inter-packet timing

PPS/BPS ratios

Burst behavior

All without relying on protocol-specific signatures.

✔ Adaptive Rate Limiting

Dynamic per-IP PPS/BPS limits

Burst detection and mitigation

Automatic temporary blackholing of malicious IPs

✔ Port/Service Profiles

Supports multiple services and ports with custom behavioral profiles, including:

Game servers (Steam, FiveM, Rust, Arma, Battlefield, etc.)

VPN servers (OpenVPN, WireGuard)

DNS servers

Voice servers (TeamSpeak 3)

Profiles define expected packet sizes, timing, and behavioral heuristics to distinguish legitimate traffic from attacks.

✔ Dynamic Defense Modes

Adjusts automatically based on attack intensity:

Normal mode – standard traffic filtering

Elevated mode – tighter limits during increased traffic

Critical mode – aggressive filtering during high-volume attacks

✔ Monitoring & Statistics

Tracks per-IP traffic patterns

Logs drops, passes, and blackholed IPs

Monitors PPS, burst rates, and CPU usage

Ready for integration with dashboards (Grafana/Prometheus)
