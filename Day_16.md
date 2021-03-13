# `[Scripting]` Help! Where's Santa?
## Intro

>Oh no! Santa 🎅 has taken off, leaving you -- the faithful elves behind! Can you help find Santa's location?
>
>Luckily, the elves are OSINT masters and remember a thing or two. Specifically, they remember:
>
>Santa has a webpage at MACHINE_IP/static/index.html to help lost elves find their way home. Santa never told the elves what port number the webserver is on. Can you find out?!
>This webpage has a link somewhere on it, hidden away so anyone that isn't an elf can't find it.
>Santa's Sled has an API we can talk too. The key for the API is between 0 and 100, and it's an odd number. But be careful! After an unknown number of attempts, Santa's Sled will ban your IP address. 
>
>Using your Python skills from Day 15 to find the correct key for the API.

# Tasks

### 1. What is the port number for the web server? `[**]`

This one was quite obvious. I went with port 80 as it is quite a common one, so I did a quick `nmap` scan on the server with ports 1-100. (we also know the port number is at most 99 due to only 2 digits)

```
PORT   STATE SERVICE
22/tcp open  ssh
80/tcp open  http
```

I then went to `10.10.***.***:80` in the browser and it took me to the webpage.

Answer = `80`

### 2. Without using enumerations tools such as Dirbuster, what is the directory for the API?  (without the API key) `[/***/]`

The webpage and the intro claims that there is a link hidden. Honestly I just moused over all of the links until it changed. The odd link out directs to `http://machine_ip/api/api_key` I wanted to also try doing it the Python way so I went about doing that. Unfortunately on Windows it was a bit of a pain (I think I messed up the install directories/PATH) so I moved over to my Manjaro machine.

Answer = `/api/`

### 3. Where is Santa right now?

>Okay this stumpped me for a while. The reason being, at the time this challenge was going on, 3 & 4 were in a different order. I found this out by looking at the video provided, then stopped there so not to cheat my way through. 

### 4. Find out the correct API key. Remember, this is an odd number between 0-100. After too many attempts, Santa's Sled will block you. 



```
Tags:
    python
    scripts
    osint
```