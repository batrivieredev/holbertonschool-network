## Resources

**Read or watch**:

*   [What is localhost](/rltoken/7n2kKjq50U_Uv-TrEK-NUA "What is localhost")
*   [What is 0.0.0.0](/rltoken/1efC1iImna8ubDSgokLbpQ "What is 0.0.0.0")
*   [What is the hosts file](/rltoken/6o7mmDL8joIrC5DXNRSnKw "What is the hosts file")
*   [Netcat examples](/rltoken/_TN2G4Djh-f7MSukzToXpw "Netcat examples")

**man or help**:

*   `ifconfig`
*   `telnet`
*   `nc`
*   `cut`

## Learning Objectives

At the end of this project, you are expected to be able to [explain to anyone](/rltoken/uKUo9khaCQlS8vVxhZQXiQ "explain to anyone"), **without the help of Google**:

### General

*   What is localhost/127.0.0.1
*   What is 0.0.0.0
*   What is `/etc/hosts`
*   How to display your machine’s active network interfaces

## Requirements

### General

*   Allowed editors: `vi`, `vim`, `emacs`
*   All your files will be interpreted on Ubuntu 20.04 LTS
*   All your files should end with a new line
*   A `README.md` file, at the root of the folder of the project, is mandatory
*   All your Bash script files must be executable
*   Your Bash script must pass `Shellcheck` (version `0.7.0` via `apt-get`) without any errors
*   The first line of all your Bash scripts should be exactly `#!/usr/bin/env bash`
*   The second line of all your Bash scripts should be a comment explaining what is the script doing

## Tasks

### 3.



Write a Bash script that configures an Ubuntu server with the below requirements.

Requirements:

*   `localhost` resolves to `127.0.0.2`
*   `facebook.com` resolves to `8.8.8.8`.

Example:
```
sylvain@ubuntu$ ping localhost
PING localhost (127.0.0.1) 56(84) bytes of data.
64 bytes from localhost (127.0.0.1): icmp\_seq=1 ttl=64 time=0.012 ms
^C
--- localhost ping statistics ---
1 packets transmitted, 1 received, 0% packet loss, time 0ms
rtt min/avg/max/mdev = 0.012/0.012/0.012/0.000 ms
sylvain@ubuntu$
sylvain@ubuntu$ ping facebook.com
PING facebook.com (157.240.11.35) 56(84) bytes of data.
64 bytes from edge-star-mini-shv-02-lax3.facebook.com (157.240.11.35): icmp\_seq=1 ttl=63 time=15.4 ms
^C
--- facebook.com ping statistics ---
1 packets transmitted, 1 received, 0% packet loss, time 0ms
rtt min/avg/max/mdev = 15.432/15.432/15.432/0.000 ms
sylvain@ubuntu$
sylvain@ubuntu$ sudo ./0-change\_your\_home\_IP
sylvain@ubuntu$
sylvain@ubuntu$ ping localhost
PING localhost (127.0.0.2) 56(84) bytes of data.
64 bytes from localhost (127.0.0.2): icmp\_seq=1 ttl=64 time=0.012 ms
64 bytes from localhost (127.0.0.2): icmp\_seq=2 ttl=64 time=0.036 ms
^C
--- localhost ping statistics ---
2 packets transmitted, 2 received, 0% packet loss, time 1000ms
rtt min/avg/max/mdev = 0.012/0.024/0.036/0.012 ms
sylvain@ubuntu$
sylvain@ubuntu$ ping facebook.com
PING facebook.com (8.8.8.8) 56(84) bytes of data.
64 bytes from facebook.com (8.8.8.8): icmp\_seq=1 ttl=63 time=8.06 ms
^C
--- facebook.com ping statistics ---
1 packets transmitted, 1 received, 0% packet loss, time 0ms
rtt min/avg/max/mdev = 8.065/8.065/8.065/0.000 ms
```
In this example we can see that:

*   before running the script, `localhost` resolves to `127.0.0.1` and `facebook.com` resolves to `157.240.11.35`
*   after running the script, `localhost` resolves to `127.0.0.2` and `facebook.com` resolves to `8.8.8.8`

If you’re running this script on a machine that you’ll continue to use, be sure to revert `localhost` to `127.0.0.1`. Otherwise, a lot of things will stop working!



### 4.



Write a Bash script that displays all active IPv4 IPs on the machine it’s executed on.

Example:
```
sylvain@ubuntu$ ./1-show\_attached\_IPs | cat -e
10.0.2.15$
127.0.0.1$
sylvain@ubuntu$
```
Obviously, the IPs displayed may be different depending on which machine you are running the script on.

Note that we can see our `localhost` IP :)



### 5.



Write a Bash script that listens on port `98` on `localhost`.

**Terminal 0**

Starting my script.
```
sylvain@ubuntu$ sudo ./2-port\_listening\_on\_localhost
```
**Terminal 1**

Connecting to `localhost` on port `98` using `telnet` and typing some text.
```
sylvain@ubuntu$ telnet localhost 98
Trying 127.0.0.2...
Connected to localhost.
Escape character is '^\]'.
Hello world
test
```
**Terminal 0**

Receiving the text on the other side.
```
sylvain@ubuntu$ sudo ./2-port\_listening\_on\_localhost
Hello world
test
```
For the sake of the exercise, this connection is made entirely within `localhost`. This isn’t really exciting as is, but we can use this script across networks as well. Try running it between your local PC and your remote server for fun!

As you can see, this can come in very handy in a multitude of situations. Maybe you’re debugging socket connection issues, or you’re trying to connect to a software and you are unsure if the issue is the software or the network, or you’re working on firewall rules… Another tool to add to your debugging toolbox!
Curriculum
[C#25] Foundations v2 - Part 3
Average: 99.39%
Project badge
What happens when you type google.com in your browser and press Enter
 Master
 By: Sylvain Kalache
 Weight: 1
 Manual QA review must be done (request it when you are done with the project)
Description
For this project, we expect you to look at this concept:

Technical Writing Tips and Tricks for students
Background Context
Being a Full-Stack Software Engineer means you’re comfortable interacting with any layer of the stack.

A way to easily assess this is to simply ask an engineer to explain how a software system works. They can have a general overview of the flow or can choose to dig deep in a certain area.

Let’s practice by exploring the infrastructure side (network, servers, security…) of the question.



Requirements
General
You can post your blog post on the platform of your choice, LinkedIn or Medium are good ones
A README.md file, at the root of the folder of the project, is mandatory
Tasks
0. What happens when...
mandatory
This question is a classic and still widely used interview question for many types of software engineering position. It is used to assess a candidate’s general knowledge of how the web stack works on top of the internet. One important guideline to begin answering this question is that you should ask your interviewer whether they would like you to focus in on one specific area of the workflow. For a front-end position they may want you to talk at length about how the DOM is rendering. For an SRE position they may want you to go into the load balancing mechanism.

This question is a good test of whether you understand DNS. Many software engineering candidates struggle with this concept, so if you do well on this question, you are already way ahead of the curve. If you take this project seriously and write an excellent article, it may be something that will grab the attention of future employers.

Write a blog post explaining what happens when you type https://www.google.com in your browser and press Enter.

Requirements, your post must cover:

DNS request
TCP/IP
Firewall
HTTPS/SSL
Load-balancer
Web server
Application server
Database
Publish your blog post on Medium or LinkedIn; share the URL of your blog post in your answer file and in the field below.

Please, remember that these blogs must be written in English to further your technical ability in a variety of settings.

Repo:

GitHub repository: holbertonschool-network
Directory: what_happens_when_your_type_google_com_in_your_browser_and_press_enter
File: 0-blog_post

0/8 pts
1. Everything's better with a pretty diagram
mandatory
Add a schema to your blog post illustrating the flow of the request created when you type https://www.google.com in your browser and press Enter.

The diagram should show:

DNS resolution
that the request hitting server IP on the appropriate port
that the traffic is encrypted
that the traffic goes through a firewall
that the request is distributed via a load balancer
that the web server answers the request by serving a web page
that the application server generates the web page
that the application server request data from the database
Gliffy is free and what I personally use, but feel free to use what fits you best.

Some unrelated examples:





Share the URL of your diagram image in your answer file and il the field below.

Please, remember that these blogs must be written in English to further your technical ability in a variety of settings.

Repo:

GitHub repository: holbertonschool-network
Directory: what_happens_when_your_type_google_com_in_your_browser_and_press_enter
File: 1-what_happen_when_diagram

0/7 pts
Score
Project badge
Please review all the tasks before you start the peer review.

Tasks list
Mandatory
Advanced
0. What happens when...
1. Everything's better with a pretty diagram

