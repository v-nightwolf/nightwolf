# HTTP Protocols and major version differences

---

HTTP (Hypertext Transfer Protocol) is a set of rules that govern how data is transmitted and exchanged between a client (such as a web browser) and a server (where websites and web applications are hosted) over the internet. It forms the foundation of data communication on the World Wide Web.

There are several versions of the HTTP protocol, each with its own features and improvements. The main HTTP protocol versions include:

---

{!inpage-ads.md!}

---

**HTTP/0.9**
- Only transmitted plain HTML files
- Supported only the GET method

**HTTP/1.0**
- Introduced headers for requests and responses
- Added flexibility with headers like GET, POST, HEAD
- Included version information
- Enabled a single request/response per TCP connection
- Introduced status codes for request outcomes
- Supported various content types with the content-type header

**HTTP/1.1**
- Introduced persistent connections with keep-alive header
- Allowed multiple requests/responses per TCP connection
- Added Upgrade header for protocol preference
- Supported chunk transfers for dynamic content streaming
- Introduced features like pipelining, content negotiation, cache control

**HTTP/2**
- Introduced server push for efficient resource delivery
- Implemented multiplexing over a single TCP connection
- Used binary protocol for enhanced efficiency
- Utilized HPACK header compression algorithm
- Enhanced security, compression, and multiplexing

**HTTP/3:**
- Under development as of my knowledge cutoff date in September 2021.
- Designed to improve performance over unreliable networks, like mobile connections.
- Based on the QUIC transport protocol instead of TCP, offering better reliability and faster connections.

**Differences Impacting Performance (HTTP/2 vs HTTP/1.1):**
1. **Multiplexing:**
   - HTTP/1.1 loads resources sequentially, causing blocks.
   - HTTP/2 sends multiple data streams simultaneously, avoiding blocks.
   - Achieved through binary-coded messages and numbering.

2. **Server Push:**
   - HTTP/1.1 serves content on request, inefficient for modern pages.
   - HTTP/2 "pushes" content before client requests.
   - Allows a preview of pushed content.

3. **Header Compression:**
   - Both versions compress HTTP messages.
   - HTTP/2 employs advanced HPACK compression.
   - Eliminates redundant information, speeding up loading.

**Priority in HTTP/2 and Its Impact on Performance:**
- HTTP/2 offers detailed control over prioritization.
- Weighted prioritization enables choosing resource load order.
- Data streams are sent simultaneously (multiplexing).
- Developers assign weighted values for rendering order.

**Analogy for Multiplexing:**
- HTTP/1.1-style: One chapter at a time, confirmed receipt.
- HTTP/2-style: All chapters sent at once, numbered.
- Reader assembles chapters for faster reading.

These different versions of the HTTP protocol reflect the evolution of the web and the changing needs of users and developers. Each version aims to address various challenges and enhance the efficiency, security, and performance of data transfer over the internet.

<br>
<br>

 {!inpage-ads.md!}

---
<br>
{!footer.md!}
