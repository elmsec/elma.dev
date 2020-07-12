---
title: "Git: Pushing to multiple remote repositories at once"
date: 2018-08-09T05:27:18+03:00
draft: false
tags: ["git"]
categories: ["Development"]
toc: false
---

If you have more than one repository for your project and want to push your latest commits to these repositories at once, there's an easy way to do this.

Prepare the URLs of your remote repositories and use the command below for each of these URLs. Do not forget to replace the <REPO_URL> with your own URL.

```
git remote set-url --add --push origin <REPO_URL>
```

With this, you've added all the remote repository URLs into the **origin** namespace. You know what to do now:

```
git push origin master
```

It's what exactly we want. It pushes the latest committed changes to the first URL, then does the same for other URLs too. You can clearly see these steps in your terminal screen.
