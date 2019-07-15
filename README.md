# seattle-airbnb
Analysis of Airbnb listings data

### Table of Contents

1. [Installation](#installation)
2. [Project Motivation](#motivation)
3. [File Descriptions](#files)
4. [Results](#results)
5. [Licensing, Authors, and Acknowledgements](#licensing)

## Installation <a name="installation"></a>

This code uses Python 3 and the packages listed at the top of the notebook. 
These are numpy, pandas, matplotlib, sklearn, seaborn, re and time.

If the packages need installing, then all of them are available through PIP.

## Project Motivation<a name="motivation"></a>

The purpose of this project was to check the listings data from Airbnb to look for ways that an individual could boost their rental income. The three questions explored are:

1. How does rental income change for each extra individual that can be accomodated
2. Taking account of multiple factors, what can increase rental income by $5 or more per night
3. Taking account of multiple factors, what can decrease rental income by $5 or more per night

This project was also used as part of a Udacity course in Data Science

## File Descriptions <a name="files"></a>

There is one notebook (analysis.ipynb) which reads in the CSV data, cleans it, and performs all analysis.
Markdown cells and comments give some insights into the process taken and why.
There are also two folders:
- data - this contains three csv files as taken from Kaggle. Only the file listings.csv is used in this project.
- picture_outputs - this contains the file occupancy_graph.png which is output by the notebook and was used in a Medium post

## Results<a name="results"></a>

The main findings of the code can be found at the post available [here](https://medium.com/@sheffseankiely/how-to-maximise-your-income-on-airbnb-in-seattle-40b60a9acd7f?sk=bcd45e6e9feb43e99d7fe3de0580b136).
A simple regression model was created to answer two of the questions. 
Initial results had issues with multiple coefficients having the same value, and the conclusions that might be drawn from them not making sense. 
The cause of this was that some of the variables were fully correlated, so these had to be dropped. For example where the dummy variable for 'Cable TV' was present, then the dummy variable for just 'TV' was also always set to true because it is a sub string of the former. The solution to this was to drop these variables, and this fixed the issue.

## Licensing, Authors, Acknowledgements<a name="licensing"></a>

Must give credit to Airbnb for the data.  You can find the Licensing for the data and other descriptive information at the Kaggle link available [here](https://www.kaggle.com/airbnb/seattle/data).  Otherwise, feel free to use the code here as you would like! 
