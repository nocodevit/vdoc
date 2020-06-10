---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
nav_order: 1
---
# First

### Scope
This document defines the interface between the enterprise device management system and the CMP platform to render connectivity control and management to the enterprise users.

### Char set
`UTF-8` encoding is used by default

### Protocol
HTTP protocol is used to interact, using HTTP POST requests, where the HTTP packet data is in `json` format, and the relevant data in  json is signed using the HMAC-SHA1 algorithm to prevent data from being tampered during transmission.

The CMP platform provides multiple Http interface addresses (the formal access address is subsequently determined) so that the access party can send the request.

---
[Get Started](format/){: .btn .btn-purple }

