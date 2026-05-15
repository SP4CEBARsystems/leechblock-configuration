# uBlock Origin Configuration
This configuration of mine (see [my filters](#my-filters) below) allows the [uBlock origin](https://ublockorigin.com/) browser extention to block full-screen recommendations for the YouTube website on PC, mobile, and YouTube players embedded into other websites. It is recommended to combine this with browser extentions as [unhook](https://unhook.app/) or [untrap](https://untrap.app/) to block all remaining YouTube recommendations. It is recommended to use this alongside [my leechblock configuration](https://github.com/SP4CEBARsystems/leechblock-configuration/blob/main/README.md).

## Setup guide
1. Install the [uBlock Origin](https://ublockorigin.com/) browser extention
2. Open the extentions panel or open "manage extentions" (which is on [about:addons](about:addons) on browsers like Firefox) then look for uBlock Origin
3. Go to uBlock's options, you may need to click on a `...` before you can see the `options` button to go there.
4. Go to the my filters tab
5. Paste the code below (see [my filters](#my-filters)) in the big text field
6. Click `Apply changes` to save

## My filters
```
youtube.com##.ytp-fullscreen-grid-stills-container
m.youtube.com##.ytFullscreenVideoRecommendationsHost
youtube.com##:matches-path(/embed/) .ytFullscreenVideoRecommendationsHost
```

## When used with my leechblock configuration
Note that when using this alongside [my leechblock configuration](https://github.com/SP4CEBARsystems/leechblock-configuration/blob/main/README.md), you can leave the the leechblock block set that redirects YouTube to a custom embedded player website disabled as the YouTube player itself can now be considered "distraction free".

## How long will it work to banish all of YouTube's recommendations
This will work until YouTube changes their UI in a way that introduces new recommendations or changes the css class of them.

## How did I find what youtube classes to block
If youtube were to change in a way that breaks this blocking setup, you may need to be able to find these classes to block for yourself, below is the instruction to do this. I used the dev tools that come with the Firefox' browser, these are very similar to the dev tools on any other browser, the shortcuts used are likely the same across browsers.

### PC
- find the youtube page with the browser element you are interested in such as a video page,
- hold: `ctrl`+`shift `+`c` to open dev tools,
- then you can hover the mouse over the element you want to know more about,
- click it, copy its class name (like `class="ytp-fullscreen-grid-stills-container"` or `.ytp-fullscreen-grid-stills-container`),
- this can then be written like a ublock filter (like `youtube.com##.ytp-fullscreen-grid-stills-container`) and added to the ublock filter list.

### Mobile
- Use a PC (mobile dev tools browser extentions seem limited in capabillity and a bit clunky to use compared to the PC browsers' built in dev tools),
- open a browser like firefox
- press `ctrl`+`shift`+`m`,
- Find the menu to emulate a device, it is likely on the top left of your screen
- choose to emulate a mobile device (like a "galaxy note 7" but not a "1080p Full HD Television") 
- set the url of the page with the mobile device emulation to https://m.youtube.com (mobile phone youtube),
- continue with [the steps above (under "PC")](#pc)
