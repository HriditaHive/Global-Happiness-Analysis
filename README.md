# Global-Happiness-Analysis
In this project, we leverage generative AI to streamline the creation of Python code for data preparation, analysis, visualization, and dashboarding. By automating these steps, the project facilitates efficient and reproducible workflows, making it easier to generate insights on the state of global happiness.

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

## Software And Libraries Used
Jupyter Notebook - A web-based tool that enables users to write, execute, and document code in an interactive environment, ideal for data analysis, visualization, and sharing reproducible research.
AI Classroom by Skills Network - A generative AI tool designed to help explore and master AI skills, including prompt engineering and large language model selection. 
Python 3 - Libraries used are Pandas, Numpy, Seaborn and Plotly.

## Setup
In Jupyter Notebook, do the following things to set it up to run the prompt-generated Python codes:

- **Install required libraries**
  ```
  %pip install seaborn
  ```

- **Downloading the dataset**
  ```
  import requests

  # Fetch the CSV file
  response = requests.get(URL)

  # Check if the request was successful
  if response.status_code == 200:

     # Write the response content to a local file
     with open("dataset.csv", 'wb') as f:
         f.write(response.content)
  ```       
   Replace the URL with the path of the dataset. 
  

## Process Overview
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

3. **Exploratory Data Analysis**
   Write prompts that generate codes to perform the following actions:     

   1. Identify the GDP per capita and Healthy Life Expectancy of the top 10 countries:
      ```
      Write a python code that identifies the GDP per capita and Healthy Life Expectancy of the top 10 countries and create a bar chart named fig1 to show the GDP per capita and Healthy Life Expectancy of these top 10 countries using plotly.
      ```

   2. Find the correlation between the Economy (GDP per Capita), Family, Health (Life Expectancy), Freedom, Trust (Government Corruption), Generosity and Happiness score:
      ```
      Write a python code that performs the following actions:
      1. Create a sub-dataset including Economy (GDP per Capita), Family, Health (Life Expectancy), Freedom, Trust (Government Corruption), Generosity, and Happiness Score attributes from the dataframe (df).
      2. Find the correlation between the attributes in the subdataset as a heatmap named fig2 using Plotly of width 800 and height 600.
      ```

   3. Create a scatter plot to identify the effect of GDP per Capita on Happiness Score in various Regions. Plotly is used for creating the plot:
      ```
      Write a code that creates a scatter plot named fig3 between Happiness Score and GDP per Capita attributes of a dataframe using Plotly. Use Region to color the data points on the scatter plot.
      ```

   4. Create a pie chart to present Happiness Score by Regions:
      ```
      Write a Plotly code that creates a pie chart named fig4 to present Happiness Score by Region attributes of dataframe df.
      ```

   5. Create a map to display GDP per capita of countries and include Healthy life expectancy to be shown as a tooltip:
      ```
      Write a Plotly code that creates a map named fig5 to display GDP per capita of countries and include Healthy Life Expectancy to be shown as a tooltip.
      ```

4. **Dashboard Creation**
   The prompt that generates the code to write the graph plots generated in the previous steps into a HTML page called ```dashboard.html``` is as follows:
   ```
   Write Python code to write the Plotly figures (fig1, fig2, fig3, fig4, fig5) to a single HTML file named “dashboard.html”
   ```

5. **Narrative Generation**
   The prompt is as follows:
   ```
   Generate a narrative to present the dashboard on world happiness report with the following charts:-
   1. A heatmap showing correlation
   2. A scatter plot to identify the effect of GDP per Capita on Happiness Score in various Regions
   3. A pie chart to present Happiness score by Regions
   4. A map to display `GDP per capita` of `countries` and include `Healthy Life Expectancy` to be shown as a tooltip
   ```
   
## Conclusion
In conclusion, the analysis of global happiness highlights that economic stability, health, social support, and governance are key determinants of happiness across nations. Wealthier countries with higher GDP per capita and longer life expectancies consistently report higher happiness levels, underscoring the importance of financial security and healthcare access. Furthermore, the positive correlation between happiness and factors like freedom, low corruption, and social support suggests that the quality of life is also closely tied to societal trust and individual freedoms. While regional disparities exist, with Western nations generally scoring higher in happiness, these findings emphasize that fostering environments with strong economic foundations, accessible healthcare, and trustworthy institutions can improve life satisfaction worldwide. These insights can inform policy efforts, especially in regions where happiness scores are lower, to focus on strengthening healthcare, economic opportunity, and institutional integrity to enhance overall well-being.

## Acknowledgments
Special thanks go to the World Happiness Report team for compiling and making this valuable dataset publicly available, allowing for deep insights into the factors influencing happiness across various countries. We also appreciate the open-source Python libraries, including Pandas, Seaborn, and Matplotlib, which facilitated efficient data handling, visualization, and analysis throughout this project. Additionally, we acknowledge the contributions of the data analytics community for their shared knowledge, which was instrumental in enhancing our approach to data exploration and visualization. Finally, thanks to the generative AI tools that helped streamline the code generation process, making it possible to analyze and present complex data insights effectively.
