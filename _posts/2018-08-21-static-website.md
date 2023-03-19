---
layout: page
author: isaac
title: Why make a static website?
---
A lot of people may be wondering, "Isaac, why should I make a static website? Why not pay for a domain and start my own website on WordPress or Wix?"
Well, good question. I see WordPress as the sort of main player in the development game. And sure, if you are serious about starting a dynamic website then WordPress can suit you. However, I am heavily biased toward the static website and here is the mini cost benefit analysis of the two services, a little old school analytic breakdown of the two technology classes:

| Static Website | Dynamic Website |
|--------|---------|
| **Advantages**|
|time-saving|easy to update|
|cost-effective|interactive|
|inexpensive hosting|quick to responsiveness|
|easy indexing|smooth navigation|
|fast transferring||
|**Disadvantages**|
|Difficult to Change|higher cost|
|not good in the long run|slow processing|
|limited functionality||

## Static Websites

The great thing about static websites is that they basically are changed from a remote client. WIth a dynamic website you need to host your content/ databases in an external server. Now the updates are faster because yo9u required your content to be always available to your audience. \n

The beauty for a static website is that all my assets are stored within my repository in github. This means I don't need to be reliant on the HTML or FTP protocol for retrieving anything from external servers. I just want to record my writings! However, note that the changes you do from remote client may take
ages to propagate to the actual content in the server! Why is that? \n

Well in a dynamic website, the content is usually cached at an edge location/ CDN (Content Delivery Network) so that everytime your website loads its easy to update from the servers already mentioned. And that is actually the real reason why you need a host. See, my host is not unique, but why should it? There are people who pay to have a unique global name. But technically, the unique name only looks good on paper - or for businessmen. In other words, if you are just a blogger / writer like me, you don't need all that shinanigans! The naming is actually stored in the index of a DNS (Domain Name System) server. \n

The only weekness of a static website is that it is obviously slow to update the main website. As the content is probably not cached at an edge location near to you, the server is probably stored in a cheap location that may or may not be regionally redundant! That means, if some "act of God" or natural
disaster were to destroy the regional data centre that the servers are housed in, it still can have backups from other regions! Anyway, all I'm saying is that your static website may probably take loads of time to update, since the changes need to be routed to the website you are changing. Unlike a dynamic website which can have its changes taken from block storage (side note: that is storage stored in separate blocks of loosely coupled services like HTML, FTP, SMTP), static websites have to propagate all changes from remote! \n

But its cheaper! If you want to find out why block storage is faster, this is where the computer science of data structures come in. The read time from block storage is actually not the concern here, it is write time. The HTML, FTP, and SMTP services write very quickly to a business website because it is easy to have writers that have a specific job to do, and they know how to get these files served. So whether it is a change to text, there is a HTML writer 
going through a certain port, if its a change in layout, it goes through a certain port, if its a file that has to be uploaded, it goes through FTP
or port 21, if it is SMTP it is port 80 and so on.

I am going to continue studying about computer science and here are some useful links:

- [github repo for free computer science training](https://github.com/ossu/computer-science)
- [more free computer science courses through medium](https://medium.com/free-code-camp/370-free-online-programming-computer-science-courses-you-can-start-this-month-fc5b9867769e)