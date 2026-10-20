# Meow

| | |
|---|---|
| **Tier** | 0 |
| **OS** | Linux |
| **Date solved** | 2026-10-19 |
| **Tags** | Nmap, Telnet, default credentials |

## Summary
Meow is an introductory Linux machine that exposes Telnet on port 23 and allows a root login with a blank password. The exercise demonstrates VPN connectivity, basic port scanning, and why unauthenticated remote root access is unsafe.

## Recon
Connect to the Hack The Box lab network. If you are not using Pwnbox, start the provided OpenVPN configuration and leave it running. Verify connectivity to the target:

```sh
ping <TARGET_IP>
```

Scan the target for open ports:

```sh
nmap <TARGET_IP>
```

The scan identifies TCP port 23 running Telnet.

## Exploitation
Connect to the Telnet service:

```sh
telnet <TARGET_IP> 23
```

At the `Meow login:` prompt, enter `root`. Leave the password blank and press Enter. The login provides a root shell. List the files and read `flag.txt` to complete the lab; the flag is intentionally redacted here.

```sh
ls
cat flag.txt
```

## Task questions
| # | Question (paraphrased) | Answer |
|---|---|---|
| 1 | What does VM stand for? | Virtual Machine |
| 2 | What is the command-line interface also known as a console or shell? | Terminal |
| 3 | What service forms the VPN connection to HTB labs? | OpenVPN |
| 4 | Which tool sends ICMP echo requests to test connectivity? | `ping` |
| 5 | What is the common tool used to find open ports? | `nmap` |
| 6 | What service is running on TCP port 23? | Telnet |
| 7 | Which username logs in over Telnet with a blank password? | `root` |

## Lessons learned
- Confirm VPN connectivity before scanning a lab target.
- Nmap can identify exposed ports and services.
- Telnet sends traffic without encryption and should not expose privileged access.
- Never allow remote root login with a blank password.

## Remediation
- Disable Telnet and use SSH with key-based authentication.
- Disable direct root login and enforce strong authentication.
- Restrict remote management access to trusted networks.

