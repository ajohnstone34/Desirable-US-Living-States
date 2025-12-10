Recap Background & Question

The intent of this study is to identify the most desirable places in the United States to live, based off of a combination of different cost, infrastructure, and safety statistics. 
My hypothesis is that the most desirable states will be areas will be border sitting counties neighboring the more expensive states. For example, Hillsborough County New Hampshire which borders Massachusetts, allowing you for easy access but to still benefit from some of the tax incentives of being a New Hampshire resident. 

Methods

The plan for preprocessing has been to load and clean all individual datasets, join them, and the test and create a penultimate model. Amidst completing the individual steps of this process it became clear that many of the sources at the county level appeared to have mismatches in their county overall count and/or had holes within the datasets in numerous regions. Due to this there would not be enough data to properly complete our analysis so we adjusted to make a multilayer approach where we will now first filter by desirable states, and then introduce county data where possible. 

Some of the preprocessing steps taken in this study include feature selection, deletion, and imputation among others. These steps are intended to organize and clean the data, making it so the eventual data exploration and analysis is a much easier process.

To perform feature selection I used a combination of statistical analysis and correlation tests to ultimately determine what to leave in and out of the initial models that were tested. Results of correlation tests that showed extremely high correlation indicated that it may be redundant to include both fields, leading to the list of included fields being narrowed down. 

Results 

Each table required unique cleaning and adjusting in order to be ready for the joining, data analysis, and model testing. The below will step through adjustments made for each data table. 
For the 2024 Reported Violent and Property Crime dataset I took the necessary actions of combining the crime totals as reported by each agency as well as combining the totals of each crime across all agencies. This provides us with a unique field where we have the totals of all crimes reported by all groups. As a part of this formulating I also added the median of the total count to be listed as the count on two of the states as their crime data was not collected/reported like it was for the alternative majority of states. 
All other tables that have fields included in the eventual model testing period were adjusted by removing redundant fields as determined by correlation tests as well as statistical analysis. In most of the utilized tables, the majority of redundant fields were variables that were tracked over time, removing older years information so that the model is focused solely on the most recently available data in each category. 

