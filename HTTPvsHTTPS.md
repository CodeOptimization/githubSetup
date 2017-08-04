>  “Last October, Mozilla recorded that more than half of its page loads were encrypted with HTTPS while many major sites, such as Twitter and Facebook, are using HTTPS by default. Another security researcher, Scott Helme, found that of the top million sites listed on Alexa, 18.4 percent are redirecting users’ browsers from HTTP to HTTPS. Granted, 18.4 percent may not seem like a huge segment but that’s more than double the percentage from August 2015.”

>    * By Digital Trends

# HTTP
HyperText Transfer Protocol is an __application layer protocol__, which means it focuses on how information is __presented__ to the user of
the computer but doesn’t care a whit about how data gets __transferred__. It is __stateless__, which means it doesn’t attempt to remember 
anything about the previous Web session. This is great because there is less data to send, and that means __speed__. And HTTP operates on 
__Transmission Control Protocol (TCP) Port 80 by default__, meaning your computer must send and receive data through this port to use HTTP. 
Not just any old port will do.

# HTTPS
Secure HyperText Transfer Protocol (HTTPS) is for __all practical purposes HTTP__. The chief distinction is that it uses __TCP Port 
443__ by default, so __HTTP and HTTPS are two separate communications__. HTTPS works in conjunction with another protocol, __Secure 
Sockets Layer (SSL) now known as Transport Layer Security__, to transport data safely. Remember, HTTP and HTTPS don’t care how the data 
gets to its destination. In contrast, SSL doesn’t care what the data looks like. People often use the terms HTTPS and SSL interchangeably, 
but this isn’t accurate. __HTTPS is secure because it uses SSL to move data__.  It means all communications between your browser and the 
website are encrypted. HTTPS is often used to protect highly confidential online transactions like online banking and online shopping 
order forms.

### SSL versus TLS
TLS (Transport Layer Security) and SSL (Secure Sockets Layer) are protocols that provide data encryption and authentication between 
applications and servers in scenarios where that data is being sent across an insecure network, such as checking your email (How does 
the Secure Socket Layer work?). The terms SSL and TLS are often used interchangeably or in conjunction with each other (TLS/SSL), but 
one is in fact the predecessor of the other — SSL 3.0 served as the basis for TLS 1.0 which, as a result, is sometimes referred to as 
SSL 3.1. With this said though.

### How Does HTTPS Work?
HTTPS pages typically use one of two secure protocols to encrypt communications - SSL (Secure Sockets Layer) or TLS (Transport Layer 
Security). Both the TLS and SSL protocols use what is known as an 'asymmetric' Public Key Infrastructure (PKI) system. An asymmetric 
system uses two 'keys' to encrypt communications, a 'public' key and a 'private' key. Anything encrypted with the public key can only 
be decrypted by the private key and vice-versa.

As the names suggest, the 'private' key should be kept strictly protected and should only be accessible the owner of the private key. 
In the case of a website, the private key remains securely ensconced on the web server. Conversely, the public key is intended to be 
distributed to anybody and everybody that needs to be able to decrypt information that was encrypted with the private key.


### What is a HTTPS certificate?

What is a HTTPS certificate?
When you request a HTTPS connection to a webpage, the website will initially send its SSL certificate to your browser. This certificate 
contains the public key needed to begin the secure session. Based on this initial exchange, your browser and the website then initiate 
the 'SSL handshake'. The SSL handshake involves the generation of shared secrets to establish a uniquely secure connection between 
yourself and the website.

When a trusted SSL Digital Certificate is used during a HTTPS connection, users will see a padlock icon in the browser address bar. 
When an Extended Validation Certificate is installed on a web site, the address bar will turn green.

### Why Is an SSL Certificate Required?
All communications sent over regular HTTP connections are in 'plain text' and can be read by any hacker that manages to break into the 
connection between your browser and the website. This presents a clear danger if the 'communication' is on an order form and includes 
your credit card details or social security number. With a HTTPS connection, all communications are securely encrypted. This means that 
even if somebody managed to break into the connection, they would not be able decrypt any of the data which passes between you and the 
website.

### Benefits of Hypertext Transfer Protocol Secure

The major benefits of a HTTPS certificate are:
  * Customer information, like credit card numbers, is encrypted and cannot be intercepted
  * Visitors can verify you are a registered business and that you own the domain
  * Customers are more likely to trust and complete purchases from sites that use HTTPS

#### Reference
  * https://www.entrust.com/is-it-ssl-tls-or-https/
  * https://www.instantssl.com/https-tutorials/what-is-https.html
  * https://www.instantssl.com/ssl-certificate-products/https.html
  * https://luxsci.com/blog/ssl-versus-tls-whats-the-difference.html
  * https://biztechmagazine.com/article/2017/06/http-vs-https-debate-over-only-one-helps-keep-your-business-safe-cybercrime
  
