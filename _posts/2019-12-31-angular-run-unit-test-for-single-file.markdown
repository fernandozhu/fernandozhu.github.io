---
layout: post
date: 2019-12-31 07:00:00 +1300
title: "Angular: Run Unit Test for Single File"
author: Fernando
categories: Web
tags: Angular
---

If ```fdescribe``` doesn't speed up your unit testing enough, there is an another "hacky" way of running a single selected .spec file:

```npm run test -- --main <path-to-spec>```

```--main``` specifies the entry point of the unit test

