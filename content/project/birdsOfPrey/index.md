---
author: Libby Mohr
categories:
date: "2021-11-15"
draft: false
excerpt: Where do the birds of prey hang out in Madison, WI? 
layout: single
links:
- icon: github
  icon_pack: fab
  name: code
  url: https://github.com/elizabethjmohr/birds
subtitle: 
tags:
- hugo-site
title: Birds of Prey of Madison
---

As a recent transplant to Madison, WI I wanted to get a handle on the birding scene here. Luckily, there's an overwhelming amount of bird observational data, freely-available courtesy of [eBird](https://ebird.org/home)[^1] and its users. For my initial exploration, I created an interactive map of observations of five different species of birds of prey. Specifically, I first split up Dane County into a grid, and then counted the number of observations since 2010 in each grid cell. Then I plotted points in any grid cell with at least one observation, and sized the points by the number of observations. Simply put, larger points = more observations. 

Check out the map below, making sure to toggle through the different species in the top right corner!

<iframe src="map.html" width = "100%" height = "400"> </iframe>

There's a few interesting trends: 
1. Most of the peregrine falcon sightings are near downtown Madison on the isthmus; they're city slickers!
2. Bald eagles are seen all over the place.
3. Great horned owls and sharp-shinned hawks tend to be spotted in forested parks and in residential areas.
4. Rough-legged hawks steer clear of the city and prefer the wide-open agricultural areas north of Madison.

[^1]: eBird Basic Dataset. Version: EBD_relOct-2021. Cornell Lab of Ornithology, Ithaca, New York. Oct 2021.