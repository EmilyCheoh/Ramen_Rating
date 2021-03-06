## My Visualization 

The dataset I chose is about ratings of different brands of ramens from a variety number of countries. I think a Sankey diagram would be a good match for this dataset because there are many different components in the dataset, (i.e. brand, rating, country, type, etc). I imagine that this type of visualization can allow users have a general idea of how the pattern is like at first glance (like which brands has the best rating ramen overall), and get more information if they hover on the links.  

In the actual implementation of the visulization, I got rid of the variety (which contains the name of each type of ramen), style (whether the ramen is in a bowl or a pack), review (which acts as the surrogate key and has no actual meaning), and the top ten (which has a lot of NULL values in most of the rows) columns. I ran some SQL queries agained the dataset. I filtered out all the NULL values and the brands which have less than 3 products listed. Then I grouped the rows by the brand names. This data cleansing process took the majority of my time because, as I will mention later, my code requires a specific format of the csv file. 

After the dataset is ready to use, I started to code the Sankey diagram. I reused most of code from [this website](http://bl.ocks.org/d3noob/c9b90689c1438f57d649), which demonstrates the construction of a sankey diagram using d3. It requires the dataset to be "formatted using just link data and named values", yet I didn't realized this at first. 

![the final look](https://github.com/EmilyCheoh/Ramen_Rating/blob/master/diagram-01.png)

My final visualization looks like this, which shows that Nissin is the predominant ramen brand (and, interestingly, cup noodle was actually invented by the foudner of Nissin! ) There are several problems with my visualization. One  is that it looks really big that it cannot fit to the screen. I tried to resized my diragram, but maybe because there are too many brand names, I was unable to make it look smaller. The other one for the ratings, '5 stars' comes first, but followed by '3 stars', which is very counterintuitive. 
