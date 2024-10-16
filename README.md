# Deciphering Consumer Preferences and Perceptions: An Integrated Conjoint Analysis and PCA Approach for Sustainable Product Development

![image](https://github.com/user-attachments/assets/412eb70f-a0b0-4752-8061-104f202b5d6b)

## Introduction and Background

In the competitive landscape of product development, understanding customer preferences and market demands is a crucial aspect for success. This report focuses on leveraging advanced marketing analytics to inform the development of a new, market-friendly product. We employed two main analytical methods, conjoint analysis and principal component analysis (PCA), which are significant in translating complex consumer data into actionable insights.

Conjoint analysis is a widely used method in product design and marketing. It is employed to analyse and forecast consumer behaviour in relation to new products or enhancements to existing products (Pistol and Bucea-Manea-Tonis, 2017). This method is particularly valuable in measuring the value that consumers place on specific product features and attributes, making it a powerful tool for understanding consumer preferences (Olson, 2008). In the context of new product development, conjoint analysis has been used to refine feature selection and make design trade-off decisions among various features (Kim et al., 2017). It is considered the method of choice for quantitative preference measurement and is highly regarded in marketing science and practice (Netzer et al., 2008).

For this analysis, we have focused on attributes identified as most influential through market research: environmental friendliness, delivery time, service level, price, quality of material, and marketing proficiency. This method helps in understanding the trade-offs consumers are willing to make and can also provide a quantification of the consumers' willingness to pay for specific attributes.
Additionally, this report also highlights future directions to determine the optimal product concept by identifying market segments that value specific product concepts (Salhieh and Al-Harris, 2014).

On the other hand, PCA is employed to reduce the dimension of large datasets, improving interpretability of the results while minimizing information loss. This method helps in identifying the patterns in data by transforming the original variables into a new set of variables, which are linear combinations of the original variables (Abdi and Williams, 2010). These components help in visualizing the importance of various attributes in the perception of the product.
Both methods combined offer a comprehensive approach in understanding both the stated preferences through conjoint analysis and the perceived importance of different attributes through PCA. The insights gained from these analyses will guide strategic decisions in product design and marketing, ensuring that the new product aligns with consumer expectations and market trends.

## Methodology

### Conjoint Analysis

The conjoint analysis was structured to understand consumer preferences by examining how different attributes influence their decision making process. This analysis began with the meticulous selection of product attributes and levels. Initial customer studies highlighted a set of fifty attributes, which were narrowed down to six critical ones through interviews and discussions within a focus group. The attributes finalized for analysis were environmental friendliness, delivery time, service level, price, quality of material, and marketing proficiency. Each attribute was defined at several levels to reflect the realistic variations in the market offerings.

**Why were only 18 product profiles chosen?**
In conjoint analysis, the selection of product profiles is a critical step that must balance comprehensiveness with practical considerations of survey length and complexity. The choice of 18 product profiles for this study was guided by a fractional factorial design approach, which is a common technique used to create a representative subset of profiles from the potentially vast number of possible combinations (Gunst and Mason, 2009).
A full factorial design, which includes all possible combinations of attribute levels, can result in an unwieldy number of profiles, especially when multiple attributes are considered. This can be overwhelming for respondents and may lead to fatigue, reducing the quality of the data collected. To mitigate this, a fractional factorial design is guessed to select a subset of profiles that still captures the essential information needed to estimate the part-worths of each attribute level effectively (Eggers and Sattler, 2009).

The 18 profiles chosen are a balanced and strategically selected sample that represents the full set of attribute combinations without requiring respondents to evaluate an excessive number of products. This selection ensures that each attribute is systematically varied across profiles, allowing for the estimation of main effects and potentially some interaction effects while keeping the number of profiles to a manageable level, furthermore, the results were validated by correlation analysis, with negligible correlation between the attributes.

![image](https://github.com/user-attachments/assets/982f077e-fd0b-4d55-98e0-a47c320177f6)

Figure: Correlation Matrix

The results ensured the orthogonality of design, means that the effect of each attribute can be independently estimated by these 18 profiles without introducing significant bias or confounding effects (Aoki and Takemura, 2012).

The chosen profiles were then used to collect data on consumer preferences and rated on a scale from 1 to 10. The collected data were first processed using R to calculate the initial part-worth utilities by assigning the base level for each attribute to measure the effect within the different level of an attributes.

![image](https://github.com/user-attachments/assets/dd36f115-b4dc-48d9-ab57-84d399cdce02)

Table: Base Variables
Part-worth indicate the perceived value of each attribute level. These part-worth’s were further analysed in Tableau, where calculated fields were used to estimate the importance and willingness to pay (WTP) for each attribute, enhancing the understanding of consumer valuation.

### Principal Component Analysis (PCA)

The PCA was employed to analyse customer perception data, specifically how customers perceive and prioritize different product attributes. The data preparation involved organizing the scores given by consumers to 32 models of the product, each evaluated on 11 distinct attributes. This preparation included scaling the data to standardize the range of variables, ensuring that variables with larger scales do not disproportionately influence the outcome.
The PCA computation was carried out using the prcomp function in R, which involves calculating the eigenvalues and eigenvectors of the data covariance matrix. This step helps in determining the principal components (PCs) — the directions in which the data varies most. The number of components retained was based on their ability to explain a significant amount of the variance within the dataset (Abdi and Williams, 2010).

The loading factors of each component were examined to understand which attributes contributed most to each principal component. These factors indicate the weight or coefficient of each original variable on the principal component, providing insights into which attributes are most influential in the perception of the product. A perceptual map was then created using the scores from the first two principal components to visually show the relative standing of each model based on these components. This map was plotted in Tableau, providing a graphical representation of data clusters and distances, illustrating how different product models are perceived relative to each other based on the most impactful attributes.

This methodology ensures a comprehensive analysis of both stated preferences through conjoint analysis and perceived importance through PCA, providing meaningful insights for strategic product positioning and design decisions.

## Results and Discussion:

### Conjoint Analysis
The conjoint analysis provided detailed insights into how consumers value different levels of product attributes. The computed average part-worths for each attribute, adjusted for a base level as defined in the analysis methodology, indicate the relative importance of attribute changes from the base level (Orme, 2002).
Computed Part-Worth

![image](https://github.com/user-attachments/assets/00c59fae-5d52-49be-a5b2-6afd4dd9a550)

Figure: Average part-worth’s

![image](https://github.com/user-attachments/assets/2e6f3d38-9622-4753-81f6-bba2cf247956)
![image](https://github.com/user-attachments/assets/c1dcf088-160d-4a21-9891-12c623e03748)


### Willingness to Pay (WTP) Calculations

The willingness to pay for different attribute levels was calculated using part-worths, transformed into monetary values to represent what consumers would be willing to pay extra for each attribute level (Orme, 2002). This table below indicates the additional amount consumers are willing to pay for enhancements above the base level, or the amount they expect to be discounted for levels below the perceived value of the base. It reflects the economic value consumers assign to each attribute, guiding pricing and product development strategies.

![image](https://github.com/user-attachments/assets/e56fc442-8972-4124-a589-a5f190fcc5e3)

Figure: Average willingness to pay

![image](https://github.com/user-attachments/assets/5f0a91f9-b6cd-44b5-9001-f9a67f5ff1bf)


### Visualization and Analysis of Results

Visualizations created in Tableau provided a clear depiction of these findings. The attribute importance chart highlighted that ‘Delivery time' and 'service level' were the most valued by consumers, suggesting these are critical factors in their decision-making process. This visualization aids in understanding the weight consumers place on different attributes and how these preferences distribute across the product features.

![image](https://github.com/user-attachments/assets/f295c3f8-648c-4535-be2d-5ca5eeef1e12)

Figure: Attribute importance

![image](https://github.com/user-attachments/assets/0396fa6a-1e93-42d1-af55-f492ff473f16)


These values suggest a consumer preference hierarchy, where logistics and service are dominant, followed by economic and environmental considerations, with material quality being less of a priority but still relevant.

### Implications for Product Design

The insights from the part-worth’s and willingness to pay analyses offer clear implications for product design. The strong preference for substantial CO2 reductions indicates that emphasizing environmental sustainability could be a key differentiator in the market. However, while consumer’s value enhanced service options, there is a tipping point in price sensitivity, as shown by the negative part-worth for higher price levels. This suggests that while adding features and services can enhance the product's appeal, these attributes need to be balanced against cost considerations. Moreover, the less importance placed on marketing proficiency relative to other attributes signals that while clear communication is necessary, the product's inherent features and environmental benefits should be the focus of design and communication strategies. This complete view emphasises the need for a carefully balanced product offering that aligns with consumer priorities: eco-friendliness, cost-efficiency, and valuable service.

### Market Segmentation

The results from conjoint analysis can further be leveraged to segment the market based on attribute preferences identified by analysing the part-worths from the conjoint study. Here’s how conjoint analysis aids in market segmentation (Dolnicar et al., 2018):
1. Cluster Analysis: Statistical techniques like cluster analysis can be applied to the part-worths to group consumers into segments based on their utility scores. Each segment would consist of consumers who value product attributes similarly (Djokic et al., 2013).

2. Targeted Product Offerings: Once segments are identified, products or services can be tailored to meet the unique preferences of each segment. For instance, one segment may value environmental friendliness above all, while another prioritizes cost or delivery time.

3. Strategic Marketing: Marketing campaigns can be customized for each segment, emphasizing the attributes that are most important to those consumers. This personalized approach can increase the effectiveness of marketing efforts and customer satisfaction.

4. Pricing Strategy: Conjoint analysis can also inform pricing strategy by identifying the willingness to pay within each segment. Companies can price their products according to the value that each segment places on different product features.
Summing up, market segmentation through conjoint analysis allows companies to move beyond a one-size-fits-all strategy towards a more focused, targeted approach that cater and capitalizes on the diversity of consumer preferences.

### PCA

#### Importance of Attributes:
The singular values and the corresponding variance explained indicate how much of the data's variability each principal component accounts for. The first principal component (PC1) with highest singular value, explains 60% of the variance, followed by PC2, together explain 84% of the variance. Which is a significant proportion, indicating that the attributes associated with PC1 and PC2 are very important in how customers perceive the products.

![image](https://github.com/user-attachments/assets/c14f2012-d5a2-47ad-b858-22f29c6a9df9)

Table: singular values and variance explained of PC’s

The loading factors for each PC show how much each attribute contributes to that component. Attributes with higher absolute loading values are more significant for that component.

![image](https://github.com/user-attachments/assets/bfd62d20-9d21-4277-8799-459bd654cf82)

Table: Loading score of individual feature in different PC

For PC1, the attributes with the highest absolute loadings appear to be Feature2, Feature3, and Feature6. These attributes represent key factors that influence the customer's decision-making process in the most significant dimension.
For PC2, although the variance explained is less than PC1, we would still consider attributes with the highest loadings for this component. Feature7 and Feature8 have relatively high loadings on PC2, making them significant in the second dimension.

#### Perceptual Map

![image](https://github.com/user-attachments/assets/b3234b8e-f32a-4695-80d8-948305b93e7f)

Figure: Perceptual Map

#### Perceptual Map Interpretation

The perceptual map displays how each product model is perceived based on the scores from the first two principal components. Models with higher scores on PC1 are perceived favourable e.g in terms of the quality or value they offer. Those with higher scores on PC2 might offer specific features that some consumers prefer, or represent differentiating factors like usability or aesthetic appeal.

#### Model Positioning and Strategic Implications:
**Model 14 and 15** has high positive scores on both factors, suggesting it is perceived as superior in terms of the attributes captured by both PC1 and PC2. This could indicate a product that balances quality with other desirable features.

**Model 18** shows extreme negative scores on PC1, indicating that it is perceived poorly in terms of the most important attributes to customers. It might require significant product improvements or repositioning.

**Model 30** has a high score on PC1 but a very low score on PC2, which may suggest that while it ranks well in quality or core performance, it may lack in other areas such as design or additional features.

**Model 32 and 1** is moderate on both factors, indicating a balanced but not standout perception. It could be positioned as an all-rounder or may benefit from marketing that enhances its perceived value

**Comparison with Existing Research**
The findings from the PCA correlate with existing research that suggests consumers often evaluate products on a multi-dimensional scale (Hauser and Urban, 1986), where certain features are given more weight depending on the consumer's personal preferences and the product's market positioning. The attributes represented by Factor1 and Factor2 are consistent with key dimensions often cited in consumer behaviour literature, such as the quality-performance dimension and the aesthetic-usability dimension.


## Conclusions

**Summary of Key Findings**

This comprehensive report combines findings from conjoint analysis and PCA to steer product strategy. Conjoint analysis revealed that consumers highly value CO2 reduction and service features, while exhibiting price sensitivity. The optimal product profiles suggested a strategic emphasis on environmental and service quality enhancements balanced with cost considerations. Furthermore, PCA highlighted the most significant attributes influencing customer perception offering a blueprint for product differentiation and targeted improvements. The resultant perceptual map highlighted the positioning of each model, guiding decisions on product development, marketing, and competitive strategy. Together, these analyses provide a comprehensive view of consumer preferences, critical for informed decision-making in product portfolio management.

### Limitations and Future Research
While the analysis provide robust insights, they come with limitations. The conjoint analysis assumes that all attributes are equally tradeable and that consumer preferences are linear and additive, which may not always reflect real-world scenarios (Green and Srinivasan, 1990). Additionally, Jolliffe's book "Principal Component Analysis" (2002) provides a comprehensive overview of PCA and its underlying assumptions, including the assumption of linearity, potentially overlooking complex, non-linear relationships between attributes.

Future research could explore non-linear models in conjoint analysis to account for possible interaction effects between attributes. Similarly, alternative dimensionality reduction techniques, such as t-SNE, could be used to capture non-linear patterns in product perceptions
In conclusion, the findings provide actionable insights that can inform strategic decisions in product design, marketing, and positioning. However, continuous research is necessary to adapt and refine the understanding of consumer behaviour in a dynamic market.



## References

Abdi, H. and Williams, L.J., 2010. Principal component analysis. Wiley interdisciplinary reviews: computational statistics, 2(4), pp.433-459.
Aoki, S. and Takemura, A., 2012. Design and analysis of fractional factorial experiments from the viewpoint of computational algebraic statistics. Journal of Statistical Theory and Practice, 6(1), pp.147-161.
Djokic, N., Salai, S., Kovac-Znidersic, R., Djokic, I. and Tomic, G., 2013. The use of conjoint and cluster analysis for preference-based market segmentation. Engineering Economics, 24(4), pp.343-355.
Dolnicar, S., Grün, B., Leisch, F., Dolnicar, S., Grün, B. and Leisch, F., 2018. Market Segmentation. Market segmentation analysis: Understanding it, doing it, and making it useful, pp.3-9.
Eggers, F. and Sattler, H., 2009. Hybrid individualized two-level choice-based conjoint (HIT-CBC): A new method for measuring preference structures with many attribute levels. International Journal of Research in Marketing, 26(2), pp.108-118.
Green, P.E. and Srinivasan, V., 1990. Conjoint analysis in marketing: new developments with implications for research and practice. Journal of marketing, 54(4), pp.3-19.
Gunst, R.F. and Mason, R.L., 2009. Fractional factorial design. Wiley Interdisciplinary Reviews: Computational Statistics, 1(2), pp.234-244.
Hauser, J.R. and Urban, G.L., 1986. The value priority hypotheses for consumer budget plans. Journal of consumer research, 12(4), pp.446-462.
Jolliffe, I.T., 2002. Principal Component Analysis. SpringerSeries in Statistics/Springer google schola, 2, pp.903-995.
Kim, H., Chen, J., Kim, E. and Agogino, A.M., 2017, August. Scenario-based conjoint analysis: measuring preferences for user experiences in early stage design. In International Design Engineering Technical Conferences and Computers and Information in Engineering Conference (Vol. 58219, p. V007T06A042). American Society of Mechanical Engineers
Marketing Analytics Muhammad Mattin Sharif
17
Netzer, O., Toubia, O., Bradlow, E.T., Dahan, E., Evgeniou, T., Feinberg, F.M., Feit, E.M., Hui, S.K., Johnson, J., Liechty, J.C. and Orlin, J.B., 2008. Beyond conjoint analysis: Advances in preference measurement. Marketing Letters, 19, pp.337-354.
Olson, E.L., 2008. The implications of platform sharing on brand value. Journal of Product & Brand Management, 17(4), pp.244-253.
Orme, B., 2002. Interpreting conjoint analysis data. Sawtooth Software Research Paper Series.
Pistol, L. and Bucea-Manea-Tonis, R., 2017. Model of Simulation for Optimizing Marketing Mix through Conjoint Analysis Case Study: Launching a Product on a New Market. Economics World, 5(4), pp.311-315.
Sa'Ed, M.S. and Al-Harris, M.Y., 2014. New product concept selection: an integrated approach using data envelopment analysis (DEA) and conjoint analysis (CA). International Journal of Engineering & Technology, 3(1), p.44.

