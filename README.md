# Car Brand Analysis - Text Analytics (Project I)

This project is part of a learning process on how to undertake Text Analytics. This is one of the first projects that we did and hence we have applied only limited techniques. As we proceed in the learning, more comprehensive techniques and analysis were done.

![alt text](https://github.com/snithin13/Car-Brand-Analysis/blob/master/Images/edmunds_1.jpeg)

Edmunds is a popular online user forum in the US where people discuss about car brands, features etc. The aim here is to use this user generated content to perform a car brand analysis and derive insights. For our analysis, we decided to focus on the mid-size sedan forum.

## Project Objectives:
1. Write a scraper using Selenium to fetch messages posted in Edmunds.com discussion forum. We scraped around 5000 posts from the mid-size sedan forum.
2. Identify the top 10 brand by frequency.
3. Calculate lift ratios for associations between the brands and show them on a multi-dimensional scaling (MDS) map.
4. Identify the most frequently mentioned attributes of cars in the discussions and additionally identify the attributes thar are most strongly associated with certain brands.
5. Identify the most aspirational brand.
6. Based on inferences, formulate advices for i) product manager, and (ii) marketing/advertising manager of these brands.

## Contributors:
* Namita Ramesh
* Karan Palsani
* Nithin Saseendran
* Prathik Ullur
* Rachel Meade

## Approach:

* Used selenium package in python to scrape [Edmunds Midsize Sedans 2.0](https://forums.edmunds.com/discussion/7526/general/x/midsize-sedans-2-0/p540) forum.
* Tokenized into words and removed stop words.
* People can mention both brands and model names in their posts. Hence created a model to brand mapping.
* Created a word frequency dictionary for brands and identified the top 10 brands. Below is the result:

![alt text](https://github.com/snithin13/Car-Brand-Analysis/blob/master/Images/image_top10.JPG)

* Calculated lift ratios for associations between brands. Below are the brands associated together the most:

![alt text](https://github.com/snithin13/Car-Brand-Analysis/blob/master/Images/image_top_lift.JPG)

* Created a MDS map to show the degree of associations between these top 10 brands. See below:

![alt text](https://github.com/snithin13/Car-Brand-Analysis/blob/master/Images/mds%20map.JPG)

* Identified the different attributes that people generally discuss about for cars and identified the associations of the top attributes with the top brands using lift calculations. See below:

![alt text](https://github.com/snithin13/Car-Brand-Analysis/blob/master/Images/top_attri%20and%20brand.JPG)

* Formulated aspirational words like "desire to", "eager to buy", "would like to buy", "dream car" to identify the most aspirational car brand by performing lift calculations. Below are the results.

![alt text](https://github.com/snithin13/Car-Brand-Analysis/blob/master/Images/aspirational_brand.JPG)

## Inference and Advice:

**For Product Managers**

* Honda:

Honda has a low lift for “comfort” and “interior” compared to a Toyota or a Hyundai. All three brands compete in the same space in the market, but our analysis shows that customers perceive Toyota and Hyundai sedans as confortable cars having pleasant interiors.

Product managers for Honda's upcoming model years should focus on improving the quality of their models' interiors, paying particular attention to features like more leg room, quiet cabins, and sufficient head room for tall passengers. Addressing buyers' lack of enthusiasm about interiors and comfort will help Honda to be more competitive and bring them on par with their competitors.

* Ford:

Ford was the second most frequently mentioned maker in the midsize sedans forum, but it scores low on every attribute association compared to the other top brands. This does not mean that people strongly dislike Ford cars, but instead that there is ambivalence and a lack of association with Ford and any given attribute. It seems to suggest that public perception of Ford cars is somewhat bland.

In order to increase passion for Ford cars, a product manager at Ford, can afford to take more risks in their approach to building future models, innovating their design and improving performance and comfort. In a highly competitive market, if Ford wants to maintain its popularity it will have to generate more enthusiasm in future buyers. Otherwise, there is a high probability that customers could move on to purchase other brands that are highly associated with the attributes that they desire.

**For Marketing/Advertising Managers**

* Mazda:

Mazda stands out above the competition in its association with performance in discussions on Edmunds. When people mention Mazda in their posts, they are more likely to also use words like “power”, “speed”, “engine” and “turbo,” among others. Mazda can capitalize on this association by advertising to this strength. People already perceive Mazda cars as sporty and fun to drive, so they should exploit this public opinion by targeting their advertising to young potential buyers and older mid-life-crisis buyers.

Buyers looking for high performance cars may not place as high importance on fuel economy, so Mazda should not worry about slightly lower lift values for fuel economy. However, if it has cars with fuel economy that is similar to other makers, it might be able to gain market share by advertising that it is able to maintain top performance and fuel economy.

* Toyota:

Toyota has a low lift value in “fuel economy” compared to a Hyundai, and the lowest "fuel economy" lift of any brand in the top 5. This means that people don’t strongly associate Toyota with fuel economy. This is does not reflect differences in these brands' products: in reality, gas mileage for Hyundai and Toyota models are similar as per car specifications. For example, the 2019 Toyota Corolla gets 32 combined miles per gallon (MPG), while the 2019 Hyundai Elantra gets only 28 combined MPG.

The Toyota car is actually superior to Hyundai in MPG, but this advantage is not perceived by the end customer. Therefore, Marketing and Advertising managers for Toyota should focus in their upcoming campaigns to project a fuel-efficient image of Toyota.

## Code:

https://github.com/snithin13/Car-Brand-Analysis/blob/master/Edmunds%20Scrape%20Script%20Final.ipynb
