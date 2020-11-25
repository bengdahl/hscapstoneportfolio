---
title: "Interpret/Ideate"
---

[Return to Home]({{ "/" | relative_url}})


# Interpret Statement

> Software developers need an all-platform, easy to set up SSH/alternative system because I learned there is no SSH client/server that meets these requirements.

# Design Principles

The solution I'm looking for needs to satisfy the following requirements:
* ## The solution must be available on all platforms.
  
  Several devices today still may not have SSH clients, so this solution must be able to run on all platforms possible.

* ## The solution must be easy to set up and easy to use.
  
  The main drawbacks of using SSH come from the difficulties presented by setting up a port-forwarded server, and the restriction of using the user-unfriendly terminal.

* ## The solution must be secure.

  Sensitive information such as API keys and passwords will be sent over the network during remote development, so high-quality security is an absolute requirement.

# Ideas

## VPN
A program like LogMeIn Hamachi that can virtually connect two distant computers to the same virtual network could bypass the need for port-forwarding. 

### Pros:
* Easy to set up. Just install on both computers and use whatever remote tools you want as if the other computer was on the same network.

### Cons:
* High development costs due to the need to host a server for routing VPN traffic, and native clients for every platform needed.
* All traffic will be routed through a central server, which brings security concerns.

## IDE Webapp on original protocol

### Pros:
* A web-based client means anything with a browser will be able to use this tool.

### Cons:
* I am not a cryptographic expert, so an original protocol would not be secure at all.
* This requires port-forwarding to be set up on the host.

## IDE Webapp on top of SSH

This is the solution I have decided on.

### Pros:
* A web-based client means anything with a browser will be able to use this tool.
* SSH is an open-source well-documented secure protocol that has become a standard part of the internet toolkit.

### Cons:
* This requires port-forwarding to be set up on the host.
