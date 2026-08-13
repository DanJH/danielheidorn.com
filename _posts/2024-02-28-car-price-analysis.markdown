---
layout: post
title:  "Webscraping and Multivariate Car Price Analysis"
date:   2024-02-28 12:00:00 -0400
categories: project personal
lastpost: "Game Design Capstone: Coconaut"
lastposthref: "/project/school/2022/04/19/game-design-proj-3-exploration.html"
# nextpost: "Arduino Buttonbox for Sim- Racing, Flying, and more!"
# nextposthref: "./project/personal/2026/06/22/arduino-buttonbox.html"
---

*Note: this was developed before the [meteoric rise of A.I. webscrapers](https://arstechnica.com/ai/2025/03/devs-say-ai-crawlers-dominate-traffic-forcing-blocks-on-entire-countries/). So now a majority of websites will block repeated requests. Thus, this project no longer works.*

## T-Boned by Oppurtunity 

I absolutely loved my Ford Focus ST. The gearbox and the steering were constantly tantalizing you to push it a little faster, take the turn a little tighter. The ride was a splendid balance for a daily hot-hatch; not backbreaking when cruising around bumpy Michigan roads and not rolling or wimping out in tight corners. You could tell I loved it by the way I adorned it with a custom intake, grill, and lights. I guess you could say he was my *Brad*.

But, much like commerical, some sleep-deprived teenager T-boned my Brad. Long story, short, the other driver blew a stop sign after working a long shift and careened into my front left fender. I barely had time to notice a big silver object fly towards my left, and next thing I know I am spun out in the street and hunched forward in my seatbelt. I was so lucky to be able to walk away from the accident with the scratch but I couldn't shake being a like irked that the Chevy Impala was able to hobble away but mine had to be dragged by a flatbed to a junkyard - the entire powertrain was toast.  

I thought I had enough headaches but then came insurance.

## Try Again, Insurance 

If you've ever read *When McKinsey Comes to Town* by Walt Bogdanich and Michael Forsythe, then you're likely aware of the insurance practice pioneering by All State and McKinsey where they expect unscrupulous customers to take a lower payout than their vehicle is actually worth [^1]. Keeping that in mind, I received my first quote and let's say it was much less than expected. In fact, it was more than 10% lower than the cheapest trim I could find on websites like cars.com. It was quite frustrating but I didn't feel right going back to my insurance agent just off a gut feel - I needed an actual number to show.

I decided to run some simple analysis and see where other cars on the market landed. 

### Webscraper for Data

After looking through some sites, the first site I decided upon was `cars.com` because they could display up to 100 results a page and the page iterator was in the URL (this made it have fewer requests (less likley to be denied) and easy for a script to iteratre)
The Python library beautifulsoup is great for webscraping 

## Planning to Purchase 

On the flipside, I could use the same webscraper to browse the value of cars and run some nice multivariate analayses like seeing how much value declines by mileage, year, etc. for a specific make or model relative to another.



## Future Plans [RIP to Webscraping]

I initially had a long-term vision to having something similar to Autotempest.com but instead of showing active offers through multiple websites, it would instead give 

Yes, this plan would require an API long term but I am a single software developer with not nearly enough capital, or even demand, to recreate it with a large DB of car prices.

## Links

[^1]: From Good Hands to Boxing Gloves: The Dark Side of Insurance; A Berardinelli, D.J.


