# uBlock Origin Configuration
This configuration of mine (see [my filters](#my-filters)) allows the [uBlock origin](https://ublockorigin.com/) browser extention to block full-screen recommendations for the YouTube website on PC, mobile, and YouTube players embedded into other websites. It is recommended to combine this with browser extentions as [unhook](https://unhook.app/) or [untrap](https://untrap.app/) to block all remaining YouTube recommendations.

## When used with my leechblock configuration
Note that when using this alongside my leechblock configuration, you can disable the leechblock block set that redirects YouTube to a custom embedded player website as the YouTube player itself can now be considered "distraction free". 

## How long will it work to banish all of YouTube's recommendations
This will work until YouTube changes their UI in a way that introduces new recommendations or changes the css class of them.

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
