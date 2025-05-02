# Http-Assignment
 HTTP/0.9
Introduced: 1991
Key Traits:
Very simple protocol.
Only GET method supported.
No headers (only raw HTML responses).
No support for metadata or MIME types.
Stateless and short-lived (one request per connection).
Use Case: Purely static content.

 HTTP/1.0 (1996)
 As previously presented, the first version of HTTP only allowed getting information from a server. However, it became insufficient as the Internet evolved and new functionalities arose.
In this context, version 1.0 of HTTP was released in 1996, about five years after version 0.9.
Version 1.0 of HTTP brings several new utilities. Let’s see some of them
Header: only the method and the resource name composed an HTTP 0.9 request. HTTP 1.0, in turn, introduced the HTTP header, thus allowing the transmission of metadata that made the protocol flexible and extensible
Versioning: the HTTP requests explicitly informs the employed version, appending it in the request line
Status code: HTTP responses now contain a status code, thus enabling the receiver to check the request processing status (successful or failed)
Content-type: thanks to the HTTP header, in specific to the Content-Type field, HTTP can transmit other documents types than a plain HTML file
New methods: besides GET, HTTP 1.0 provides two new methods (POST and HEAD)
In summary, HTTP 1.0 got much more robust than the 0.9 version.Â The most responsible for the protocol improvements are the HTTP header and the new HTTP methods.
So, the HTTP header enabled clients to send and receive different file types and exchange relevant metadata. The new methods, in turn, enabled the clients to both recover only the metadata about a document (HEAD) and transfer data from the client to the server (POST).
Improvements:
Headers introduced for metadata (e.g., Content-Type)
Status codes (e.g., 200, 404
New methods: POST, HEAD
Explicit versioning (HTTP/1.0)
Limitation: Each request opens a new TCP connection

 HTTP/1.1 (1997)
 Version 1.1 of HTTP was released in 1997, only one year after the previous version 1.0.Â HTTP 1.1 is an enhancement of HTTP 1.0, providing several extensions.

Among the most relevant enhancements, we can cite the following:

Host header: HTTP 1.0 does not officially require the host header. HTTP 1.1 requires it by the specification. The host header is specially important to route messages through proxy servers, allowing to distinguish domains that point to the same IP
Persistent connections: in HTTP 1.0, each request/response pair requires opening a new connection. In HTTP 1.1, it is possible to execute several requests using a single connection
Continue status: to avoid servers refusing unprocessable requests,Â  now clients can first send only the request headers and check if they receive a continue status code (100)Â 
New methods: besides the already available methods of HTTP 1.0, the 1.1 version added six extra methods: PUT, PATCH, DELETE, CONNECT, TRACE, and OPTIONS
In addition to the highlighted enhancements, there are many others introduced in version 1.1 of HTTP, such as compression and decompression, multi-language support, and byte-range transfers.
Specifically, the new methods represented a real improvement in using HTTP. The PUT methods got in charge of replacing already existing resources. The PATCH method updates particular data of an already existing resource. On the other hand, DELETE removes an already existing resource.
The HTTP CONNECT can create a tunnel through a proxy server. TRACE executes a loopback test in the path from a client to the destination server. Finally, OPTIONS returns information about the available communications options with the server.

Enhancements:
Persistent connections (keep-alive)
Host header mandatory (for virtual hosting)
New methods: PUT, PATCH, DELETE, CONNECT, TRACE, OPTIONS
Supports compression, multi-language, byte ranges
100 Continue status for better flow control

 HTTP/2.0 (2015)
 HTTP version 2.0 was officially released in 2015, about eighteen years after the HTTP 1.1. Particularly, HTTP 2.0 focused on improving the protocol performance.
To do that, HTTP 2.0 implemented several features to improve connections and data exchange. Let’s see some of them:
Request multiplexing: HTTP 1.1 is a sequential protocol. So, we can send a single request at a time. HTTP 2.0, in turn, allows to send requests and receive responses asynchronously. In this way, we can do multiple requests at the same time using a single connection
Request prioritization: with HTTP 2.0, we can set a numeric prioritization in a batch of requests. Thus, we can be explicit in which order we expect the responses, such as getting a webpage CSS before its JS files
Automatic compressing: in the previous version of HTTP (1.1), we must explicitly require the compression of requests and responses. HTTP 2.0, however, executes a GZip compression automatically
Connection reset: a functionality that allows closing a connection between a server and a client for some reason, thus immediately opening a new one
Server push: to avoid a server receiving lots of requests, HTTP 2.0 introduced a server push functionality. With that, the server tries to predict the resources that will be requested soon. So, the server proactively pushes these resources to the client cache
Key Changes:
Binary protocol (not plain text)
Multiplexing: multiple requests over a single connection
Request prioritization
Automatic compression (e.g., GZip)
Server push: server can preemptively send resources
Connection reset support

 HTTP/3.0 (2020 Draft)
 HTTP 3.0 is an Internet-Draft, different from the previous HTTP versions, which were/are Request For Comments (RFC) documents of the Internet Engineering Task Force (IETF). Its first draft was published in 2020.
The main difference between HTTP 2.0 and HTTP 3.0 is the employed transport layer protocol. In HTTP 2.0, we have TCP connections with or not TLS (HTTPS and HTTP). HTTP 3.0, in turn, is designed over QUIC (Quick UDP Internet Connections).
QUIC, in short, is a transport layer protocol with native multiplexing and built-in encryption. QUIC provides a quick handshake process, besides being able to mitigate latency problems in lossy and slow connections.
In addition to the potential benefits inherited from QUIC, another relevant characteristic of HTTP 3.0 is that it always creates encrypted connections. So, it is similar to always employing HTTPS in current HTTP 2.0.
Major Shift:
Uses QUIC (based on UDP), not TCP
Built-in encryption (always HTTPS)
Native multiplexing (no head-of-line blocking like TCP)
Faster handshakes and better performance over lossy networks




Difference Table

| Feature                | HTTP/0.9 | HTTP/1.1       | HTTP/2           | HTTP/3                  |
| ---------------------- | -------- | -------------- | ---------------- | ----------------------- |
| Request Methods        | GET only | Many           | Many             | Many                    |
| Headers                | ❌        | ✅              | ✅                | ✅                       |
| Persistent Connections | ❌        | ✅              | ✅                | ✅                       |
| Multiplexing           | ❌        | ❌ (pipelining) | ✅                | ✅                       |
| Protocol Format        | Text     | Text           | Binary           | Binary                  |
| Transport Protocol     | TCP      | TCP            | TCP              | **QUIC (UDP)**          |
| Head-of-line Blocking  | ✅        | ✅              | ✅ (at TCP layer) | ❌                       |
| Encryption (TLS)       | ❌        | Optional       | Optional         | **Mandatory (TLS 1.3)** |


UseFull Links - https://www.baeldung.com/cs/http-versions
             https://www.youtube.com/watch?v=UMwQjFzTQXw
