---
layout: post
title: "Full Width Azure Portal for Big Monitors!"
description: ""
category: 
tags: []
---
{% include JB/setup %}

**DISCLAIMER:** I work on the Azure team, but not on the portal. I think the portal is great, I just prefer a full-width layout. Use **at your own risk**.

I use the Azure portal A LOT. Since [nuget.org](nuget.org) is hosted on Azure, that's probably not a shock :). One thing I don't like (personal preference, I know some people like it) is that it's a fixed-width site. I have all this space on my monitor going unused!

<img src="/assets/2013-04-29-full-width-azure-portal-for-big-monitors/FixedWidthSadness.png" alt="Boo. Fixed Width :(" style="height: 300px;" />

You know what would look better? A full width layout:

<img src="/assets/2013-04-29-full-width-azure-portal-for-big-monitors/FullWidthHappiness.png" alt="Yay! Full Width :)" style="height: 300px;" />

Fortunately, it's easy to make it look like that, at least on Chrome. First, download the [Stylish](https://chrome.google.com/webstore/detail/stylish/fjnbnpbmkenffdnngjfgmeleoegfcffe?hl=en) extension.

![Download Stylish](/assets/2013-04-29-full-width-azure-portal-for-big-monitors/DownloadStylish.png)

Then, click the new Stylish button on your toolbar and choose "Manage installed styles"

![Click Dat Button!](/assets/2013-04-29-full-width-azure-portal-for-big-monitors/StylishButton.png)

Choose "Write new style" to go to the style editor. Enter the following CSS and mark it to run for all URLs on the domain "manage.windowsazure.com":

	#headerbar-wrapper {
		width: 100%;
		margin-left: 0;
		left: 0;
	}
	#fxshell-navpane {
		left: 0;
		margin-left: 0;
	}
	#drawer {
		margin-left: 0;
		left: 0;
		width: 100%;
	}
	#aux-foreground {
		width: 100%;
		left: 0;
		margin-left: 0;
	}

I also put it on a Gist here: [https://gist.github.com/anurse/5485124](https://gist.github.com/anurse/5485124)

Save the stylesheet, reload the portal and POOF, instant full-width layout! Enjoy!