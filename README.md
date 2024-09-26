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
# Perform Footprinting Through Search Engines

**1. Gather information using advanced Google hacking techniques**
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

**2. Gather information from video search engines**

- https://mattw.io/youtube-metadata/
- https://www.google.com/videohp
- https://in.video.search.yahoo.com
- https://ezgif.com), VideoReverser.com
- https://www.videoreverser.com
- https://tineye.com
- https://images.search.yahoo.com

Check sections under Snippet, Statistics, Geolocation, Status, etc.

**3. Gather Information from FTP Search Engines**
https://www.searchftps.net/
**4. Gather Information from IoT Search Engines**
https://www.shodan.io/ or https://censys.io

---
# Perform footprinting through web services

**1. Find the Company’s Domains and Sub-domains using _Netcraft_**
A company's top-level domains (TLDs) and sub-domains can provide much useful information such as organizational history, services and products, and contact information.

https://www.netcraft.com [Resources -> Tools -> Site Report] (or https://sitereport.netcraft.com)

-> Results containing information related to Background, Network, Hosting History, etc. [Click on the domain link to see the subdomains]

You can also use tools such as Sublist3r (https://github.com), Pentest-Tools Find Subdomains (https://pentest-tools.com), etc. to identify the domains and sub-domains of any target website.

**2. Gather Personal Information using _PeekYou_ Online People Search Service**

https://www.peekyou.com
-> The result shows information such as public records, background details, email addresses, contact information, address history, etc. ou can further click on View Full Report

You can also use Spokeo (https://www.spokeo.com), pipl (https://pipl.com), Intelius (https://www.intelius.com), BeenVerified (https://www.beenverified.com), etc., people search services to gather personal information of key employees in the target organization.

**3. Gather an Email List using _theHarvester_**

Open terminal in parrot.
1. `sudo su` to run the programs as a root user
2. `cd` to jump to root directory
3. `theHarvester -d microsoft.com -l 200 -b baidu` In this command, `-d` specifies the domain or company name to search, `-l` specifies the number of results to be retrieved, and `-b` specifies the data source.

You can see the email IDs related to the target company and target company hosts obtained from the Baidu source

**4. Gather Information using Deep and Dark Web Searching**

Open a File Explorer, navigate to C:\Users\Admin\Desktop\Tor Browser, and double-click Start Tor Browser.

If Tor is censored in your country or if you want to connect through Proxy, click the Tor Network Settings button and select any default built-in bridge as shown in the screenshot below and continue.
![image](https://github.com/user-attachments/assets/08b86bb5-826a-4f6d-848a-d73249f25068)

https://www.hackerforhire.net

You can also anonymously explore the following onion sites using Tor Brower to gather other relevant information about the target organization:

- The Hidden Wiki is an onion site that works as a Wikipedia service of hidden websites. (http://zqktlwiuavvvqqt4ybvgvi7tyo4hjl5xgfuvpdf6otjiycgwqbym2qad.onion/wiki)
- FakeID is an onion site for creating fake passports (http://ymvhtqya23wqpez63gyc3ke4svju3mqsby2awnhd3bk2e65izt7baqad.onion)
- Cardshop is an onion site that sells cards with good balances (http://s57divisqlcjtsyutxjz2ww77vlbwpxgodtijcsrgsuts4js5hnxkhqd.onion)

You can also use tools such as ExoneraTor (https://metrics.torproject.org), OnionLand Search engine (https://onionlandsearchengine.com), etc. to perform deep and dark web browsing.

**5. Determine Target OS Through Passive Footprinting**

https://search.censys.io/?q=

You can also use webservices such as Netcraft (https://www.netcraft.com), Shodan (https://www.shodan.io), etc. to gather OS information of target organization through passive footprinting.

---
# Perform Footprinting Through Social Networking Sites

**1. Gather Employees’ Information from LinkedIn using theHarvester**
LinkedIN site contains personal information such as name, position, organization name, current location, educational qualifications, etc.

1. `sudo su`
2. `cd`
3. `theHarvester -d eccouncil -l 200 -b linkedin`

**2. Gather Personal Information from Various Social Networking Sites using _Sherlock_**
Sherlock is a python-based tool that is used to gather information about a target person over various social networking sites. Sherlock searches a vast number of social networking sites for a given target user, locates the person, and displays the results along with the complete URL related to the target person.

1. sudo su
2. sherlock "satya nadella"

The attackers can further use the gathered URLs to obtain sensitive information about the target such as DOB, employment status and information about the organization that they are working for, including the business strategy, potential clients, and upcoming project plans.

You can also use tools such as Social Searcher (https://www.social-searcher.com), UserRecon (https://github.com), etc. to gather additional information related to the target company and its employees from social networking sites.

---
# Perform Website Footprinting
Website footprinting is a technique used to collect information regarding the target organization’s website.

**1. Gather Information About a Target Website using _Ping_ Command Line Utility**

1. Enter to command Prompt
2. `ping www.certifiedhacker.com` You obtained IP, Ping stats, and approximate round-trip time.
3. `ping www.certifiedhacker.com -f -l 1500` In this command, `-f` Specifies setting not fragmenting flag in packet and `-l` Specifies buffer size.

The response, Packet needs to be fragmented but DF set, means that the frame is too large to be on the network and needs to be fragmented. The packet was not sent as we used the -f switch with the ping command, and the ping command returned this error. **So ping you need to trail and error.**

4. `ping www.certifiedhacker.com -i 3` This option sets the time to live (-i) value as 3.
5. `ping www.certifiedhacker.com -i 2 -n 1` Here, we set the TTL value to 2 and the -n value to 1 to check the life span of the packet. [-n specifies the number of echo requests to be sent to the target.]

You can change the ttl value until you find the hop value by trying different TTL value to reach www.certifiedhacker.com.

**2. Gather Information about a Target Website using _Photon_**
Photon is a Python script used to crawl a given target URL to obtain information.

1. `sudo su`
2. `cd Photon`
3. `python3 photon.py -h` to view the list of options that Photon provides.
4. `python3 photon.py -u http://www.certifiedhacker.com` to crawl the target website for internal, external and scripts URLs. `-u` specifies the target website (here, www.certifiedhacker.com).

Now you realised taht the filed are saved in the photon folder. Navigate to the directory through 'places'.
![image](https://github.com/user-attachments/assets/756953f5-3e38-49fa-a2b3-f45bafb1166e)





















