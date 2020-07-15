---
title: Changing wallpapers along with system theme
i18n-link: theme-sensitive-wp-automate
tags: automate android
---
By default, I always use dark mode on my phone, but sometimes (usually when I'm outside) I need to turn the light theme back on to actually see what's on my screen.

However, recently I realized that may not be enough, as my wallpaper stays dim, so I still have problems finding apps in the launcher.
The solution seems obvious: _change the wallpaper whenever I change the system theme._

<!--more-->

At first, I thought there would already be some app that could do this automatically.
[Turns out there _is_](https://play.google.com/store/apps/details?id=com.cannic.apps.automaticdarktheme), but what I need it for is just a tiny feature inside a more complex application.
Too much for too little.

Then, I remembered _another_, more useful app called [Automate](https://play.google.com/store/apps/details?id=com.llamalab.automate).
Although it can still do way more than just changing a wallpaper, it's not a problem because that isn't the only thing I need it for.
Also, Automatic Dark Theme doesn't allow me to change the lock screen `¯\_(ツ)_/¯`

Anyways, I ended up creating a pretty simple flow chart:

<img
	src="{{ page.blog-media }}/{{ page.i18n-link }}/flow.png"
	class="float"/>

- Wait until night mode changes
  - If it got enabled, set a dark wallpaper 
  - Otherwise, set a light wallpaper
- Repeat

Here's what it looks like:

<video controls>
	<source
		src="{{ page.blog-media }}/{{ page.i18n-link }}/demo.webm"
		type="video/webm">

	<p>Your browser doesn't support WebMs. Please <a href="{{ page.blog-media }}/{{ page.i18n-link }}/demo.webm">download the file</a> and open it with your favorite video player.</p>
	<small><i>Here's a nickel. Get yourself a better browser.</i></small>
</video>


If you want to download use this Flow, follow these steps:
1. Download the [flow file](https://mega.nz/file/jQkBiQJL#lG6rRVFWttmH0X_X66d5yz_3cyxnN0F8r3JoZHnPWoU) to your phone.
2. Download [Automate.](https://play.google.com/store/apps/details?id=com.llamalab.automate)
3. Once installed, go to Options ➡ Import and select the file with your file browser.
4. Then, select the item "Theme-sensitive wallpaper", click the Edit button and open the flow editor.
5. Open each of the _"Set image wallpaper"_ blocks and click the ▼ to select an image
(**NOTE:** The image should already be cropped and positioned to your liking).
6. Finally, exit the editor and click START.

In addition to that, if you don't want to change your lock screen, just delete the last two blocks.

That's all.
Now, every time you toggle the system dark mode, your wallpaper will change too.
Neat, huh? 😄
