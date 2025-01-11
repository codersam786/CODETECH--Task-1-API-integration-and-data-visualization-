# CODETECH--Task1

**Name:** MD SAMEER ANSARI

**Company:** CODTECH IT SOLUTIONS

**ID:** CT12WDS94

**Domain:** Python Programming

**Duration:** December to March 2024 


# CODETECH--Task-1-API-integration-and-data-visualization-
To fetch data from a public API such as OpenWeatherMap, you can use Python's requests library to make HTTP requests and retrieve the data. Here's a step-by-step guide to get data from the OpenWeatherMap API:

Steps:
# 1. Install the required libraries: If you haven't installed the requests library, install it using pip:

bash
Copy code
pip install requests

# 2. Obtain an API Key: To use the OpenWeatherMap API, you need to sign up at OpenWeatherMap and get your API key.

# 3.Write the Python Script: Below is an example script to fetch current weather data for a specific city:

# Explanation:
API_KEY: Replace 'your_api_key_here' with your actual OpenWeatherMap API key.
BASE_URL: The URL for the API endpoint.
params: The dictionary containing the parameters for the API request.
q: The city name (e.g., London).
appid: Your API key.
units: The units for temperature (metric for Celsius, imperial for Fahrenheit).






# OUTPUT
![Screenshot 2025-01-11 133001](https://github.com/user-attachments/assets/334a34a2-adc9-4565-8d61-089d747b0eb2)

# Create Visualization using matplotib
To create a simple visualization of the weather data using matplotlib, we can display the weather data (e.g., temperature, humidity, and wind speed) in a bar chart or other types of graphs.

Steps:
Install the required libraries (if you don't have them installed):

bash
Copy code
pip install matplotlib requests
Extend the previous script by adding code to visualize the data.

# Explanation:
matplotlib.pyplot: This library is used to create the bar chart.
labels: The labels represent the weather metrics (temperature, humidity, wind speed).
values: The values correspond to the actual weather data fetched from the API.
plt.bar(): This function is used to create the bar chart.
plt.show(): Displays the chart.

# Example Visualization:
This will display a simple bar chart where:

The x-axis contains the labels (Temperature, Humidity, Wind Speed).
The y-axis contains the actual values (in the respective units).
You can adjust the chart's style, colors, and other parameters to customize the visualization.

# Matplotlib supports a variety of plots including line charts, bar charts, histograms, scatter plots, etc. We will discuss the most commonly used charts in this article with the help of some good examples and will also see how to customize each plot.  

# 1. Line Chart
Line chart is one of the basic plots and can be created using the plot() function. It is used to represent a relationship between two data X and Y on a different axis.

Syntax:

matplotlib.pyplot.plot(\*args, scalex=True, scaley=True, data=None, \*\*kwargs)

# 2. Bar chart
 A bar chart is a graph that represents the category of data with rectangular bars with lengths and heights that is proportional to the values which they represent. The bar plots can be plotted horizontally or vertically. A bar chart describes the comparisons between the discrete categories. It can be created using the bar() method.

In the below example, we will use the tips dataset. Tips database is the record of the tip given by the customers in a restaurant for two and a half months in the early 1990s. It contains 6 columns as total_bill, tip, sex, smoker, day, time, size.

# 3. Histogram
A histogram is basically used to represent data provided in a form of some groups. It is a type of bar plot where the X-axis represents the bin ranges while the Y-axis gives information about frequency. The hist() function is used to compute and create histogram of x.

Syntax:

matplotlib.pyplot.hist(x, bins=None, range=None, density=False, weights=None, cumulative=False, bottom=None, histtype=’bar’, align=’mid’, orientation=’vertical’, rwidth=None, log=False, color=None, label=None, stacked=False, \*, data=None, \*\*kwargs)



# OUTPUT
1. Line chart
     ![Screenshot 2025-01-11 134253](https://github.com/user-attachments/assets/9fab1b34-9dc6-4e36-ba02-7931b5992690)
2. Bar chart
     ![Screenshot 2025-01-11 134308](https://github.com/user-attachments/assets/19c5da1b-fc01-468c-a919-572c7c7a72ba)
3. Histogram
     ![Screenshot 2025-01-11 134337](https://github.com/user-attachments/assets/a8734e47-7902-415b-8791-7e98fd45949f)





# A script and visualization dashboard
The above functions are commonly used. In this example, We can create three types of charts named Line Chart, Bar Chart, and Bubble Chart. Here, we have four conditions as well ‘Formerly_Smoked’, ‘Smoked’, ‘Never_Smoked’, and ‘Unknown’. With the help of this example, We can create any chart diagram for any conditions means a total of 12 chart diagrams. 

Step 1: First, We are going to set a title and some description for the main dashboard window using the above functions:


st.title(“Stroke Prediction Dashboard”)


st.markdown(“The dashboard will help a researcher to get to know more about the given datasets and it’s output”)


Step 2: Now, Let’s create a sidebar with a simple title and description.


st.sidebar.title(“Select Visual Charts”)


st.sidebar.markdown(“Select the Charts/Plots accordingly:”)


Step 3: Using pandas Library, we need to read our .csv file for creating a data frame. You can use this dataset for demonstration.

data = pd.read_csv("<Path_for_.csv_file>")
Step 4: Streamlit also provides us some functions through which we can easily create a select box within a single line of code. In our program, we are giving two arguments first as title or Captions and second for select box options in form of a tuple.


chart_visual = st.sidebar.selectbox(‘Select Charts/Plot type’, (‘Line Chart’, ‘Bar Chart’, ‘Bubble Chart’))


Step 5: As similar to the select box, we have another method for creating a checkbox.

st.sidebar.checkbox("Show Analysis by Smoking Status", True, key=1)
Step 6: Using selectbox() function, we are going to create a selectbox with four options. 


selected_status = st.sidebar.selectbox(‘Select Smoking Status’, options=[‘Formerly_Smoked’, ‘Smoked’, ‘Never_Smoked’, ‘Unknown’])


Step 7: When we select one option from the first selection box that value gets stored into the chart_visual variable. This variable value represents the chart type. Through the second selection box, that value gets stored into the selected_status variable. Using this value, we will create the main graph. Using the simple if_else condition, we will make conditions for drawing the graphs.

Step 8: Using the add_trace() method, New traces will be added to a graph object figure. This method will take a graph object trace (an instance of go.Bar, go.Scatter etc.) as an argument and adds it to the figure. 

Step 9: Using go.Scatter(), go.Bar() method, We will create informative graphs through which a researcher can easily understand the output of the datasets. First, go.Scatter() takes four arguments in our program, first as x_axis value, second as y-axis value, third as a mode of the figure, and fourth as the name of the newly created graph.

fig.add_trace(go.Scatter(x=data.Country, y=data.formerly_smoked,
                                 mode='lines',
                                 name='Formerly_Smoked'))
Step 10: Second, go.Bar() method takes three arguments in our program, first as x_axis value, second as y-axis value, and third as the name of the newly created graph.

fig.add_trace(go.Bar(x=data.Country, y=data.Unknown,
                             name="Unknown"))
![Screenshot 2025-01-11 141038](https://github.com/user-attachments/assets/a2a8777e-0e5a-4b16-821f-4ce14a4e87cb)
![Screenshot 2025-01-11 141049](https://github.com/user-attachments/assets/4aec4ba8-be3c-4938-b735-9afead03c72e)
