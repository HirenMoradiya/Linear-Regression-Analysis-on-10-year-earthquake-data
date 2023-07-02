# Linear-Regression-Analysis-on-10-year-earthquake-data
Working with real-time earthquake data, our objective is to perform a linear regression on the desired real-time earthquake data. Most countries have their own earthquake databases. We make use of the "GeoForschungsZentrum (GFZ)" earthquake database. The data was represented using several visualizations provided by the Matplotlib packages.

- In this assignment, you define a new Class to characterize the earthquakes nearby one epicenter.
Your object instances contain the properties of earthquakes. The properties are taken from real-time
data of earthquakes. You prepare these data as training data to be used by an artificial neural network,
visualize them and perform linear regression on the data.

- “The number of earthquakes with small magnitudes is higher compared to the number of earthquakes
with large magnitudes”.
This is a qualifying expression that we can all agree on even without any seismological knowledge. In
order to quantify the seismicity, the Gutenberg-Richter recurrence relationship is defined as follows and
can be used for any region and time interval where an earthquake occurs:
log 𝑁 = 𝑎 − 𝑏 𝑀
In which M is the value of magnitude, and N is the cumulative number of earthquakes with a magnitude
higher-or-equal than M. Two constants, a and b, should be derived from regression analysis and they are
individual for each earthquake.
You derive a and b by performing a linear regression on your desired real-time data of earthquakes.

- To-Do tasks:

1. The first step is to download the real-time data from the proper platform. Most of the countries have
their own earthquake catalogs. We use the earthquake catalog of Germany provided by
‘GeoForschungsZentrum (GFZ)’.
If you open the webpage of GEOFON – GFZ, you can search in the earthquake catalog and get your
desired data. It is required to customize the following filters:
Search Criteria: Select any interval you like, with a minimum magnitude of 2.5. It is not
necessary to insert the specific latitude and longitude ranges. Leave it empty. Your search will be on
data of the whole world.
Output Format: Select HTML. The default of 40 for the number of events that have your criteria is
enough but you are free to increase it to have access to more events.

- 2. After clicking on search, you see a list of earthquakes with your criteria. Select one of them as you
like. You will see a part of the map where the epicenter of this earthquake is shown by red circles. On
the bottom of this image, go to Nearby Events and select Text(CSV). You are finished with getting
your first data set related to all occurred earthquakes near the selected epicenter. Download the data.
Repeat the process and download two more data sets. Totally, you need to have three different data
sets.
Now, it is time to read downloaded data sets in your Jupyter notebook, explore them, prepare them as
training data, and derive a and b constants for each! These operations have to be done through Class
definition.

- 3. Firstly, define one Class for a new data type that characterizes the available earthquakes in each
data set.
Based on the following tasks, select the attributes and methods of your instance objects. Totally, you
should generate three instance objects from your Class. Each instance should represent one of the
downloaded data sets.
You can use inheritance at least once in your code. It is up to you which attribute or method to be added or
changed in the inherited Class.

- 4. The first row of each data set looks like as following. Find the missing values in your downloaded
data and visualize the missing values.

#EventID|Time|Latitude|Longitude|Depth/km|Author|Catalog|Contributor|ContributorID|MagType|Magnitude|MagAuthor|EventLocat
ionName|EventType

- 5. The contents of different columns of your downloaded data have different types, like floats and
strings.
You want to prepare these data as training data for an artificial neural network (ANN). You should
convert categoric data to numeric data.
Classify the numeric data also in different intervals. Pay attention to the range of numeric data when
you want to define different intervals. This means, for example, based on the maximum and minimum
values, the incrementation of the intervals needs to be different.
After preparing the data as training data of an ANN, save the new equivalent data in your desired data
structure (DataFrame or Array). Consider the first ten lines of the data set, and print the associated data
lines with original values in columns and the modified columns.

- 6. Use your originally downloaded data and generate a three-dimensional scatter plot using the
geographical properties for axes: longitude, latitude, and depth
• Report the unit of the properties selected for the axes.
• Show the occurrence of earthquakes at the correct location.
• The magnitude value and magnitude type of each earthquake should be shown on the curve. Use a
visualization method that better describes these data on your map. (There is no correct or wrong
solution for it!)
• Include a legend for the plot. The plot and its elements should be understandable.

- 7. Extract the values of the ‘MagType’ and ‘Magnitude’ columns. The magnitude of earthquakes can be
reported in different types. Therefore, you see different notations in the ‘MagType’ column. For example,
ML is used for Richter.
• Find the notation with maximum repetition in your data. Report it.
• Find the corresponding ‘Magnitude’ values to this type and highlight them (in any way that could be
understandable) on the generated plot in step 6.

- 8. Calculate N as the cumulative number of earthquakes with a magnitude higher-or-equal to M.
For example, if the magnitude values are M1 = 2.5, M2 = 3, M3 = 4, M4 = 7
The associated cumulative number of earthquake would be N1 = 4, N2 = 3, N3 = 2, N4 = 1

- 9. Plot a new figure containing the data points of (M, log(N)). Put labels for your axes.

- 10. Perform a linear regression analysis by using the available function in the SciPy library to fit a line
to your data.

- 11. Show the fitted line on the plot of task no.9.
• Include a legend for scattered data and fitted lines.
• On the plot, show the equation of the fitted line with the derived values of a and b, representing the
Gutenberg-Richter relationship:
log 𝑁 = 𝑎 − 𝑏 𝑀

- 12. The tasks should be performed for all three downloaded data sets by generating three instance
objects from the defined Class(es).
