# Cybersecurity Learning Report - Day 3

**Target IP:** 10.0.2.2  
**Scan Date:** 2025-05-27  
**Tools:** Nmap 7.95

## Port Scan Summary

| Port  | State | Service         | Version/Info                            | Vulnerabilities           |
|-------|-------|-----------------|---------------------------------------|--------------------------|
| 135   | Open  | msrpc           | Microsoft Windows RPC                  | No critical vulns found   |
| 445   | Open  | microsoft-ds    | SMB/CIFS Service                      | No critical vulns found   |
| 902   | Open  | vmware-auth     | VMware Authentication Daemon 1.10     | -                        |
| 912   | Open  | vmware-auth     | VMware Authentication Daemon 1.0      | -                        |
| 27000 | Open  | flexlm          | FlexLM License Manager                 | -                        |

## Details

- Used SYN Stealth scan (`-sS`) to discover open ports.  
- Identified services running on each port with service version detection (`-sV`).  
- Ran vulnerability scripts (`--script=vuln`) to check for known issues.  
- Some SMB vulnerability scripts could not negotiate connections — possibly due to service restrictions.

## Summary

The target is a Windows-based system running Microsoft RPC, SMB services, VMware authentication services, and FlexLM license management. No critical vulnerabilities were detected with the scripts used. Some ports are protected or filtered (`tcpwrapped`), requiring further analysis.

---

*Report generated using Nmap scans on Kali Linux.*

