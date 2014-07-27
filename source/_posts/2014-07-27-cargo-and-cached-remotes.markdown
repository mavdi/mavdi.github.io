---
layout: post
title: "Cargo and cached remotes"
date: 2014-07-27 21:18:16 +0100
comments: true
categories: 
---

I've been playing around with Rust and Cargo recently. Just seems like the next thing to do. Coming from ```node``` and ```npm``` world I'm used to have versioned packages. Once I noticed that versions were missing from Cargo I assumed it would always get the lastest (For now at least).

Apparently that's not the case. Once a repo is downloaded, it will be cached in your ```~/.cargo``` directory. So to get the latest repo (Which you often need to do because of nightly breaks), you either need to delete the contents of this folder or pass a ```-u``` option when building. Cargo by default does not updates remotes.

Used cached repos when possible:

```
cargo build
```

Updates all remotes:

```
cargo -u build
```