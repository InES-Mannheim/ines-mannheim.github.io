---
section-id: usage-java
layout: default
img: usage-java.png
category: Services
title: Usage in Java
short-title: Java
description: |
---

Currently SPA supports 3 different triple stores; namely [Jena TDB](https://jena.apache.org/documentation/tdb/), jena in-memory and [Virtuoso](http://virtuoso.openlinksw.com/). Each [SPA](../master/core/src/main/java/de/unima/core/application/SPA.java) instance is configured using the [SPABuilder](../master/core/src/main/java/de/unima/core/application/SPABuilder.java). The code below depicts how one can obtain instances.