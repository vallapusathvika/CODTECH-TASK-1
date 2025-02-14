# CODTECH-TASK-1
COMPANY:CODTECH IT SOLUTIONS
NAME:VALLAPU SATHVIKA
INTERN ID:COD123
DOMAIN:PYTHON PROGRAMMING
DURATION:4 WEEKS
MENTOR:NEELA SANTOSH
  **DESCRIPTION OF THE CODE***

This code is executed in a **Jupyter Notebook** and demonstrates how to load, preprocess, and visualize weather data using **Pandas**, **Matplotlib**, and **Seaborn**. The main objective of the code is to analyze and present weather parameters, including temperature, humidity, wind speed, and precipitation, over time through various plots.


 **Libraries and Tools Used**

1. **Pandas**: 
   - **Pandas** is a powerful Python library used for data manipulation and analysis. It provides data structures like DataFrames and Series that allow for efficient handling of structured data. In this code, **Pandas** is used to load the CSV file, preprocess the data, and clean it by removing rows with missing values in essential columns.
   
2. **Matplotlib**:
   - **Matplotlib** is a popular plotting library in Python. It is used to generate static, animated, and interactive plots. In this code, **Matplotlib** is used for creating time-series plots of weather parameters like temperature, humidity, wind speed, and precipitation, across different subplots.

3. **Seaborn**:
   - **Seaborn** is built on top of **Matplotlib** and simplifies the process of creating attractive, informative statistical visualizations. While **Seaborn** is imported in the code, it is not directly used here. However, it could be easily integrated into the plotting process to enhance the style and appearance of the visualizations.

 **Step-by-Step Breakdown of the Code**

 1. **Loading the Data**
   - The weather data is loaded from a CSV file using **Pandas'** `pd.read_csv(file_path)`. The CSV file contains weather-related information such as temperature, humidity, wind speed, and precipitation type. The DataFrame `df` stores this data, allowing easy manipulation and analysis. The file path points to the location where the data is stored on the local machine.

 2. **Date Parsing and Preprocessing**
   - The `'Formatted Date'` column contains date information stored as strings. These strings are converted to **datetime** objects using **Pandas'** `pd.to_datetime()`. This conversion allows for easier manipulation of the data based on time, such as plotting time-series graphs.
   - The `errors='coerce'` parameter ensures that any invalid date formats are converted to `NaT` (Not a Time), which allows the code to handle errors gracefully.
   - The next step is to clean the data by removing any rows with missing values in essential columns such as `'Formatted Date'`, `'Temperature (C)'`, `'Humidity'`, `'Wind Speed (km/h)'`, and `'Precip Type'`. The `df.dropna()` function achieves this, ensuring that only rows with complete data are used for plotting.
 3. **Creating Subplots**
   - The core of the visualization is the creation of subplots using **Matplotlib**. The code creates a figure with a size of 12x10 inches to accommodate the plots. It then defines a 2x2 grid of subplots, where each subplot represents one weather parameter over time:
     - **Temperature (°C) over Time**: The first subplot (top-left) shows how the temperature changes over time. This plot uses red markers to represent the data points.
     - **Humidity (%) over Time**: The second subplot (top-right) shows the variation of humidity over time. The plot uses blue markers.
     - **Wind Speed (km/h) over Time**: The third subplot (bottom-left) visualizes wind speed variations over time with green markers.
     - **Precipitation (Rain) over Time**: The fourth subplot (bottom-right) shows whether it rained or not at each time point. A new column `'Rain'` is created by applying a lambda function to the `'Precip Type'` column, where the value is 1 if it rained (i.e., `'rain'` in the `'Precip Type'` column) and 0 if there was no rain. This is represented by a bar chart with purple bars.

 4. **Final Plot Adjustments**
   - After plotting the individual subplots, the `plt.tight_layout()` function is called to automatically adjust the spacing between the subplots to prevent overlap and ensure that each plot is clearly visible. This function improves the layout and presentation of the figure.
   - Finally, `plt.show()` is used to display the complete figure with all four subplots.

 **Conclusion**

This code effectively demonstrates how to use **Pandas** for data preprocessing and **Matplotlib** for visualization. By creating time-series plots, it allows the user to analyze trends in various weather parameters like temperature, humidity, wind speed, and precipitation over time. The use of **Jupyter Notebook** enables interactive execution, making it easy to view and modify the code step-by-step. The preprocessing steps ensure that only valid and complete data is used for analysis, providing accurate visualizations. Although **Seaborn** is not utilized here, it could be integrated to enhance the appearance of the plots or provide more advanced statistical visualizations.
***OUTPUT***: ![Image](https://github.com/user-attachments/assets/09f4b32e-8a11-47f2-87dd-d0949e5da114)


