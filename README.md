# usedcarsales
# Used car sale price predication using Linear Algorithm and EDA
# Overview
In this application, we delved into a dataset sourced from Kaggle, initially comprising information on 3 million used cars, which we downsized to 426K entries to expedite processing. Our primary aim was to discern the factors influencing a car's pricing. Through our analysis, we seek to furnish the client, a used car dealership, with actionable insights into the features consumers value in a pre-owned vehicle.

# CRISP-DM
We adhered to the CRISP-DM framework, a standard methodology, to guide our approach and analysis.

# Business Understanding
From a business standpoint, our objective is to uncover the key determinants of used car prices. This entails transforming our business goal into a data-centric problem statement.

# Determine Business Objectives
a. Background: We possess a dataset featuring details on 426k used cars alongside their respective prices.

b. Business Objectives: Our aim is to decipher which features contribute to a car's pricing, ultimately facilitating informed advice to our client regarding consumer preferences.

c. Business Success Criteria: The model's success lies in its ability to offer recommendations to the client based on consumer-valued features, achieved through accurate price predictions using the provided feature set.

# Assess Situation
a. Inventory of Resources: We leveraged past lectures, notebooks, assignments, and online resources like search engines.

b. Requirements, Assumptions, and Constraints: We operated with a subset of the dataset to circumvent hardware limitations and assumed data accuracy.

c. Risks and Contingencies Terminology: A flawed or overfitted model poses risks to our client, necessitating robust validation measures.

d. Costs and Benefits: The model's potential benefits include optimizing sales by targeting appealing car features, applicable to dealerships nationwide.

# Determine Data Mining Goals
a. Data Mining Goals: Our immediate focus is on exploratory data analysis and data preprocessing to prepare the dataset for model training.

b. Data Mining Success Criteria: Success hinges on having sufficient data to unveil feature-target relationships and ensuring data cleanliness to derive meaningful insights from both categorical and continuous features.

Produce Project Plan
a. Project Plan: Following the CRISP-DM framework, our plan involves data exploration, preprocessing, feature selection, model exploration, evaluation, and model selection.

b. Initial Assessment of Tools and Techniques: We opted for libraries like scikit-learn, NumPy, Pandas, and Seaborn for data exploration and modeling.

# Findings
Data Exploration
Eliminated the "id" feature as redundant.
Retained key features: manufacturer, year, cylinders, fuel, odometer, transmission, state, model, 
Dropped features with excessive missing data or negligible correlation: VIN and Size
Our analysis highlights the significance of several features:
Identified 40K VIN has duplicate records amounting to 170K+ . identified and dropped rows related to duplicate VIN

Year: Positively correlates with price; newer vehicles command higher prices.
Mileage: Inversely related to price; lower mileage translates to higher prices.
Condition: Better condition correlates with higher prices.
Title status: Affects price positively, along with condition.
Tyoe : SUV/Pick up vs sedan 
fuel : GAS/Electric vs Diesel plays a important role in price

Based on our findings, crucial factors influencing price include year of year, mileage, condition, title status, and fuel type.

Models:
Based on our analyis simple Lasso or Ridge model is best suited to model and predict the price using low MSE/MAE and better R2 scores. 
Further refinement could involve narrowing down features and exploring alternative models. Additional features could be sourced, and insights from domain experts could be sought for enhanced model performance.

Conclusion
Our analysis underscores the importance of key features in determining used car prices. By leveraging these insights, we are poised to deliver valuable recommendations to our client, aiding them in catering to consumer preferences effectively.
