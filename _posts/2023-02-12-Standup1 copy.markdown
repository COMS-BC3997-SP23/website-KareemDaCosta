---
layout: post
title: "Standup 2"
date: 2023-02-19 14:04:10 -0500
categories: standup
---

I noticed a couple issues with the scraper I created last week.

1. I was unable to get the categories for the items I was scraping
2. Many of the images weren't loading. Upon inspection, it appears the images are only loaded once the browser scrolls to the products. Before then, there is just an empty image field
3. The website I was scraping changed their CSS and selectors (so I had to refind those). To make matters more annoying, 50% of the time I would get the old version of the website, and 50% of the time I would get the new version. I never changed the URL, so it seems to be an issue with their servers.

To fix these, I had to interact with the JavaScript of the webiste, something that the scraper I was using wasn't capable of doing. I decided to use Selenium, a headless browser that could interact with elements on the webpage. This allowed me to 1) click through the different categories in order to categorize the products that I was scraping and 2) scroll down to load the images. To fix the third issue, I just decided to make a little script that detected if I was looking at the old webpage or the new webpage. If the old webpage was loaded, I just forced the webdriver to restart until I got the new one.

However, this method proved extremely inefficient. Having to scroll to the individual elements was very time consuming, and this doubled with having to use a headless browser made it take around 15 minutes for a single store to be inventoried.

I then realized that the inventory items were being sent to the browser through some sort of network request. I looked on the network tab and found the endpoint that sent the items along with all the data that I needed; however, it only triggered under certain circumstances (which did not occur when the page first loaded). I researched and found selenium-wire, a package that could intercept network requests. I implemented this new method (I stayed up until 5 am :sob:) and it worked! The main bottleneck now is the fact that I have to launch a headless browser which still takes a long time to go between the various links, but I can't change that.

For future improvements, I will look into using scrapy with selenium through something like [this](https://pypi.org/project/scrapy-selenium/) or using [this](https://github.com/scrapy-plugins/scrapy-splash) to run JavaScript with Scrapy. The main advantage is that Scrapy uses multithreading, which could make the scraping process much faster if I am able to make it work with JavaScript. I also need to figure out if it is possible to intercept the requests with Scrapy since that method is much faster.
