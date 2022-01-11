---
title: How to fix your data builds after Github's breaking change on 11 January 2022
excerpt: Details on an easy fix for data build errors you may be seeing after a GitHub policy change
date: 2022-01-11
---
GitHub has enforced a new security policy as of 11 January 2022 which may prevent your data builds from running. To see whether you are affected by the problem, take a look at the `scripts/requirements.txt` file in your data repository. (For example, [here is this file in the data starter repository](https://github.com/open-sdg/open-sdg-data-starter/blob/develop/scripts/requirements.txt)).

If you see any lines that start with...

```
git+git
```

...then you will need to change them. Instead of `git+git` you should change them to `git+https`. Here is a step-by-step for doing that:

1. Login to GitHub.com
2. Go to your data repository and navigate to the `scripts` folder, and then click on `requirements.txt`.
3. Edit the file by clicking the pencil icon
4. Change any occurrences of `git+git` to `git+https`.
5. At the bottom press "Propose changes" and then "Create pull request"
6. Wait for any automated tests to complete, and then press "Merge pull request".
