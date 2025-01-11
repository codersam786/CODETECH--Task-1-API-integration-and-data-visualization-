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

# OUTPUT
1. Line chart
     ![Screenshot 2025-01-11 134253](https://github.com/user-attachments/assets/9fab1b34-9dc6-4e36-ba02-7931b5992690)
2. Bar chart
     ![Screenshot 2025-01-11 134308](https://github.com/user-attachments/assets/19c5da1b-fc01-468c-a919-572c7c7a72ba)
3. Histogram
     ![Screenshot 2025-01-11 134337](https://github.com/user-attachments/assets/a8734e47-7902-415b-8791-7e98fd45949f)







