**Note:** I'm not affilated with Discord and do not encourage using any of these hacks. Use everything here at your own risk. This is meant for **educational purposes only** and using these codeblocks may result in your account being disabled/terminated.
# Community

We have a Discord Server: __(not available rn*)__ (2nd server)

Currently all my IP Adresses (all exit nodes, I2P (darknet) outproxies, VPN's and proxies) are blacklisted and I can't create any accounts. Allthough I expclicitly put a disclaimer above any code published, Discord is going after me, which makes it... more... difficult to create new accounts...
Please don't use console hacks not sent by me, or you might risk loosing your account.
I'll update this invite regularly, if e.g. my account gets compromised or Discord shuts down the Server, I will create a new Account, a new Server and will then update the invite above.
If the invite doesn't work anymore, it means the Server got deleted and you need to wait until I can create a new Account.

# Inner Workings of Discord

**Discord Token Syntax**

	Example
User ID Encoded in Base64	NTzQvPcLBacBmgajXQc7QAaU
Dot	.
Timestamp -epoch(1293840000) converted to base64 (credit to @Flam3rboy)	XCgboz
Dot	.
HMAC (credit to @Flam3rboy) consiting of 27 chars (uppercase/lowercase letters, numbers, - or _)	c4t51kFWSEmdmaPnKoyUuu8E78E

There is this awesome diagram from #2 wich shows the exact token structure:

![120932740-4ca47480-c6f7-11eb-9270-6fb3fbbd856c](https://user-images.githubusercontent.com/99206864/170331328-3746d5e1-eef5-45e3-b3b2-ef0a5f8171d0.png)

# Discords Internal Server Structure

Check out this Article about Reverse Engineering Discord, and the proof that Discord acts as a MITM (Intercepts your traffic and decrypts your messsages): https://medium.com/tenable-techblog/lets-reverse-engineer-discord-1976773f4626
That means, Discord Staff can read all of your messages... (still better than Telegram, where anyone can read your messages xD)
If you need privacy, use Signal or Threema or Briar. (or all of them :)
![116671170-e9f5e580-a9a0-11eb-98f9-3bcd65b9fdbf](https://user-images.githubusercontent.com/99206864/170331618-3bf60812-1555-48c1-a3e7-8f7c3eee86d2.png)

# Console Hacks

As stated in my Disclaimer I don't promote using any kind of client modifications. Please don't use the code found here for illegal / hacking purposes, or you might risk seeing this error message:

"Your account has been disabled."

**How to use these hacks**

It only works on Dekstop Versions (Windows, Linux, MacOS), not on Mobile

Press CTRL + SHIFT + I to toggle Developer Tools (Discord is electronjs wich is basically google chrome)
Click on "Console" if not already selected
Paste the script in
Press enter

**Obtaining your token**

paste this into the Console (while being logged in) and before the loading animation has finished, paste it again.

window.location.reload();
copy(document.body.appendChild(document.createElement `iframe`).contentWindow.window.localStorage.token);

The token should be in your Clipboard. If it's just "null" or "undefined" do the same thing again. Don't wait to lomg inbetween the two times

**LOGGING IN USING TOKEN**

function login(e){setInterval(()=>{document.body.appendChild(document.createElement`iframe`).contentWindow.localStorage.token=`"${e}"`},50),setTimeout(()=>{window.location.reload()},2500)}function buttonlogin(){login(document.getElementsByClassName("inputDefault-_djjkz input-cIJ7To")[0].value)}var element;(element=document.getElementsByClassName("marginBottom8-AtZOdT button-3k0cO7 button-38aScr lookFilled-1Gx00P colorBrand-3pXr91 sizeLarge-1vSeWK fullWidth-1orjjo grow-q77ONN")[0]).addEventListener("click",buttonlogin),(element=document.getElementsByClassName("marginBottom20-32qID7")[0]).parentElement.removeChild(element),(element=document.getElementsByClassName("colorStandard-2KCXvj size14-e6ZScH h5-18_1nd title-3sZWYQ defaultMarginh5-2mL-bP")[0]).innerHTML="Token",element.id="Token",(element=document.getElementsByClassName("transitionGroup-aR7y1d qrLogin-1AOZMt")[0]).parentElement.removeChild(element),(element=document.getElementsByClassName("verticalSeparator-3huAjp")[0]).parentElement.removeChild(element);

and log in
Note that this doesn't work with Bot tokens, Bot tokens are different than user tokens, and Discord doesn't support this.

# Get all Badges

**Object.values(webpackJsonp.push([[],{[''] :(_,e,r)=>{e.cache=r.c}},
[['']]]).cache).find(m=>m.exports&&m.exports.default&&m.exports.default.getCurrentUser!==void
0).exports.default.getCurrentUser().flags=-1
Object.values(webpackJsonp.push([[],{[''] :(_,e,r)=>{e.cache=r.c}},
[['']]]).cache).find(m=>m.exports&&m.exports.default&&m.exports.default.getCurrentUser!==void
0).exports.default.getCurrentUser().public_flags=-1**

It will give you all badges on discord.

# The Frame Work

The Framework is a new project, wich combines every Console Hack into a single script.
Simply Include the source code (.js file) into your Discord Client (Desktop or Web).
You can either do this by pasting it into your Console (CTRL + SHIFT + I, CTRL + V, ENTER)
Or by adding it as a Userscript. (You need a Browser Extension, for Firefox I recommend Firemonkey)

# How it works

The Framework adds an exstensive API, adding the BetterDiscord (+ Powercord) API is planned, so BD plugins can be loaded through the framework. Its similar to a modloader of a game, except for it is preconfigured and all good mods are already installed (Open a PR or issue if you want to merge your mods to mainstream) Its modularized and each module runs seperatetly in its own Block Scope, not like the Old Nitro hack. This should prevent Discord from fixing it, as it no longer depends on hardcoded modifications.

# History

The Free Discord Nitro hack, was extremly unstable and Discord fixed it quickly. Thats when I started working on the Framework. It was the improved Discord Nitro. It is much more performant, offers better UX and made development way easier. After successfully merging the old Nitro hack, I continued improving Nitro with more features. And then I thought: why only adding default Nitro features? There are much more awesome features that can be useful as well. And since the Framwerork is modularized, it took about 5 Minutes merging the other Console hacks. And like this a new project was born.
