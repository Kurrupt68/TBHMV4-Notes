## Mental Hurdles 
-  Client Reputation, does not really matter  (Google has bugs.)
-  Don't let size get you down, more complexity = more bugs 
-  Things like input acceptance probably are templates, test some = test all? 
-  Are you only touching the surface? 
## Pre Manual Testing & Automation 
-  Tech Profiling
	What exactly is the target running, built with?
	-  Browser Extensions 
		[wappalyzer](https://www.wappalyzer.com/) , [whatruns](https://www.whatruns.com/)
	-  CLI 
		[webanalyze](https://github.com/rverton/webanalyze)
		
-  Finding CVE/ Misconfig
-  Port Scan 
	`naabu, (I would rather use rustscan.)`
	-  [rustscan](https://github.com/RustScan/RustScan)
	
## Testing layers 
-  Open Ports & Services 
	-  Default Credentials?
-  Web Hosting Software 
	-  Apache, NGINX, Tomcat?
-  Application Framework 
-  Custom Code
-  Library Dependencies (`Usually JS`)
-  Integrations

## Content Discovery 
-  Based on Tech
	-  Assetnote  language specific wordlist + SecLists
 -  Commercial off the shelf (COTS) / Paid/ Open Source Software. 
	 -  Open Source :  [source2url](https://github.com/danielmiessler/Source2URL/tree/master)
	 -  CRM 
		 - Free Trial ? 
		 - Demo ? 
-  Custom Wordlist 
	-  [Burp_scavenger](https://github.com/0xDexter0us/Scavenger)
	-   [That tomnomnom's talk : Who What Where When](https://www.youtube.com/watch?v=W4_QCSIujQ4) 
-  Historical
	-  [gau](https://github.com/lc/gau)  into  [trashcompactor](https://github.com/michael1026/trashcompactor)
-  Recursion 
	-   Fuzz deeper 
	Every 401 should probably be fuzzed recursively. 
			`example.com/administrator/ 401`
			`example.com/administrator/dashboard/ 401`
			`example.com/administrator/dashboard/settings 200`
-  Mobile APIs 
	-  [ApkLeaks](https://github.com/dwisiswant0/apkleaks)
-  Change Detection
	-  Newsletter
	-  Affiliate Programs.
	-  Domain Monitoring. 
`Tools :`  [Feroxbuster](https://github.com/epi052/feroxbuster),[ffuf](https://github.com/ffuf/ffuf), [gobuster](https://github.com/OJ/gobuster)  (Use Which ever works for you xD )
`wordlists:` [Assetnote Wordlists ](https://wordlists.assetnote.com) 

## Application Analysis
Here, you want to answer the following questions based on the applications design/functionalities. 
-  1. How Does the Application Pass Data? 
		- Parameter values? or  Routes? 
-  2. How and Where does the Application talk about users? 
	-  Where ? 
		 - Cookies
		-  API Calls
	-   How? 
		 - UID 
		 - Email 
		-  Username
	        - UUID 	 
-  3. Does the Application have multi tenancy or User Levels? 
	-  Application is for Customers? 
		- e.g Sport Betting Applications. 
	- Appliction has Multiple User Levels
		- Admin (CMS/Framework)
		- Tenant (Account Admin)
		- Tenant (Account User)
		- Unauth users functionality. 
-  4. Does the Application have  unique threat model? 
	- e.g Twitch - Stream Key. 
		- Airlines - Customer PII
-  5 How does the Application handle bad inputs
	-  XSS 
	- CSRF
	- Code Injection 
-  6. Previous Security Research & Vulnerabilities ? 
	-   Hacktivity / Crowdstream / Individual write ups (Medium, Linkedin)
## Spidering
-  CLI 
	-  [Hakrawler](https://github.com/hakluke/hakrawler) / [GoSpider](https://github.com/jaeles-project/gospider)
- Burpsuite 
	- Crawler settings 
		- Do not stop due errors
		- Max Concurrent requests  ~ 75 
	- Recurisve crawl? 
## Javascript Parsing
- CLI 
	- [Xnlinkfinder](https://github.com/xnl-h4ck3r/xnLinkFinder)
- Burp 
	- GAP 
- Obfusticated ? 
	- [beautifier.io](https://beautifier.io/)
- [Retrie.js](https://github.com/RetireJS/retire.js)

## Heat Mapping  
- Places inside the application can normally happen 
- Interesting places to explore 
	- Upload Functions 
		- Integration with 3rd Party
			- XSS? 
		- Self Uploads
			- XML based (Docs/ PDF)
				- SSRF,XSS
			- Image
				- XSS,Shell
					- Name
					- Binary header
					- Metadata
		- Where is data Stored? 
			- s3 Permissions. 
	-  Content Types
		-  Look for multipart-forms
		- Look for Content type XML
		- Look for content type JSON 
	- APIs 
		- Methods
	- Account Section
		- Profile
			- Stored Xss
		- App Custom Fields
		- Integrations
			- SSRF, XSS 
	- Errors

## Parameter Analysis
- [HUNT](https://github.com/bugcrowd/HUNT)
- [XSSed.com](http://xssed.com/)
