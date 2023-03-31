---
title: integrate-cdn-resource-with-xenforo
displayName: XenForo
published: true
order: 240
toc:
---
Before you take any steps please back up your files and database. The plugin works only with default CMS pattern. If you manually changed CMS patterns, the plugin might not help you.

Connect to your FTP account.

Go to library folder.

Edit config.php file and add two lines as in the example below:

$config \['externalDataUrl'\] = 'http://cdn.site.com/data';  
$config \['javaScriptUrl'\] = 'http://cdn.site.com/js';

Login to your XenForo admin area.

<img src="https://support.gcore.com/hc/ru/article_attachments/115000082689/xenadmin.png" alt="">

Navigate to Style -> General -> Settings.  
<img src="https://support.gcore.com/hc/ru/article_attachments/115000082709/xensettings.png" alt="">  
Replace the Path to images field existing record (/styles/default) with the following:

http://cdn.site.com/styles/default

Instead of cdn.site.com type in the CNAME that you specified in the G-Core [control panel](https://control.gcdn.co/). Ensure that your CNAME record has been [configured](https://support.gcore.com/hc/en-us/articles/213969769-%D0%A1NAME) in a proper way before using it for integration.

Click Update Style Properties to save your settings.

Integration has been completed! We highly recommend you to check the HTML code of your web page to ensure that URLs have been rewritten properly from your original ones to CNAME from the control panel.

To do that press F12 or open Developers Tools in your browser, choose the Network tab and refresh the page. All static files should have your CNAME in URLs.