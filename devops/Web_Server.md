# Web Server

## How the Web works

Full details are provided [here](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/How_the_Web_works)

### Clients and servers

- Computers connected to the web are called clients and servers.
- Clients are the typical web user's internet-connected devices
- Servers are computers that store webpages, sites, or apps. When a client device wants to access a webpage, a copy of the webpage is downloaded from the server onto the client machine to be displayed in the user's web browser

### The other parts of the toolbox

- **Your internet connection**: Allows you to send and receive data on the web
- **TCP/IP**: Transmission Control Protocol and Internet Protocol are communication protocols that define how data should travel across the internet
- **DNS**: Domain Name System is like an address book for websites. When you type a web address in your browser, the browser looks at the DNS to find the website's IP address before it can retrieve the website
- **HTTP**: Hypertext Transfer Protocol is an application protocol that defines a language for clients and servers to speak to each other
- **Component files**: A website is made up of many different files
  - *Code files*: Websites are built primarily from HTML, CSS, and JavaScript
  - *Assets*: This is a collective name for all the other stuff that makes up a website, such as images, music, video, Word documents, and PDFs.

### So what happens, exactly?
- The browser goes to the DNS server
- The browser sends an HTTP request message to the server
- If the server approves the client's request, it sends an Ok message
- The browser assembles the small chunks into a complete web page and displays it to you

## Nginx

- Nginx is a web server that can also be used as a reverse proxy, load balancer, mail proxy and HTTP cache.
- Nginx is easy to configure in order to serve static web content or to act as a proxy server
- Nginx can be deployed to also serve dynamic content on the network using FastCGI, SCGI handlers for scripts
- Nginx uses an asynchronous event-driven approach, rather than threads, to handle requests

## How To Set Up Nginx

(A complete guide is provided [here](https://www.digitalocean.com/community/tutorials/how-to-set-up-nginx-server-blocks-virtual-hosts-on-ubuntu-16-04))

### Setting Up New Document Root Directories

- By default, Nginx on Ubuntu 16.04 has one server block enabled at `/var/www/html`
- We will create a directory structure within `/var/www` for each of our sites.

```bash
sudo mkdir -p /var/www/example.com/html
sudo mkdir -p /var/www/test.com/html
```