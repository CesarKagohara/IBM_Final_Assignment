# IBM_Final_Assignment

# Covid-19 - Food deliveries

<h3> Introduction/Business Problem </h3>
Nowadays, due to Covid-19, restaurants around the world are closed. Many jobs have been lost, with chances of never opening again. The businesses need to reinvent themselves, being creative to develop new ways of working, and creating new sales channels, but the small and new restaurants maybe don't have the budget to improve the service or they are indebted to the Bank.
As a support to the new and small restaurant, a map will be created displaying the venues with a low number of likes, photos, and created this year(2020). The people that can't go out due to lockdown, can exchange experience and supporting the local restaurants, sharing dices photos and liking the pages.


<h3> Data </h3>
The Data will be collected using the Foursquare API. 
First, collect locations in the Food category within 10,000 meters of my home using the regular call explore endpoint (Foursquare API). With this list, split the "venue.id" column and use them to use a premium call to collect all details from the restaurants in a loop and append in a data frame. In this data frame, we can sort the venues with low likes. As part of Foursquare API, it'll provide all coordinates of the venues.
The Python Folium module will be used to create a map with each restaurant with name, address, category (Pizza, Hamburger, etc..), Rating and Foursquare link.


<h4> Exploratory Data Analysis </h4>
The Foursquare API has the endpoint called "explore". In this regular endpoint, I have used 4 parameters, the first is the "ll" to register the my current location(latitude and longitude), categoryId to get the "Food" category, radius to define the maximum distance and the results limits. The Foursquare have returned a Json file and using the Json and Requests libraries, the file was modified to a Dataframe as you can see below the example with 1 row in transpose mode:<br>

![Imgur Image](https://raw.githubusercontent.com/CesarKagohara/IBM_Final_Assignment/master/images/Foursquare_Regular.PNG)

With this dataframe above, just the venueID was used as parameter to the Foursquare premium call to collect the details one by one, as you can see in the example below:<br>
![Imgur Image](https://raw.githubusercontent.com/CesarKagohara/IBM_Final_Assignment/master/images/Foursquare_Premium.PNG)

For this example, I have used the venues with less than 10 likes and returned a bunch of restaurants. With this data, the Folium library was used to create and add markers in the maps with some details of the elected restaurants, as you can see below:<br>
![Imgur Image](https://raw.githubusercontent.com/CesarKagohara/IBM_Final_Assignment/master/images/map.PNG)


<h3>Results section where you discuss the results.</h3>
According to the notebook created, We can create an application to support our local business during the pandemic of Covid-19. Find a restaurant that doesn't have visibility and highlight them.

<h3>Discussion</h3>
The Foursquare API is very useful to explore any venue around the world using address or latitude/longitude. Depending on the choose location, sometimes the venue details are not accurate, due to missing recent updates. It'll depend on the popularity of the Foursquare in the Country.

<h3>Conclusion</h3>
Using data science, we can help each others exploring many API around the internet. During this pandemic, it'll be very helpful for some people that don't have conditions to understand the impact of Covid-19 on their business. The world is changing and We're here to understand thought the data, where the business should go.