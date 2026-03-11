# NetPractice

## Description

NetPractice is a practical networking exercise from the 42 curriculum. The goal is to configure small-scale networks by solving routing and addressing problems across 10 levels of increasing complexity. Each level presents a broken network diagram, and you must fix it by adjusting IP addresses, subnet masks, and routing tables until all communication goals are met.

Through this project, you gain hands-on understanding of how data travels across networks — from a single host to the internet — and how routers, switches, and gateways make that possible.

## Instructions

### Running the training interface

1. Clone this repository:
   ```
   git clone https://github.com/ak-za01/NetPractice.git
   ```

2. Navigate into the project folder and run the launch script:
   ```
   ./run.sh
   ```
   This starts a local web server and opens the NetPractice interface in your browser.

3. If `run.sh` doesn't work, start the server manually:
   ```
   python3 -m http.server 49242
   ```
   Then open `http://localhost:49242` in your browser.

### Using the interface

- Enter your 42 login in the field and click **Start** to load your personal configuration.
- Use the **Evaluation** tab to generate a random configuration for practice or mock evaluations.
- Modify the white (unlocked) fields until all goals show **OK**.
- Click **Check again** to verify your configuration.
- Once all goals pass, click **Get my config** to export the level's configuration file.

### Submission

- 10 exported configuration files (one per level) must be placed at the **root of this repository**.
- Make sure your 42 login was entered in the interface before exporting — each file is tied to your login.

## Resources

### Networking concepts studied

- **TCP/IP addressing** — how IP addresses identify devices on a network
- **Subnet masks** — how masks define the range of a network (e.g. /24, /26, /30)
- **CIDR notation** — shorthand for expressing subnet masks (e.g. 255.255.255.192 = /26)
- **Default gateways** — the router interface a host sends packets to when the destination is outside its subnet
- **Routers** — devices that forward packets between different networks using routing tables
- **Switches** — devices that connect multiple hosts within the same network (Layer 2)
- **Routing tables** — rules that tell a router where to forward packets based on destination IP
- **Public vs private IP ranges** — why private IPs (10.x, 192.168.x) can't cross the internet
- **OSI layers** — understanding where IP (Layer 3) and Ethernet (Layer 2) operate

### References

- [Cisco — IP Addressing and Subnetting](https://www.cisco.com/c/en/us/support/docs/ip/routing-information-protocol-rip/13788-3.html)
- [Subnet Calculator](https://www.subnet-calculator.com/)
- [Wikipedia — Classless Inter-Domain Routing (CIDR)](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing)
- [Wikipedia — OSI Model](https://en.wikipedia.org/wiki/OSI_model)
- [RFC 791 — Internet Protocol](https://www.rfc-editor.org/rfc/rfc791)

### AI usage

Claude (Anthropic) was used throughout this project as a learning assistant. Specifically:

- Explaining core networking concepts such as what a network is, how devices 
  communicate, and the role of routers, switches, and gateways
- Breaking down the OSI model (7 layers) and TCP/IP model (4 layers), their 
  differences, and why TCP/IP is the model the internet actually runs on
- Clarifying how a packet travels from a host to its destination across multiple 
  networks, and what happens at each step
- Helping prepare for the peer evaluation by practicing how to explain 
  networking concepts clearly and concisely
- All concepts were understood and internalized — nothing was copied blindly
