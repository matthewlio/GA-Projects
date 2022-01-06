# Project 2 - Ames Housing Data and Kaggle Challenge

## Introduction and Problem Statement

This project examines a housing dataset from Ames, a city in Story County, Iowa, in United States ([source](https://en.wikipedia.org/wiki/Ames,_Iowa)). Often times, it is difficult for real estate agents to predict a price for home owners looking to sell their houses. This is especially so for the houses in United States in general, as there are numerous features that need to be considered. On the other hand, people looking to buy houses want the best house they can afford, yet do not have a reliable way to consider all the factors versus their budget. Investors also need a reliable way to know what kind of features they should look out for a good investment. This project aims to predict the selling prices of houses to address these concerns.

- Which features increase or decrease the value of a house?
- What are some features homeowners can add or improve on to increase the value of their house?
- What features should investors look out for when buying a house for investment?

To predict the selling prices of houses in Ames as accurately as possible, all features will be examined in depth for houses previously sold. Different plots will be used to find out these features correlation with sale price. Those that influenced previous sale prices the most will go through a feature selection process, which would shape the final production model that would be able to accurately predict future selling prices for houses in Ames.

This project is split into 3 notebooks:
- Exploratory Data Analysis
- Preprocessing and Feature Engineering
- Model Tuning and Insights

## Production Model Feature Dictionary
[data description](http://jse.amstat.org/v19n3/decock/DataDocumentation.txt)


|Feature|Coef|Abs Coef|
|---|---|---|
|gr_liv_area|26442.475440|26442.475440|
|overall_qual|13806.951825|13806.951825|
|total_bsmt_sf|11235.386428|11235.386428|
|exter_qual|8318.171748|8318.171748|
|lot_area|7780.658024|7780.658024|
|neighborhood|6773.247420|6773.247420|
|kitchen_qual|6750.080679|6750.080679|
|garage_area|6210.841857|6210.841857|
|bsmt_exposure|6198.768469|6198.768469|
|functional|4382.939053|4382.939053|
|bsmt_full_bath|4305.262468|4305.262468|
|bsmt_cond|-4159.611725|4159.611725|
|kitchen_abvgr|-4145.089450|4145.089450|
|foundation_Slab|4036.494240|4036.494240|
|bsmt_qual|3997.786441|3997.786441|
|bedroom_abvgr|-3556.858974|3556.858974|
|fireplace_qu|3010.820449|3010.820449|
|heating_qc|2583.698405|2583.698405|
|mas_vnr_area|2480.487846|2480.487846|
|bsmtfin_type_1|2093.362315|2093.362315|
|garage_qual|-1962.406202|1962.406202|
|total_porch_area|1738.230695|1738.230695|
|wood_deck_sf|1530.932337|1530.932337|
|age_sold|1117.363618|1117.363618|
|paved_drive|962.554246|962.554246|


## Conclusion and Recommendations

Our Linear Regression model, scaled with Standard Scaler, had the best predictive performance on housing sale price in Ames, out-performing Ridge and Lasso regression models. We also used Lasso regression to help us feature select the features that affect sale price the most.

From the above coefficient summary table, the top 5 features that determine the sale price are the size (living, basement and total lot area) and quality (overall and external quality) of the house. Neighborhood of the house comes in at a close 6th place. Other important features that affect sale prices include garage and porches areas, and quality of kitchen, basement and garage. In order to maintain the value of a house, quality is very important.

For home-seekers with specific budget, this model tells them what features they need to consider to be able to afford a house. Houses that are smaller in living, basement and lot areas might be ideal for them. They might also need to settle for an older house, at a less desirable neighborhood. They could also look at houses with lesser masonry veneer area.

For investors looking to invest in a house, they should take a look at the top 3 most desirable neighborhoods like Stone Brook, Northridge heights and Northridge. They have the potential to sell for high prices. In order to buy for lower prices and sell high, they could look for houses with little to no masonry veneer, and small porch areas. They could then improve the value of their house by installing those features themselves, installing masonry veneers and building porches. They should also consider selling their house as soon as they can, as the value decreases the older a house is. Lastly, they should maintain the quality of their house as much as possible.

This model is not without its disadvantages. As the model was developed based on data on houses sold between 2006 - 2010 in Ames, the small time frame limits the annual patterns in sale price that could arise from external factors, like economy or policy changes. The sale prices most likely were not adjusted based on inflation, which could have given us a variation in price through the years. Right now at the beginning of 2022, after 12 years, this model may not be as accurate present day. To improve the applicability of the model, we need to consider more data from a wider time frame.

In reality, house prices are difficult to predict as it may also be affected by factors hard to include in a dataset, for example like buyer's or seller's psychology, how everyone place different emphasis on different features, and also the economic climate. This model therefore does not give perfect predictions, but should rather be used as just a guide for a more informed decision.