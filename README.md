# leechblock-configuration
Configures leechblock extention to redirect common distracting sites as well as distracting YouTube features to a bible randomizer ([randombiblizer](https://randombibleizer.spiffy.tech)) (to read the bible instead of watching YouTube).

## Setup Instructions
1. Download the [text file from this repository with the configuration](https://github.com/SP4CEBARsystems/leechblock-configuration/blob/main/LeechBlockOptions.txt)
2. Install the [LeechBlock browser extention](https://www.proginosko.com/leechblock/) for your browser
3. Open your browser's extentions menu and click on leechblock to open its control panel
4. Open LeechBlock's options
5. Go to the general tab
6. Scroll all the way down to the section named "Export / Import"
7. Click browser and select the json file you just downloaded
8. Click "import options from text file"

## How To Block All Of YouTube's recommendations
1. Install [unhook](https://unhook.app/) or [untrap](https://untrap.app/) to block most of YouTube's recommendations
2. Use my [custom filters](https://github.com/SP4CEBARsystems/leechblock-configuration/blob/main/ublock-origin-configuration.md) for the [uBlock Origin](https://ublockorigin.com/) browser extention to block the remaining full-screen recommendations, these filters support both the PC and mobile versions of the YouTube website as well as YouTube players embedded into other sites.

## The filters folder
The filters that are used by leechblock are stored inside the [filters folder](https://github.com/SP4CEBARsystems/leechblock-configuration/tree/main/filters). The github urls are converted to github CDN urls to be used by leechblock's ["Load list of sites from URL" field](https://www.proginosko.com/leechblock/faq/load-from-url/) through the process below.

If you open a file like [this one](https://github.com/SP4CEBARsystems/leechblock-configuration/blob/main/filters/no%20youtube%20channels.txt) on GitHub, you will see that the page has an URL like the one below.
```
https://github.com/SP4CEBARsystems/leechblock-configuration/blob/main/filters/no%20youtube%20channels.txt
```
A GitHub CDN url may look like the below URL, opening this URL will immediately download the file ([try it](https://raw.githubusercontent.com/SP4CEBARsystems/leechblock-configuration/refs/heads/main/filters/no%20youtube%20channels.txt)). Leechblock can only load filters from a URL like this.
```
https://raw.githubusercontent.com/SP4CEBARsystems/leechblock-configuration/refs/heads/main/filters/no%20youtube%20channels.txt
```
You can convert the first into the second by replacing `https://github.com` with `https://raw.githubusercontent.com` and `/blob` with `/heads/main`. Below is a side by side comparison.
```
https://    github           .com/SP4CEBARsystems/leechblock-configuration/blob      /main/filters/no%20youtube%20channels.txt
https://raw.githubusercontent.com/SP4CEBARsystems/leechblock-configuration/refs/heads/main/filters/no%20youtube%20channels.txt
```

## YT embed (not recommended)
If you want to redirect all YouTube videos to an embedded YouTube video player you can use [yt embed](https://github.com/SP4CEBARsystems/yt-embed/).
Note that this doesn't help much in blocking YouTube's recommendations as it doesn't block end screens, and it has a recommendations bar below the video. So I recommend using [my other method](#how-to-block-all-of-youtubes-recommendations) instead. Also not that an embedded player is logged out to YouTube so you can not save a video to playlists or place comments.
