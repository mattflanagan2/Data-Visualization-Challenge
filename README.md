# Data Visualization Challenge

## Instructions
* Prepare the data.
* Generate summary statistics.
* Create bar charts and pie charts.
* Calculate quartiles, find outliers, and create a box plot.
* Create a line plot and a scatter plot.
* Calculate correlation and regression.
* Submit your final analysis.

## Process

### Preparing the Data
I prepared the data by running the provided package dependency and data imports. Then, I merged the mouse_metadata and study_results DataFrames into a single DataFrame.

![Screenshot 2024-03-26 at 4 25 53 PM](https://github.com/mattflanagan2/Data-Visualization-Challenge/assets/146908072/85698aae-b8a9-4e03-b3d8-f32e93da8213)


Next, I displayed the number of unique mice IDs in the data and checked for any mouse ID with duplicate time points. After identifying the mouse ID with duplicate time points, I displayed the data associated with that mouse ID and created a new DataFrame where this data was removed. I used this cleaned DataFrame for the remaining steps.
Finally, I displayed the updated number of unique mice IDs.

<img width="1307" alt="Screenshot 2024-03-26 at 4 27 43 PM" src="https://github.com/mattflanagan2/Data-Visualization-Challenge/assets/146908072/bc3d0fe5-025b-4d3e-a9aa-10d3fce238fe">
<img width="1307" alt="Screenshot 2024-03-26 at 4 28 55 PM" src="https://github.com/mattflanagan2/Data-Visualization-Challenge/assets/146908072/f80fb8ab-2a3b-433a-adf2-4f25a0706b02">

### Summary Statistics
Next, I created a DataFrame of summary statistics.
The Summary Statistics included:

A row for each drug regimen, with the regimen names contained in the index column.
Columns for each of the following statistics: mean, median, variance, standard deviation, and SEM of the tumor volume.

<img width="1307" alt="Screenshot 2024-03-26 at 4 31 33 PM" src="https://github.com/mattflanagan2/Data-Visualization-Challenge/assets/146908072/058cd274-8c31-45bb-9a8c-acf3f714bd04">
<img width="1307" alt="Screenshot 2024-03-26 at 4 31 33 PM" src="https://github.com/mattflanagan2/Data-Visualization-Challenge/assets/146908072/fa226bde-e16a-451d-926b-f1075634f2a7">


### Bar Charts and Pie Charts
Next, I generated two bar charts. Both charts were identical and showed the total number of rows (Mouse ID/Timepoints) for each drug regimen throughout the study.

For the first bar chart, I used the Pandas DataFrame.plot() method. For the second bar chart, I utilized Matplotlib's pyplot methods.

<img width="1307" alt="Screenshot 2024-03-26 at 4 34 15 PM" src="https://github.com/mattflanagan2/Data-Visualization-Challenge/assets/146908072/57260833-3fa0-4cac-8f1f-688907d76a31">
<img width="714" alt="Screenshot 2024-03-26 at 4 34 25 PM" src="https://github.com/mattflanagan2/Data-Visualization-Challenge/assets/146908072/cfe53453-d0d5-442a-8559-888ff52aad8c">
<img width="1250" alt="Screenshot 2024-03-26 at 4 34 38 PM" src="https://github.com/mattflanagan2/Data-Visualization-Challenge/assets/146908072/5c978bf9-3f18-496d-9faf-e1fb6158b71e">
<img width="696" alt="Screenshot 2024-03-26 at 4 34 50 PM" src="https://github.com/mattflanagan2/Data-Visualization-Challenge/assets/146908072/bb1f166a-7ff7-4d02-9652-d71b7b716cfe">


Additionally, I generated two pie charts. Both charts were identical and displayed the distribution of female versus male mice in the study.

For the first pie chart, I used the Pandas DataFrame.plot() method. For the second pie chart, I employed Matplotlib's pyplot methods.

<img width="1161" alt="Screenshot 2024-03-26 at 4 36 31 PM" src="https://github.com/mattflanagan2/Data-Visualization-Challenge/assets/146908072/96447dee-f0c6-4adc-b826-9b0d5ebcc356">
<img width="505" alt="Screenshot 2024-03-26 at 4 36 50 PM" src="https://github.com/mattflanagan2/Data-Visualization-Challenge/assets/146908072/7ab55959-e70a-4d34-b909-06288fed6cfa">
<img width="1161" alt="Screenshot 2024-03-26 at 4 36 41 PM" src="https://github.com/mattflanagan2/Data-Visualization-Challenge/assets/146908072/4c87b507-0457-4091-9c62-a219bd687605">
<img width="505" alt="Screenshot 2024-03-26 at 4 36 59 PM" src="https://github.com/mattflanagan2/Data-Visualization-Challenge/assets/146908072/75a638cc-af5d-4d7d-91d8-2a1d8a7b22ad">


### Quartiles, Outliers, & Box Plot
Next, I calculated the final tumor volume of each mouse across four of the most promising treatment regimens: Capomulin, Ramicane, Infubinol, and Ceftamin. Then, I calculated the quartiles and IQR, and determined if there were any potential outliers across all four treatment regimens.
Here are the steps I followed:

Created a grouped DataFrame that showed the last (greatest) time point for each mouse, and then merged this grouped DataFrame with the original cleaned DataFrame.

<img width="1316" alt="Screenshot 2024-03-26 at 4 40 11 PM" src="https://github.com/mattflanagan2/Data-Visualization-Challenge/assets/146908072/a26dc45a-b318-4653-b0cb-e7cc813a4d44">


Created a list to hold the treatment names as well as a second, empty list to hold the tumor volume data.
Looped through each drug in the treatment list, locating the rows in the merged DataFrame that corresponded to each treatment. I appended the resulting final tumor volumes for each drug to the empty list.
Determined outliers by using the upper and lower bounds, and then printed the results.

<img width="1316" alt="Screenshot 2024-03-26 at 4 41 07 PM" src="https://github.com/mattflanagan2/Data-Visualization-Challenge/assets/146908072/9bdf1a86-75a1-437d-aa8a-42cabc08eeff">
<img width="846" alt="Screenshot 2024-03-26 at 4 41 58 PM" src="https://github.com/mattflanagan2/Data-Visualization-Challenge/assets/146908072/d8012e45-7c36-4880-a0e2-7c0011cbbd5a">

Used Matplotlib to generate a box plot that showed the distribution of the final tumor volume for all the mice in each treatment group. I highlighted any potential outliers in the plot by changing their color and style.

<img width="1081" alt="Screenshot 2024-03-26 at 4 42 37 PM" src="https://github.com/mattflanagan2/Data-Visualization-Challenge/assets/146908072/ca5915e4-1670-4980-b7a4-5c7dac9d84aa">
<img width="687" alt="Screenshot 2024-03-26 at 4 42 46 PM" src="https://github.com/mattflanagan2/Data-Visualization-Challenge/assets/146908072/fc2b1fc1-8120-415b-bd30-478d1819ba88">

### Line Plot & Scatter Plot
Next, I selected a single mouse that was treated with Capomulin and generated a line plot of tumor volume versus time point for that mouse.

<img width="1306" alt="Screenshot 2024-03-26 at 4 45 31 PM" src="https://github.com/mattflanagan2/Data-Visualization-Challenge/assets/146908072/5a7ae6d0-a105-44b5-80b9-1609bf386804">
<img width="684" alt="Screenshot 2024-03-26 at 4 45 49 PM" src="https://github.com/mattflanagan2/Data-Visualization-Challenge/assets/146908072/88008392-83d4-4de5-a67f-3f4b126c9ead">

Additionally, I generated a scatter plot of mouse weight versus average observed tumor volume for the entire Capomulin treatment regimen.

<img width="1306" alt="Screenshot 2024-03-26 at 4 45 39 PM" src="https://github.com/mattflanagan2/Data-Visualization-Challenge/assets/146908072/5fc7b6d4-099a-485c-89e0-c8d7a40462e9">
<img width="684" alt="Screenshot 2024-03-26 at 4 45 57 PM" src="https://github.com/mattflanagan2/Data-Visualization-Challenge/assets/146908072/5c63b4a2-6a76-4d59-b24f-0b29a6ef549e">


### Correlation and Linear Regression
I calculated the correlation coefficient and linear regression model between mouse weight and average observed tumor volume for the entire Capomulin treatment regimen.
Furthermore, I plotted the linear regression model on top of the previous scatter plot.

<img width="1176" alt="Screenshot 2024-03-26 at 4 48 49 PM" src="https://github.com/mattflanagan2/Data-Visualization-Challenge/assets/146908072/63104ff2-12df-4a54-bcc5-1fa82fb67e31">
<img width="683" alt="Screenshot 2024-03-26 at 4 48 59 PM" src="https://github.com/mattflanagan2/Data-Visualization-Challenge/assets/146908072/ed9cf54a-5678-4242-b80d-7be9c7ee761e">

