<<<<<<< HEAD
# network-port-scan-task
Task 1: Network port scanning results, commands, and analysis
=======
# Network Port Scanning (Task 1) — Gowtham
>>>>>>> 6513c82 (Task 1: Add Nmap results and investigation files)
cat > README.md <<'RD'
# Network Port Scanning (Task 1) — Gowtham

Task 1: Network port scanning results, commands, and analysis.

## Objective
Scan the local network (10.0.2.0/24) to find open ports, enumerate services, and assess security exposure.

## Environment
- Machine: Hanuman (Ubuntu) — 10.0.2.4
- Virtual Hosts visible: 10.0.2.1, 10.0.2.2, 10.0.2.3
- Tools: Nmap, smbclient, rpcinfo, enum4linux, tcpdump, Wireshark

## Key Findings
- 10.0.2.1: 53/tcp open (DNS)
- 10.0.2.2: 135/tcp open (msrpc), 445/tcp open (microsoft-ds)
- 10.0.2.3: filtered (no reply)
- 10.0.2.4 (Hanuman): all scanned tcp ports closed

## Actions taken
- Performed SYN scan and service/version detection
- Enumerated SMB/RPC using smbclient, rpcinfo, enum4linux
- Captured traffic with tcpdump for Wireshark analysis (optional)

## Recommendations
- Restrict DNS recursion & zone-transfers
- Disable SMBv1, restrict SMB access, patch systems
- Harden Hanuman: stop unused services and use UFW

## Files included
- scan_results.txt
- svc_versions.txt
- aggressive_10.0.2.2.txt
- hanuman_listening.txt
- smbclient_10.0.2.2.txt
- rpcinfo_10.0.2.2.txt
- probe_capture.pcap (optional)
- investigation_commands.txt
- analysis.md
RD
