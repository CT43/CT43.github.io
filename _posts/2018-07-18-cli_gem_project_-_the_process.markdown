---
layout: post
title:      "CLI Gem Project - The Process"
date:       2018-07-18 19:19:08 +0000
permalink:  cli_gem_project_-_the_process
---


When I first set out to tackle the CLI gem project and read through what was expected of me, I thought to myself "this will be a breeze". I felt like I had a great understanding of the OO programming in ruby and had completed the scraping lab project fairly easily. 

So I began... And as you might guess, I was met with quite a wakeup call. 

What I had guessed would take me a couple days outside of work, took a week. It wasn't that the programming aspect of the project that was difficult, but it was the lack of understanding I had of all of the other components that went into the project. 

This whole time I had been coding inside the Learn IDE and I love the IDE, I do. It takes care of all the other moving parts so that I've been able to just focus and learn the programming. And so far I have been able to cruise through and I feel very confident in my programming abilities. Had the project been able to be done in the IDE, I would've been golden, but that wasn't the case.

So here I was, ready to begin the project, without the safety and ease of my IDE. Well, first thing's first, I need somewhere to code my program. How do I apropriately set up the files? I don't know. I go to open up the examples and can't use any of them. Well, it turns out I needed to update my ruby so I figure out that and then its Youtube and teachings to the rescue haha but

Alright, folders and files are all set up thanks to bundler, I list out my ideas and architecture and I start building the classes and first traces of a CLI. I need to test to see if I've done everything correctly. So I open up my terminal...  and I hit another roadblock...  I realize my knowledge of the terminal is seriously lacking so off to the internet I go to fix that.

I come back a few hours later after learning the terminals ins and outs (as well as plenty of tricks and customizations to it and my text editor, clipboard managers, etc..) and am ready to test my program. Aaaannnd... Errors. From the unknown files and constant errors, I've realized I don't have the full understanding of the load path. 

Fix that lack of understanding and finally test my skeleton code. It works!! Awesome, everything is set up and after all this time I'm finally ready to code my heart out. I build out the CLI and begin scraping the site. The site I need is full of tables and very complex but I make it through. I gather almost all of my needed data (my program is taking stock market and stock data) and am just missing the description of each stock in my program. I realize this can be solved by pulling it from each stocks individual page so I navigate to it...

aaaannnnd another roadblock... No matter how hard I try I can't scrape the company description from the page. After hours and hours of trying and researching different methods I finally learn that it is because the description is coded through javascript and is populated after the page is loaded. So Nokogiri can't access it. 

I could find a work around through various gems but decide giving the user the option to open the individual stocks webpage through the terminal is even cooler than listing the description, so I dive into figuring that out. 

Problem solved and back to coding out the rest of the program. This is the fun part for me. I get in the "zone" and as I progress I keep thinking of ways to improve my program, I'm not one to not back down from a challenge, so improvements ensue. 

My original idea was pretty straight forward - Scrape a site listing the top gaining stocks in terms of percentage gain for the day, list those stocks in order, and allow the user to select a stock to get more information about the stock.

What I ended up with was a little more complex - A gem that gives the user the option to view today's stock market through 7 different formats; the top gainers, losers, most volatile, most active, overbought, oversold, and large cap, with explanations of each. Based on their choice, the program scrapes a specific url for that information that is different from the others. Also based on their choice, it lists out and sorts the category on different information, for example, the initial list is sorted by positive percentage change for top gainers, volume traded for most active, and absolute percentage change for most volatile. These sorting options were based on what I believed to be the most useful to the user in the overview list format per the category they selected. From the now populated list, the user is able to select which stock they would like more information for, their selection would return 10 scraped pieces of info from the stock price to the sector, and then ask the user if they would like to open up the stock's webpage? If they select "y", they would be taken to the page through their default browser. At any point they could relist all the previous information or go back and select more. Finally I had to call it quits as I needed to keep progressing through the program haha. 

With my programming done, I figure I might as well publish it as a gem. And as you may have guessed by now... roadblock, of course haha. From getting the access key, to publishing various versions, renaming parts of it, and numerous miscellaneous errors, I am finally done!!

If you would like to try it out you can install it via terminal with:

```
$ gem install top_stock_movers 
```

And run it using the command: 
```
$ top-stock-movers
```

Then just follow the prompts!!


Anyways, it was quite the journey navigating the territory that was my first big project but the amount I learned was nothing short of incredible. I truly loved each roadblock as they were avenues to more learning. 

Well, I just got off work for the day so it's back to learn I go! 

-Christian

                        

