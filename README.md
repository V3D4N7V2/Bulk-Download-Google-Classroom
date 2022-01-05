# Bulk Download Google Classroom
This Bookmarklet lets you bulk download files shared on Google Classroom

To use this bookmarklet 
+ Create a new bookmark and add the line given below in the address of the bookmark.

```
javascript:(function() {let i = 0;let win = window.open("https://google.com");win.close();let list = document.getElementsByClassName("VkhHKd e7EEH nQaZq");var interval = setInterval(function() {if (i == list.length) {clearInterval(interval);alert("Done !");return;}if (win.closed) {win = window.open("https://drive.google.com/u/" + location.href.split("/")[4] + "/uc?id=" + list[i].href.split("/")[list[i].href.split("/").length - 2] + "&export=download");i = i + 1;}}, 500);})();
```
+ Scroll to the bottom of the page until the loading sign dosen't appear anymore.
+ Click the bookmarklet on your Bookmarks Toolbar.

Alternatively you can also refer to this [page](https://support.mozilla.org/en-US/kb/bookmarklets-perform-common-web-page-tasks) about Bookmarklets by Mozilla 

What Does it Do ?
- It opens the link for one file at a time to avoid opening a ton of tabs.
When the browser closes the tab after starting the download same process is repeated for next url until all file downloads are started.

 Note: Browsers open some (PDFs for example ) files directly , Those might not be downloaded automatically unless some settings are changed.
+ To change these settings for Firefox
    + Go to Settings
    + Go to Applications Section
    + Search PDF in the search box
    + Select Save File from the dropdown list in  Action Column.

