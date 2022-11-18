# Sales Prediction 
## The way an Item is treated and how it is presented at what location has a lot to do with its sales. 

### Author: Navnoor Singh Kahlon

## Sales Prediction Dataset:
<img width="500" alt="Screen Shot 2022-11-18 at 1 30 11 AM" src="https://user-images.githubusercontent.com/86537623/202668900-0a3322ea-2bd2-4fdb-abbc-885532801271.png">

<img width="500" alt="Screen Shot 2022-11-18 at 1 30 41 AM" src="https://user-images.githubusercontent.com/86537623/202668922-8924cf8d-5e04-4eb3-8692-c247250ad86a.png">

## Methods:
### Data Cleaning
- Used python methods like .isna() and .duplicated() to understand the data and dealt with it appropriately.
- Imputed missing values with mean and most frequent categories. 
- Dropped columns that were not adding much to the understanding of the dataset. 

### Visualization

![Sales_histogram](https://user-images.githubusercontent.com/86537623/202663934-b6b3084a-d005-4480-8c7c-a6d717561ccb.png)
- This Outlet Sales histogram shows that sales are heavily right skewed.

![sales_outlet_type_barplot](https://user-images.githubusercontent.com/86537623/202663954-a0b465e3-3790-4ab8-930d-08293ffe5939.png)

- Supermarket Type 3 does the most sales of all the other Outlet types, including some of the largest sales as well.
- All Outlet types have outliers.

![Price_Sales_Fat_Content](https://user-images.githubusercontent.com/86537623/202663966-0ff8d0d1-1cbe-4f30-88b1-3fd1be4f4538.png)
- At every price, every type of fat content item has does some amount of sale.

![price_items_fat_content](https://user-images.githubusercontent.com/86537623/202663974-45d793bd-2db6-4592-8c0c-1e227ca6d68f.png)
- There is a Low Fat content option available for every item in the store, while some items don't have any Regular Fat content items.

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








