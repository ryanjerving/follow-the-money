# Follow The Money
**One Rust-Belt State's Redistribution of Wealth**

https://ryanjerving.github.io/follow-the-money/

By Ryan Jerving, for TrinityX course Data Visualization for All (T005x), Spring 2017

### Cities and the Wealth of States

When we were challenged at the beginning of this course to come up with a "data story" worth telling, I had a pretty good idea of what that story would be for me. As I wrote to the discussion board:

> I live in Milwaukee, Wisconsin: a city that -- like a lot of former Rust Belt industrial powerhouses -- is very challenged these days as it tries to fund all the things its people need (schools, police, parks, garbage pickup, lead pipe mitigation, transit infrastructure, etc.). We also often find ourselves stereotyped by the rest of the state as a drain on shared resources. But, in fact, Milwaukee, like urban areas in general, is a net creator rather than a net taker of tax revenues.[...] 

> So I'd like to try to visualize this in a way that can effectively make this simple point: cities generate more wealth than they spend. 

My hand-drawn illustration of how I might make that point in a map looked like this:

![hand-drawn map](https://raw.githubusercontent.com/ryanjerving/WI-State-Aid-Gap/master/StateRevenueMilwaukeeWisconsin.png "Hand-drawn estimated of State revenue-aid gap across Wisconsin")

As it turns out, my instincts weren't terrible. My final polygon map would turn out to look a lot like this one, with its dark green crosshatching at the southeast corner of the state representing the Milwaukee-Waukesha-Madison corner flinging money into the Bon Iver hinterland of the driftless West and the Northwoods.

BUT over the course of learning the tools to which we've been introduced and applying them to this question, there were a couple of surprises in store. First, I was surprised by the power of visualization to crystalize in really vivid form something at which I'd previously only been able to gesture at, vaguely. Second, I was surprised (though maybe I shouldn't have been) by how complicated the data got when looked at on a more than superficial level, and how quickly it became clear that "how (not) to lie with maps" would be an issue.

### Revenue and Where To Find It

I'd thought of this visualization idea after reading an op-ed piece in the *Milwaukee Journal-Sentinel* by our mayor, Tom Barrett, and the president of the city's Common Council, Ashanti Hamilton. (See <a href="http://www.jsonline.com/story/opinion/crossroads/2017/01/28/barrett-hamilton-milwaukee-needs-balanced-state-approach/97196352/">"Milwaukee Needs Balanced State Approach"</a>, Jan. 28, 2017. You'll see my hand-drawn version of their line chart in the image of above.) 

Barrett and Hamilton had written about the State's systematic reduction of aid to Milwaukee over a 20-year period, as reported by our State tax collecting body, the Wisconsin Department of Revenue, who annually publish an accounting of the revenues collected and returned by locality. (See Wisconsin Department of Revenue, Division of Research and Policy, "State Taxes and Aids By Municipality and County For Calendar Year 2015," at <a href="https://www.revenue.wi.gov/Pages/Report/s.aspx#state_aids">https://www.revenue.wi.gov/Pages/Report/s.aspx#state_aids</a>.)

As it turns out, this reduction has hit local governments statewide: counties and municipalities are only seeing a 55% return of revenue as aid, as compared with 63% in 1996 (and as compared with the 90% "return to origin" goal of the revenue sharing arrangement first put in place in Wisconsin in 1911). 

But to see how "average" this 55% average might be across the state, I created this scatter plot snapshot to normalize revenue collected on a per capita basis for 2015, the most recent year for which data is available. 

<iframe src= "https://ryanjerving.github.io/highcharts-scatter-WI-pop-rev/index.html" width="90%" height="450"></iframe>

It shows about what you'd expect: that the more populous of Wisconsin's 72 counties produce more State revenue to collect. But this doesn't tell us much about any statewide patterns, particularly if you're not intimately familiar with where places like Outgamie or Ozaukee counties are!

### Go West, Young Money!

A better illustration of where the money comes from and then where it goes can be seen in the following polygon map, to which, for context, I've added points for any cities with a population of more than 50,000.

<iframe src= "https://ryanjerving.github.io/WI-State-Aid-Gap/" width="90%" height="750"></iframe>
<small><em>View full size at <a href="https://ryanjerving.github.io/WI-State-Aid-Gap/">WI State Aid Gap</a></em></small>

Toggling between the revenue/aid views offers a surprisingly compelling visualization of this data. It shows a pretty stark regional disparity between the urban Southeast third of the state where revenue is disproportionately generated and the less urban Northwest third to which the aid is disproportionately distributed. (One notable exception to this pattern of aid distribution is the deep purple Rock County you'll see along the southern border with Illinois: home to the U.S. Congress's Speaker of the House -- and Janesville's own -- Paul Ryan!) 

### Takeaways and Limitations

The pattern is starker than I'd expected from just spot-checking the numbers alone, and is a testament to the power of visualization. 

However, the project raised more questions than it answered for me as it quickly became clear how this seemingly straightforward revenue-collected-vs-aid-distributed calculated was actually quite messy.

1. It doesn't account for all kinds of aid -- most notably, aid to individuals such as healthcare, welfare, or farm subidies, any of which would change the rural/urban balance we see here.
2. The income tax portion of the revenue was attributed according to where the filer lived rather than where the tax was actually collected -- a fact that skews the numbers toward bedroom commuter counties and away from the metro centers where the wealth is actually generated. This problem is clear with the ring counties of Waukesha, Washington, and Ozaukee that surround Milwaukee County, where many of those people work. 

Finally, there were limits that the availability of the data itself placed on me. 
+ I went with a snapshot of 2015 rather than a longitudinal look over time and did so, frankly, because the Wisconsin Dept. of Revenue only had spreadsheet versions of the data available for the most recent two years (only PDFs before that, and only back to 2007). 
+ Similarly, I made counties rather than the more granular municipalities the basis of my comparison because geocoding all 1,913 Wisconsin cities, towns, and villages was going to be a logistical nightmare -- especially given that some municipalities are split between counties and that every single county in Wisconsin seems to have a "Holland" and a "Greenfield" and a "Caledonia!"
