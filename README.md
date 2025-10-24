# Analysis of NYC Boutique Luxury Fashion Market
Heather Choi, Lucy Cheng, Stephanie Pratikna

# 1. Project Overview
## 1.1 Summary
The Luxury Store (TLS) is a company looking to enter the luxury fashion market in New York City and has hired our group, Data Divas, as consultants to explore market competition in the local luxury fashion scene. They are interested in opening a location that also maintains an online presence for e-commerce, but are at the early stages of this process and require more research. They currently have stores across America, so they have little knowledge of the market and their competitors. The luxury boutique market in New York City is competitive, and TLS wants to position itself as a highly exclusive, innovative brand while ensuring pricing parity. 

## 1.2 Motivation
Our team’s goal was to conduct thorough research on market competition to provide insight into opportunities for competitive advantage.

To give a comprehensive analysis of competitors in the boutique luxury fashion market, we broke down our exploration into three main driving questions:

1. Product Type and Market Focus: What types of products do our competitors sell?
   - What is the distribution of product types across local competitors? What tier of luxury do they fall into?
2. Market Pricing: How are competitors pricing their products? 
   - More specifically, what are the price distributions among competing retailers and in total?
3. Product Transparency: What product information do our competitors give customers?
   - Is there a relationship between product price and description length? How often do retailers provide size guides?
  
## 1.3 Methodology 
To address these inquiries, we honed in on three local luxury retailers and boutiques in the market:
1. Nili Lotan
2. IF SOHO NEW YORK
3. La Garçonne
   
Nili Lotan is a store based in New York City that takes pride in elevated, clean, and functional clothing design, drawing inspiration from art, music, and rock ‘n’ roll. 

IF SOHO NEW YORK is located in SoHo, New York, and specializes in handmade European and Japanese designer fashion. 

La Garçonne is also based in New York City and features a collection of designer apparel curated by the founder. 

These three are smaller, high-end stores with a variety of products and established in-person and online stores that allow them to serve global clients. 

Using BeautifulSoup, Requests, and Pandas, we scraped valuable market data from their websites to draw our insights from. We scraped each website for vendors, product names, and categories in preparation to examine luxury product selection on the market. We then scraped the websites for product prices and categorized them by tier of luxury to better understand local luxury market pricing. Finally, we scraped the sites for product link, product description, product details, size guides, and the number of pictures on individual product detail pages. This was to aid in generating conclusions about competitors’ product transparency and demand-side knowledge. From here, we also extracted lexical diversity and description length to gain a deeper understanding of competitors’ tonal richness when providing product information. 

# 2. Overview of Data Structure
Our individual retailer datasets were combined into a single dataframe containing 308 products. The dataset’s 12 columns contain information about products sold, pricing, and provided product details, as seen in **Figure 1**. 

![columns-image](/Data_Bootcamp/columns.png)
<sub>**Figure 1.**Summary of Data Structure.</sub>

The dataset includes several key columns that facilitate both qualitative and quantitative analyses. The ‘Category’ column classifies products to capture the range and diversity of products across retailers. The ‘Descriptions’ and ‘Product Details’ columns provide qualitative information, which serves as the foundation for quantitative measures such as ‘Lexical Diversity’ and ‘Description Length’, offering insights into how linguistic expression and product positioning relate to measurable characteristics within the dataset. The ‘Price’ column, formatted as a float, enables the categorization of products into defined ‘Luxury Tiers’, while the ‘Number of Pictures’ column reflects the degree of visual representation and richness for each product entry.

# 3. Conclusions
## 3.1 What types of products do other retailers offer?
Understanding the types of products currently sold by luxury retailers influences strategic decisions around market positioning, targeted customer demographics, and profitability. Understanding competing products can help TLS differentiate itself and capture the right audience.

![category-dist](/Data_Bootcamp/category_distribution.png)
<sub>**Figure 2.** Distribution of product categories across each retailer.</sub>

From our dataset, we created bar charts (**Figure 2**) depicting the distribution of product categories across each retailer. From **Figure 2**, it can be observed that jackets, pants, and sweaters comprise the largest proportion of products. On the other hand, knits appear to be one of the smallest categories among all of the retailers. More market research can be conducted into competitor sales in order to explain the reason for this particular distribution, as it may reflect current trends, product popularity, or reveal customer preferences and unmet customer needs that TLS can take advantage of. 

![luxury-tier](/Data_Bootcamp/luxury_tier_distribution.png)
<sub>**Figure 3.** Distribution of products across luxury tiers.</sub>

To assess how localized luxury products are distributed across luxury tiers, we created pie charts for each competitor of interest. Our data, shown in **Figure 3**, indicates that most products fall into the category of accessible luxury, the tier comprising 53.8% of La Garçonne’s products, 80.6% of IF SOHO’s products, and 50% of Nili Lotan’s products. Affordable fashion comprised the second largest part of La Garçonne and Nili Lotan’s products, while high luxury makes up the second largest part of IF SOHO’s products. These distributions suggest that the local luxury industry largely caters to upper-middle-class and lower-upper-class customers. This analysis provides insights for TLS into the profitability of targeting specific customer tiers, while also revealing untapped opportunities within segments that remain underrepresented by existing luxury brands in the market.

## 3.2 How are competitors pricing their products?
Competitor pricing is an essential component TLS will have to consider when opening a new store, as it contributes to brand identity, customer perception, competitiveness, and profitability. Due to New York City’s position as a global fashion capital, with highly discerning consumers and intense competition, pricing decisions carry strategic importance beyond supply costs.

![price-comparison](/Data_Bootcamp/price_comparison.png) <br/>
<sub>**Figure 4.** Distribution of prices across retailers.</sub>

We created a box plot to compare product prices across the selected retailers of interest. Our data showed that the price of all items carried by local retailers averaged around $1200. A general distribution of these prices is shown below in the Total column of **Figure 4**. This column indicated a broad price range of $0, meaning a product was sold out or unavailable for sale, to $6395. Across specific retailers, however, these metrics changed drastically. For instance, our data reflected that IF SOHO’s product prices averaged around $1510, La Garçonne’s averaged around $782, and Nili Lotan’s prices averaged $1122. Furthermore, the data showed that 75% of IF SOHO’s products fell within the range of $425 to around $1800, while La Garçonne and Nili Lotan fell into ranges $0 to ~$800 and $300 to ~$1500, respectively. These results were demonstrative of some pricing flexibility in the luxury fashion market that TLS should keep in mind when pricing products.

IF SOHO New York, La Garçonne, and Nili Lotan occupy distinct market positions and target different consumer segments, where IF SOHO representing a more boutique, avant-garde style, while La Garçonne and Nili Lotan emphasize advanced contemporary fashion and lifestyle appeal. The discrepancies in their pricing strategies offer TLS valuable insights into how pricing aligns with brand positioning and target market differentiation.

## 3.3 What product details and information do other retailers give their customers? 
 Product transparency is a key component of consumer trust in the luxury e-commerce space. While luxury brands often want to maintain exclusivity and mystique, a balance of product detail is required to assure quality and justify premium pricing.

![price-vs-desc](/Data_Bootcamp/price_vs_description.png) <br/>
<sub>**Figure 5.** Relationship between price and description length.</sub>

To observe whether or not there is a relationship between product price and description length, we created a regression plot with a line of best fit. The regression plot in **Figure 5** shows a weak correlation of 0.3 between description length and product price. We conclude that while description length is not a large factor affecting price, perhaps a longer, more detailed description could be used to explain high product prices to customers. Hence, the product details are expected to vary as TLS aims to target different tiers of the market in order to provide buyers with services appropriate to their respective segments.

![size-guide](/Data_Bootcamp/size_guide.png) <br/>
<sub>**Figure 6.** Prevalence of size guides on product detail pages by retailer.</sub>

Furthermore, isolating retailers and products in a stacked bar plot (**Figure 6**) indicated that retailers provide size guides for around 80% of their products. This visibility of sizing charts on product pages reflects an industry standard of commitment to customer experience, transparency, and benefits reputation. 

# 4. Key Takeaways
After conducting research and market analysis, our data reveals potential market openings and information that TLS can take advantage of as they move closer towards opening their new store location. 

For instance, as shown in **3.1**, competitor products appear to be dominated by jackets, pants, and sweaters, indicating that underrepresented categories such as knits could potentially make for good entry points into the luxury fashion industry. 

Additionally, our findings in **3.1** indicate that the local luxury market is oversaturated with “accessible luxury” in the $500 to $2000 price range. Fewer products reside in the high-fashion sector of the industry, indicating opportunities for TLS to cater to a neglected customer base in the area. Moreover, we concluded from **3.2** that this product price range has some flexibility, as local luxury boutiques often have products in an extensive range, likely allowing them to slightly broaden their range of customer demographics. 

Alongside this, our conclusions from **3.3** indicated that it would be ideal for TLS to supplement their online product listings with rich digital transparency. TLS should implement standardized sizing charts and comprehensive product descriptions to align with industry standards and boost the store’s reputation. From here, TLS can take action to conduct further market research to explore local fashion trends, unmet consumer demands, and better address whatever target demographic they choose.

