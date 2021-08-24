---
layout: post
title: Screenshot a window using C#
excerpt_separator: <!--more-->
---
I'm starting a new project (will be a future post!) and one of the things I needed to get working for this project, was getting a screenshot of an individual window so that I can work perform some image detection. Whilst there was documentation on how to do this, there was a couple of 'gotcha' moments when trying to get it to function as I needed, so I created an example project that contains just the code on how to get it working.
<!--more-->
My example repo can be found [here](https://github.com/MrDKOz/example-screenshot) and takes the form of a simple Windows Console App that exists purely to take a screenshot of any current open window and save it to a [bitmap](https://en.wikipedia.org/wiki/BMP_file_format) file.

The console app will present you with a list of windows you can select, and once a valid choice has been made, it will lean on the [GetWindowRect](https://docs.microsoft.com/en-us/windows/win32/api/winuser/nf-winuser-getwindowrect) function to grab a screenshot for your viewing pleasure (make note of the fact I'm using ``MainWindowHandle`` and not just ``Handle`` during the screenshotting process).

Improvements and fixes are welcome, I hope this helps.

[![Example-Screenshot-Repo](https://img.shields.io/badge/GitHub-Repository-76189C?style=for-the-badge&logo=github)](https://github.com/MrDKOz/example-screenshot)

### A Glorious Screenshot
![Screenshot of console app](https://i.vgy.me/pOsxK5.png)