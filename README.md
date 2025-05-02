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
Improvements:
Headers introduced for metadata (e.g., Content-Type)
Status codes (e.g., 200, 404
New methods: POST, HEAD
Explicit versioning (HTTP/1.0)
Limitation: Each request opens a new TCP connection

 HTTP/1.1 (1997)
Enhancements:
Persistent connections (keep-alive)
Host header mandatory (for virtual hosting)
New methods: PUT, PATCH, DELETE, CONNECT, TRACE, OPTIONS
Supports compression, multi-language, byte ranges
100 Continue status for better flow control

 HTTP/2.0 (2015)
Key Changes:
Binary protocol (not plain text)
Multiplexing: multiple requests over a single connection
Request prioritization
Automatic compression (e.g., GZip)
Server push: server can preemptively send resources
Connection reset support

 HTTP/3.0 (2020 Draft)
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
