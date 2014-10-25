---
layout: post
title:  "QML Test Adapter For Visual Studio"
date:   2014-10-26 00:20:00
categories: development
---

<img src="/images/qmltestadapter.png" class="center" />

After using the GTest adapter for Visual Studio for a while, I got the idea to make my own for running QML tests. Not that I write particularly many QML tests, but more as an excuse to try to write a Visual Studio extension. It turned out to be straight forward, as there are a few good examples of test runners on GitHub already. I used the [Chutzpah Test Adapter](https://github.com/mmanela/chutzpah) as a starting point, and borrowed the solution file interaction from it.

One thing that is maybe not as intuitive as writing plugins for Visual Studio as Qt Creator (for which I wrote the Team Foundation plugin) is the MEF plugin framework. In Qt Creator, you simply inherit the correct interface and put the plugin in the correct folder and Qt Creator will call your functions as you expect. In Visual Studio, the MEF framework magically detects functionality you require from Visual Studio and injects it (for example via Importing Constructors). I had not used MEF before, so this was a bit confusing at first.

The debugging experience is very streamlined in Visual Studio - as soon as you add a VSIX project to the solution, you get a debug configuration that will launch a special "Experimental Instance" of Visual Studio with your plugin already loaded. However, for test adapters you also need to attach to 2 additional processes, the vtest.discoveryengine.x86.exe (or x64) and vtest.executionengine.x86.exe (or x64), as they carry out the actual test discovery and execution.

I have not yet added the project to the Visual Studio gallery, but the source is available on [GitHub](https://github.com/jesperhh/QmlTestAdapter). Just write me if you have trouble compiling and installing the VSIX file, then I will look into adding it to the Visual Studio gallery.