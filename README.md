      Project: Networking basics #1 | Holberton Rennes, France Intranet           Cookies.set('timezone', (new Date()).getTimezoneOffset() / -60.0);

Toggle navigation[

](/)

*   [

    Help

    ](https://students-support.hbtn.io/hc)
*   [

    Projects

    ](/projects/current)
*   [

    My reports

    ](/users/my_reports)
*   [

    QA Reviews I can make

    ](/corrections/to_review)
*   [

    Mock interviews

    ](/dashboards/my_current_reefineries)
*   [

    Evaluation quizzes

    ](/dashboards/my_current_evaluation_quizzes)

* * *

*   [

    Concepts

    ](/concepts)
*   [

    Servers

    ](/servers)
*   [

    Sandboxes

    ](/user_sandboxes)
*   [

    Tools

    ](/dashboards/my_tools)

* * *

*   [

    Peers

    ](/users/peers)
*   [

    Captain's Logs

    ](/dashboards/my_captain_log)
*   [

    Officers

    ](/dashboards/my_officers)
*   [

    Speakers of the Day

    ](/dashboards/my_speakers_of_the_day)

* * *

*   [

    Slack

    ](https://holberton-school-org.slack.com)

    [

    Search

    ](#)

    [

    My Profile

    ](/users/my_profile)


[

](/)

*   [

    Help

    ](https://students-support.hbtn.io/hc)
*   [

    Projects

    ](/projects/current)
*   [

    My reports

    ](/users/my_reports)
*   [

    QA Reviews I can make

    ](/corrections/to_review)
*   [

    Mock interviews

    ](/dashboards/my_current_reefineries)
*   [

    Evaluation quizzes

    ](/dashboards/my_current_evaluation_quizzes)

* * *

*   [

    Concepts

    ](/concepts)
*   [

    Servers

    ](/servers)
*   [

    Sandboxes

    ](/user_sandboxes)
*   [

    Tools

    ](/dashboards/my_tools)

* * *

*   [

    Peers

    ](/users/peers)
*   [

    Captain's Logs

    ](/dashboards/my_captain_log)
*   [

    Officers

    ](/dashboards/my_officers)
*   [

    Speakers of the Day

    ](/dashboards/my_speakers_of_the_day)

* * *

*   [

    Slack

    ](https://holberton-school-org.slack.com)

    [

    Search

    ](#)

    [

    My Profile

    ](/users/my_profile)


Curriculum

\[C#25\] Foundations v2 - Part 3 Average: 86.67%

*   [

    \[C#25\] Foundations v2 - Part 1 Average: 92.05%



    ](/curriculums/327/observe/46657)
*   [

    \[C#25\] IBM Certificates - France Average: 25.0%



    ](/curriculums/441/observe/54238)
*   [

    \[C#25\] Foundations v2 - Part 2 Average: 100.0%



    ](/curriculums/394/observe/55193)
*   [

    \[C#25\] HBnB v2 Average: 94.33%



    ](/curriculums/392/observe/56448)
*   [

    \[C#25\] Foundations v2 - Part 3 Average: 86.67% ( Technical: 86.67% - Professional: 100.0%)



    ](/curriculums/382/observe/65785)
*   [

    \[C#25\] Portfolio Project v2 Average: 100.0%



    ](/curriculums/427/observe/66206)
*   [

    \[C#25\] RNCP 5 - Parcours de préparation Average: %



    ](/curriculums/423/observe/68502)

*   [Description](#description)
*   [Quiz](#quiz)

[Go to tasks](#)

![](https://s3.eu-west-3.amazonaws.com/hbtn.intranet.project.files/holbertonschool-sysadmin_devops/285/s7kpNYq.png)

Resources
---------

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

Learning Objectives
-------------------

At the end of this project, you are expected to be able to [explain to anyone](/rltoken/uKUo9khaCQlS8vVxhZQXiQ "explain to anyone"), **without the help of Google**:

### General

*   What is localhost/127.0.0.1
*   What is 0.0.0.0
*   What is `/etc/hosts`
*   How to display your machine’s active network interfaces

Requirements
------------

### General

*   Allowed editors: `vi`, `vim`, `emacs`
*   All your files will be interpreted on Ubuntu 20.04 LTS
*   All your files should end with a new line
*   A `README.md` file, at the root of the folder of the project, is mandatory
*   All your Bash script files must be executable
*   Your Bash script must pass `Shellcheck` (version `0.7.0` via `apt-get`) without any errors
*   The first line of all your Bash scripts should be exactly `#!/usr/bin/env bash`
*   The second line of all your Bash scripts should be a comment explaining what is the script doing

**Great!** You've completed the quiz successfully! Keep going!

#### Question #0

What is `localhost`?

*   A hostname that means _this IP_

*   A hostname that means _this computer_

*   An IP attached to a computer


#### Question #1

What is `0.0.0.0`?

*   All IPv4 addresses on the local machine

*   All the IPs

*   It means null in networking


Tasks
-----

### 0\. Change your home IP

mandatory

Write a Bash script that configures an Ubuntu server with the below requirements.

Requirements:

*   `localhost` resolves to `127.0.0.2`
*   `facebook.com` resolves to `8.8.8.8`.

Example:

    sylvain@ubuntu$ ping localhost
    PING localhost (127.0.0.1) 56(84) bytes of data.
    64 bytes from localhost (127.0.0.1): icmp_seq=1 ttl=64 time=0.012 ms
    ^C
    --- localhost ping statistics ---
    1 packets transmitted, 1 received, 0% packet loss, time 0ms
    rtt min/avg/max/mdev = 0.012/0.012/0.012/0.000 ms
    sylvain@ubuntu$
    sylvain@ubuntu$ ping facebook.com
    PING facebook.com (157.240.11.35) 56(84) bytes of data.
    64 bytes from edge-star-mini-shv-02-lax3.facebook.com (157.240.11.35): icmp_seq=1 ttl=63 time=15.4 ms
    ^C
    --- facebook.com ping statistics ---
    1 packets transmitted, 1 received, 0% packet loss, time 0ms
    rtt min/avg/max/mdev = 15.432/15.432/15.432/0.000 ms
    sylvain@ubuntu$
    sylvain@ubuntu$ sudo ./0-change_your_home_IP
    sylvain@ubuntu$
    sylvain@ubuntu$ ping localhost
    PING localhost (127.0.0.2) 56(84) bytes of data.
    64 bytes from localhost (127.0.0.2): icmp_seq=1 ttl=64 time=0.012 ms
    64 bytes from localhost (127.0.0.2): icmp_seq=2 ttl=64 time=0.036 ms
    ^C
    --- localhost ping statistics ---
    2 packets transmitted, 2 received, 0% packet loss, time 1000ms
    rtt min/avg/max/mdev = 0.012/0.024/0.036/0.012 ms
    sylvain@ubuntu$
    sylvain@ubuntu$ ping facebook.com
    PING facebook.com (8.8.8.8) 56(84) bytes of data.
    64 bytes from facebook.com (8.8.8.8): icmp_seq=1 ttl=63 time=8.06 ms
    ^C
    --- facebook.com ping statistics ---
    1 packets transmitted, 1 received, 0% packet loss, time 0ms
    rtt min/avg/max/mdev = 8.065/8.065/8.065/0.000 ms


In this example we can see that:

*   before running the script, `localhost` resolves to `127.0.0.1` and `facebook.com` resolves to `157.240.11.35`
*   after running the script, `localhost` resolves to `127.0.0.2` and `facebook.com` resolves to `8.8.8.8`

If you’re running this script on a machine that you’ll continue to use, be sure to revert `localhost` to `127.0.0.1`. Otherwise, a lot of things will stop working!

**Repo:**

*   GitHub repository: `holbertonschool-network`
*   Directory: `basics_1`
*   File: `0-change_your_home_IP`

Help

×

#### Students who are done with "0. Change your home IP"

Review your work

×

#### Correction of "0. Change your home IP"

Start a new test Close

Requirement success

Requirement fail

Code success

Code fail

Efficiency success

Efficiency fail

Text answer success

Text answer fail

Skipped - Previous check failed

Get a sandbox

**0/2** pts

### 1\. Show attached IPs

mandatory

Write a Bash script that displays all active IPv4 IPs on the machine it’s executed on.

Example:

    sylvain@ubuntu$ ./1-show_attached_IPs | cat -e
    10.0.2.15$
    127.0.0.1$
    sylvain@ubuntu$


Obviously, the IPs displayed may be different depending on which machine you are running the script on.

Note that we can see our `localhost` IP :)

**Repo:**

*   GitHub repository: `holbertonschool-network`
*   Directory: `basics_1`
*   File: `1-show_attached_IPs`

Help

×

#### Students who are done with "1. Show attached IPs"

Review your work

×

#### Correction of "1. Show attached IPs"

Start a new test Close

Requirement success

Requirement fail

Code success

Code fail

Efficiency success

Efficiency fail

Text answer success

Text answer fail

Skipped - Previous check failed

Get a sandbox

**0/1** pt

### 2\. Port listening on localhost

mandatory

Write a Bash script that listens on port `98` on `localhost`.

**Terminal 0**

Starting my script.

    sylvain@ubuntu$ sudo ./2-port_listening_on_localhost


**Terminal 1**

Connecting to `localhost` on port `98` using `telnet` and typing some text.

    sylvain@ubuntu$ telnet localhost 98
    Trying 127.0.0.2...
    Connected to localhost.
    Escape character is '^]'.
    Hello world
    test


**Terminal 0**

Receiving the text on the other side.

    sylvain@ubuntu$ sudo ./2-port_listening_on_localhost
    Hello world
    test


For the sake of the exercise, this connection is made entirely within `localhost`. This isn’t really exciting as is, but we can use this script across networks as well. Try running it between your local PC and your remote server for fun!

As you can see, this can come in very handy in a multitude of situations. Maybe you’re debugging socket connection issues, or you’re trying to connect to a software and you are unsure if the issue is the software or the network, or you’re working on firewall rules… Another tool to add to your debugging toolbox!

**Repo:**

*   GitHub repository: `holbertonschool-network`
*   Directory: `basics_1`
*   File: `2-port_listening_on_localhost`

Help

×

#### Students who are done with "2. Port listening on localhost"

Review your work

×

#### Correction of "2. Port listening on localhost"

Start a new test Close

Requirement success

Requirement fail

Code success

Code fail

Efficiency success

Efficiency fail

Text answer success

Text answer fail

Skipped - Previous check failed

Get a sandbox

**0/1** pt

[Previous project](/projects/2017 "Networking basics #0")

 Next project

### Tasks list

*   [Mandatory](#mandatory)
*   [Advanced](#advanced)

0\. `Change your home IP`

1\. `Show attached IPs`

2\. `Port listening on localhost`

×

#### Recommended Sandbox

×

#### Recommended Sandboxes

[Previous project](/projects/2017 "Networking basics #0")

 Next project

×

#### Markdown Guide

#### Emphasis

\*\***bold**\*\*
\*_italics_\*
~~strikethrough~~

#### Headers

\# Big header
## Medium header
### Small header
#### Tiny header

#### Lists

\* Generic list item
\* Generic list item
\* Generic list item

1. Numbered list item
2. Numbered list item
3. Numbered list item

#### Links

\[Text to display\](http://www.example.com)

#### Quotes

\> This is a quote.
> It can span multiple lines!

#### Images

CSS style available: `width, height, opacity`

!\[\](http://www.example.com/image.jpg)
!\[\](http://www.example.com/image.jpg | width: 200px)
!\[\](http://www.example.com/image.jpg | height: 124px | width: 80px | opacity: 0.6)

#### Tables

| Column 1 | Column 2 | Column 3 |
| -------- | -------- | -------- |
| John     | Doe      | Male     |
| Mary     | Smith    | Female   |

_Or without aligning the columns..._

| Column 1 | Column 2 | Column 3 |
| -------- | -------- | -------- |
| John | Doe | Male |
| Mary | Smith | Female |

#### Displaying code

\`var example = "hello!";\`

_Or spanning multiple lines..._

\`\`\`
var example = "hello!";
alert(example);
\`\`\`

(function(i,s,o,g,r,a,m){i\['GoogleAnalyticsObject'\]=r;i\[r\]=i\[r\]||function(){ (i\[r\].q=i\[r\].q||\[\]).push(arguments)},i\[r\].l=1\*new Date();a=s.createElement(o), m=s.getElementsByTagName(o)\[0\];a.async=1;a.src=g;m.parentNode.insertBefore(a,m) })(window,document,'script','//www.google-analytics.com/analytics.js','ga'); ga('create', 'UA-67152800-6', 'auto', { userId: '10039' } ); ga('send', 'pageview'); $(document).ready(function() { ga(function(tracker) { var clientId = tracker.get('clientId'); $('.ga-client-id').val(clientId); }); });
