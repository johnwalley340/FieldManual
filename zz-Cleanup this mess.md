Reconnaissance
==============
Created Monday 27 January 2020

##### Usernames/Passwords
Begin with hunter.io when provided with a domain to evaluate.
https://hunter.io/search
run breach-parse.sh 

##### Subdomins & Fingerprinting
Hunt out all subsomains
theHarverstor
Will need to set up API keys as you go.

sublist3r
sublist3r -d <domain name>
sublist3r will allow you to improve by increaseing the threads with the -t switch.
tomnomnomnom http

crt.sh
https://crt.sh
Thsi will find certificates for more subdomains. 

OWASP Amass
amass -d <domain>
see amass --help

BuiltWith
https://builtwith.com
looking for frameworks. 

Wappalizer (this is more active than passive)
Dont for get yout built in tool wappalizer.

Whatweb
whatweb <url>

BurpSuite
Passive in the  beginning. Look at heeders 

Google Foo
google google search operators
site: domain
- removes a word such as -www, -ir
filetype: <type> 

Social Media (linkedIn, Twitter, Facebook, etc.)
Create bogus profiles for information gathering.
Look at images for badges, documents, desk pictures etc. 