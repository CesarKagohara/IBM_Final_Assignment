# IBM_Final_Assignment

# Covid-19 - Food deliveries

<h3> Introduction/Business Problem </h3>
Nowadays, due to Covid-19, restaurants around the world are closed. Many jobs have been lost, with chances of never opening again. The businesses need to reinvent themselves, being creative to develop new ways of working, and creating new sales channels, but the small and new restaurants maybe don't have the budget to improve the service or they are indebted to the Bank.
As a support to the new and small restaurant, a map will be created displaying the venues with a low number of likes, photos, and created this year(2020). The people that can't go out due to lockdown, can exchange experience and supporting the local restaurants, sharing dices photos and liking the pages.


<h3> Data </h3>
The Data will be collected using the Foursquare API. 
First, collect locations in the Food category within 10,000 meters of my home using the regular call explore endpoint (Foursquare API). With this list, split the "venue.id" column and use them to use a premium call to collect all details from the restaurants in a loop and append in a data frame. In this data frame, we can sort the venues with low likes. As part of Foursquare API, it'll provide all coordinates of the venues.
The Python Folium module will be used to create a map with each restaurant with name, address, category (Pizza, Hamburger, etc..), Rating and Foursquare link.
