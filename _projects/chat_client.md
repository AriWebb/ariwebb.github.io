---
title: "Chat Client"
date: 2022-02-28
last_modified_at: 2022-07-18
header:
  teaser: /assets/images/chat_client/signal.png
sidebar:
  - title: "Role"
    image: /assets/images/case_shiller/country.png
    text: "Completed Assignment"
  - title: "Languages"
    text: "Javascript, SubtleCrypto Library"    
  - title: "Built For"
    text: "CS 255: Cryptography Assignment"
  - text: "Time Spent: 2 weeks"
toc: true
---

# Introduction

Normally, I wouldn't include a class assignment under my personal projects tab. This implementation, though, was so cool that I couldn't resist writing a little about it. 

This is an assignment I did for [CS 255: Intro to Cryptography][stanford]. The course is taught by crypto genius Dan Boneh, who is also committed to publicizing his course content. You can find the free Coursera course [here][coursera]. I would highly reccomend signing up for the Coursera course if you have basic programming proficiency and interest in how information is secured. 

Unfortunately, I can't make my personal implementation public, as that is a violation of Stanford policies.

# Theoretical Foundations

This project tasked the student with implementing a secure end to end chat client. The client needs to have a few features including:

1. Forward Secrecy. A compromise of the system's current state (keys) cannot compromise past communications. Say your computer is taken by hackers. Your past communications must stay hidden even if the hacker sees your current key!

2. Break-in Recovery. Say an attacker compromises one side and gains all of that persons (person A's) current information. Then, later, person A regains control of their keys and sends a message unimpeded by the attacker. The attacker must not be able to decrypt any future communications.

# Implementation

When I first learned that I would have to implement a system with such specifications, I was overwhelmed. I wasn't sure how such a client could even be built. Luckily, a popular messaging app called Signal has implemented such a system using a data structure called a KDF chain. 

In short, a KDF chain works as follows. It takes in a secret KDF key and input data. It outputs another KDF key and an output key, which is used to encrypt the message. The new KDF key can then be used again to create yet another output key KDF pair, which is repeated for each message. 

One feature of KDF is that having the state of a KDF at one time tells one nothing about the prior states of it. This offers us forward security.

Another feature of KDF is that the ratcheted keys are totally unpredictable. So, if an attacker learns what the KDF is at a point in time, then it is used by the user once, then the attackers knowledge is lost.

Read more about it [here][kdf].

# Conclusion

I hope you are as impressed as I am by this cryptographic system. I learned so much from coding this up: making applications secure isn't something the average developer has to think about. Again, if you are interested in how this sytem works, you can find the full spec [here][kdf]. And, if you want to learn more about cryptography in general, sign up for Prof. Boneh's Coursera course [here][coursera]!

[stanford]: http://crypto.stanford.edu/~dabo/cs255/
[coursera]: https://www.coursera.org/learn/crypto
[kdf]: https://signal.org/docs/specifications/doubleratchet/