---
layout: post
title:  "Team Foundation Server Plugin for Qt Creator"
date:   2014-02-04 21:15:00
categories: development
---
**Update:** Builds for Qt Creator 4.0 and later can be found on the [GitHub releases page](https://github.com/jesperhh/teamfoundation/releases).

**Update:** A new build for Qt Creator 3.6 has been added - [download]({{ site.url }}/files/TeamFoundation360.zip).

**Update:** A new build for Qt Creator 3.5 has been added - [download]({{ site.url }}/files/TeamFoundation350.zip).

**Update:** A new build for Qt Creator 3.4 has been added - [download]({{ site.url }}/files/TeamFoundation340.zip).

**Update:** A new build for Qt Creator 3.3 has been added - [download]({{ site.url }}/files/TeamFoundation330.zip).

**Update:** A new build for Qt Creator 3.2 has been added - [download]({{ site.url }}/files/TeamFoundation320.zip).

**Update:** A new build for Qt Creator 3.1 has been added.

A few days ago I published my first contribution to an open source project. I chose to make a TFS plugin for Qt Creator, which did not exist, and seemed straight forward to implement, as the command line client for TFS (TF.exe) already implements a lot of the UI needed (check-in dialog, diff, annotate via Team Foundation Power Tools). This has the downside that it does not feel as integrated as other VCS plugins for Qt Creator, but it makes the plugin a lot simpler.

Source can be downloaded at [Github](https://github.com/jesperhh/teamfoundation) and builds for Qt Creator 4.0 and later can be found on the [GitHub releases page](https://github.com/jesperhh/teamfoundation/releases).

Older binaries are available here for [Qt Creator 3.0]({{ site.url }}/files/teamfoundation.zip), [Qt Creator 3.1]({{ site.url }}/files/teamfoundation310.zip), [Qt Creator 3.2]({{ site.url }}/files/TeamFoundation320.zip),  [Qt Creator 3.3]({{ site.url }}/files/TeamFoundation330.zip),  [Qt Creator 3.4]({{ site.url }}/files/TeamFoundation340.zip), [Qt Creator 3.5]({{ site.url }}/files/TeamFoundation350.zip) and  [Qt Creator 3.6]({{ site.url }}/files/TeamFoundation360.zip). 

To install, extract files to a subfolder in Qt Creators plugin directory (example: C:\Qt\Tools\QtCreator\lib\qtcreator\plugins\TeamFoundation). For Qt Creator 3.2, the sub folder structure has been abandoned, and all plugins are stored in the same folder. For Qt 3.5 and later, the initial checkout wizard (icon.png and wizard.json) must be moved to C:\Qt\Tools\QtCreator\share\qtcreator\templates\wizards\projects\vcs\teamfoundation (or where you have installed Qt Creator).
