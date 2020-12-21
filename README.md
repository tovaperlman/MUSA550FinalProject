# Introduction
This ReadME will briefly expand upon my [blog posts](https://tovaperlman.github.io/MUSA550FinalProject/) in Github. The objective of this project was to analyze protests trends from both Summer 2020 and Summer 2019 in order to find some similarities or differences in each summer. After analyzing trends from categories such as claims, event types and crowd size, we wanted to determine which counties in the US fit with the 3.5% rule. This rule, theorized by Erica Chenoweth, states that if 3.5% of the total population protests a specific cause then citizens can overturn the existing power and create change. Thus, my project seeks to find out if this occurred in any counties in the US in 2019 and 2020. 


## Steps:
1.	Importing Crowd Counting Dataset from the Crowd Counting Consortium
The files were downloaded from the Crowd Counting Consortium website and are in the repository. They were concatenated together to make up one dataset for Summer 2019 and one for Summer 2020.

2.	Clean the data: 
This dataset was created by humans and had many human errors because of that. This included comma’s in the wrong place, strings where there should be numbers and mis-categorizing or miswriting counties and states. I also filtered out anything not in the continental US.  I engaged in some data cleaning wherever I found errors but ultimately there are still a great many errors I was not able to clean. I used .replace to do most of this. 

3.	Protests By Claim: 
I sorted the protests by claim and used .explode and np.select to create broader categories for these protests. Ultimately, this dataset was not created in a user friendly way and more time should be spent cleaning and categorizing the thousands of claims that existed. I then used matplotlib to display static images of the top protest claims and Altair to display claims by State in an effort to see what protest claims were popular in each state. 

4.	Protests By Event Type: 
I sorted the protest by event type using a similar combination of .explode and .replace. This proved somewhat easier than the protest claims though there were many event types strung together with commas, semicolons, and slashes. I then sorted the event types to see the overall most popular ones by summer in matplotlib and then the most popular types within each state using Altair. 

5. Protests By Crowd Size: 
Then I used the pd.rolling feature to take the average crowd size for a two week period and compared crowd sizes in Summer 2019 and Summer 2020. The crowd size showed us the dates of each summer where people engaged in the most protesting. 

7. Query Cenpy to get the total population for each county
Before the query, I grouped the protest dataframe by County and summed up the low estimate protest size. I chose low estimate because after inspecting the data it was not dissimilar to high estimate and I thought a more conservative estimate might be better. Then I imported cenpy in order to get the total population information for each county. I merged the county codes back into our protest dataframe on “County” and “StateTerritory” columns using a left outer merge. Because of the creation of the dataset, many counties did not end up merging or were duplicates which we tried to clean and then ultimately dropped the rest. Once I had the FIPS codes, I merged the Total Population back into the dataframe as well.  

8. Calculate the percentage of total population the crowd size was for each county
Once I had the total population in the protest dataframe, I did a simple calculation to find what percentage of each county’s population did the crowd sizes make up. Then I created a percentage index and normalized the field in order to calculate it later on. 

9. Merge county to county geometries
I used Cenpy Tiger to get the geometries for every county in the US and merge them into our protest dataframe as well.  We also dropped any counties not in the continental US. 


10. Mapping it
Now that we have a dataframe with protest sizes, county population and county geometries, we can map it! We used matplotlib to map choropleth static maps of the counties which had protests. The lighter colors indicate counties where the crowd size was a higher percentage of total population. Secondly, we created maps in Altair with a tooltip which can show you each county and the crowd percentage of the county’s population. Somewhere, in this last step we lost a few counties including all of California. 


# Most interesting conclusions:
• Immigration was the most popular claim in 2019 and Anti-racism was the most popular in 2020. In 2020, protests around saving the post office and against child sex trafficking (which is a far right conspiracy theory) were also very popular.

•	There were many more protests and larger crowd sizes in 2020 than 2019

•	As mentioned, car caravans were a feature of 2020 event types

•	In August 2019, vigils were a popular event type in response to multiple mass shootings.

•	In both summers, there was a specific moment in which crowd sizes peaked and then they did not peak again for the rest of the summer. 

•	In 2019, there appears to be three counties that exceed the 3.5% rule. In 2020, there were 24 counties that did so. 
