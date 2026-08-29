---
layout: post
title: "Your game version history"
date: 2026-08-29
categories: [article]
---

> [!NOTE]
> Automate Your Unity Changelogs Like a Boss! 🚀

In my daily development workflow, I stick to a strict set of [coding conventions](https://github.com/cholushkin/dev-conventions). It's actually part of a much larger infrastructure designed for a small gamedev studio, which includes our custom `GameLib`, `rMVVM` architecture, and a bunch of handy modular tools.

Today, I want to focus on a specific part of that ecosystem: our **Version History Management System**.

![Logo](https://raw.githubusercontent.com/cholushkin/VersionHistory/master/Documentation/Logo.jpg)

<!--more-->

If you are already formatting every commit using the [Conventional Commits standard](https://github.com/cholushkin/dev-conventions/blob/master/UnityConventionalCommitSystem.md), and you actively tag your releases using [Semantic Versioning](https://github.com/cholushkin/dev-conventions/blob/master/SemanticVersioning.md) (adapted perfectly from semver.org for Unity), you are already winning. Doing this gives your project some massive benefits:

* **Crystal-Clear History:** You never have to guess what a 6-month-old commit actually did.
* **Painless Debugging:** Hunting down exactly when a specific bug was introduced becomes trivial.
* **AI-Friendly:** Standardized logs make it way easier for AI assistants to understand your project's context.
* **CI/CD Magic:** Your build pipelines can read your semantic tags to automatically trigger the right release workflows.

But on top of all those structural benefits, you unlock an absolute superpower: **you can generate your game's version history almost entirely automatically!**

It looks a little something like this:

```markdown
# CHANGELOG
All significant updates to this product will be recorded in this file.

## v0.0.2
### Features
- Better notification and reward screen
- Autokill API for ActivityService
- Dialog service implementation

### Bug Fixes
- Fixed error when deleting activity from the list

## v0.0.1
### Features
- Weather widget and Weather Service
- Added rMVVM module
- Render version history from dev menu
- **art**: integrated new UI fonts

---
© 2026 YourCompany. All rights reserved.

```


This snippet is a standard Markdown output, but the system is flexible enough to organize your history into Plain Text, HTML, or even JSON if that's what your pipeline needs. Pretty cool to get all of this automatically, right? =)

But here is the absolute tastiest part 🤤: Paired with our GameLib DevTools, we can inject this generated output *straight into the game's runtime!* You can pop open a dev-overlay while actively playing the game and instantly scroll through what was added or fixed in the exact build you are running. 

If you want to see exactly how all of this is configured, maintained, and edited under the hood, I highly recommend checking out the README in the repository:
👉 [https://github.com/cholushkin/VersionHistory](https://github.com/cholushkin/VersionHistory)

The main goal of this post is just to share the existence of this awesome tool so you can grab it and streamline your own Unity projects!