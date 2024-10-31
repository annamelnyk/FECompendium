# How Internet works

(https://developer.mozilla.org/en-US/docs/Learn/Common_questions/How_does_the_Internet_work)

The **Internet** is a large network of computers which communicate all together. (1980)
**A simple network** - When two computers need to communicate, you have to link them, either physically (usually with an Ethernet cable) or wirelessly (for example with Wi-Fi or Bluetooth systems). All modern computers can sustain any of those connections.
To create a network of many computers - needed bunch of cables. To solve this problem, each computer on a network is connected to a special tiny computer called a **router** (has switch port). This router has only one job: it makes sure that a message sent from a given computer arrives at the right destination computer.
**A network of networks** - By connecting computers to routers, then routers to routers, we are able to scale infinitely. In such way we can only connect specific computers. The telephone infrastructure already connects your house with anyone in the world so it is the perfect wire we need. To connect our network to the telephone infrastructure, we need a special piece of equipment called a modem. This modem turns the information from our network into information manageable by the telephone infrastructure and vice versa. So we are connected to the telephone infrastructure. The next step is to send the messages from our network to the network we want to reach. To do that, we will connect our network to an **Internet Service Provider (ISP)**.
An ISP is a company that manages some special routers that are all linked together and can also access other ISPs' routers. So the message from our network is carried through the network of ISP networks to the destination network. **The Internet consists of this whole infrastructure of networks.**

**Finding computers**
If you want to send a message to a computer, you have to specify which one. Thus any computer linked to a network has a unique address that identifies it, called an "IP address" (where IP stands for Internet Protocol). It's an address made of a series of four numbers separated by dots, for example: 192.168.2.10.
To make things easier, we can alias an IP address with a human-readable name called a **domain name**. For example (at the time of writing; IP addresses can change) **google.com** is the domain name used on top of the IP address 142.250.190.78. So using the domain name is the easiest way for us to reach a computer over the Internet.

**Internet and the web**
When we browse the Web with a Web browser, we usually use the domain name to reach a website. Does that mean the Internet and the Web are the same thing? It's not that simple. As we saw, the Internet is a technical infrastructure which allows billions of computers to be connected all together. Among those computers, some computers (called Web servers) can send messages intelligible to web browsers. **The Internet is an infrastructure, whereas the Web is a service built on top of the infrastructure.** It is worth noting there are several other services built on top of the Internet

# How the web works

(https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/How_the_Web_works)
**Clients and servers** - Computers connected to the internet are called clients and servers.
**Clients** are the typical web user's internet-connected devices (for example, your computer connected to your Wi-Fi, or your phone connected to your mobile network) and web-accessing software available on those devices (usually a web browser like Firefox or Chrome).
**Servers** are computers that store webpages, sites, or apps. When a client device wants to access a webpage, a copy of the webpage is downloaded from the server onto the client machine to be displayed in the user's web browser.

**Your internet connection**: Allows you to send and receive data on the web. It's basically like the street between your house and the shop.
**TCP/IP:** Transmission Control Protocol and Internet Protocol are communication protocols that define how data should travel across the internet. This is like the transport mechanisms that let you place an order, go to the shop, and buy your goods. In our example, this is like a car or a bike (or however else you might get around).
**DNS:** Domain Name System is like an address book for websites. When you type a web address in your browser, the browser looks at the DNS to find the website's IP address before it can retrieve the website. The browser needs to find out which server the website lives on, so it can send HTTP messages to the right place (see below). This is like looking up the address of the shop so you can access it.
**HTTP:** Hypertext Transfer Protocol is an application protocol that defines a language for clients and servers to speak to each other. This is like the language you use to order your goods.
**Component files:** A website is made up of many different files, which are like the different parts of the goods you buy from the shop. These files come in two main types:

- **Code files:** Websites are built primarily from HTML, CSS, and JavaScript, though you'll meet other technologies a bit later.
- **Assets:** This is a collective name for all the other stuff that makes up a website, such as images, music, video, Word documents, and PDFs.

**_Order in which component files are parsed_**
When browsers send requests to servers for HTML files, those HTML files often contain <link> elements referencing external CSS stylesheets and <script> elements referencing external JavaScript scripts. It's important to know the order in which those files are parsed by the browser as the browser loads the page:

- The browser parses the HTML file first, and that leads to the browser recognizing any <link>-element references to external CSS stylesheets and any <script>-element references to scripts.

- As the browser parses the HTML, it sends requests back to the server for any CSS files it has found from <link> elements, and any JavaScript files it has found from <script> elements, and from those, then parses the CSS and JavaScript.

- The browser generates an in-memory DOM tree from the parsed HTML, generates an in-memory CSSOM structure from the parsed CSS, and compiles and executes the parsed JavaScript.

- As the browser builds the DOM tree and applies the styles from the CSSOM tree and executes the JavaScript, a visual representation of the page is painted to the screen, and the user sees the page content and can begin to interact with it.

**Packets explained**
Earlier we used the term "packets" to describe the format in which the data is sent from server to client. What do we mean here? Basically, when data is sent across the web, it is sent in thousands of small chunks. There are multiple reasons why data is sent in small packets. They are sometimes dropped or corrupted, and it's easier to replace small chunks when this happens. Additionally, the packets can be routed along different paths, making the exchange faster and allowing many different users to download the same website at the same time. If each website was sent as a single big chunk, only one user could download it at a time, which obviously would make the web very inefficient and not much fun to use.

# Terminology

- The **internet** is worldwide, and **Ethernet** is local.
