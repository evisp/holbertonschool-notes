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

```console
sudo mkdir -p /var/www/example.com/html
sudo mkdir -p /var/www/test.com/html
```

- We can use the `$USER` environmental variable to assign ownership to the account that we are currently signed in on

```console
sudo chown -R $USER:$USER /var/www/example.com/html
sudo chown -R $USER:$USER /var/www/test.com/html
```

- We can change access rights accordingly using

```console
sudo chmod -R 755 /var/www
```

### Creating Sample Pages for Each Site

- Let’s create a default page for each of our sites

```console
nano /var/www/example.com/html/index.html
```

- Inside the file, we’ll create a really basic file that indicates what site we are currently accessing

```html
<html>
    <head>
        <title>Welcome to Example.com!</title>
    </head>
    <body>
        <h1>Success! The example.com server block is working!</h1>
    </body>
</html>
```

### Creating Server Block Files for Each Domain

- Now that we have the content we wish to serve, we need to create the server blocks that will tell Nginx how to do this
- Nginx contains one server block called `default` which we can use as a template for our own configurations

#### Creating the First Server Block File

- We create the file and open it with sudo privileges

```console
sudo cp /etc/nginx/sites-available/default /etc/nginx/sites-available/example.com
sudo nano /etc/nginx/sites-available/example.com
```

- First, we need to look at the listen directives. Only one of our server blocks on the server can have the `default_server` option enabled. This specifies which block should serve a request if the server_name requested does not match any of the available server blocks.
- You can choose to designate one of your sites as the “`default`” by including the `default_server` option in the listen directive, or you can leave the default server block enabled
- we’ll leave the default server block in place to serve non-matching requests, so we’ll remove the `default_server` from this and the next server block
- The next thing we’re going to have to adjust is the document root, specified by the `root` directive. Point it to the site’s document root that you created:

```console
server {
        listen 80;
        listen [::]:80;

        root /var/www/example.com/html;

}
```

- Next, we need to modify the server_name to match requests for our first domain

```console
server {
        listen 80;
        listen [::]:80;

        root /var/www/example.com/html;
        index index.html index.htm index.nginx-debian.html;

        server_name example.com www.example.com;

        location / {
                try_files $uri $uri/ =404;
        }
}
```

### Enabling your Server Blocks and Restart Nginx

- We can do this by creating symbolic links from these files to the `sites-enabled` directory, which Nginx reads from during startup.

```console
sudo ln -s /etc/nginx/sites-available/example.com /etc/nginx/sites-enabled/
sudo ln -s /etc/nginx/sites-available/test.com /etc/nginx/sites-enabled/
```

- Restart Nginx to enable your changes:

```console
sudo systemctl restart nginx
```

## Root and subdomain

### What's an internet domain?

- An internet domain is the identity or representation (in the form of letters) of an IP address
- This is an example of a root domain: `mycompany.com`

### What’s a subdomain?

- This is an example of a subdomain: `home.mycompany.com`
- A subdomain belongs to the root domain. The subdomain name comes before the root domain name and is separated from it by a dot

### A path / subfolder

- This is an example of a subdomain with a path: `home.mycompany.com/about`

## HTTP Requests

| Method      | Description |
| ----------- | ----------- |
| Get 	      | used to retrieve information from the given server using a given URI       |
| Head	      | Same as GET, but transfers the status line and header section only        |
| Post	      | A POST request is used to send data to the server        |
| Put	      | Replaces all current representations of the target resource with the uploaded content.       |
| Delete      | Removes all current representations of the target resource given by a URI        |
| Connect     | Establishes a tunnel to the server identified by a given URI |

## HTTP Redirection

- Redirection is the process of forwarding one URL to a different URL.
- A redirect is a way to send both users and search engines to a different URL from the one they originally requested
- Types of redirect
  - 301, "Moved Permanently"—recommended for SEO
  - 302, "Found" or "Moved Temporarily"
  - Meta Refresh

## Not found HTTP response code

- `HTTP 404`, `404 not found`, `404`, `404 error`, `page not found` or `file not found` error message is a hypertext transfer protocol (HTTP) standard response code, to indicate that the browser was able to communicate with a given server, but the server could not find what was requested

## Log files on Linux

- All logs are stored in `/var/log` directory under Ubuntu

## Get domain from .tech (task #2 from 0x0C. Web server project)

- Go to Intranet and find **My tools**
- **Coupons** then click `request my coupons` (It will show a text containing numbers and characters)
- Click `.TECH domains` which will redirect you to [get.tech](get.tech) website
- In the search box enter the domain you want for example (someone.tech) and press Enter
- Click the shop icon 🛒 then click on **PROCEED**
- Click **PROCEED** again in the end of the page
- Remove **Privacy Protection**
- In the **Have a coupon?** section click **Remove**
- Copy the coupon code from the step 2
- Enter the coupon code in the **Coupon code** box and click **Apply**
- The total of domain will be $0.00
- Then click **PLACE ORDER** button
- Create an account
- Confirm the email account

## Configuration of DNS record of an A entry

- Go to [get.tech](get.tech)
- Login to your account
- Click on **My account**
- Enter your domain (e.g someone.tech) to **Jump to Domain** section then press Enter
- Go to the end of the page
- To the **DNS Management** section click on **Manage DNS**
- Click **Add A Record** button
- In the **Destination IPv4 Address** enter the IP address of your web-01 server then click **Add Record** button
