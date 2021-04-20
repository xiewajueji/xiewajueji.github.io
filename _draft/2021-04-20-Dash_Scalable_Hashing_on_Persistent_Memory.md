---
layout: post
title:  "[Paper Reading] Dash: Scalable Hashing on Persistent Memory"
date:   2021-04-20 16:05:00 +0800
author: xiewajueji
tags: Paper-Reading Data-Structure Persist-Memory
---

## Problems
+ the bottle-neck of scalability is the bandwidth of pmem
+ read cost more than you think
+ bucket-level locking is bad (why?)
+ use big bucket can add locality of data
+ lose instant recovery ability

## Design
+ reduce probing
+ use lightweight concurrency control to reduce PM writes (WTF)

## Technology
+ fingerprint (one byte of hash)
+ optimistic lock
+ a new load balancing strategy
+ lazy recovery
+ use PM programming models

## Innovation
+ Dynamic Hashing on PM

## Reference
1. [intro to hash index Berkeley ppt](https://dsf.berkeley.edu/jmh/cs186/f02/lecs/lec18_2up.pdf)

## Think
+ CCEH is rubbish