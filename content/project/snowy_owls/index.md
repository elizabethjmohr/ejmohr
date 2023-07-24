---
author: Libby Mohr
categories:
date: "2021-11-19"
draft: false
excerpt: Visualizing the most irruptive migration seasons
layout: single
links:
- icon: github
  icon_pack: fab
  name: code
  url: https://github.com/elizabethjmohr/birds
subtitle: 
tags:
- hugo-site
title: Snowy Owls 
---

## Background
I'm probably not the first person to admit that snowy owls first crossed my radar when reading and watching the Harry Potter series as a child. Years later, I had the chance to see one sitting on a streetlamp on a busy street in Madison, WI, patiently surveying its surroundings and seemingly unperturbed by the traffic below. As it turns out, this was a particularly "irruptive" year for snowy owls, meaning the owls migrated further South from the Arctic in much larger numbers than normal. Interestingly, the reason for this phenomenon is not well understood. 

## Sightings 
I wanted to visualize the irruptions that have occurred in the recent past, so I got some observation data from 
[eBird](https://ebird.org/home) [^1], a platform for birders to track and share their observations. I started by visualizing snowy owl observations for each migration season (October - April) from 2009-2020 in Wisconsin [^6]. 

<figure>
<iframe src= "interactiveSightingsWI.html" width = "100%" height = 475 seamless = "seamless" frameBorder = "0" > </iframe>

<figcaption align = "center"><b>Figure 1.</b> Snowy owl observations reported on eBird in Wisconsin for migrations seasons from 2009-2020. Hover over the bar for any migration to see which observations happened in that season!</figcaption>
</figure>

I then expanded my focus area to the Midwestern and Northeastern United States. For each migration season (October - April) from 2009-2020, I determined the number of snowy owl sightings reported on eBird in each state. I then divided by the area of each state to get the number of sightings per 100 km<sup>2</sup>.

<figure>
<iframe src="chloropleth1.png" width = 100% height = 520 seamless = "seamless" frameBorder = "0"> </iframe>
<figcaption align = "center"><b>Figure 2.</b> Density of snowy owl observations reported on eBird during winter, 2009-2021. </figcaption>
</figure>

This set of maps shows that some of the highest numbers of reported sightings occurred during the 2013-2104, 2014-2015, 2017-2018, and 2020-2021 migration seasons. Further, the 2011-2012 and 2017-2018 seasons saw higher numbers of sightings in the southern part of the study area.

## Caveat

At the point, you might be thinking,

> Wait a second, how do we know that the high number of snowy owls sightings aren't an artifact of birding activity in that state? In other words, shouldn't we expect more reported snowy owl sightings if everyone in the state were just birding non-stop? 

Well, we should account for that. Luckily, eBird also provides data on the total number of "checklists", where each checklist corresponds to a birding sessions in a given location. Let's take a quick gander at the per-capita number of birding checklists for each state in the Midwest and Northeast.

<figure>
<iframe src="checklistCountsInt.html" width = "100%" height = 480 seamless = "seamless" frameBorder = "0"> </iframe>
<figcaption align = "center"><b>Figure 3.</b> Number of eBird checklists (birding sessions) per 1,000 residents, 2010-2019. </figcaption>
</figure>

The number of checklists per year is rising for all states, indicating one or more of the following: 
  1. more people have started birding
  2. existing birders have started getting out more
  3. more people are reporting their birding observations on eBird
  
Also, Vermont and Maine are dominating in the per capita checklist count arena.  Unfortunately, this makes it a bit hard to compare states other than Vermont and Maine in the chart above. The heat map table below provides an alternative visualization of the same data.

<figure>
<iframe src="heatmap.html" width = "100%" height = 500 seamless = "seamless" frameBorder = "0"> </iframe>
<figcaption align = "center"><b>Figure 4.</b> Number of eBird checklists (birding sessions) per 1,000 residents, 2010-2019. </figcaption>
</figure>

All in all, the checklist data allows us to account for the number of birders in each state, how often they go birding, and how often they report their sightings on eBird. This then allows us to determine if the patterns we're observing are due to snowy owl behavior rather than human birder behavior. Let's visualize locations of snowy owl observations (blue) alongside all birding sessions. [^3]

<figure>
<iframe src="sightings.png" width = "100%" height = 460 seamless = "seamless" frameBorder = "0"> </iframe>
<figcaption align = "center"><b>Figure 5.</b> Snowy owl sightings reported on eBird during winter migration seasons from 2009-2021. Sightings are more concentrated in areas with higher concentrations of birding activity or eBird checklists. </figcaption>
</figure>

It's apparent that many of the snowy owl sightings occur along the east coast and shores of the Great Lakes and often overlap with areas that have more birding activity (i.e.areas where grey dots are dense). Still, some areas with high birding activity have relatively lower numbers of snowy owl sightings - take St.Louis, MO, for example, or even the inland areas of the eastern US. On the flip side, northwestern North Dakota has a relatively high number of snowy owl sightings relative to the amount of birding activity. 

We can again now summarize these data taking the number of owl observations in an area and dividing by the number of birding sessions in that area [^2]. The resulting metric is the percentage of birding sessions during which a birder observed a snowy owl (i.e. the percent of checklists). 

<figure>
<iframe src="chloropleth2.png" width = "100%" height = 520 seamless = "seamless" frameBorder = "0"> </iframe>
<figcaption align = "center"><b>Figure 6.</b> Proportion of birding outings reported on eBird where a snowy owl was observed, 2009-2021. </figcaption>
</figure>

This set of maps tells a slightly different story than the previous set. First, the 2011-2012, 2013-2014, and 2017-2018 migration seasons stand out as the most "irruptive". During these years, the percentage of birding outings that resulted in a snowy owl sighting was non-zero in all states[^4] and much higher relative to other years. In contrast to the first set of maps, this set of maps suggests that North Dakota would be a great place to go in the winter if you wanted to see a snowy owl in any given year [^5]. This was not apparent in Figure 2 because the area-normalized observation counts in that figure don't account for the fact that there isn't a whole lot of birding activity in North Dakota relative to other states. Finally, while the 2020-2021 wasn't a "bad" year for owl sightings, it doesn't appear quite as "good" as some past seasons where migration was more irruptive. This wasn't obvious in Figure 2, where the observations per unit area metric doesn't account for higher amounts of birding during that season (pandemic birding, anyone?). 


[^1]: eBird Basic Dataset. Version: EBD_relOct-2021. Cornell Lab of Ornithology, Ithaca, New York. Oct 2021.
[^6]:Inspired by [this map](https://labs.waterdata.usgs.gov/visualizations/gages-through-the-ages/index.html#/)
[^2]: Technically, we divide by the number of "complete" checklists, or those where the birder recorded every species that they observed. This also means we need to restrict observation counts to those from complete checklists.   
[^3]: Inspired by [this map](https://cornelllabofornithology.github.io/ebird-best-practices/ebird.html#ebird-explore)
[^4]: Except Nebraska, 2013-2014
[^5]: Warning! North Dakota is cooooold in the winter.