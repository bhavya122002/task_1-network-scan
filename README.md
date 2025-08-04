# task_1-network-scan
Using nmap to scan open ports in the system.

## Tools Used
- Nmap

## Steps Performed
1. Installed Nmap
2. Identified local IP range: 192.168.132.67
3. Performed SYN scan using nmap -sS 192.168.132.67/24
4. Collected results and saved as 'Scan_resultnmap.txt'
5. Identified open ports and noted potential security risks


Risks associated with the found open ports.
|   Port   |      Service        |                                    Risk                                            |
| -------- | ------------------- | ---------------------------------------------------------------------------------- |
| 135/tcp  | msrpc               | Can be exploited for remote code execution or service enumeration.                 |
| 139/tcp  | netbios-ssn         | Allows NetBIOS attacks like file share enumeration or SMB session hijacking.       |
| 445/tcp  | microsoft-ds        | Highly targeted by ransomware and worms; used for SMB which can allow RCE.         |
| 5357/tcp | ws-discovery/wsdapi | May leak device details and expose the host to local privilege escalation threats. |
