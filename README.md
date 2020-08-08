# use-python-visual-data
Use python to visual data using matplotlib

#Import the required library
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

# Import your data: use .csv file to import
# I will use data retrieved from ourworldindata.org 
data=pd.read_csv('B:\WebBuild\Post_Document\Lesson_part\international-tourist-arrivals-by-world-region.csv', header=0)

# As we use time series to plot the data, we will define index_col function to set the Year/Month Variable
data=pd.read_csv('B:\WebBuild\Post_Document\Lesson_part\international-tourist-arrivals-by-world-region.csv', header=0, index_col=0)

# To view the data call the name for your defined dataframe; we what to view first five row
data.head(5)

# Now plot the data: one by one variable
plt.plot(data.Africa, color = 'black', label = 'Africa')# to select 'Africa' column or variable
plt.plot(data.America, color = 'red', label = 'America')# to select 'America' variable
plt.plot(data.AsiaPaci, color = 'green', label = 'Asia & Pacific')# to select 'Asia & Pacific' variable
plt.plot(data.Europe, color = 'blue', label = 'Europe')# to select 'Europe' variable
plt.plot(data.MidEast, color = 'yellow', label = 'Middle East')# to select 'Middle East' variable

# Individual graphs were shown but we need in a single graph< Just wait and see
##Give title and label of axis 
plt.plot(data.Africa, color = 'black', label = 'Africa')
plt.plot(data.America, color = 'red', label = 'America')
plt.plot(data.AsiaPaci, color = 'green', label = 'Asia & Pacific')
plt.plot(data.Europe, color = 'blue', label = 'Europe')
plt.plot(data.MidEast, color = 'yellow', label = 'Middle East')
plt.title('International Tourist Arrivals by World Region')
plt.xlabel('Time')
plt.ylabel('Number of Arrivals (100 Million)')
plt.legend()
plt.show()
