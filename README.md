# python-api-challenge
Python API

All the comments for each diagram/scatter plot have been showed within the code and popped up at the bottom of each diagram.
Please put your keys for Weather API and google key for GMAPS.

Background
Data's true power is its ability to definitively answer questions. So, let's take what you've learned about Python requests, APIs, and JSON traversals to answer a fundamental question: "What is the weather like as we approach the equator?"

Now, we know what you may be thinking: “That’s obvious. It gets hotter.” But, if pressed for more information, how would you prove that?

Before You Begin
Create a new repository for this assignment called python-api-challenge. Do not add this assignment to an existing repository.

Clone the new repository to your computer.

Inside your local Git repository, create a directory for this assignment. Use a folder name that corresponds to the Challenges, such as WeatherPy.

Inside the folder you just created, add new files called WeatherPy.ipynb and VacationPy.ipynb. These will be the main scripts to run for each analysis.

Push your changes to GitHub.

Add a .gitignore File
For this assignment, you will need to add a .gitignore file to your repo. This is so you don’texpose the api_keys.py file with your API key to the public, which would allow anyone using GitHub to copy and use your API key, possibly incurring charges.

When you type git status in the command line, you’ll get a list of all the untracked files that you have created so far.

If you wanted to add only the WeatherPy.ipynb file to GitHub, you would type git add WeatherPy.ipynb. However, whenever you want to add or update a file, you would have to add each file individually, which is time-consuming and cumbersome. Instead, you can add the files that you don't want to track to the .gitignore file.

Before adding your files to GitHub, add api_keys.py to the .gitignore file by following these steps:

Open your python-api-challenge GitHub folder in VS Code.

Open the .gitignore file, and on the first line, type the following code:

# Adding config.py file.
api_keys.py
While the .gitignore file is open, add the API_practice.ipynb and random_numbers.ipynb files and save the file.

In the command line, type git status and press Enter. The output should indicate that the .gitignore file has been modified and the WeatherPy.ipynb file is untracked.

Use git add, git commit, and git push to commit the modifications to .gitignore and the WeatherPy.ipynb file to GitHub.

On GitHub, the only new file you should find is the WeatherPy.ipynb file.

Files
Download the following files to help you get started:

Module 6 Challenge files

Instructions
This activity is broken down into two parts, WeatherPy and VacationPy.

Part 1: WeatherPy
In this section, you'll create a Python script to visualise the weather of over 500 cities of varying distances from the equator. You'll use a simple Python library (Links to an external site.), the OpenWeatherMap API (Links to an external site.), and your problem-solving skills to create a representative model of weather across cities.

The first requirement is to create a series of scatter plots to showcase the following relationships:

Temperature (C) vs. Latitude

Humidity (%) vs. Latitude

Cloudiness (%) vs. Latitude

Wind Speed (m/s) vs. Latitude

After each plot, add one to two sentences to explain what the code is analysing.

The second requirement is to compute the linear regression for each relationship. This time, separate the plots into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude):

Northern Hemisphere: Temperature (C) vs. Latitude

Southern Hemisphere: Temperature (C) vs. Latitude

Northern Hemisphere: Humidity (%) vs. Latitude

Southern Hemisphere: Humidity (%) vs. Latitude

Northern Hemisphere: Cloudiness (%) vs. Latitude

Southern Hemisphere: Cloudiness (%) vs. Latitude

Northern Hemisphere: Wind Speed (m/s) vs. Latitude

Southern Hemisphere: Wind Speed (m/s) vs. Latitude

After each pair of plots, explain what the linear regression is modelling. Describe any relationships that you notice and any other findings you may uncover.

Your final notebook must meet the following requirements:

Randomly select at least 500 unique (not repeated) cities based on latitude and longitude.

Perform a weather check on each of the cities by using a series of successive API calls.

Include a print log of each city as it's being processed, with the city number and city name.

Save a CSV of all retrieved data and a PNG image for each scatter plot.

Part 2: VacationPy
Now, use your weather data skills to plan future vacations. Use Jupyter gmaps and the Google Places API for this part of the assignment.

NOTE
Remember that any API usage beyond the $200 credit will be charged to your personal account. You can set quotas and limits to your daily requests to be sure that you won’t be charged. Check out Google Maps Platform Billing (Links to an external site.) and Manage your cost of use (Links to an external site.) for more information.

Hint: If you are having trouble displaying the maps, run jupyter nbextension enable --py gmaps in your environment and then try again.
To complete this part of the assignment, complete the following steps:

Create a heat map that displays the humidity for every city from Part 1, as in the following image:
heatmap

Narrow down the DataFrame to find your ideal weather condition. For example:
A max temperature lower than 27 degrees but higher than 21

Wind speed less than 4.5 m/s

Zero cloudiness

Drop any rows that don't satisfy all three conditions. You want to be sure that the weather is ideal.
NOTE
Feel free to adjust your specifications, but make sure to set a reasonable limit to the number of rows returned by your API requests.

For each city, use the Google Places API to find the first hotel located within 5,000 metres of your coordinates.

Plot the hotels on top of the humidity heatmap, with each pin containing the Hotel Name, City, and Country, as in the following image:

hotel map

Finally, make sure to meet the following requirements:

You must complete your analysis using a Jupyter notebook.

You must use the Matplotlib or Pandas plotting libraries.

For Part 1, you must include a written description of three observable trends based on the data.

For Part 2, you must take a screenshot of the heatmap that you create and include it in your submission.

Your plots must include labelling aspects like plot title (with date of analysis) and axis labels.

For max intensity in the heatmap, try setting it to the highest humidity found in the dataset.

Hints and Considerations
The city data that you generate is based on random coordinates and different query times, so your outputs will not be an exact match to the provided starter notebook.

If you'd like a refresher on the geographic coordinate system, this site (Links to an external site.) has great information.

Take some time to study the OpenWeatherMap API. Based on your initial study, you should be able to answer basic questions about the API: Where do you request the API key? Which Weather API in particular will you need? What URL endpoints does it expect? What JSON structure does it respond with? Before you write a line of code, you should have a crystal-clear understanding of your intended outcome.

A starter code for citipy has been provided. However, if you're craving an extra challenge, push yourself to learn how it works by using the citipy Python library (Links to an external site.). Before you try to incorporate the library in your analysis, start with simple test cases outside of your main script to confirm that you are using it correctly. Often, when introduced to a new library, learners spend hours trying to figure out errors in their code when a simple test case can save you a lot of time and frustration.

You will need to apply your critical thinking skills to understand how and why we're recommending these tools. What is citipy used for? Why would you use it in conjunction with the OpenWeatherMap API? How would you do so?

While building your script, pay attention to the cities you are using in your query pool. Are you covering the full range of latitudes and longitudes? Or are you choosing 500 cities from one region of the world? Even if you were a geography genius, simply listing 500 cities based on your personal selection would create a biased dataset. Try to think of ways that you can counter these selection issues.

Hint: Consider the full range of latitudes.
Once you have computed the linear regression for one relationship, you will follow a similar process for all other charts. As a bonus, try to create a function that will create these charts based on different parameters.

Remember that each coordinate will trigger a separate call to the Google API. If you're creating your own criteria to plan your vacation, try to reduce the results in your DataFrame to 10 or fewer cities.

Ensure that your repository has regular commits and a thorough README.md file.

Lastly, remember that this is a challenging assignment. Push yourself! If you complete this task, you can safely say that you've gained a strong understanding of the core foundations of data analytics, and it will only get better from here. Good luck!
