---
layout: post
title:      "Scraping What's Not There Poltergiest and Phantom JS "
date:       2018-04-13 19:31:05 +0000
permalink:  scraping_whats_not_there_poltergiest_and_phantom_js
---


Have you ever tried to scrape a page using Nokogiri and all you get is empty array after empty array? Well…that was me while working on my CLI Gem Data Project. 

There I was. I had finally put all the bones in my program, and now it was time for the scraping! Went to my page to scrape away, and I kept…getting…empty arrays! Why? It turns out I was dealing with some PHANTOM JS! 

Yes, you heard it correctly. A lot of websites use Javascript these days, and content that is added with javascript isn’t detected by our good friend Nokogiri (which is all I knew at the time). I spent HOURS trying to figure out what was going on until I finally went to one-on-one project help. The coach there was the one to explain to me what was going on and point me in the direction  of the Poltergeist Gem (hehe) which also links to phantom JS.  (Shout-out and Big thanks to Kevin Webster)

Here is the link he shared with more info: 
https://readysteadycode.com/howto-scrape-websites-with-ruby-and-poltergeist


GREAT! Back on track to complete my project - woot woot! DUN DUN, the plot thickens. 
I added the gem to my GEMFILE and went to install, but kept getting an error: 

Cliver::Dependency::NotFound: Could not find an executable ["phantomjs"] on your path.


After more fun research (what is life without Stack Overflow), I realized I should have looked deeper into the documents! You infact must install Phantom JS manually

https://github.com/teampoltergeist/poltergeist


After that, I was able to scrape some Javascript content! I will say using Poltergeist does cause my program to run a little slow - a problem I will look into later - but for now it does the trick (which I’ve heard/found/learned is the best way to go about programming, step-by-step). 


