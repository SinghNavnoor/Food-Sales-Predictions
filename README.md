# Grocery Sales Predictions 
## Analyzing various aspects of Item placement and features to predict its sales. 

### Navnoor Singh Kahlon

## Dataset:

<img width="500" alt="Screen Shot 2022-11-19 at 12 53 54 AM" src="https://user-images.githubusercontent.com/86537623/202843169-a05e30dd-9de5-4be4-9906-5da813b0c3e1.png">


## Methods for preparing and understanding the data:
### Data Cleaning
- Used python methods like .isna() and .duplicated() to see if any columns had null values or any duplicates. 
- The missing values were imputed with mean and most frequent categories. The duplicate rows were dropped.
- Columns with inconsistencies like spelling mistakes were dealth accordingly. 
- For the machine learning, three columns were dropped which were not adding much to the understanding of the dataset. 

### Exploratory Visualization:
#### First a heatmap was created to look for any correlation between the columns.

![heatmap_of_correlation_final5](https://user-images.githubusercontent.com/86537623/202860920-72a7b68a-a89a-42ef-bf63-658bdd3e23b6.png)
- In the heatmap we saw that most columns had either weak negative correlation or weak positive correlation.
- The most positively correlated columns were the Sales and their Price. 

#### Columns with high correlation were further explored with a combination of histogram, boxplot, barplot or scatterplot. 

![sales_histo_ _boxplot](https://user-images.githubusercontent.com/86537623/202860773-fe55a3b1-3594-4413-9d4c-ec2dd6ec9755.png)
- This Outlet Sales histogram shows that sales are heavily right skewed.
- Boxplot showed that while most of the Sales happened under the 4000 price range some items sold for upto 12000 as well. 

![sales_outlet_type_barplot](https://user-images.githubusercontent.com/86537623/202663954-a0b465e3-3790-4ab8-930d-08293ffe5939.png)

- Supermarket Type 3 has done the most sales of all the other Outlet types, including some of the largest sales as well.
- All Outlet types have some items that sold at an unusual amount compare to where most items were.

### Explanatory Visualizations:
![price_sales_fat_content2](https://user-images.githubusercontent.com/86537623/202863415-962f1804-4231-44e7-b6ce-860727944fcc.png)
- At every price, every type of fat content item has does some amount of sale.

![price_items_fat_content](https://user-images.githubusercontent.com/86537623/202663974-45d793bd-2db6-4592-8c0c-1e227ca6d68f.png)
- There is a Low Fat content option available for every item in the store, while some items don't have any Regular Fat content items.

### Fat Content - Sales - Price - Outlet Type
![sales_outlet_type4](https://user-images.githubusercontent.com/86537623/202863046-8b1fce4f-f1f0-4341-88a5-8cfa6dcc76af.png)

![price_outlet_type4](https://user-images.githubusercontent.com/86537623/202863044-8733f593-2f6c-452d-a73d-97df06c2e446.png)
#### Analysis:
- Considering both barplots, we found that if a Low Fat content item in an outlet is priced higher than its regular fat content counterpart and vis-versa it will also have a higher number of sales. 

### Machine Learning
#### Decision Tree 
##### With a pipeline
<img width="500" alt="Screen Shot 2022-11-18 at 12 56 16 AM" src="https://user-images.githubusercontent.com/86537623/202663979-f0764817-f022-47ce-ab95-7e4f1b44d41e.png">

#### Random Forest
##### With a pipeline
<img width="500" alt="Screen Shot 2022-11-18 at 12 56 53 AM" src="https://user-images.githubusercontent.com/86537623/202663987-093b65d0-4aa4-40ce-acbe-5ae2ba73f845.png">

## Results:
- The best prediction models came out of tuning the Decision Tree and Random Forest. 
- Linear Regression model turned out to be inadequate.

### Decision Tree:
- Training Score = 60%
- Testing Score = 57%

### Random Forest:
- Training Score = 93%
- Testing Score = 53%

### Which Model to implement?
- Implementing Decision Tree is the better option.
- Considering that no model had an R^2 score of greater than 60%,  Decisions Tree has the most well fit model as its training and testing R^2 score are only apart by 3 percent points. 
- We might get into overfitting if we use Random Forest. 








