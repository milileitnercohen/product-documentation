---
title: about-meet
displayName: Overview Meet (paid)
published: true
order: 10
toc:
   --1--Meet features: "meet-features"
   --1--How does Meet work?: "how-does-meet-work"
   --1--How to use and integrate Meet: "how-to-use-and-integrate-meet"
   --2--Without integration into a website code: "how-to-use-meet-without-integration-into-the-website-code"
   --2--With integration into a website code: "how-to-use-meet-by-integrating-the-video-call-room-into-the-website-code"
---
Meet is a service for video calls, video conferences, and webinars in real-time for a large number of participants. One of the advantages is the ability to integrate a call room into your website or mobile app. 

Meet abilities   
=================

*   Video calls one-on-one or in small groups of 2- 4 people (e-commerce, finance, telemedicine). 
*   Video conferences in groups of 2–20 people (small and medium businesses). 
*   Webinars for 1–5 speakers and 2000 viewers (online education). 
*   Joint viewing of online broadcasts (entertainment). 

 <img src="https://support.gcore.com/hc/article_attachments/360017042737/call_room.png" alt="call_room.png" width="493" height="253">

Meet features 
==============

*   No time limit for any kind of video calls.  
*   No account registration and additional applications or extension installation.   
*   Communication via text chat and screen sharing for desktops.   
*   Camera switching for mobile devices.   
*   Availability of a private room creation with access with a pin code.  
*   Calls security and privacy: no video record, no data storage, no chat history saving.   
*   Works on any devices, supporting WebRTC. 
*   Integration into a website via iframe, branding, and custom settings (write to [sales@gcore.com](mailto:sales@gcorelabs.com) to  contact our manager).  

How does Meet work? 
====================

For Meet video calls, WebRTC technology is used, which provides real-time video and audio delivery.  

**_To deliver video signals from users' cameras,_** the SFU (Selective Forwarding Unit) architecture is used, which allows transmitting the same outgoing signal to the server, where it is distributed among all users: a participant sends an outgoing signal and receives the signals of all other users from a common server. 

**Please, note!**  Meet does not use a P2P (peer-to-peer) connection. All communication is broadcast via the server, even if there are 2 people in the room.  

Simulcast Streaming technology is used **_for live broadcasts_**, it helps to deliver video to each user, even with an unstable Internet channel.  Using this technology, several video streams of different quality and resolution are created on the client-side. They are delivered to a server, where based on the Internet channel of each user, it is determined what quality it is possible to deliver. After that, the selected stream is sent to the users according to the capabilities of their bandwidth and device.  

! A list of supported operating systems and browsers can be found [here](https://support.gcore.com/hc/en-us/articles/360015663098). 

**_Data streams are encrypted using_** the DTLS protocol (Datagram Transport Layer Security), which allows providing a secure connection that prevents interception, listening, and interference, without violating data integrity protection. 

**_Standard encryption is used_** to encrypt media streams. It is possible to strengthen the protection with SRTP (Secure Real-time Transport Protocol) encryption. 

How to use and integrate Meet  
===============================

Meet can be used as a browser-based solution for video calls, or as a video call room integrated into your website. 

How to use Meet without integration into the website code 
----------------------------------------------------------

*   Create a video call room on the  [https://meet.gcore.com](https://meet.gcore.com/new)  
*   Invite participants by copying and sharing the link or using the Share to \[social network\] buttons.   
      
    <img src="https://support.gcore.com/hc/article_attachments/360017043677/invite.png" alt="invite.png" width="510" height="312">

How to use Meet by integrating the video call room into the website code 
-------------------------------------------------------------------------

Use the iframe code to integrate the video call room into the website code manually or via CRM.  

1\. Generate the video call room ID. It can be any alphanumeric character set. _For example, bokxlj33._

2\. Before the alphanumeric character set, add the server location code. For test purposes use the Luxembourg server with the **"_serv2"_** location code. As a result, the video call room ID will be _serv2bokxlj33._

**Important!** To get a location code for public usage of a call room, write to support@gcore.com

3\. The iframe URL to insert into the website is consists of the _[https://meet.gcore.com/call/?roomId=](https://meet.gcore.com/call/?roomId=)_ and _the video call room ID_ you created, for example, _https://meet.gcore.com/call/?roomId= serv2bokxlj33._

4\. Paste the URL into the iframe to insert it into the website code: 

<iframe allow = "fullscreen display-capture camera microphone" src = " https://meet.gcore.com/call/?roomId= serv2bokxlj33" width = "700" height = "800"> </iframe>