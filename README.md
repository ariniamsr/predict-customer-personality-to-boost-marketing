# Predict-Customer-Personality-to-boost-marketing-campaign-by-using-Machine-Learning

## overview

“ A company can develop rapidly when it knows the behavior of it’s customer personality, so that it can provide better services and benefits to customers who have the potential to become loyal customers. By processing historical marketing campaign data to improve performance and target the right customers, so they can transcat on the company’s platform, from this data insight our focus is to create a cluster prediction model to make it easir for companies to make decisions.

## Exploratory Data Analysis

### Univariate Analysis

#### Numerical Boxplot
![image](https://github.com/ariniamsr/Predict-Customer-Personality-to-Boost-Marketing-Campaign-by-Using-Machine-Learning/blob/main/Pic/EDA%20uni%20num.png)

From the boxplot above, it can be seen that there is an outlier that is not too far from the other data. This outlier is located between the upper and lower bounds of the boxplot. This indicates that the outlier is still within the reasonable range of values for the data.

#### Numerical Distplot
![image](https://github.com/ariniamsr/Predict-Customer-Personality-to-Boost-Marketing-Campaign-by-Using-Machine-Learning/blob/main/Pic/EDA%20uni%20num2.png)

1. The following variables are normally distributed: 'total_transaksi', NumWebVisitsMonth, NumStorePurchases, NumWebPurchases, NumDealsPurchases, Recency, Year_Birth
2. The following variables are positively skewed: MntCoke, MntFruits, MntMeatProducts, MntFishProducts, MntSweetProducts, MntGoldProds, conversion_rate
3. The following variables are bimodal or have more than 1 mode: total_acc_cmp, jumlah_anak, Kidhome, Teenhome
   
### Multivariate Analysis
![image](https://github.com/ariniamsr/Predict-Customer-Personality-to-Boost-Marketing-Campaign-by-Using-Machine-Learning/blob/main/Pic/Multivariate%20Analysis.png
)

## Conversion Rate 
### Conversion Rate Based On Age
![image](https://github.com/ariniamsr/Predict-Customer-Personality-to-Boost-Marketing-Campaign-by-Using-Machine-Learning/blob/main/Pic/Conversion%20Ratio%20Based%20on%20Age.png
)
There is a significant relationship between customer age and conversion rate, where adults tend to have a greater impact on conversion rate than teenagers and the elderly. This is because adults are in their active age and have a higher income than teenagers and are more active than the elderly.

### Conversion Rate Based On Jumlah Anak
![image](https://github.com/ariniamsr/Predict-Customer-Personality-to-Boost-Marketing-Campaign-by-Using-Machine-Learning/blob/main/Pic/Conversion%20Ratio%20Based%20on%20Anak.png
)
The graph above shows the relationship between conversion rate and the number of children. It can be seen that people with no children tend to have a higher conversion rate than people with one or more children.




















![image](https://user-images.githubusercontent.com/94748637/215256808-4dad30ba-9444-4d81-b16b-144b2a834e4a.png)

From picture above, we can see at total amount and income have a low positive correlation with cvr, at total children, if the customer have fewer children, the value of cvr will be higher.

![image](https://user-images.githubusercontent.com/94748637/215256824-1c8472ee-78dc-4a81-b186-555a1bf3b277.png)

From picture above, the distribution of data in the response column looks quite even, and at total purchase have a low positive correlation with cvr.

## Data Preprocessing

![image](https://user-images.githubusercontent.com/94748637/215256867-42623f1d-a79f-41de-8718-b466a5ef920b.png)

![image](https://user-images.githubusercontent.com/94748637/215256878-d47cde77-c9b7-49f8-855d-0feac05d4966.png)

![image](https://user-images.githubusercontent.com/94748637/215256890-4961decb-86b2-41ab-bda1-58ec8dd96827.png)

![image](https://user-images.githubusercontent.com/94748637/215256908-f72097ec-85c4-411a-8577-b7a3cda08cbf.png)

![image](https://user-images.githubusercontent.com/94748637/215256913-89fb9967-0d58-43c4-9093-c048e0c912e8.png)


## Modelling K-Means

For segmenting customer, there is a method called RFM Analysis, for you want to know deeply about RFM can read this reference
https://www.barilliance.com/rfm-analysis/#:~:text=RFM%20analysis%20is%20a%20data,much%20they've%20spent%20overall.

![image](https://user-images.githubusercontent.com/94748637/215256927-f9105917-d8e9-4237-8335-590ae2a0da8b.png)

### Elbow Score

![image](https://user-images.githubusercontent.com/94748637/215256931-72357e29-da18-4476-b214-d7f0ccf6871e.png)

### Silhouette Score

![image](https://user-images.githubusercontent.com/94748637/215256957-57d383fe-ce9a-4afc-bfbc-15aa27906276.png)

### Modelling Result

![image](https://user-images.githubusercontent.com/94748637/215256975-43a2920d-ba75-4d97-baaf-b69bd67df3fc.png)

1. High Valued Customer
Customers on this group have low average recency (21 days), high average total purchase (22 times) and high average total amount (1,23 Million Rupiah).
There 18,44 % of our customer fall into this category.
There are 236 customer never accept our campaign, 107 accepted it once, 42 accepted it twice, 20 accepted it three times and 6 accepted it four times.

2. Medium Valued Customer
Customers on this group have high average recency (71 days), high average total purchase (22 times) and high average total amount (1,18 Million Rupiah).
There 24.09 % of our customer fall into this category.
There are 354 customer never accept our campaign, 116 accepted it once, 38 accepted it twice, 24 accepted it th

3. Low Valued Customer
Customers on this group have low average recency (23 days), low average total purchase (10 times) and low average total amount (172K Rupiah).
There 29.03 % of our customer fall into this category.
There are 590 customer never accept our campaign, 54 accepted it once and 3 accepted it twice.

4. Very Low Valued Customer
Customers on this group have high average recency (73 days), low average total purchase (10 times) and low average total amount (151K Rupiah).
There 28,44 % of our customer fall into this category.
There are 587 customer never accept our campaign and 47 accepted it once.

### Potential Impact

If we keep prioritize on customer cluster and they have similar character like in our data, we still have potential GMV Rp 1.34 Billion with details :

High Value Customer : Rp 506 Million
Medium Value Customer : Rp 365 Million
Low Value Customer : Rp 111 Million
Very Low Value Customer : Rp 95 Million

## Business Recommendation

If we calculate the potential impact by focusing on retargeting marketing on Cluster 3 and Cluster 1, then the total spending we will receive is Rp 626855000 for Cluster 3 and Rp 557668000 for Cluster 1, with a potential impact of 46.33% and 41.21%.

Explanation:

In this case, the potential impact is calculated as the percentage increase in total spending that is expected to occur as a result of retargeting marketing. The potential impact for Cluster 3 is 46.33%, which means that we can expect total spending to increase by 46.33% if we focus our retargeting marketing efforts on this cluster. The potential impact for Cluster 1 is 41.21%, which means that we can expect total spending to increase by 41.21% if we focus our retargeting marketing efforts on this cluster.

It is important to note that these potential impacts are just estimates. The actual impact of retargeting marketing will vary depending on a number of factors, such as the quality of the targeting, the effectiveness of the messaging, and the overall economic climate.
