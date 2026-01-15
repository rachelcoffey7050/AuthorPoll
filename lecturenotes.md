# Intro Principles
## Jan 8: Intro
Introduced the project and learned about Git and GitHub.
Useful references include this helpful [guide](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) to writing in github.
## Jan 10: readings
Command line hints:
- echo - Output the parameters of the command
- cd - Change directory
- mkdir - Make directory
- rmdir - Remove directory
- rm - Remove file(s)
- mv - Move file(s)
- cp - Copy files
- ls - List files
- curl - Command line client URL browser
- grep - Regular expression search
- find - Find files
- top - View running processes with CPU and memory usage
- df - View disk statistics
- cat - Output the contents of a file
- less - Interactively output the contents of a file
- wc - Count the words in a file
- ps - View the currently running processes
- kill - Kill a currently running process
- sudo - Execute a command as a super user (admin)
- ssh - Create a secure shell on a remote computer
- scp - Securely copy files to a remote computer
- history - Show the history of commands
- ping - Check if a website is up
- tracert - Trace the connections to a website
- dig - Show the DNS information for a domain
- man - Look up a command in the manual
## Jan 13 - Development Environment
### History of the web

There was redundancy built in by the department of defense.

More computers in this classroom than on the internet in 1973.

The Web Father - Tim Berners-Lee. Sharing papers over the internet. Took TCP and DNS ideas and made the world wide web. 
stml from the publishing industry was adapted to html

Hakin Wium Lie thought html was ugly so he created CSS for styling and animation.
Go play with it! Revert back with git if you mess it up.

Brendan Eich - Javascript. Makes things interactive. "Always bet on JS." 

### Asking Questions
In order to succeed in this class, you need to know how to ask questions. Ask yourself first (use your brain), then Web/AI, Peers, TA, Instructor.
Guidelines for getting help:
- don't use anything you don't understand
- Ask AI to explain, _then rewrite it from scratch_
- Ask AI to critique your code

### Editors
*Look up how to do multiple select in VS Code
Console - navigates the disk, runs console applications, run scripts. (git bash)
vi/vim is on everyone's computers. Important to know.

# Server
Tech stack

## Jan 15
Upgrade to paid plan in AWS

### How does the internet work?
user, facilitator, website
Layers
- Application (HTTPS or SSH) - functionality like web browsing
- Transport (TCP/UDP) - packet delivery (make sure they get there and get there in order) UDP is fast (good for streaming), TCP will get everything correct
- Internet (IP) - Establishing connections, routing
- Link (Fiber, Hardware) physical connections

When you connect, you look up the IP address and it looks up address in domain name list. You are also talking to the webserver to actally get you to the correct address. 

Use nslookup (your website) to look for more info. And there is a command that starts with who, and dns

**Domain names:** subdomain.secondary.top. Root is secondary (sld) and top (tld). localhost (127.0.0.1) - talking to yourself.

DNS record type - basically you can control where things will take you
- A/AAAA - AAAA has a lot more than A. It brings you directly to the site.
- CNAME - an alias that brings you to something else before bringing you to an IP address.

Different organizations own the top level domain, and you are leasing from them

**Renting a Sever:** EC2 -> instances -> launch an instance. Name it something specific like byu-cs260-webserver. Follow the instructions. Make sure you are in N Virginia. 
network settings - allow SSH, allow traffic from the internet.

Caddy - looks at the request and decides where it should go. Set up for on port 4000 it goes to startup and port 3000 it goes to simon. TELL IT WHAT YOUR DOMAIN NAME IS. 'your domain name here'

HTTPS - you need a host name. But Caddy takes care of everything else for you. sudo service restart or something like that.


