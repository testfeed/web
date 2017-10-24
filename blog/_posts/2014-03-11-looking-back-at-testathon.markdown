---
layout: post
status: publish
published: true
title: Looking back at Testathon
author:
  display_name: Adrian
  login: admin
  email: adyon2004@yahoo.com
  url: http://www.testfeed.co.uk
author_login: admin
author_email: adyon2004@yahoo.com
author_url: http://www.testfeed.co.uk
wordpress_id: 141
wordpress_url: http://www.testfeed.co.uk/?p=141
date: '2014-03-11 04:57:00 +0000'
date_gmt: '2014-03-11 04:57:00 +0000'
categories:
- Uncategorized
- Testing
tags:
- coaching
- lessons learned
- exploratory testing
comments: []
---
<p>On 25th of January I went to meet with some great folks from the testing industry at a testathon (hackathon for testers).</p>
<p>Our purpose was to team up and find some bugs. We had a team in less than 5 minutes from meeting up so we were team 1.</p>
<p>We did plenty of bug finding, networking and overall good fun.</p>
<p>We were logging bugs as quickly as possible and the rules were that if somebody else was raising the same bug with an earlier time stamp they would have the full rights to it.</p>
<p>Overall the number of bugs per app went down as we went through the day. Not sure if it was because the apps were getting more mature or if our blood alcohol level was increasing.</p>
<p>Lots of prize categories , and I managed to snap the one for "The Most Hacker Way of finding a bug" which came with a ticket to Test Bash from The Ministry of Testing and 50 pounds to spend on a luxury cab ride with Uber. Also team 1 got some King marketing prizes for being the most chatty (ahem....collaborative) team.</p>
<p>My strategy was to focus on a few heuristics and apply them to obscure areas of the mobile applications we were testing. All three apps had account management features that could be exercised from both the mobile app and the web app. So I started verifying how synchronising between the two worked. And I came across some interesting findings. Mostly it was around modifying my account details in one of the apps and checking for that update in the other one. Or removing something from my account in the web app and checking the side effects in the mobile app. The app provided by King had a limitation here as it uses Facebook for sharing game state (scores, lives etc) between devices and Facebook doesn't allow too many requests to be made by third parties in a 5 minute window so getting different devices into different states was quite easy. Knowing the limitations of any 3rd party libraries employed by the app is always a good thing to know.</p>
<p>Some impressions from the providers of the mobile apps: Anthony Rose from Zeebox admitted being surprised at the many ways everybody approached testing while Dominic Assirati from King was impressed at the level of attention to detail of the testers.</p>
<p>Pros:</p>
<p>- was on a Saturday for a full day in an excellent location; food was abundant; prizes; excellent organisation and presentation; lots of interesting people from all over the globe.</p>
<p>Cons:</p>
<p>- apps were already known; not a lot of interaction within the team in terms of strategizing and learning new testing techniques/tools/etc.</p>
<p>&nbsp;</p>
<p>I would definitely attend the next one. Also the organisers promised a document to sum up the participants' experiences. When that surfaces I'll add it here.</p>
