---
layout: post
status: publish
published: true
title: Integration vs Acceptance tests
author:
  display_name: Adrian
  login: admin
  email: adyon2004@yahoo.com
  url: http://www.testfeed.co.uk
author_login: admin
author_email: adyon2004@yahoo.com
author_url: http://www.testfeed.co.uk
wordpress_id: 3
wordpress_url: http://www.testfeed.co.uk/?p=3
date: '2013-01-30 00:17:38 +0000'
date_gmt: '2013-01-30 00:17:38 +0000'
categories:
- Automation
tags:
- integration tests
- acceptance tests
- LMAX Exchange
comments: []
---
<p>Recently at LMAX Exchange, we've started using more and more of what we call integration tests which prompted a post on how we use integration tests and how we differentiate them from acceptance tests.</p>
<p>To start off, a few definitions are in order:</p>
<ul>
<li>we define an <em>acceptance test</em> as an external client that encompasses enough information on how to drive the system under test (SUT) in order to bring it to the point of asserting something.</li>
<li><em>integration tests</em>, on the other hand, are used for testing the internals of the system and are geared towards validating contracts between modules of code.</li>
</ul>
<p>[table colalign="left|left"]<br />
Acceptance Tests,Integration Tests<br />
cover at a minimum"," all the requirements in a story,focus on the same set of requirements as acceptance tests<br />
used to capture the emergent behaviour that's inherent to a story,the code produces emergent behaviour as well; with the help of integration tests the units that drive the emergent behaviour can be tested</p>
<p>use the business domain language, they tend to leak implementation and use more of the code base language since they're targeting lower functional units which don't necessarily translate into business concepts</p>
<p>usually built on top of several abstraction layers and can be understood by the business users,we use abstraction layers in a similar way to our acceptance test framework to get the same efficiency in writing integration tests; business users have a limited interest in them</p>
<p>test the end to end wiring"," starting from the internals of the system all the way to the external users of the system,they focus more on the internals of the system and tend to be kept simple in terms of how many modules participate in making a test pass<br />
feedback is slow but more comprehensive,quick feedback as the system doesn't need to be brought up<br />
they will suffer from intermittency due to so many outside factors,quick to debug and run as part of every commit; it's hard to introduce any intermittency</p>
<p>they use third party tools/dependencies"," e.g. webdriver"," to complement testing the system through external clients like a browser,keep clear of external tools and the only dependencies are the ones used by the production code</p>
<p>have a well defined external API (most probably the same API that clients use) for interacting with the SUT,use the internal APIs of the modules under test</p>
<p>have bigger costs in terms of authoring and maintaining; there's always a judgement call about encoding a specific behaviour in an acceptance test,with integration tests you can go nuts and test a lot of edge and negative cases</p>
<p>although more costly"," acceptance tests catch more complex bugs,act as a pin pointing method for isolating bugs; they'll always be easier to debug</p>
<p>can successfully be used in proving the functionality to the users through showcases; their side effects are observable and familiar to the users,the output from an integration test run will seem cryptic and uninteresting to people outside of the feature teams<br />
[/table]</p>
<p>We've started using more and more integration tests to validate requirements. This means they're no longer the lost cousin of unit tests but rather the new kid on the block right up there with the acceptance tests when it comes to testing in an agile environment.</p>
<p>If you're using integration tests leave a comment about how you're using them and how your peers see them.</p>
