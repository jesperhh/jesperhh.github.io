---
layout: post
title:  "Team Foundation Server Plugin for Qt Creator"
date:   2014-02-04 21:15:00
categories: development
---

**Update:** A new build for Qt Creator 3.1 has been added.

**Update 2:** A bug has been fixed that prevented check out from working correctly.

A few days ago I published my first contribution to an open source project. I chose to make a TFS plugin for Qt Creator, which did not exist, and seemed straight forward to implement, as the command line client for TFS (TF.exe) already implements a lot of the UI needed (check-in dialog, diff, annotate via Team Foundation Power Tools). This has the downside that it does not feel as integrated as other VCS plugins for Qt Creator, but it makes the plugin a lot simpler.

Source can be downloaded at [Github](https://github.com/jesperhh/teamfoundation) and binaries are available for [Qt Creator 3.0]({{ site.url }}/files/teamfoundation.zip) and [Qt Creator 3.1]({{ site.url }}/files/teamfoundation310.zip). 

To install, extract files to a subfolder in Qt Creators plugin directory (example: C:\Qt\Tools\QtCreator\lib\qtcreator\plugins\TeamFoundation).