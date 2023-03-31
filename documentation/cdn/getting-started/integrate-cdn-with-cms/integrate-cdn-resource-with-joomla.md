---
title: integrate-cdn-resource-with-joomla
displayName: Joomla
published: true
order: 120
toc:
---
Before you take any steps please back up your files and database. The plugin works only with default CMS pattern. If you manually changed CMS patterns, the plugin might not help you.

Check the Joomla Version

Open the administration panel, click on System, then System Information. You will see a window with the system details.

Your system should meet the following requirements:

*   Joomla 3.4.1 or later
*   PHP 5.3.13
*   PHP mbstring (Multibyte String) - should be enabled
*   MySQL 5 or later

Install the plugin 

Download the extension CDN for Joomla! from NoNumber.nl. (you don't need to unpack the file). The extension is for versions after Joomla 3.4.1. If you use Joomla 2, download the CDN for Joomla 2 extension.

Login to Joomla administration area.

Click the Extensions tab on the top navigation bar and go to the Extension Manager section. You will be automatically transferred to the Install section, if not - click Install at the top.

Find the Upload Package File section, click the Choose File button and find the CDN extension for Joomla! which you have downloaded.

Click the Upload & Install button to upload and install the extension on your website.

Set up the extension 

Click the Extensions tab on the top navigation bar and go to Plugins.

Find the CDN plugin for Joomla! It will be displayed as System - CDN for Joomla!, click it to edit settings.

<img src="https://support.gcore.com/hc/ru/article_attachments/115000107985/joomla-1-edit.png" alt="">In the CDN section of the settings page type the CNAME that you specified in the G-CORE [control panel](https://control.gcdn.co/).

Ensure that your CNAME record has been [configured](https://support.gcore.com/hc/en-us/articles/213969769-%D0%A1NAME) in a proper way before using it for.

Click Save to save settings.

<img src="https://support.gcore.com/hc/ru/article_attachments/115000107985/joomla-1-edit.png" alt="">Integration has been completed! We highly recommend you to check the HTML code of your web page to ensure that URLs have been rewritten properly from your original ones to CNAME from the control panel.

To do that press F12 or open Developers Tools in your browser, choose the Network tab and refresh the page. All static files should have your CNAME in URLs.