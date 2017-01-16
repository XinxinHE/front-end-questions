# front-end-questions
Front-end interview questions and answers

##What will happen after I input an url in a browser and hit enter?

1. Browser checks the DNS cache, if the destination host is existed, it uses that information; Otherwise, browser asks OS for server's IP address. 
2. OS makes a DNS lookup and replies the IP address to the browser
3. Browser opens a TCP connection to the destination host and sends the HTTP request through the TCP connection 
4. The destination server looks up the required resources and responses using HTTP protocol
5. Browser receives HTTP response and may close the TCP connection, or reuse it for another request. 
6. Browser checks if the response is a redirect or a conditional response
  1. 3xx result status codes
  2. 401 authorization request 
  3. 4xx 5XX error 
  4. 2xx normal 
7. If cacheable, response is stored in cache
8. The browser decodes response and uses HTML parser to recreate the document structure and present it on the screen. If it finds references to the external resources, such as pictures, css or javascript files, these are delivered the same way as HTML document itself. 

##What is a DNS server?

The Domain Name System (DNS) is a technology standard for managing names of public Web sites and other Internet domains. DNS technology allows you to type names into your Web browser like lifewire.com and your computer to automatically find that address on the Internet. A key element of the DNS is a worldwide collection of DNS servers.

A DNS server is any computer registered to join the Domain Name System. A DNS server runs special-purpose networking software, features a public IP address, and contains a database of network names and addresses for other Internet hosts.

##How DNS works?
The DNS is a distributed database system. Only the 13 root servers contain the complete database of names and addresses.All other DNS servers are installed at lower levels of the hierarchy and maintain only certain pieces of the overall database.

Most lower level DNS servers are owned by businesses or Internet Service Providers (ISPs). For example, Google maintains various DNS servers around the world that manage the google.com, google.co.uk, and other domains.Your ISP also maintains DNS servers as part of your Internet connection setup.

DNS is based on the client/server network architecture. Your Web browser functions as a DNS client (also called a DNS resolver) and issues requests to your Internet provider's DNS servers when navigating between Web sites.

Whenever a DNS server receives a request not in its database (such as one for a geographically distant or rarely visited Web site), it temporarily behaves as a DNS client. The server (acting on behalf of the original client) automatically passes that request to another DNS server or up to the next higher level in the server hierarchy. This process continues until the request eventually arrives at a server that has the matching name and IP address in its database - passing all the way to the root level if necessary - and the response flows back through the chain of DNS servers to the original client.

You can use publicly available DNS tools can be used to search for information related to Internet domains. Professional network administrators use these same basic tools on business networks.

##What does a doctype do?

The doctype declaration should be the very first thing in an HTML document, before the tag. The doctype declaration is not an HTML tag; it is an instruction to the web browser about what version of the markup language the page is written in.

The doctype declaration refers to a Document Type Definition (DTD). The DTD specifies the rules for the markup language, so that the browsers render the content correctly.

If the web page coding does not include a DOCTYPE Declaration (DTD or Document Type Declaration) or it is done incorrectly:

1. You will not be able to use a HTML (HyperText Markup Language) Validator to check the page coding. HTML validation requires the DOCTYPE declaration.
2. The browser rending the web page will process the coding in Quirks Mode.
3. The stylesheet may not be implemented as planned.


##What's the difference between full standards mode, almost standards mode and quirks mode?

In the old days, pages were written in two versions:

1. Netscape Navigator
2. Microsoft Internet Exploreer
	
When W3C, was introduced, browsers could not just start using them as doing so would break most existing sites on the web. Browsers introduced two modes to treat new standards compliant sites differently from old legacy sites. 

Layout engines in browsers uses three modes:
	
1. Quirks mode: In quirks mode, layout engine emulates nonstandard behavior in Navigator 4 and IE 5. These were needed for websites written before introduction of web standards. 
2. Full standard mode: In this mode, the behavior described is same as described by HTML and CSS specifications. Most of the modern browsers uses full standard mode.  
Almost standard Mode: In almost standard mode there is very small number of quirks implementation. 
