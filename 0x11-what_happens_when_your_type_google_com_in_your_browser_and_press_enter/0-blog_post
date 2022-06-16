What happens when you type google.com in your browser and press Enter
=====================================================================

![An image describing enter touch on a keyboard](https://miro.medium.com/max/1400/1*1NuSjTdxAYYaYiLjeP3avg.jpeg)

Enter key on a keyboard

> Being a Full-Stack Software Engineer means you're comfortable interacting with any layer of the stack.
>
> A way to easily assess this is to simply ask an engineer to explain how a software system works. They can have a general overview of the flow or can choose to dig deep in a certain area.

> Let's practice by exploring the infrastructure side (network, servers, security...) of the question.

Terminology
===========

It would be a harm to go further without defining essential key concepts to our topic: server, network protocol, client, http/https, dns, firewall, proxy, tls/ssl, tcp/udp...

-   **Server**

In [computing](https://en.wikipedia.org/wiki/Computing), a **server** is a piece of [computer](https://en.wikipedia.org/wiki/Computer) hardware or software ([computer program](https://en.wikipedia.org/wiki/Computer_program)) that provides functionality for other programs or devices, called "[clients](https://en.wikipedia.org/wiki/Client_(computing))".

-   **Client**

In [computing](https://en.wikipedia.org/wiki/Computing), a **client** is a piece of [computer hardware](https://en.wikipedia.org/wiki/Computer_hardware) or [software](https://en.wikipedia.org/wiki/Software) that accesses a service made available by a [server](https://en.wikipedia.org/wiki/Server_(computing)) as part of the [client--server model](https://en.wikipedia.org/wiki/Client%E2%80%93server_model) of [computer networks](https://en.wikipedia.org/wiki/Computer_network).

-   **Network Protocol**

A network protocol is an established set of rules that determine how data is transmitted between different devices in the same network.

--- HTTP ---

Hypertext Transfer Protocol (HTTP) is an application layer protocol used to transmit hypermedia documents, such as HTML. It was designed for communication between web browsers and web servers but can also be used for other purposes.

--- HTTPS ---

HTTPS (Hypertext Transfer Protocol Secure or secure hypertext transfer protocol) is an Internet communication protocol that protects the integrity and confidentiality of data during the transfer of information between the Internet user's computer and the site.

--- DNS ---

Domain name system (DNS) is the system that is used to translate human-memorable domain names like namecheap.com and hostnames like support.namecheap.com into the corresponding numeric Internet Protocol (IP) addresses as well as to identify and locate computer systems and resources on the Internet.

---TLS / SSL ---

**Transport Layer Security** (**TLS**) is a [cryptographic protocol](https://en.wikipedia.org/wiki/Cryptographic_protocols) designed to provide communications security over a computer network. The [protocol](https://en.wikipedia.org/wiki/Communication_protocol) is widely used in applications such as [email](https://en.wikipedia.org/wiki/Email), [instant messaging](https://en.wikipedia.org/wiki/Instant_messaging), and [voice over IP](https://en.wikipedia.org/wiki/Voice_over_IP), but its use in securing [HTTPS](https://en.wikipedia.org/wiki/HTTPS) remains the most publicly visible.

**. Proxy**

In [computer networking](https://en.wikipedia.org/wiki/Computer_networking), a **proxy server** is a [server application](https://en.wikipedia.org/wiki/Server_application) that acts as an [intermediary](https://en.wikipedia.org/wiki/Intermediary) between a [client](https://en.wikipedia.org/wiki/Client_(computing)) requesting a [resource](https://en.wikipedia.org/wiki/Web_resource) and the server providing that resource.

**. Load Balancing**

In [computing](https://en.wikipedia.org/wiki/Computing), **load balancing** refers to the process of distributing a set of [tasks](https://en.wikipedia.org/wiki/Task_(computing)) over a set of [resources](https://en.wikipedia.org/wiki/System_resource) (computing units), with the aim of making their overall processing more efficient.

**Scenario**
============

> Done with key concepts ? It is time to follow step-by-step what happens from the moment we type *enter to the moment we see the response of google.*

We are going to walk through 8 defined steps which are detailed as follow:

1- URL Parsing

2- DNS Lookup

3- TCP / IP

4- SSL

5- HTTPS

6- Load Balancer

7- Firewall

8- Host Server

9- Page rendering

1- URL Parsing
==============

![](https://miro.medium.com/max/1276/1*oz1W26rGL77Hso_STfQEXg.png)

URL parsing

URL parsing is a function of traffic management and load-balancing products that scan URLs to determine how to forward traffic across different links or into different servers. A URL includes a protocol identifier (http, for Web traffic) and a resource name, such as [www.microsoft.com](http://www.microsoft.com/).

2- DNS Lookup
=============

A DNS lookup, in a general sense, is the process by which a DNS record is returned from a DNS server. This is like looking up a phone number in a phone book --- that is why it is referred to as a "lookup". Interconnected computers, servers and smart phones need to know how to translate the email addresses and domain names people use into meaningful numerical addresses. A DNS lookup performs this function.

![](https://miro.medium.com/max/1400/1*yfKwsrIgreeB02WLsF0dwg.jpeg)

DNS Lookup journey

So, what exactly happened after I hit the Enter key?

1.  My **browser** looks at its DNS cache to see if it'd been there before and knew the IP address mapped to it. Let's say it didn't.
2.  My **computer** also looks into its local DNS cache to see if it knows an IP address mapped to that domain. Nope.
3.  My home **router** comes in to try its local DNS cache. Still no luck.
4.  We go out to ask my **ISP's DNS server** if that domain is in its cache. Sorry it is not there, but that recursive DNS server can help us resolve it.
5.  The resolver goes to ask the **root name servers** about the domain name, let's say it is *example.com*
6.  Root name servers know all the **TLD (top level domain) name servers**. Since we came with a *.com* domain, it forwards our query to one TLD name server that handles *.com* domains.
7.  The .com TLD name server knows the **authoritative name server** who stores DNS record for the domain *example.com* so it forwards the query ahead.
8.  The authoritative name server respond with an *A record* (address record which is an IP address) mapped to the domain name.
9.  The IP address was then passed all the way back to our browser, each one in between who has a DNS cache will cache it on the way so next time when we or someone else asks about example.com, the answer comes faster.
10. Browser opens a TCP/IP connection to the IP address, which is the address of the server hosting *example.com*, then sends an HTTP request. If the server is up and running, it sends back HTTP responses to our browser.

3- TCP / IP
===========

![TCP/IP process](https://miro.medium.com/max/868/1*AKwC9h1wKki1_dzdzOXLvA.gif)

TCP/IP process

Step 1: Establish connection
----------------------------

When two computers want to send data to each other over TCP, they first need to establish a connection using a **three-way handshake**.

Step 2: Send packets of data
----------------------------

When a packet of data is sent over TCP, the recipient must always acknowledge what they received.

Step 3: Close the connection
----------------------------

Either computer can close the connection when they no longer want to send or receive data.

Detecting lost packets
----------------------

TCP connections can detect lost packets using a timeout.

Handling out of order packets
-----------------------------

TCP connections can detect out of order packets by using the sequence and acknowledgement numbers.

4- SSL
======

![](https://miro.medium.com/max/1400/1*Y4AzZOlwNgaOrbwSDHibeg.png)

SSL handleshacke

How do SSL certificates work?
=============================

SSL works by ensuring that any data transferred between users and websites, or between two systems, remains impossible to read. It uses encryption algorithms to scramble data in transit, which prevents hackers from reading it as it is sent over the connection. This data includes potentially sensitive information such as names, addresses, credit card numbers, or other financial details.

The process works like this:

1.  A browser or server attempts to connect to a website (i.e., a web server) secured with SSL.
2.  The browser or server requests that the web server identifies itself.
3.  The web server sends the browser or server a copy of its SSL certificate in response.
4.  The browser or server checks to see whether it trusts the SSL certificate. If it does, it signals this to the webserver.
5.  The web server then returns a digitally signed acknowledgment to start an SSL encrypted session.
6.  Encrypted data is shared between the browser or server and the webserver.

5- HTTPS
========

HTTPS requires a TLS certificate to be installed on your server. You can apply certificates to different protocols, like HTTP (web), SMTP (email) and FTP. An SSL or TLS certificate works by storing your randomly generated keys (public and private) in your server. The public key is verified with the client and the private key used in the decryption process.

HTTP is just a protocol, but when paired with TLS or transport layer security it becomes encrypted.

![](https://miro.medium.com/max/1400/1*AR83GZhw_6WMuGozCtXmHQ.jpeg)

HTTPS Stack

When your browser connects to an HTTPS server, the server will answer with its certificate. The browser checks if the certificate is valid:

1.  the owner information need to match the server name that the user requested
2.  the certificate needs to be signed by a trusted certification authority

If one of these conditions is not met, the user is informed about the problem.

![](https://miro.medium.com/max/1400/1*neEbP2ZXFVasPmSPFo_J2w.png)

HTTPPS Handleshack

When HTTP is used, a series of handshakes takes place.

The initial request is sent to the server for a verification. When the server responds that it is the desired server the client then sends a hello message.

At this point the communication becomes encrypted.

Is to exchange encryption keys or ciphers.

At this point the reader communication can proceed. The initial handshakes steps take place in a matter of milliseconds.

6- load Balancer
================

![](https://miro.medium.com/max/1120/1*s2lnov3kDTN3seSpB8BWmQ.png)

Load balancing

As an organization meets demand for its applications, the load balancer plays the role of the traffic cop in the network, deciding which servers can handle that traffic. This [traffic management](https://dzone.com/articles/load-balancers-and-high-volume-traffic-management-1#:~:text=Load%20balancers%2C%20also%20referred%20to,performance%20of%20websites%20and%20applications.&text=Load%20balancers%20are%20responsible%20for%20the%20traffic%20distribution.) is intended to deliver a good user experience. Load balancers [monitor the health](https://blogs.tensult.com/2020/01/29/how-to-configure-verify-and-update-health-checks-of-classic-load-balancer/) of web servers and backend servers to ensure they can handle requests. If necessary, it removes unhealthy servers from the pool until they are restored. Some even trigger the creation of new virtualized application servers to cope with increased demand and maintain response times. The most effective load balancers operate with workloads across multiple environments (on-premises and cloud) and diverse infrastructures (bare metal servers, VMs, and containers).

A load balancer is an intermediary responsible for handling this traffic-splitting work. A load balancer is a software that can be configured either on the same server as that hosting web content or on a server all its own. One such common and free load balancer software is [HAProxy](https://www.haproxy.org/).

![](https://miro.medium.com/max/1400/1*GCvWoR1uAoF9dEPtf9cWnA.png)

Haproxy

HTTP request traffic is split up by a program such as HAProxy according to a load balancing algorithm. There are various types of load balancing algorithms, each with their own advantages and disadvantages. One such example includes round-robin load balancing, which sends requests to servers in turn according to a queue. Another is least connections, which sends a new request to the server currently handling the least number of connections. You can read about more load balancing algorithms [here](https://devcentral.f5.com/articles/intro-to-load-balancing-for-developers-ndash-the-algorithms).

7- Firewall
===========

![](https://miro.medium.com/max/636/1*exUmkkFw6shiin4xJw0-hw.png)

Firewall

Firewalls are software or hardware that work as a filtration system for the data attempting to enter your computer or network. [Firewalls scan packets for malicious code](https://www.n-able.com/blog/malware-analysis-steps) or attack vectors that have already been identified as established threats. Should a data packet be flagged and determined to be a security risk, thefirewall prevents it from entering the network or reaching your computer.

Firewall in load balancing configuration are sandwiched between Server Load Balancing systems. Traffic from the Internet is directed to one firewall within a group of firewalls. Traffic from the organization's internet work is distributed in a similar fashion.

8- Host server
==============

A hosting server is generic term for a type of server that hosts or houses websites and/or related data, applications and services. It is a remotely accessible Internet server with complete Web server functionality and resources.

A hosting server is also known as a Web hosting server.

![Lamp stack](https://miro.medium.com/max/518/1*LJOL10wI320kST6SBI0njQ.png)

Lamp stack

-   **L** --- Linux --- the operating system on which the host server runs. Pick your favorite distribution.
-   **A** --- Apache --- the HTTP web server. This is the software that handles HTTP request/response messages and ultimately delivers the static web page. Apache is the most common HTTP web server used, although others such as Nginx are equally capable.
-   **M** --- MySQL --- the database server. This is the database software, typically SQL-based, that stores information such as user accounts. MySQL is a free and popular one, but again, any database software works. A typical website will be configured with multiple database servers, with one configured as a "primary" database having exclusive write privileges whose changes are echoed out to "replicant" databases only having read privileges. This setup is referred to as a "primary-replica" model.
-   **P** --- PHP/Python --- the application server. Web servers are fine for delivering static, unchanging web pages, but lack the capability of representing dynamic content crucial to modern sites. PHP and Python are two high-level languages supported by web servers that can handle dynamic content, but other languages include JavaScript and Ruby.

Delivery of a web page works as follows:

-   A GET request is received by the web server. The web server pulls up the file configured at the given location (in our example, the HTML file configured at the root (`/`) of the machine).
-   If the file contains dynamic content, the application server is run (ie. the corresponding Python scripts are run). The result of these scripts is inserted into the web page.
-   If the dynamic content involves stored data, the Python scripts queries from the database server (probably through Python libraries such as [MySQLdb](https://mysqlclient.readthedocs.io/#) or [SQLAlchemy](https://www.sqlalchemy.org/)).
-   The web server delivers the web page.

9- Page rendering
=================

The initial status line of this response message includes a status code indicating the success of the handled request. Upon successful retrieval and delivery of the web page, the host server signals `200`. Other common status codes include `301` (page redirection) and `404` (page not found).
====================================================================================================================================================================================================================================================================================================

In the response header, the host server states information about the delivered page such as its type (HTML, in our case) and size.

Finally, in the response message body, the host server delivers the actual, entire HTML code itself. This is what the browser has been looking for since the start! Now it shows off, utilizing its HTML and CSS engines to parse the code, break it down into its Document Object Model, and render the page. Any JavaScript scripts written in the file are run. When its all said and done, Firefox displays a beauty, a joy, a realization of our dream --- the google website home page.

![](https://miro.medium.com/max/1400/1*GNMwynSjDu0eO83qjDX3jA.png)

Google homepage

Summary
=======

To summarize the whole process , the following diagram has been done for you:

![Page rendering Process explained](https://miro.medium.com/max/1400/1*50H2mSlUaGK9B6uZS072oA.png)

Page rendering process

Resources
=========

[

Client (computing) - Wikipedia
------------------------------

### In computing, a client is a piece of computer hardware or software that accesses a service made available by a server...

en.wikipedia.org

](https://en.wikipedia.org/wiki/Client_%28computing%29)

[

Client-server model - Wikipedia
-------------------------------

### Client-server model is a distributed application structure that partitions tasks or workloads between the providers of...

en.wikipedia.org

](https://en.wikipedia.org/wiki/Client%E2%80%93server_model)

[

HTTP | MDN
----------

### Hypertext Transfer Protocol (HTTP) (ou protocole de transfert hypertexte en français) est un protocole de la couche...

developer.mozilla.org

](https://developer.mozilla.org/fr/docs/Web/HTTP)

[

Sécuriser votre site à l'aide du protocole HTTPS | Google Search Central | Documentation | Google...
--------------------------------------------------------------------------------------------------

### HTTPS (Hypertext Transfer Protocol Secure ou protocole de transfert hypertexte sécurisé) est un protocole de...

developers.google.com

](https://developers.google.com/search/docs/advanced/security/https?hl=fr#:~:text=HTTPS%20%28Hypertext%20Transfer%20Protocol%20Secure,l%27internaute%20et%20le%20site.)

[

What is DNS Server (name server)? - Domains - Namecheap.com
-----------------------------------------------------------

### Learn more about What is DNS Server (name server)?. Find your answers at Namecheap Knowledge Base.

www.namecheap.com

](https://www.namecheap.com/support/knowledgebase/article.aspx/766/10/what-is-dns-server-name-server/?gclid=CjwKCAjwtIaVBhBkEiwAsr7-cxm7rDjJnEp_ToW0WvyoesaKtO_EfvBTkX4xgnB5_XhidlC1mfC1bxoC73YQAvD_BwE)

[

Transport Layer Security - Wikipedia
------------------------------------

### Transport Layer Security ( TLS) is a cryptographic protocol designed to provide communications security over a computer...

en.wikipedia.org

](https://en.wikipedia.org/wiki/Transport_Layer_Security)

[

Proxy server - Wikipedia
------------------------

### In computer networking, a proxy server is a server application that acts as an intermediary between a client requesting...

en.wikipedia.org

](https://en.wikipedia.org/wiki/Proxy_server)

[

Load balancing (computing) - Wikipedia
--------------------------------------

### In computing, load balancing refers to the process of distributing a set of tasks over a set of resources (computing...

en.wikipedia.org

](https://en.wikipedia.org/wiki/Load_balancing_%28computing%29)

[

Transmission Control Protocol (TCP) (article) | Khan Academy
------------------------------------------------------------

### Learn about the Transmission Control Protocol (TCP), a data transport protocol that works on top of the Internet...

www.khanacademy.org

](https://www.khanacademy.org/computing/computers-and-internet/xcae6f4a7ff015e7d:the-internet/xcae6f4a7ff015e7d:transporting-packets/a/transmission-control-protocol--tcp)

[

What is an SSL certificate - Definition and Explanation
-------------------------------------------------------

### An SSL certificate is a digital certificate that authenticates a website's identity and enables an encrypted...

www.kaspersky.com

](https://www.kaspersky.com/resource-center/definitions/what-is-a-ssl-certificate)[](https://www.kaspersky.com/resource-center/definitions/what-is-a-ssl-certificate)