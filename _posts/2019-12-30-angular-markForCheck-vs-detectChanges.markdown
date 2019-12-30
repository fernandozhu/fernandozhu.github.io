---
layout: post
title: "Angular markForCheck vs detectChanges"
date: 2019-12-30 8:00 +1300
author: Fernando
categories: Web
tags: Angular
---

Run into an Angular component unit testing failure today, the solution was to replace `markForCheck()` with `detectChanges()`.

### markForCheck()

> When a view uses the OnPush (checkOnce) change detection strategy, explicitly makes the view as changed so that it can be checked again. - Angular.io

Form the definition above, ```markForCheck()``` informs Angular that there is a view change, and the change will be handled in the next change detection cycle. 

### detectChanges()

> Checks this view and its children. Use in combination with detach to implement local change detection checks. - Angular.io

Unlike ```markForCheck()```, ```detectChanges()``` fires change detection straight away, the current view and its children all get re-rendered.