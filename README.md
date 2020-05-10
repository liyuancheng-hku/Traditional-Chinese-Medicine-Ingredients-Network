# ABSTRACT

Traditional Chinese Medicines (TCM) have been heavily promoted in the Covid-19 pandemic. They achieve treatment effects by prescribing different combinations of medical herbal ingredients. Here we illustrate how these combinations form a network for the visual analysis and provide insights for those who are in the TCM value chain.  

# Introduction

During the Covid-19 pandemic, remedies known as traditional Chinese medicine, or commonly TCM, are heavily promoted by the state government of China. Some TCM treatments, notably Lianhua Qingwen, became frequently recommended Chinese patent medicine for the alleviation of mild symptoms of Covid-19. Moreover, in recent years, TCM has been expanding at a notable rate as advocating natural ingredients becomes a worldwide trend. According to Global Trade Magazine, in 2016, the sector totaled $139bn, then expanded a further 20% throughout 2017, and the pattern of growth can be seen not only domestically but also overseas. According to Nature, the selling of TCM and other related products to One Belt One Road countries has surged, experiencing a whopping 54% growth to $295mm. The project group sees tremendous business opportunities behind this swelling demand and combines data and analysis to unearth actionable insights that help relevant businesses improve their performance.

Grounded in the idea of harmony between humans and nature, TCM could in principle refer to a broad range of Chinese medical practices including herbal medicine, acupuncture, massage, exercise (qigong), etc. This project focuses on studying Chinese herbal medicines, and more specifically, the interconnection between them and how to make the best use of this information. Unlike Western medicine, which often relies on the same set of chemical formulas to address health issues for patients with similar symptoms, Chinese medicine provides a more personalized and targeted approach. Chinese medicine combines, adds or removes certain ingredients based on a patient’s symptoms as well as response to the treatment. Doctors can prescribe different formulas for the same disease upon the patient’s conditions. More specifically, Chinese medicine is commonly categorized by herbal functionality and some ingredients are used in conjunction with those in other categories to reach the maximum benefits. The interconnection between different ingredients and their functional groups would thus make an impact on their prices, demand, and availability. In this project, we will put it into perspective, depict relations among different ingredients and functionality groups, indicate alternative uses or combinations of ingredients, and analyze how TCM-related businesses can make use of this information which may have been overlooked before. 

# Data 
To understand how various herbal ingredients relate to different prescriptions, we collected information about both ingredients and prescriptions.

## Ingredients 
The database (https://herbaltcm.sn.polyu.edu.hk/herbal/) contains information of more than four hundred types of commonly used Chinese medicinal herbs (ingredients). Available attributes include the source, medicinal group, flavor, and meridian affinity.
## Ingredients price 
This is an official website (https://www.zyctd.com/) run by the Chinese Medicine Association. It updates information about TCM ingredients promptly from the four largest TCM ingredients markets in China, Anguo, Bozhou, Yulin, and Lotus Lake. It contains pricing information for TCM ingredients, including the price, price trends, Week Over Week (WoW), Month Over Month (MoM), and Year Over Year (YoY) comparisons. The format of the website is well-formed, so we directly built a list of ingredients, took them as keywords in the URL, and got the detailed price information. 
## TCM prescription 
The website (http://zhongyaofangji.com/) gathers some most common fang ji (TCM prescriptions) and ingredients used in each fang ji. These fang ji are mainly from traditional medical books, for example, Treatise on Febrile and Miscellaneous Diseases. We scraped them according to the solution to different diseases. To authenticate these prescriptions, we also refer to the textbook of fang ji published by the Chinese Press of Traditional Chinese Medicine. To facilitate the construction of the network edges in Gephi, we mutated the data into small pieces with only one ingredient and one prescription in each row. 
## Baidu Index 
Baidu Index (http://index.baidu.com), similar to Google Trends, provides insights over the popularity of top search queries in the Baidu search engine. We scraped the search engine index each day for the past year and calculated the change in the index for the past month and year. This change was used in regression and correlation analysis. For some rare keywords or those with low search volumes, the Baidu Index did not provide any results. We filled in zero for the rare words. 

The raw data from web scraping covered 408 herbal ingredients and 943 TCM prescriptions. This relatively small number of ingredients compared to the number of prescriptions indicates that TCM is exploiting different combinations of ingredients to achieve treatment effects.

# Network Analysis
We start with a network-based approach to explore the underlying pattern of ingredients combinations in TCM prescriptions. The nodes represent ingredients, linked if they co-exist in at least one prescription. The weight of each link represents the frequency of co-existence, turning the ingredient network into a weighted network. While ideally the ingredient concentration in each prescription should be taken into account, the lack of systematic data prevents us from analyzing at this level of detail. We take advantage of the Baidu Index to visualize the trending - red edges indicate a decrease in trending and green indicates otherwise. We detected network communities and visualized the communities using the Radial Axis layout, as implemented in Gephi (Figure 2).

![Image of Network](https://github.com/liyuancheng-hku/TCM-Network-Analysis/blob/master/Final.png)

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).
