# `[Web Exploit]` Someone Stole Santa's Gift List!

## Intro
>*After last year's attack, Santa and the security team have worked hard on reviving Santa's personal portal. Hence, 'Santa's forum 2' went live.*
>
>*After the attack, logs have revealed that someone has found Santa's panel on the website and logged into his account! After doing so, they were able to dump the whole gift list database, getting all the 2020 gifts in their hands. An attacker has threatened to publish a wishlist.txt file, containing all information, but happily, for us, he was caught by the CBI (Christmas Bureau of Investigation) before that. On `MACHINE_IP:8000` you'll find the copy of the website and your goal is to replicate the attacker's actions by dumping the gift list!*

## Additional Info to Note
### Challenge
>Visit the vulnerable application in Firefox, find Santa's secret login panel and bypass the login. Use some of the commands and tools covered throughout today's task to answer Questions #3 to #6.
>
>Santa reads some documentation that he wrote when setting up the application, it reads:
>
>Santa's TODO: Look at alternative database systems that are better than sqlite. Also, don't forget that you installed a Web Application Firewall (WAF) after last year's attack. In case you've forgotten the command, you can tell SQLMap to try and bypass the WAF by using `--tamper=space2comment`

# Tasks

### 1. Without using directory brute forcing, what's Santa's secret login panel? `[/**********]`

Answer = `/santapanel`

>Visit Santa's secret login panel and bypass the login using SQLi

### 2. How many entries are there in the gift database?

I can't seem to get any of this to work right now. I think I will leave Web Exploits for a bit and move on to something else. 

**I will come back to it.**

```
Tags:
SQL injection
sqlmap
burpsuite
proxy
```