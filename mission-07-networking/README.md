# Mission 7 — How computers communicate

## 1. Task / objective
Explain basic network types and concepts, observe network lookup and connectivity information, and describe what happens when a website opens.

## 2. Work completed
I filled in a table of network concepts in my own words, tested connectivity to a public example website with `ping`, did a DNS lookup with `nslookup`, and wrote a step-by-step explanation of what happens when a website opens. I did not include my own IP address, Wi-Fi name or other private network details.

### Task 7.1 — Network concepts

| Concept | Explanation in my own words | Example |
|---------|-----------------------------|---------|
| LAN | A network that covers a small area where devices are close together | Wi-Fi at home or the computer lab in college |
| MAN | A network that covers a whole city or a large campus, bigger than a LAN and smaller than a WAN | A city-wide cable network or a university with several campuses connected |
| WAN | A network that covers a very large area, even countries, by linking many smaller networks | The internet |
| DNS | A system that translates a website name into the IP address a computer needs to find it | Turning example.com into a numeric address |
| Router | A device that connects different networks and sends data to the right place | My home Wi-Fi router connecting my devices to the internet |
| Protocol | A set of rules that devices follow so they can understand each other | HTTP and HTTPS for websites, TCP/IP for sending data |
| Packet switching | Data is broken into small packets that travel separately across the network and are put back together at the destination | Sending an image over the internet in many small pieces |
| Client-server | A client asks for a service and a server provides it | My browser (client) requesting a page from a web server |

### Task 7.2 — Network observations

**Connectivity test:** I ran `ping -c 4 example.com`. It sent 4 small test messages to the website and received replies. The result showed the reply time (in milliseconds) and the packet loss was REPLACE_WITH_YOURS (for example 0%).

**DNS lookup:** I ran `nslookup example.com`. It showed the domain name and the IP address (or addresses) that belong to it. I left out the lines about my own DNS server, since they can show private network details.

- **What a connectivity test helps me check:** It shows whether my computer can reach another computer over the network, how long the reply takes, and whether any packets are lost.
- **What a DNS lookup displays:** It displays the IP address connected to a domain name.
- **The role of DNS when I type a website name:** Computers find each other using IP addresses, not names. When I type a website name, my browser asks DNS for the matching IP address, and only then can it connect to the right server.

### Task 7.3 — What happens when I open a website
1. I type a website address in my browser. The browser is the **client** that will ask for the page.
2. The browser asks **DNS** to translate the website name into an IP address.
3. DNS replies with the IP address of the server.
4. The browser sends a request to that address using a **protocol**, usually HTTPS. The request leaves my device and goes through my router.
5. The data travels as packets across many networks (the WAN/internet) until it reaches the website's **server**.
6. The server finds the page and sends the response back to me in packets, following the same protocol rules.
7. My browser puts the packets together and shows the page on my screen.

## 3. Commands / tools used
- `ping -c 4 example.com`: tests whether I can reach a website and how fast it replies.
- `nslookup example.com`: looks up the IP address for a domain name using DNS.
- `git switch main`, `cd`: used to move to the right branch and folder.
- Tools: Terminal (zsh), VS Code, Git.

## 4. My understanding
A network connects devices so they can share data. LAN, MAN and WAN differ by the area they cover, from a room to the whole world. DNS works like a phone book that turns names into IP addresses, routers pass data between networks, and protocols are the shared rules that let devices understand each other. Data travels in small packets, and in the client-server model my browser asks and a server answers. This matters because every website, video call or message depends on these ideas working together.

## 5. Difficulties faced
No major difficulties.

## 6. How I resolved them
Not applicable.

## 7. Evidence / files
- `mission-07-networking/README.md` (concepts, observations and website explanation; private network details left out)

## 8. Commit details
Commit message: "Explain networking concepts and website communication"
I pushed this commit to GitHub and checked that it is visible.