---
title: create-a-cdn-resource-for-only-static-files
displayName: For static files
published: true
order: 10
toc:
   --1--1. Start the creation: "step-1-start-the-creation"
   --1--2. Choose acceleration type: "step-2-choose-acceleration-type"
   --1--3. Set up initial configuration: "step-3-set-up-initial-configuration"
   --1--4. Set up DNS (add CNAME): "step-4-set-up-dns-add-cname"
   --1--5. Integrate with website: "step-5-integrate-the-cdn-resource-with-your-website"
   --1--Issues: "issues-with-the-creation"
pageTitle: Guide to Create a CDN Resource for Static Assets | Gcore
pageDescription: Detailed instructions on how to set up a CDN resource for accelerating and protecting static assets on your website.
---
# Create a CDN resource for static assets only 

## Step 1. Start the creation 

Go to the <a href="https://cdn.gcore.com/resources/list" target="_blank">CDN</a> page and click **Create CDN resource**. 


<img src="https://assets.gcore.pro/docs/cdn/getting-started/create-a-cdn-resource/create-a-cdn-resource-for-only-static-files/cdn-resource-10.png" alt="Create CDN resource button" width="80%">  

## Step 2. Choose acceleration type

Select **Accelerate and protect only static files** on the open page and click **Confirm**.


<img src="https://assets.gcore.pro/docs/cdn/getting-started/create-a-cdn-resource/create-a-cdn-resource-for-only-static-files/cdn-resource-20.png" alt="Acceleration and protection type" width="50%">  

## Step 3. Set up initial configuration

Fill in the fields to configure your CDN resource on the open page.

<img src="https://assets.gcore.pro/docs/cdn/getting-started/create-a-cdn-resource/create-a-cdn-resource-for-only-static-files/cdn-resource-30.png" alt="Initial configuration" width="70%">

1\. (Optional) Add **Description**. Enter an internal comment about the CDN resource. It will not affect any setting but will only be displayed in the <a href="https://cdn.gcore.com/resources/list" target="_blank">CDN resources</a> section next to the resource CNAME.

<p id="origin">2. Configure <b>Origin</b>. An Origin is a source (e.g., a website, an application, a private bucket) from where the CDN resource will request the content. In the Gcore customer portal, each origin is allocated to an origins group.</p> 

There are two options for the Origin:

- **Specify content origin**—select if you didn’t create the origin group previously and follow our instructions to <a href="https://gcore.com/docs/cdn/add-an-origin-group#step-3-select-the-type-of-origin-authentication" target="_blank">add an origin group (step 4)</a>
- **Select origins group**—select if you created it previously, click the “Select the origins group” field, and select the required origin group.

<p id="custom-domain">3. Specify <b>Custom domain</b>. Assign a custom domain as <code>cdn.[your website domain]</code> for delivering static files via CDN. For example, if your website is <i>yourwebsite.com</i>, enter <i>cdn.yourwebsite.com</i>. Dynamic content will be sent to users from <i>yourwebsite.com</i>, while static files will be delivered from <i>cdn.yourwebsite.com</i>.</p> 

You can specify multiple domains by clicking the "+" icon. Later in Step 5, you can configure your website to deliver different types of static files from separate domains. Please note that a custom domain such as cdn.yourdomain.com cannot be changed after creating a CDN resource. 

4\. Click **Confirm**.

## Step 4. Set up DNS (add CNAME)

Add a <a href="https://gcore.com/docs/dns/dns-records/supported-dns-record-types#cname-record" target="_blank">CNAME record</a> for the domain specified in Step 3 as cdn.yourwebsite.com. You need to do it in your DNS providers personal account. For a CNAME value, enter a subdomain shown in your Gcore customer portal as ```*.gcdn.co```. 

For example, in the screenshot below it is written as ```cl-1ab23456.gcdn```.co, so, for the cdn.yourdomain.com subdomain, you need to create a CNAME record with the value ```cl-1ab23456.gcdn.co```. 

<img src="https://assets.gcore.pro/docs/cdn/getting-started/create-a-cdn-resource/create-a-cdn-resource-for-only-static-files/cdn-resource-40.png" alt="DNS setting" width="65%">  

If you specified additional domain names in Step 3, create CNAME records for them with the same value.

## Step 5. Integrate the CDN resource with your website

1\. Go to the admin panel of your origin website and change URLs of static files. 

Replace the origin source domain with a <a href="https://gcore.com/docs/cdn/getting-started/create-a-cdn-resource/create-a-cdn-resource-for-only-static-files#custom-domain">custom domain of the CDN resource</a> by script or manually. If a file path used to be ```yourwebsite.com/images/image.jpg```, change it to ```cdn.yourwebsite.com/images/image.jpg```. As a result, users will get static files from the CDN cache, and only the requests to the files that haven't yet been cashed will be forwarded to your origin server.

If your site is built on a CMS (WordPress, Joomla, Drupal, or other), you can replace a domain name in file paths using special plugins. You can find a necessary plugin and instructions for replacing the URLs in the <a href="https://gcore.com/docs/cdn/getting-started/integrate-cdn-with-cms" target="_blank">Integrate CDN with CMS</a> section.

2\. Go back to Gcore customer portal and click **Confirm**.

<img src="https://assets.gcore.pro/docs/cdn/getting-started/create-a-cdn-resource/create-a-cdn-resource-for-only-static-files/cdn-resource-50.png" alt="Integration" width="65%">  

That’s it! The CDN resource creation is completed. You will be redirected to the CDN resource settings—on this page, you can configure advanced settings. 

If there is no text box **... steps left** in the upper-right corner, everything is ok, and the resource is working. 

## Issues with the creation

If you see the ... steps left text box, something went wrong while creating or integrating the CDN resource. 

<img src="https://assets.gcore.pro/docs/cdn/getting-started/create-a-cdn-resource/create-a-cdn-resource-for-only-static-files/cdn-resource-60.png" alt="Issues" width="70%">  

To find out exactly where an error occurred:

1\. Click **Setup guide**.

You will see a sliding panel indicating the status of each step of CDN resource creation. 

2\. Click **Check DNS setup status**.

<img src="https://assets.gcore.pro/docs/cdn/getting-started/create-a-cdn-resource/create-a-cdn-resource-for-only-static-files/cdn-resource-70.png" alt="Check DNS setup" width="70%">  

- If a CNAME record is configured correctly, it will be shown in the UI:

<img src="https://assets.gcore.pro/docs/cdn/getting-started/create-a-cdn-resource/create-a-cdn-resource-for-only-static-files/image_1468.png" alt="Configured correctly" width="50%">  

- If an error occurs, a corresponding message will appear.

<img src="https://assets.gcore.pro/docs/cdn/getting-started/create-a-cdn-resource/create-a-cdn-resource-for-only-static-files/cdn-resource-90.png" alt="Error message" width="50%">  

3\. Click **Next** in the “Setup your DNS section.” Click **Check your integration**.

<img src="https://assets.gcore.pro/docs/cdn/getting-started/create-a-cdn-resource/create-a-cdn-resource-for-only-static-files/cdn-resource-100.png" alt="Check your integration" width="70%"> 

If there are integration issues, you will see the error message. Contact [support team](maito:support@gcore.com) or retry the integration according to the <a href="https://gcore.com/docs/cdn/getting-started/integrate-cdn-with-cms" target="_blank">instructions</a>.