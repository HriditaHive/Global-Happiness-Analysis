# Global-Happiness-Analysis

## Project Scenario
A healthcare consultancy firm has been conducting a survey on the state of global happiness annually. The World Happiness Report offers valuable insights into factors influencing happiness across countries. As a data analyst, the firm wants me to produce a report to find out whether there are demographic, regional, and/or economic characteristics that lead to a better life.

## Data Source
This is a public dataset available on the Kaggle website as World Happiness Report. For this project, I have worked on the data from 2016 which has been slightly modified for the purpose of this project.
For ease of use, the dataset has been provided in this repository as **2016.csv**

## Dataset Description
The World Happiness Report is a landmark survey of the state of global happiness. The reports review the state of happiness in the world today and show how the new science of happiness explains personal and national variations in happiness.            
The attributes of this dataset have been explained below:               
- Country - Name of the country            
- Region - Region the country belongs to            
- Happiness Rank - Rank of the country based on the Happiness Score              
- Happiness Score	- A metric measured in 2016 by asking the sampled people the question: "How would you rate your happiness?"                
- Lower Confidence Interval	- Lower confidence interval of the Happiness Score               
- Upper Confidence Interval	- Upper confidence interval of the Happiness Score           
- Economy (GDP per Capita)	- The extent to which GDP contributes to the calculation of the Happiness Score           
- Family	- The extent to which family contributes to the calculation of the Happiness Score           
- Health (Life Expectancy)	- The extent to which life expectancy contributes to the calculation of the Happiness Score        
- Freedom	- The extent to which freedom contributes to the calculation of the Happiness Score           
- Trust (Government Corruption)	- The extent to which trust contributes to the calculation of the Happiness Score          
- Generosity -	The extent to which generosity contributes to the calculation of the Happiness Score              
- Dystopia Residual	- Dystopia is an imaginary country that has the world's least-happy people. The residuals, or unexplained components, differ for each country, reflecting the extent to which the six variables either over- or under-explain average 2014-2016 life evaluations. These residuals have an average value of approximately zero over the whole set of countries.

## Objectives
1. Data cleaning to check the correctness of the data types in the dataset and get rid of any possible missing values.
2. Perform exploratory data analysis to draw keen insights on the data:
  - Identify the GDP per capita and Healthy Life Expectancy of the top 10 countries.and represent it as a bar chart.
  - Find the correlation between the Economy (GDP per Capita), Family, Health (Life Expectancy), Freedom, Trust (Government Corruption), Generosity, and Happiness Score.
  - Create a scatter plot to identify the effect of GDP per Capita on Happiness Score in various Regions.
  - Create a pie chart to present Happiness Score by region.
  - Create a map to display GDP per capita of countries and include Healthy Life Expectancy as a tooltip.
3. Create a dashboard with the visualizations.
4. Generate the narrative to present the dashboard.

## Software Used
Jupyter Notebook     

## Analysis Process
The data set is analysed using Python in Jupyter Notebook. The Generative AI tool is given prompts to generate code and the prompt-generated code is tested and leveraged in Jupyter Notebook to carry out various tasks like data preparation, analysis, visualization, and dashboarding.        

1. **Load the dataset**
   The Generative AI model is used to create a python script that can load the dataset to a pandas dataframe. The dataset file already has the headers in the first row.
   The prompt is as follows:        
   ```
   Write a Python code that can perform the following tasks:
   1. Read the CSV file, located on a given file path, into a pandas data frame, assuming that the first row of the file can be used as the headers for the data.
   2. Print the first 5 rows of the dataframe to verify correct loading.
   ```

2. **Data Cleaning**
   The data needs to be cleaned in order to ensure that there are no missing values as well as the columns in the dataset have the right data type.

   - Check for correct data types:
     The prompt to list the data types of the columns and check if there is any column type that is unsuitable, is as follows:
     ```
     Write a python code that performs the following tasks:
     1. Check the data types of the columns and see if it correct.
     ```

   - Change the data types:
     The prompt to change the data type to an appropriate type is as follows:
     ```
     Write a python code to do the following tasks as per latest pandas:
     1. Remove leading and trailing whitespaces from the values in a column.
     2. Clean a column in a DataFrame by replacing empty strings with NaN values.
     3. Change the data type of the columns to appropriate type as per the latest version of pandas.
     ```

   - Check for missing values:
     The prompt to remove any missing values is as follows:
     ```
     Write a python code that performs the following tasks as per latest pandas:
     1. Identify the columns of a data frame with missing values.
     2. Replace the missing values thus identified with mean values of the column.
     ```
