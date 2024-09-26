# Footprinting-and-Reconnaissance

Reconnaissance refers to collecting information about a target, which is the first step in any attack on a system.

Footprinting refers to the process of collecting information about a target network and its environment, which helps in evaluating the security posture of the target organization’s IT infrastructure. (Passive or Active)

But before you start this process, consider the following:
- Define scope with management: systems, networks, policies, personnel.
- Agree on rules of engagement (RoE) with management.
- Obtain approval for ethical hacking activities.
- Start gathering information via footprinting.
- Develop a security blueprint from footprinting results.

There are several objective for footprinting and reconnaissance:
- **Organization Information:** Employee details, addresses and contact details, partner details, weblinks, web technologies, patents, trademarks, etc.
- **Network Information:** Domains, sub-domains, network blocks, network topologies, trusted routers, firewalls, IP addresses of the reachable systems, the Whois record, DNS records, and other related information
- **System Information:** Operating systems, web server OSes, location of web servers, user accounts and passwords, etc.

---
# 1. Perform Footprinting Through Search Engines

## Gather information using advanced Google hacking techniques
| Filter       | Example                        | Description                                                    |
|--------------|--------------------------------|----------------------------------------------------------------|
| `site`       | `site:tryhackme.com`           | Returns results only from the specified website address         |
| `inurl`      | `inurl:admin`                  | Returns results with the specified word in the URL              |
| `filetype`   | `filetype:pdf`                 | Returns results of a particular file type                      |
| `intitle`    | `intitle:admin`                | Returns results with the specified word in the title            |
| `cache`      | `cache:www.eccouncil.org`      | Returns the cached version of the specified website             |
| `allinurl`   | `allinurl:EC-Council career`   | Returns results with all query terms in the URL                 |
| `allintitle` | `allintitle:detect malware`    | Returns results with all query terms in the title               |
| `inanchor`   | `inanchor:Norton`              | Returns results with the specified word in anchor text          |
| `allinanchor`| `allinanchor:cloud provider`   | Returns results with all query terms in anchor text             |
| `link`       | `link:www.eccouncil.org`       | Finds pages linking to the specified website                   |
| `related`    | `related:www.eccouncil.org`    | Displays websites related to the specified URL                  |
| `info`       | `info:eccouncil.org`           | Provides info about the specified website                      |
| `location`   | `location:EC-Council`          | Finds information related to a specific location                |

## 2. Gather information from video search engines

- https://mattw.io/youtube-metadata/
- https://www.google.com/videohp
- https://in.video.search.yahoo.com
- https://ezgif.com), VideoReverser.com
- https://www.videoreverser.com
- https://tineye.com
- https://images.search.yahoo.com

Check sections under Snippet, Statistics, Geolocation, Status, etc.

## 3. Gather Information from FTP Search Engines
https://www.searchftps.net/
## 4. Gather Information from IoT Search Engines
https://www.shodan.io/ or https://censys.io

---
# Perform footprinting through web services

