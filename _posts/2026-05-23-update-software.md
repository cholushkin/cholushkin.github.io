---
layout: post
title: "Windows Setup Shouldn't Be Manual"
date: 2026-05-23
categories: [projects]
tags: [powershell, chocolatey, automation, projects]
---

# Windows Setup Shouldn't Be Manual

Reinstalling Windows always feels the same.

You spend hours reinstalling:

* Git
* Python
* VSCode
* Unity
* Blender
* terminal tools
* random utilities you forgot existed

Then later you realize:

> “Ah yes... I forgot ffmpeg again.”

So I made a small PowerShell bootstrap tool for myself:

https://github.com/cholushkin/windows-update-software

<!--more-->

What it does:

* installs packages using Chocolatey
* updates existing software
* validates package names before install
* supports package groups
* supports dry-run mode
* creates Python virtual environments automatically
* installs Python requirements
* generates logs
* safe to rerun multiple times

Example:

```powershell
.\install-packages.ps1
.\install-packages.ps1 -Groups gamedev
.\install-packages.ps1 -WhatIf
```

I mainly use it for:

* fresh Windows installs
* new workstations
* restoring dev environments
* keeping software versions consistent
* avoiding “what was that package called again?”

It’s one of those tiny tools that removes a surprising amount of friction.

Nothing revolutionary.
Just practical automation.
