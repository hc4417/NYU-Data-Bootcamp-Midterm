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
2. IF SOHO 
3. La Garçonne
   
Nili Lotan is a store based in New York City that takes pride in elevated, clean, and functional clothing design, drawing inspiration from art, music, and rock ‘n’ roll. IF SOHO is located in SoHo, New York, and specializes in handmade European and Japanese designer fashion. La Garçonne is also based in New York City and features a collection of designer apparel curated by the founder. These three are smaller, high-end stores with a variety of products and established in-person and online stores that allow them to serve global clients. 

Using BeautifulSoup, Requests, and Pandas, we scraped valuable market data from their websites to draw our insights from. We scraped each website for vendors, product names, and categories in preparation to examine luxury product selection on the market. We then scraped the websites for product prices and categorized them by tier of luxury to better understand local luxury market pricing. Finally, we scraped the sites for product link, product description, product details, size guides, and the number of pictures on individual product detail pages. This was to aid in generating conclusions about competitors’ product transparency and demand-side knowledge. From here, we also extracted lexical diversity and description length to gain a deeper understanding of competitors’ tonal richness when providing product information. 

