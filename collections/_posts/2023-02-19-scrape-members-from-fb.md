---
layout: post
title: "HOW TO SCRAPE MEMBERS FROM FACEBOOK GROUP 2023"
date: 2023-03-04T03:22:42Z
authors: ["Sage Kirk", "Mike Vance"]
categories: ["Pentesting"]
description: "For scraping members from Facebook, we have different reasons such as finding victims of scams and so on."
thumbnail: "/assets/images/blog/IMG_20230313_041401.jpg"
image: "/assets/images/blog/IMG_20230313_041401.jpg"
comments: false
---

# HOW TO SCRAPE MEMBERS FROM FACEBOOK GROUP

For scraping members, we have different reasons such as finding victims of scams and so on.

**==No paid tools required==**

### - [x] :tent: REQUIREMENTS 

- [x]Facebook Account
- [x]Being in that group
- [x]Browser (Desktop)

: **You need an account to make the whole requests.**

: **Being in a group is important, especially for the private groups.**

: **Having a browser is important, because you are using the dev console and being a hacker** :joy:

1. [x] Open [Facebook](https://www.facebook.com/), login and head over to your group.

Make sure you go to **"people"** or **"members"** tab so as you see the members

```html
**Example** :
https://www.facebook.com/groups/593079122334270/members
```

2. [x] Open the developer console (work in all browser on desktop and laptop)

> Usually use F12 or CTRL + SHIFT + I on your keyboard.

**â™¾ Tutorial : [](https://support.monday.com/hc/en-us/articles/360002197259-How-to-Open-the-Developer-Console)**

3. [x] Type **"allow pasting"** in the console and make sure you are allowed to paste code. This is a simple security task from the browser avoiding to manipulate elements and so on

4. [x] Now we copy this script and paste it :
```js
function exportToCsv(e,t){for(var n="",o=0;o<t.length;o++)n+=function(e){for(var t="",n=0;n<e.length;n++){var o=null===e[n]||void 0===e[n]?"":e[n].toString(),o=(o=e[n]instanceof Date?e[n].toLocaleString():o).replace(/"/g,'""');0<n&&(t+=","),t+=o=0<=o.search(/("|,|\n)/g)?'"'+o+'"':o}return t+"\n"}(t[o]);var i=new Blob([n],{type:"text/csv;charset=utf-8;"}),r=document.createElement("a");void 0!==r.download&&(i=URL.createObjectURL(i),r.setAttribute("href",i),r.setAttribute("download",e),document.body.appendChild(r),r.click(),document.body.removeChild(r))}function buildCTABtn(){var e=document.createElement("div"),t=(e.setAttribute("style",["position: fixed;","top: 0;","left: 0;","z-index: 10;","width: 100%;","height: 100%;","pointer-events: none;"].join("")),document.createElement("div")),n=(t.setAttribute("style",["position: absolute;","bottom: 30px;","right: 130px;","color: white;","min-width: 150px;","background: var(--primary-button-background);","border-radius: var(--button-corner-radius);","padding: 0px 12px;","cursor: pointer;","font-weight:600;","font-size:15px;","display: inline-flex;","pointer-events: auto;","height: 36px;","align-items: center;","justify-content: center;"].join("")),document.createTextNode("Download ")),o=document.createElement("span"),i=(o.setAttribute("id","fb-group-scraper-number-tracker"),o.textContent="0",document.createTextNode(" members"));return t.appendChild(n),t.appendChild(o),t.appendChild(i),t.addEventListener("click",function(){var e=(new Date).toISOString();exportToCsv("groupMemberExport-".concat(e,".csv"),window.members_list)}),e.appendChild(t),document.body.appendChild(e),e}function parseResponse(e){var t,n;try{t=JSON.parse(e)}catch(e){return void console.error("Fail to parse API response",e)}if(null!==(e=null==t?void 0:t.data)&&void 0!==e&&e.group)o=t.data.group;else{if("Group"!==(null===(e=null===(e=null==t?void 0:t.data)||void 0===e?void 0:e.node)||void 0===e?void 0:e.__typename))return;o=t.data.node}if(null!==(e=null==o?void 0:o.new_members)&&void 0!==e&&e.edges)n=o.new_members.edges;else{if(null===(t=null==o?void 0:o.new_forum_members)||void 0===t||!t.edges)return;n=o.new_forum_members.edges}var e=n.map(function(e){var t=e.node,n=t.id,o=t.name,i=t.bio_text,r=t.url,d=t.profile_picture,t=t.__isProfile,l=(null===(l=null==e?void 0:e.join_status_text)||void 0===l?void 0:l.text)||(null===(l=null===(l=null==e?void 0:e.membership)||void 0===l?void 0:l.join_status_text)||void 0===l?void 0:l.text),e=null===(e=e.node.group_membership)||void 0===e?void 0:e.associated_group.id;return[n,o,r,(null==i?void 0:i.text)||"",(null==d?void 0:d.uri)||"",e,l||"",t]}),o=((t=window.members_list).push.apply(t,e),document.getElementById("fb-group-scraper-number-tracker"));o&&(o.textContent=window.members_list.length.toString())}function main(){buildCTABtn();var e=XMLHttpRequest.prototype.send;XMLHttpRequest.prototype.send=function(){this.addEventListener("readystatechange",function(){this.responseURL.includes("/api/graphql/")&&4===this.readyState&&parseResponse(this.responseText)},!1),e.apply(this,arguments)}}window.members_list=window.members_list||[["Profile Id","Full Name","ProfileLink","Bio","Image Src","Groupe Id","Group Joining Text","Profile Type"]],main();
```
> Make sure you copy paste it, then you see a **"Download0Members"** button down below.

5. [x] Now we see 0 because no members loaded yet. Click the button to test it

**You will get following information** :

- Profile Id
- Full Name
- Profile Link
- Bio,
- Image Link
- Group Id
- Group Joining Text
- Profile Type

Wait a minute boss, there is nothing!!! ðŸ˜•

Yes of course because we only test the script, now we scrape in next step all members.

6. [x] To automate the scrolling we use a pre-made script with a live event.

Well yea for 10k members we don't like to scroll 5 hours manually right ?

Code and paste this script :
```js
(function() {
    var intervalObj = null;
    var retry = 0;
    var clickHandler = function() { 
        console.log("Clicked; stopping autoscroll");
        clearInterval(intervalObj);
        document.body.removeEventListener("click", clickHandler);
    }
    function scrollDown() { 
        var scrollHeight = document.body.scrollHeight,
            scrollTop = document.body.scrollTop,
            innerHeight = window.innerHeight,
            difference = (scrollHeight - scrollTop) - innerHeight

        if (difference > 0) { 
            window.scrollBy(0, difference);
            if (retry > 0) { 
                retry = 0;
            }
            console.log("scrolling down more");
        } else {
            if (retry >= 3) {
                console.log("reached bottom of page; stopping");
                clearInterval(intervalObj);
                document.body.removeEventListener("click", clickHandler);
            } else {
                console.log("[apparenty] hit bottom of page; retrying: " + (retry + 1));
                retry++;
            }
        }
    }
    document.body.addEventListener("click", clickHandler);
    intervalObj = setInterval(scrollDown, 1000);
})()
```
This script allows us, to leave the browser and minimize is for automation. It's like selenium but over the console.

If your script is scrolling too fast, you can go down to last line and change the 1000 (for 1 second) to 2000 or more.

> 1000 means just 1 second and 5000 are 5 seconds.

7. [x] Once your script is done, you can click on the console around or into the group around to stop scrolling.

[x] Finally click on **"DownloadxxxMembers"** and you get a CSV file. :fire:

**Read Also [BEST BINS REVIEW 2023](/blog/2023-03-09-bins-revew-2023-for-carders/)

**Source** : [https://github.com/floriandiud/facebook-group-members-scraper](https://github.com/floriandiud/facebook-group-members-scraper)
