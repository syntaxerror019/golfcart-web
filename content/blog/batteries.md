+++
date = '2025-08-11T12:00:10+08:00'
draft = false
title = 'The Endeavor for Better Batteries'
categories = 'Ford Think Neighbor'
tags =['battery','lifepo4','bms']
series = 'headline'
[params]
    author = 'Miles Hilliard & Jonas Wirz'
    thumbnail = 'https://assets.sunkrobotics.com/static/golfcart.sunkrobotics.com/batteries/cover.webp'
    headline = ''
+++

Throughout our time working with this vehicle, the Ford Think Neighbor has seen several iterations of power sources. Starting from lead acid batteries, we have since moved to LiFePO4 batteries.

<!--more-->

## Car Batteries

![Image](https://assets.sunkrobotics.com/static/golfcart.sunkrobotics.com/batteries/lead.png "a few tons of lead")

The Ford Think Golf Cart originally is powered by 6 12V car batteries. A few years prior, we purchased a whole new set of 6 of them. We chose deep cycle marine batteries to try to get the most longevity out of them, but we quickly found a major design flaw with this type of battery arrangement
All six batteries were arranged in a series configuration which allowed them to add up their voltage to about 72V nominally. Under load however (charge and discharge), we found that the “cell” voltage or voltage per battery would spread quite significantly. Over time, this dude got drastically more noticeable and problematic. Eventually they reached the point where by the time cell one was fully charged cell two or three would be dead due to the voltage delta and mismatch between them.
Normally, the solution to such a problem is called top-balancing. This requires manually charging each battery separately to 100%l in hopes of resetting the cell imbalance. Although this did work, the chemical and manufacturing differences between each made it impractical, as almost every charge required balancing. As a last resort, we ordered a 6-cell lead acid “BMS” for the batteries, but they weren't able to keep up with the rapid spread of voltage under several hundred amps of load. 


## LiFePO4 Pack

![Image](https://assets.sunkrobotics.com/static/golfcart.sunkrobotics.com/batteries/cells.webp "A table full of lithium cells")

After a lot of consideration we decided to invest in building our own Lithium battery pack. This was a new endeavor for all of us, but we went in optimistically. To begin, we purchased 24 Gotion 3.2v 100ah lifepo4 prismatic cells. We purchased 24 of these cells to wire in series, leaving us at a 72V pack. We had to drill and tap each battery and attach our own copper bus bars to make it work. 

![Image](https://assets.sunkrobotics.com/static/golfcart.sunkrobotics.com/batteries/bms.webp "The new BMS")

Additionally, we purchased the Jiabaida BMS and used it for roughly 6 months in tandem to keep things in check. Over this time period, we noticed that the vehicle felt more sluggish with every use. Compared to the first test drive after installing the batteries (with which we noted a significant performance increase), something was definitely changing. At the time we blamed the incoming cold weather and that it was impacting our batteries negatively. With this flawed reasoning, we ignored all of the issues. At some point, the vehicle became nearly impossible to drive one lap around the school without needing a recharge. This was the point where we knew something was wrong. After a bit of probing and investigation, we determined that tour Jiabaida BMS was in fact not working. We also noted that the cells were so imbalanced that a few of the outlier cells (ones charged too high or discharged too low) could have been damaged. As a safety measure, we quickly removed the old BMS and bought a new one. We bought the DALY BMS which has an app that allowed quick monitoring and customization… one feature among many missing with our previous BMS. 

## New Battery


After many hardships with the current battery pack, we have decided to look for a new source of power. We do not think it is smart to make our own battery pack for something so large, therefore we are in the process of ordering a prebuilt, 72V, BMS included, and charger included golf cart battery. We hope that this will be our final electronics change.

