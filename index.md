---
title       : eBay Car Price Checker
subtitle    : 
author      : James Capstick
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Purpose

This website is designed to help you find the average sold price on eBay for different types of car.

It provides:
- A search box to enter search terms (e.g. "Ford Focus")
- An output of the average eBay sold price of cars matching those search terms entered
- A list of the cars matching the search terms, with links to the eBay website

---

## UI and server code

The UI and server code for this website is to be found on GitHub [here](https://github.com/jamescapstick/eBayCarPriceChecker)

There is also a helpers.R file which provides some useful helper functions for fetching and processing eBay data from their website.

The helpers interrogate the eBay website and receive an xml response, which is then parsed before presenting the results to the user.

---

## How to use

Simply enter a search term in the box provided on the left. The output will update automatically.

For example, enter the search term "Mitsubishi Starion" and the website will show you the average sold price:


```
## [1] "Average Sale Price:  $ 3509.33"
```

---

## Item list

The website will also show you a list of the items returned, with images showing previews of each item:

<table class="data table table-bordered table-condensed">
<tbody><tr> <th>  </th> <th> image </th> <th> name </th> <th> price </th>  </tr>
  <tr> <td align="right"> 1 </td> <td> <img src="http://thumbs4.ebaystatic.com/m/mrYSM8Mu3Q9JkOxOvCK52qQ/140.jpg"> </td> <td> <a href="http://www.ebay.com/itm/Mitsubishi-Other-ESi-/322065641759" target="_blank">Mitsubishi: Other ESi 1988 mitsubishi starion</a> </td> <td align="right"> 3048.99 </td> </tr>
  <tr> <td align="right"> 2 </td> <td> <img src="http://thumbs3.ebaystatic.com/m/mmhEpf8CaLz1VhdId_mUPwQ/140.jpg"> </td> <td> <a href="http://www.ebay.com/itm/Mitsubishi-Other-ESi-R-Coupe-2-Door-/281974295138" target="_blank">Mitsubishi: Other ESi-R Coupe 2-Door 1987 mitsubishi starion esi r coupe 2 door 2.6 l</a> </td> <td align="right"> 930.00 </td> </tr>
  <tr> <td align="right"> 3 </td> <td> <img src="http://thumbs3.ebaystatic.com/m/mBFura3_SBaTnNAtbsGzh0Q/140.jpg"> </td> <td> <a href="http://www.ebay.com/itm/Mitsubishi-Other-Starion-/111928017802" target="_blank">Mitsubishi: Other Starion 1988 mitsubishi starion turbo very nice condition no reserve</a> </td> <td align="right"> 6549.00 </td> </tr>
   </tbody></table>

