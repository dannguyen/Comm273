#Question 1 




SQL Syntax:

<a href="http://imgur.com/iVr2jYp"><img src="http://i.imgur.com/iVr2jYp.jpg" title="source: imgur.com" /></a>

https://www.google.com/fusiontables/embedviz?q=select+col3+from+1VWyvsMU7nM73VkN4qAHbVBc1eN0g7z0KiaujwSZu&viz=MAP&h=false&lat=40.03789562860477&lng=-103.37530851562502&t=1&z=4&l=col3&y=2&tmplt=2&hml=KML







#Question 2



The most expensive item is "AIRCRAFT, ROTARY WING" at an 18000000 Acquisition Cost.
There are multiple counties that have this item, but the acquisition cost is not the same for all of the items that fall under this item name. I'm not sure why exeactly the same item name would have a different acquisition cost (could be models, administrative error, year, etc), BUT all the counties that had at least one item named AIRCRAFT, ROTARY WING are listed in the table below. HOWEVER, BREVARD is the only county has the item that is both labeled AIRCRAFT,ROTARY and also has the highest Acquisition Cost. 




<a href="http://imgur.com/03WRKQj"><img src="http://i.imgur.com/03WRKQj.png" title="source: imgur.com" /></a>




#Question 3




This was literally the most frustrating thing because I know nothing about guns, and naturally the Item Names were labeled by gun model, not simply the word "gun." I also needed to elimiate all the accessories associated with guns that had the word "gun" in the title as well. I'm certain I missed out on some gun models, because there are a number of calibers not on the list, but it seems like the 7.62 ml rifle was the most popular, becuase it was at the top of the list that brought me to a similar graph as the article. 


<a href="http://imgur.com/azXehOa"><img src="http://i.imgur.com/azXehOa.png" title="source: imgur.com" /></a>




#Question 4


Making sure that this one was per 1k people was literally the most annoying thing in the world. Having to figure out the mathematical equation to use was a headache, but it was kind of close to the NPR data, which is why I was ok with it. Ok but not confident. 



<a href="http://imgur.com/iH8WWow"><img src="http://i.imgur.com/iH8WWow.png" title="source: imgur.com" /></a>




#Question 5




For something I found interesting, I wanted to see how the top 10 counties for 5.56mm Rifles compared with the tope ten for 7.62mm Rifles. I was just curious if it would even be different, and it turns out it was. But, again, I know nothing about guns so I can't speculate why Salt Lake County would be the top county for one Rifle while LA is top for another. 


<a href="http://imgur.com/vHEdIAA"><img src="http://i.imgur.com/vHEdIAA.png" title="source: imgur.com" /></a>




<a href="http://imgur.com/7K8GdFe"><img src="http://i.imgur.com/7K8GdFe.png" title="source: imgur.com" /></a>




#Question 6


Map of counties that didnt have any leso supplies 

https://www.google.com/fusiontables/DataSource?docid=1Ffp8pwDjlZRgIPNJsjt0Jxd9LsBgDMny9yhYKZpe



<a href="http://imgur.com/ASjvDpq"><img src="http://i.imgur.com/ASjvDpq.png" title="source: imgur.com" /></a>





#Question 7

The same county in Florida that had all the expensive items (obviously) has the highest total Acquisition Cost. 



<a href="http://imgur.com/ffpLSQb"><img src="http://i.imgur.com/ffpLSQb.png" title="source: imgur.com" /></a>




The list of what the items were was found with this query
SELECT leso.County, leso.State, leso.`Item Name`, leso.`Acquisition Cost`
FROM leso
WHERE leso.County = "BREVARD"
GROUP BY leso.`Item Name`


The list can be found here: 
https://docs.google.com/a/stanford.edu/spreadsheets/d/1DK-oOiryyTwJEQpNuQp6UvspIrcORMOsiKj6V788G7k/edit?usp=sharing




#Question 8 

Interesting Query: 

SELECT leso.County, leso.State, leso.`Item Name`, leso.`Acquisition Cost`
FROM leso
WHERE leso.State = "MI"
AND leso.County = "WAYNE" 


For my interesting query, I wanted to see what the distribution of Items and Acquisition Costs was for Wayne county in Michigan. I chose this county because it is where Detroit is and public safety and violence are constant issues in Detroit. What I wanted to see was what type of items dominated the list. The single most common item was a 5.56mm Rifle. The most expensive item was a personel carrier. Though public safety is a topic that has been covered a great deal in Detroit, it is one that is constantly creating news. Police violence is a pretty salient problem in the area, as is violence in general. Thus, I really wanted to see how many weapons the county was getting for free, considering that area of the state is largely bankrupt and it would be difficult for cities and towns to fund such expensive equipment. Another interesting note was the fact that there were many cold weather items on the list. These didn't constitute a great deal of the cost, but it speaks to the fact that Detroit is frigid. Survival blankets, cold weather drawers, snowshoes, and others were common items. Based on this data, I think it would be an interesting news story to research how crime rates rise or fall based on the seasons, and what percentage of street-ready police are carrying assault rifles. These are specific data sets that have not been explored much (at least not by mainstream media) so I think it would resinate with the public and make quite an impact. 

the full list is viewable at this link through a Stanford email adress, I believe. 

https://docs.google.com/a/stanford.edu/spreadsheets/d/15tZLVrY1HZ8GTjrBJdMMcaK3p0UJkWvAoDmZ6_5FA-I/edit?usp=sharing






