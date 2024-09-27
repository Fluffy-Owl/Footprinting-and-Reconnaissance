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

Now you realised taht the filed are saved in the photon folder. Navigate to the directory through 'places'. Places > Home Folder > Attacker > Photon > www.certifiedhacker.com. Select the external.txt. You will see the URLs.
![image](https://github.com/user-attachments/assets/756953f5-3e38-49fa-a2b3-f45bafb1166e)

Now try this:
1. `python3 photon.py -u http://www.certifiedhacker.com -l 3 -t 200 --wayback` to crawl the target website using URLs from archive.org. `-u` specifies the target website (here, www.certifiedhacker.com), `-l` specifies level to crawl (here, 3), `-t` specifies number of threads (here, 200), `--wayback` specifes using URLs from archive.org as seeds.

**3. Gather Information About a Target Website using _Central Ops_**
CentralOps (centralops.net) is a free online network scanner that investigates domains and IP addresses, DNS records, traceroute, nslookup, whois searches, etc.

1. open Mozilla
2. https://centralops.net
3. enter the target website eg: www.certifiedhacker.com

You can also use tools such as Website Informer (https://website.informer.com), Burp Suite (https://portswigger.net), Zaproxy (https://www.zaproxy.org), etc. to perform website footprinting on a target website.

**4. Extract a Company’s Data using _Web Data Extractor_**
Web data extraction is the process of extracting data from web pages available on the company’s website.

1. In the Windows 11 machine, navigate to E:\CEH-Tools\CEHv12 Module 02 Footprinting and Reconnaissance\Web Spiders\Web Data Extractor and double-click wdepro.exe.
2. Install it.
3. Search on the search icon `Web Data Extractor Pro`. Open it up.
4. Click new session.
5. Write the target URL in the `Start URL field`. Click Start!
6. Web Data Extractor will start collecting information (Session, Meta tags, Emails, Phones, Faxes, Links, and Domains).
7. Go to Results tab and see.
8. Select the Meta Tag tab to view the URL, Title, Keywords, Description, Host, Domain, page size, etc.
9. Select the Email tab to view information related to emails such as Email address, Name, URL, Title, etc.
10. Select the Phone tab to view the Phone, Source, Tag, URL, etc.

You can also use other web spiders such as ParseHub (https://www.parsehub.com), SpiderFoot (https://www.spiderfoot.net), etc. to extract the target organization’s data.

**5. Mirror a Target Website using _HTTrack Web Site Copier_**
HTTrack is an offline browser utility that downloads a website from the Internet to a local directory, builds all directories recursively, and transfers HTML, images, and other files from the webserver to another computer.

Here, we will use the HTTrack Web Site Copier tool to mirror the entire website of the target organization, store it in the local system drive, and browse the local website to identify possible exploits and vulnerabilities.

1. Search for `WinHTTrack Website Copier` in the search icon and launch it.
2. Do a new project.
3. Enter the name of the project (here, Test Project) in the New project name: field. Select the Base path: to store the copied files; click Next >.
4. Enter a target URL (here, https://www.certifiedhacker.com) in the Web Addresses: (URL) field and click Set options….
5. WinHTTrack window appears, click the Scan Rules tab and select the checkboxes for the file types as shown in the following screenshot; click OK. [all]
6. Click the Next > button.
7. By default, the radio button will be selected for Please adjust connection parameters if necessary, then press FINISH to launch the mirroring operation. Check Disconnect when finished and click `Finish` to start mirroring the website.
8. Once the site mirroring is completed, WinHTTrack displays the message Mirroring operation complete; click on `Browse Mirrored Website`.
9. If the How do you want to open this file? pop up appears, select any web browser and click OK.
10. Once done with your analysis, close the browser window and click Finish on the WinHTTrack window to complete the process and click on EXIT to close the tool.

*If the webpage does not open, navigate to the directory where you mirrored the website and open index.html with any browser.

You can also use other mirroring tools such as Cyotek WebCopy (https://www.cyotek.com), etc. to mirror a target website.

**6. Gather Information About a Target Website using GRecon**
GRecon is a Python tool that can be used to run Google search queries to perform reconnaissance on a target to find subdomains, sub-subdomains, login pages, directory listings, exposed documents, and WordPress entries.

1. `sudo su`
2. `cd GRecon`
3. `python3 grecon.py`
4. GRecon initializes, in the **Set Target (site.com):** field type `certifiedhacker.com` and press **Enter**.

GRecon searches for available subdomains, sub-subdomains, login pages, directory listings, exposed documents, WordPress entries and pasting sites and displays the results.

**7. Gather a Wordlist from the Target Website using CeWL**

1. `sudo su`
2. `cd`
3. `cewl -d 2 -m 5 https://www.certifiedhacker.com` `-d` represents the depth to spider the website (here, 2) and `-m` represents minimum word length (here, 5).
4. or `cewl -w wordlist.txt -d 2 -m 5 https://www.certifiedhacker.com` `-w` Write the output to the file (here, wordlist.txt)
5. By default, the wordlist file gets saved in the root directory. Type `pluma wordlist.txt` and press Enter to view the extracted wordlist.
6. Type `cewl --help` and press Enter in the parrot terminal to view the list of options that cewl provides.

This wordlist can be used further to perform brute-force attacks against the previously obtained emails of the target organization’s employees.

---
# Perform Email Footprinting

**1. Gather Information about a Target by Tracing Emails using eMailTrackerPro**

1. Windows. E:\CEH-Tools\CEHv12 Module 02 Footprinting and Reconnaissance\Email Tracking Tools\eMailTrackerPro and double-click emt.exe.
2. After the installation is complete, in the **Completing the eMailTrackerPro Setup Wizard**, uncheck the Show Readme check-box and click the **Finish** button to launch the eMailTrackerPro.
3. The main window of **eMailTrackerPro** appears along with the **Edition Selection** pop-up; click **OK**.
4. To trace email headers, click the **My Trace Reports** icon from the **View** section. (here, you will see the output report of the traced email header).
5. Click the **Trace Headers** icon from the **New Email Trace** section to start the trace.
6. A pop-up window will appear; select **Trace an email I have received**. Copy the email header from the suspicious email you wish to trace and paste it in the **Email headers**: field under **Enter Details** section.
7. ![image](https://github.com/user-attachments/assets/ef92be43-8abd-47fe-a8fe-d4646fa2ff76)
8. Copy the entire email header text and paste it into the **Email headers**: field of eMailTrackerPro, and click **Trace**.
9. The **My Trace Reports** window opens.
10. The email location will be traced in a **Map** (world map GUI). You can also view the summary by selecting **Email Summary** on the right-hand side of the window. The **Table** section right below the Map shows the entire hop in the route, with the **IP** and suspected locations for each hop.
11. To examine the report, click the **View Report** button above **Map** to view the complete trace report.
12. The complete report appears in the default browser. Click **OK**.

You can also use email tracking tools such as Infoga (https://github.com), Mailtrack (https://mailtrack.io), etc. to track an email and extract target information such as sender identity, mail server, sender’s IP address, location, etc.

---
# Perform Whois Footprinting

**1. Perform Whois lookup using DomainTools**

1. In the Windows 11 machine, open any web browser (here, Mozilla Firefox). In the address bar of the browser place your mouse cursor, type **http://whois.domaintools.com** and press Enter. The Whois Lookup website appears.
2. This search result reveals the details associated with the URL entered, www.certifiedhacker.com, which includes organizational details such as **registration details**, **name servers**, **IP address**, **location**, etc.

You can also use other Whois lookup tools such as SmartWhois (https://www.tamos.com), Batch IP Converter (http://www.sabsoft.com), etc. to extract additional target Whois information.

---
# Perform DNS Footprinting

**1. Gather DNS Information using _nslookup_ Command Line Utility and Online Tool**

1. In the **Windows 11** machine, launch a **Command Prompt**, type `nslookup` and press **Enter**. This displays the default server and its address assigned to the **Windows 11** machine.
2. In the n**slookup interactive mode**, type `set type=a` and press **Enter**. Setting the type as “**a**” configures nslookup to query for the IP address of a given domain.
3. Type the target domain **www.certifiedhacker.com** and press **Enter**. This resolves the IP address and displays the result.
4. The first two lines in the result are:

  Server: **dns.google** and Address: **8.8.8.8**

  This specifies that the result was directed to the default server hosted on the local machine (**Windows 11**) that resolves your requested domain.

5. Thus, if the response is coming from your local machine’s server (Google), but not the server that legitimately hosts the domain **www.certifiedhacker.com**; it is considered to be a non-authoritative answer. Here, the IP address of the target domain **www.certifiedhacker.com** is **162.241.216.11**.
6. Since the result returned is non-authoritative, you need to obtain the domain's authoritative name server.
7. Type `set type=cname` and press **Enter**. The CNAME lookup is done directly against the domain's authoritative name server and lists the CNAME records for a domain.
8. Type `certifiedhacker.com` and press **Enter**.
9. This returns the domain’s authoritative name server (**ns1.bluehost.com**), along with the mail server address (**dnsadmin.box5331.bluehost.com**).
10. Since you have obtained the authoritative name server, you will need to determine the IP address of the name server.
11. Issue the command `set type=a` and press **Enter**.
12. Type `ns1.bluehost.com` (or the primary name server that is displayed in your lab environment) and press **Enter**. This returns the IP address of the server.
13. The authoritative name server stores the records associated with the domain. So, if an attacker can determine the authoritative name server (primary name server) and obtain its associated IP address, he/she might attempt to exploit the server to perform attacks such as DoS, DDoS, URL Redirection, etc.
14. You can also perform the same operations using the NSLOOKUP online tool. Conduct a series of queries and review the information to gain familiarity with the NSLOOKUP tool and gather information.

Now, we will use an online tool NSLOOKUP to gather DNS information about the target domain.
1. http://www.kloth.net/services/nslookup.php
2. Once the site opens, in the **Domain**: field, enter **certifiedhacker.com**. Set the **Query**: field to default [**A (IPv4 address)**] and click the **Look it up** button to review the results that are displayed.
3. In the QUery field, can try others as well. Including **AAAA (IPv6 address)**.

You can also use DNS lookup tools such as DNSdumpster (https://dnsdumpster.com), DNS Records (https://network-tools.com), etc. to extract additional target DNS information.

**2. Perform Reverse DNS Lookup using _Reverse IP Domain Check_ and _DNSRecon_**
DNS lookup is used for finding the IP addresses for a given domain name, and the reverse DNS operation is performed to obtain the domain name of a given IP address.

1. https://www.yougetsignal.com
2. **you get signal** website appears, click **Reverse IP Domain Check**.
3. On the Reverse IP Domain Check page, enter **www.certifiedhacker.com** in the **Remote Address** field and click **Check** to find other domains/sites hosted on a certifiedhacker.com web server. You will get the list of domains/sites hosted on the same server as **www.certifiedhacker.com**.
4. Now, click Parrot Security-M2 to switch to the Parrot Security machine.
5. `cd dnsrecon`
6. `chmod +x ./dnsrecon.py`
7. `./dnsrecon.py -r 162.241.216.0-162.241.216.255`

Here, we will use the IP address range, which includes the IP address of our target, that is, the certifiedhacker.com domain (162.241.216.11), which we acquired in the previous steps.

-r option specifies the range of IP addresses (first-last) for reverse lookup brute force.

**3. Gather Information of Subdomain and DNS Records using _SecurityTrails_**

1. https://securitytrails.com/
2. **SecurityTrails** website appears, In the website click on **Sign Up For Free** button at the top right corner of the page.
3. **Sign up-Free** page appears, enter the required details and check the terms and conditions check box. Click **Sign up for free**.
4. In the **Enter a Domain, IP, Keyword or Hostname** field, type **certifiedhacker.com** and press **Enter**.
5. DNS records of certifiedhacker.com will appear, containing **A records, AAAA records, MX records, NS records, SOA records, TXT, and CNAME records**.
6. After examining the DNS records tab switch to **Historical Data** tab where you can find **historical data** of A, AAAA, MX, NS, SOA and TXT records.
7. Now switch to **Subdomains** tab where you can find all the subdomains pertaining to **certifiedhacker.com**.

You can also use DNSChecker (https://dnschecker.org), and DNSdumpster (https://dnsdumpster.com), etc. to perform DNS footprinting on a target website.

---
# Perform Network Footprinting

**1. Locate the network range**
Network range information assists in creating a map of the target network.

1. https://www.arin.net/about/welcome/region
2. ARIN website appears, in the search bar, enter the IP address of the target organization (here, the target organization is **certifiedhacker.com**, whose IP is **162.241.216.11**), and then click the **Search** button.

You will get the information about the network range along with the other information such as network type, registration information, etc.

**2. Perform Network Tracerouting in Windows and Linux Machines**
Traceroute can be used to extract information about network topology, trusted routers, firewall locations, etc.

1. Command Prompt
2. `tracert www.certifiedhacker.com`
3. Type `tracert /?` and press **Enter** to show the different options for the command, as shown in the screenshot.
4. Type `tracert -h 5 www.certifiedhacker.com` and press **Enter** to perform the trace, but with only 5 maximum hops allowed.

1. Now use parrot
2. `traceroute www.certifiedhacker.com`

You can also use other traceroute tools such as VisualRoute (http://www.visualroute.com), Traceroute NG (https://www.solarwinds.com), etc. to extract additional network information of the target organization.

--- 
# Perform Footprinting using Various Footprinting Tools

**1. Recog-ng**

1. `sudo su`
2. `cd`
3. `recon-ng`
4. Type `help` and press Enter to view all the commands that allow you to add/delete records to a database, query a database, etc.
5. Type `marketplace install all` and press Enter to install all the modules available in recon-ng.
6. After the installation of modules, type the `modules search` command and press **Enter**. This displays all the modules available in recon-ng.
7. You will be able to perform network discovery, exploitation, reconnaissance, etc. by loading the required modules.
8. Type the `workspaces` command and press **Enter**. This displays the commands related to the workspaces.
9. Create a workspace in which to perform network reconnaissance. In this task, we shall be creating a workspace named **CEH**.
10. To create the workspace, type the command `workspaces create CEH` and press Enter. This creates a workspace named CEH.
11. Enter `workspaces list`. This displays a list of workspaces (along with the workspace added in the previous step) that are present within the workspaces databases.
12. Add a domain in which you want to perform network reconnaissance.
13. Type the command `db insert domains` and press **Enter**.
14. In the **domain (TEXT)** option type `certifiedhacker.com` and press **Enter**. In the **notes (TEXT)** option press **Enter**. This adds certifiedhacker.com to the present workspace.
15. You can view the added domain by issuing the `show domains` command.
16. Harvest the hosts-related information associated with certifiedhacker.com by loading network reconnaissance modules such as brute_hosts, Netcraft, and Bing.
17. Type `modules load brute` and press **Enter** to view all the modules related to brute forcing. In this task, we will be using the **recon/domains-hosts/brute_hosts** module to harvest hosts.
18. To load the **recon/domains-hosts/brute_hosts** module, type the `modules load recon/domains-hosts/brute_hosts` command and press **Enter**.
19. Type `run` and press **Enter**. This begins to harvest the hosts.
20. Observe that hosts have been added by running the recon/domains-hosts/brute_hosts module.
21. You have now harvested the hosts related to certifiedhacker.com using the brute_hosts module. You can use other modules such as Netcraft and Bing to harvest more hosts.

![image](https://github.com/user-attachments/assets/0e0e58c3-1ed9-46ff-8511-1796b351b31a)

Now, perform a reverse lookup for each IP address (the IP address that is obtained during the reconnaissance process) to resolve to respective hostnames.

1. Type `modules load reverse_resolve` command and press **Enter** to view all the modules associated with the reverse_resolve keyword. In this task, we will be using the **recon/hosts-hosts/reverse_resolve** module.
2. Type the `modules load recon/hosts-hosts/reverse_resolve` command and press **Enter** to load the module.
3. Issue the `run` command to begin the reverse lookup.
4. Once done with the reverse lookup process, type the `show hosts` command and press **Enter**. This displays all the hosts that are harvested so far.
5. Now, type the `back` command and press **Enter** to go back to the CEH attributes terminal.

Now, that you have harvested several hosts, we will prepare a report containing all the hosts.
1. Type the `modules load reporting` command and press **Enter** to view all the modules associated with the reporting keyword. In this lab, we will save the report in HTML format. So, the module used is **reporting/html**.
2. Type the `modules load reporting/html` command and press **Enter**.
3. Observe that you need to assign values for **CREATOR** and **CUSTOMER** options while the **FILENAME** value is already set, and you may change the value if required.
4. Type:

- `options set FILENAME /home/attacker/Desktop/results.html` and press **Enter**. By issuing this command, you are setting the report name as results.html and the path to store the file as **Desktop**.
- `options set CREATOR [your name]` (here, Jason) and press **Enter**.
- `options set CUSTOMER Certifiedhacker Networks` (since you have performed network reconnaissance on certifiedhacker.com domain) and press **Enter**.

![image](https://github.com/user-attachments/assets/7a646524-a702-4948-98ae-35bec6537556)

5. `run`
6. The generated report is saved to **/home/attacker/Desktop/**.
7. Click **Places** from the top-section of the **Desktop** and click **Home Folder** from the drop-down options.
8. The **attacker** window appears.
9. In the **attacker** window, double-click **Desktop**.
10. **Desktop** window appears, right-click on the **results.html file**, click on O**pen With**, and select the **Firefox browser** from the available options.
11. The generated report appears in the **Firefox** browser, displaying the summary of the harvested hosts.
12. You can expand the **Hosts** node to view all the harvested hosts.

Until now, we have used the Recon-ng tool to perform network reconnaissance on a target domain. Now, we will use Recon-ng to gather personnel information.

1. `sudo su`
2. `cd`
3. `recon-ng`
4. Add a workspace by issuing the command `workspaces create reconnaissance` and press **Enter**. This creates a workspace named reconnaissance.
5. Set a domain and perform footprinting on it to extract contacts available in the domain.
6. Type modules `load recon/domains-contacts/whois_pocs` and press **Enter**. This module uses the ARIN Whois RWS to harvest POC data from Whois queries for the given domain.
7. Type the `info command` and press **Enter** to view the options required to run this module.
8. Type `options set SOURCE facebook.com` and press **Enter** to add facebook.com as a target domain.
9. `run`

Until now, we have obtained contacts related to the domains. Note down these contacts’ names. Close all the open windows.

1. `sudo su`
2. `cd`
3. `recon-ng`
4. To extract a list of subdomains and IP addresses associated with the target URL, we need to load the **recon/domains-hosts/hackertarget** module.
5. Type the `modules load recon/domains-hosts/hackertarget` command and press **Enter**.
6. Type the `options set SOURCE certifiedhacker.com` command and press **Enter**.
7. Type the `run` command and press **Enter**. The recon/domains-hosts/hackertarget module searches for list of subdomains and IP addresses associated with the target URL and returns the list of subdomains and their IP addresses.

**2. Maltego**














