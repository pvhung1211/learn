
DNS (Domain Name System) is like the **phonebook of the internet**. It translates **human-readable domain names** (like `google.com`) into **IP addresses** (like `142.250.190.14`) so computers can understand and connect to websites.

## DNS Address

A **DNS address** refers to the IP address of a **Domain Name System (DNS) server** that translates domain names (like `google.com`) into IP addresses (like `142.250.190.78`). This allows your device to connect to websites using human-readable names instead of numerical IP addresses.

## What is a DNS record?

https://www.cloudflare.com/learning/dns/dns-records/


## A Records vs. Alias Records | EasyDMARC

https://easydmarc.com/blog/a-records-vs-alias-records/#:~:text=A%20records%20are%20standard%20DNS,point%20to%20another%20domain%20name.

>A records are standard DNS records while Alias records are custom DNS records

> ==A "DNS alias" is essentially a nickname or alternative name for a domain, pointing to another existing domain name (like a "www" subdomain), while a "DNS name" refers to the primary, canonical name of a domain that directly resolves to an IP address==; in simpler terms, an alias is a way to access a domain using a different name, while the DNS name is the actual, recognized address on the internet.

**DNS name**: domain name (google.com)
**DNS alias**: nick name for the domain 

// alias                          // domain
blog.example.com → example.medium.com

 alias => domain => ip address

## Step-by-Step DNS Resolution Process

1. **User Requests a Website**

	- You type `example.com` into your browser.

2. **Check Local Cache**

	- Your computer first checks its local DNS cache to see if it already knows the IP address for `example.com`. If found, it skips the next steps.

3. **Ask the Configured DNS Server**

    - If the IP isn’t cached, your device sends a request to the configured DNS server (e.g., `8.8.8.8` from Google Public DNS).

4. **Recursive Query (DNS Server Looks Up the IP)**

    - If the DNS server (e.g., `8.8.8.8`) doesn’t already know the IP, it asks other DNS servers in a process like this:
        - **Root DNS Server** → Knows `.com` DNS servers
        - **.com TLD DNS Server** → Knows `example.com`'s authoritative DNS
        - **Authoritative DNS Server for example.com** → Returns the actual IP address

5. **Return the IP Address**

    - The DNS server (e.g., `8.8.8.8`) gets the IP address (e.g., `192.168.1.1`) from the authoritative server and sends it back to your device.

6. **Connect to the Website**

    - Your browser now uses the IP (`192.168.1.1`) to establish a connection with the web server and load the website.

7. **Cache the Result**

    - Your computer temporarily stores the IP address in its DNS cache to speed up future visits.