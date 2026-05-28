# Day 26 – Linux Network Configuration and Networking Commands

## What I Did
- Studied Linux network configuration basics  
- Learned about the `ifconfig` command and common interface terms such as:
  - `eth`
  - `wlan`
  - `lo`
  - `UP`

- Learned that `iwconfig` is used for wireless network configuration  
- Studied that `ifconfig` and `iwconfig` are older tools and are mostly replaced by newer commands now  

- Studied the `ping` command:
  - What ping is
  - How it works
  - How it continuously sends packets until stopped
  - How to limit packets using the `-c` option  

- Studied the `ip a` command and learned that it is commonly used instead of `ifconfig` nowadays  
- Studied the `ip route` command  
- Learned about the `ss` command and options such as:
  - `-t`
  - `-r`
  - `-u`
  - `-l`
  - `-n`
  - `-p`

- Studied the `netstat` command and learned that it is older but still useful in some cases  
- Learned about the `curl` command and how it works  
- Studied the `hostname` command and learned that the `-i` option can be used to get the local IP address  

## What I Understood
- Linux provides different commands for viewing and managing network configuration  
- Modern Linux systems mostly use the `ip` command instead of older networking tools  
- `ping` helps test connectivity between systems using ICMP packets  
- Commands like `ss` and `netstat` help inspect network connections and listening ports  
- Networking commands become easier to understand with networking fundamentals knowledge  

## Concepts Covered
- `ifconfig`
- `iwconfig`
- `ip a`
- `ip route`
- `ping`
- `ss`
- `netstat`
- `curl`
- `hostname`

## Key Takeaways
- Linux networking commands provide detailed information about interfaces, routes, and connections  
- Modern networking tools are gradually replacing older utilities like `ifconfig` and `netstat`  
- Understanding networking commands is important for troubleshooting and cybersecurity work  
- Networking fundamentals help make Linux networking tools much easier to understand  

## Next Step
- Study Package Management and Password Management
