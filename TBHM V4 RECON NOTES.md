## Project Tracking
- [xmind](https://xmind.app/)
- [Obsidian](https://obsidian.md/)
- Vim 
`Use whatever works for you? Obsidan rocks btw`
## Mission
- Wide Recon
	Discovering as many assets related to the target as possible. 
	Make sure these assets are in scope before testing. 

## Scope Domains
-  See Program Details.
	- To have an idea of the seed/root domains. 

##  Acquisitions
- [Crrunchbase](https://www.crunchbase.com/)
- Wikipedia
## ASN Enumeration
- [bgb.he.net](https://bgb.he.net)
- [asnlookup.com](https://asnlookup.cm)
- CLI 
	- [asnlookup.py](https://github.com/dspruell/aslookup)
		`A problem with CLI is that you return records from another org that contain the searched keyword.`
		`Start with the gui?`
- #### Enumeration of ASN
	- amass intel -asn <asn_here>
	- ... 
## Reverse Whois
[whoxy.com](https://www.whoxy.com/)
- CLI 
	- [DOMLink](https://github.com/vysecurity/DomLink)
### Ad/ Analytic Trackers
[builtwith.com](https://builtwith.com/)
### Google-fu
	- Copyright text
	- Terms of Service
	- Privacy Text 
#### Shodan 

## Subdomain Enumeration
- Subdomain Scrapping
	- [amass](https://github.com/owasp-amass/amass)
	- [subfinder](https://github.com/projectdiscovery/subfinder) ++
	-  [github-subdomains.py](https://github.com/gwen001/github-search/blob/master/github-subdomains.py)
	-  [shosubgo](https://github.com/incogbyte/shosubgo)
	- [cloudranges](https://github.com/pry0cc/cloud-ranges) 
- Subdomain  Bruteforce
	- amass
		- `amass enum -brute -d domain.com -rf resolvers.txt -w bruteforce.list`
	- [shuffledns](https://github.com/projectdiscovery/shuffledns)
		- `shuffledns -d domain.com -w words.txt -r resolvers.txt`
	-  Wordlists 
		- [jhaddix-all.txt](https://gist.github.com/jhaddix/f64c97d0863a78454e44c2f7119c2a6a)
		- [commonspeak2](https://github.com/jhaddix/tbhm/blob/master/v4/all2.txt)
- Linked JS Discovery
	- Turn off passive scanning  
	- Set forms auto to submit (if you’re feeling frisky)  
	- Set scope to advanced control and use “keyword” of target name (not a normal FQDN)  
	- Walk+browse main site, then spider all hosts recursively!  

## Alteration Scanning
- [altdns](https://github.com/infosec-au/altdns)
	- WAF Bypsass? 

# Others 
### Port Analysis
- [RustScan](https://github.com/RustScan/RustScan)
- [masscan](https://github.com/robertdavidgraham/masscan)

	 [Brutespray](https://github.com/x90skysn3k/brutespray)
### Github Dorking
- [Jhaddix's Github Dorkring](https://gist.github.com/jhaddix/1fb7ab2409ab579178d2a79959909b33)
- ......

### Screenshots 
- [EyeWitness](https://github.com/RedSiege/EyeWitness)
- [Aquatone](https://github.com/michenriksen/aquatone)
### Subdomain Takeover
- [can-i-take-over-xyz](https://github.com/EdOverflow/can-i-take-over-xyz)

### Auttomation ++
- DYOR :) 