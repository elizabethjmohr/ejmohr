---
author: Libby Mohr
categories:
date: "2021-11-19"
draft: false
excerpt: This one's for you, Hedwig
layout: single
links:
- icon: github
  icon_pack: fab
  name: code
  url: https://github.com/elizabethjmohr/birds
subtitle: 
tags:
- hugo-site
title: Snowy Owls and Irruptive Migration
---

## Background
I should admit outright that my interest in snowy owls was initially spurred by reading and watching Harry Potter as a child. Hedwig is a loyal companion and a hero and there's no denying it. Fictional stories aside, the snowy owl is a fascinating species. In contrast other owl species, snowy owls tend to be active during daylight hours. In the summer, the birds breed in the high Arctic. Some stay in the Arctic for the winter, whereas others regularly migrate south to Canada and the northern US. However, snowy owl migration patterns are considered "irruptive"; in some years the birds migrate further South in much larger numbers than normal. I find it particularly intriguing that reasons for these irruptions is still not well understood. 

## Sightings 
I wanted to visualize the irruptions that have occurred in the recent past, so I got some observation data from 
[eBird](https://ebird.org/home) [^1], a platform for birders to track and share their observations. For each migration season (October - April) from 2009-2020, I determined the number of snowy owl sightings reported on eBird for each state in the Midwestern and Northeastern United States. I then divided by the area of each state to get the number of sightings per 100 km<sup>2</sup>.
<iframe src="chloropleth1.png" width = 100% height = 550 seamless = "seamless" frameBorder = "0"> </iframe>

*Figure 1: Density of snowy owl observations reported on eBird during winter, 2009-2021.*

This set of maps shows that some of the highest numbers of reported sightings occurred during the 2013-2104, 2014-2015, 2017-2018, and 2020-2021 migration seasons. Further, the 2011-2012 2017-2018 seasons saw higher numbers of sightings in the southern part of the study.

## Caveat

At the point, you might be thinking.

> Wait a second, how do we know that the high number of snowy owls sightings aren't an artifact of birding activity in that state? In other words, shouldn't we expect more reported snowy owl sightings if everyone in the state were just birding non-stop? 

Well golly, we should account for that. Luckily, eBird also provides data on the total number of "checklists", where each checklist corresponds to a birding sessions in a given location. This allows us to account for both the number of birders in each state and how often they go birding in order to determine if the patterns we're observing are due to snowy owl behavior rather than human birder behavior. Let's visualize locations of snowy owl observations (green) alongside all birding sessions. [^3]

<iframe src="sightings.png" width = "100%" height = 500 seamless = "seamless" frameBorder = "0"> </iframe>

*Figure 2: Snowy owl sightings report on eBird during winter, 2009-2021. Sightings are more concentrated in areas with higher concentrations of birding activity or eBird checklists.*

It's apparent that many of the snowy owl sightings occur along the east coast and shores of the Great Lakes and often overlap with areas that have more birding activity (i.e.areas where grey dots are dense). Still, some areas with high birding activity have relatively lower numbers of snowy owl sightings - take St.Louis, MO, for example, or even the inland areas of the eastern US. On the flip side, northwestern North Dakota has a relatively high number of snowy owl sightings relative to the amount of birding activity. 

We can again now summarize these data taking the number of owl observations in an area and dividing by the number of birding sessions in that area [^2]. The resulting metric is the percentage of birding sessions during which a birder observed a snowy owl (i.e. the percent of checklists). 

<iframe src="chloropleth2.png" width = "100%" height = 550 seamless = "seamless" frameBorder = "0"> </iframe>

*Figure 3: Proportion of birding outings reported on eBird where a snowy owl was observed, 2009-2021.*

This set of maps tells a slightly different story than the previous set. First, the 2011-2012, 2013-2014, and 2017-2018 migration seasons stand out as the most "irruptive". During these years, the percentage of birding outings that resulted in a snowy owl sighting was non-zero in all states[^4] and much higher relative to other years. In contrast to the first set of maps, this set of maps suggests that North Dakota would be a great place to go in the winter if you wanted to see a snowy owl in any given year [^5]. This was not apparent in Figure 1 because it didn't account for the fact that there isn't a whole lot of birding that goes on in North Dakota. Finally, while the 2020-2021 wasn't a "bad" year for owl sightings, it doesn't appear quite as "good" as some past seasons where migration appeared more irruptive. This wasn't obvious in Figure 1, where the observations per unit area metric doesn't account for higher amounts of birding during that season (pandemic birding, anyone?). 


[^1]: eBird Basic Dataset. Version: EBD_relOct-2021. Cornell Lab of Ornithology, Ithaca, New York. Oct 2021.
[^2]: Technically, we divide by the number of "complete" checklists, or those where the birder recorded every species that they observed. This also means we need to restrict observation counts to those from complete checklists.   
[^3]: Inspired by [this map](https://cornelllabofornithology.github.io/ebird-best-practices/ebird.html#ebird-explore)
[^4]: Except Nebraska, 2013-2014
[^5]: Did I just say North Dakota would be a great place to go in the winter? I take it back.
