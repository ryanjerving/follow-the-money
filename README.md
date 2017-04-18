# Follow The Money
**One Rust-Belt State's Redistribution of Wealth**

https://ryanjerving.github.io/follow-the-money/
By Ryan Jerving, for TrinityX course Data Visualization for All (T005x), Spring 2017

### Cities and the Wealth of States

When we were challenged at the beginning of this course to come up with a "data story" worth telling, I had a pretty good idea tof what that story would be for me. As I wrote to the discussion board:

> I live in Milwaukee, Wisconsin: a city that -- like a lot of former Rust Belt industrial powerhouses -- is very challenged these days as it tries to fund all the things its people need (schools, police, parks, garbage pickup, lead pipe mitigation, transit infrastructure, etc.). We also often find ourselves stereotyped by the rest of the state as a drain on shared resources. But, in fact, Milwaukee, like urban areas in general, is a net creator rather than a net taker of tax revenues.[...] 

> So I'd like to try to visualize this in a way that can effectively make this simple point: cities generate more wealth than they spend. 

My hand-drawn illustration of how I might make that point in a map looked like this:

![hand-drawn map](https://raw.githubusercontent.com/ryanjerving/WI-State-Aid-Gap/master/StateRevenueMilwaukeeWisconsin.png "Hand-drawn estimated of State revenue-aid gap across Wisconsin")

As it turns out, my instincts weren't terrible. My final polygon map would turn out to look a lot like this one, with its dark green crosshatching at the southeast corner of the state representing the Milwaukee-Waukesha-Madison corner flinging money into the Bon Iver hinterland of the driftless West and the Northwoods.

BUT over the course of learning the tools to which we've been introduced and applying them to this questions, there were a couple of surprises in store. First, I was surprised by the power of visualization to crystalize in really vivid form something at which I'd previously only been able to gesture at, vaguely. Second, I was surprised (though maybe I shouldn't have been) by how complicated the data got when looked at on a more than superficial level, and how quickly it became clear that "how (not) to lie with maps" would be an issue.

### Revenue and Where To Find It

I'd thought of this visualization idea after reading an op-ed piece in the *Milwaukee Journal-Sentinel* by our mayor, Tom Barrett, and the president of the city's Common Council, Ashanti Hamilton. (See <a href="http://www.jsonline.com/story/opinion/crossroads/2017/01/28/barrett-hamilton-milwaukee-needs-balanced-state-approach/97196352/">"Milwaukee Needs Balanced State Approach"</a>, Jan. 28, 2017. You'll see my hand-drawn version of their line chart in the image of above) 

Barrett and Hamilton had written about the State's systematic reduction of aid to Milwaukee over a 20-year period, as reported by our State tax collecting body, the Wisconsin Department of Revenue, who annually publish an accounting of the revenues collected and returned by locality. (See Wisconsin Department of Revenue, Division of Research and Policy, "State Taxes and Aids By Municipality and County For Calendar Year 2015," at <a href="https://www.revenue.wi.gov/Pages/Report/s.aspx#state_aids">https://www.revenue.wi.gov/Pages/Report/s.aspx#state_aids</a>

As it turns out, this reduction applied to all county and municipal governments which, statewide, are only seeing a 55% return of revenue in the form of aid, as compared with 63% in 1996 (and as compared with the 90% "return to origin" goal of the revenue sharing arrangement first put in place in Wisconsin in 1911). I was interested in looking at snapshot for 2015, the most recent year for which data is available, to see how average this 55% average is across the state.

Of course most raw revenue -- and most aid returned -- would be to the more heavily populated areas. But even when normalized by looking at the per capita numbers, I suspected that we'd find a clear correlation between the population density of a city, village, or town and the amount of revenue each person can be said to generate. This scatter chart uses the population number the DOR provides as an imperfect-but-close-enough proxy for density. 



<iframe src= "https://ryanjerving.github.io/WI-State-Aid-Gap/" width="90%" height="650"></iframe>
<small><em>View full size at <a href="https://ryanjerving.github.io/WI-State-Aid-Gap/">WI State Aid Gap</a></em></small>

Wisconsin Dept. of Revenue data for 2015 shows a regional disparity in the amount of State revenue collected by county and the amount returned as aid to local governments. Toggling between these two map views reveals, dramatically, how revenue earned in the more urban Southeast third of the state is redistributed to the less urban Northwest third (with the Milwaukee city region seeing a particularly large gap).

 
