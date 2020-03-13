---
title: "DNS Forgery"
date: 2019-05-01T22:25:58+02:00
draft: true
---


Parts:
1) Set up DNS server for custom testing domain based on that development test server.
- Get a VPS with two IP addresses.
- Get a domain with a registrar that allows to register your own nameservers (not just the domain name, but also the IP address). These are then converted into glue records.
- Test the glue records via dig
- Define a simple zone using dnserver


2) Add the second IP that will be returned for the same query within 3 seconds
- Explain how to circumvent caching - is this really necessary? Or could we just work with 0 TTL? The violation of the time of check/time of use principle implies no caching, since caching would prevent that and return the IP from the cache the second time.

