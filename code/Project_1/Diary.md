#Diary for "Happy people"

## Content
The European Social Survey has asked more than 40'000 Europeans how happy they feel. First, I aggregated the data to compare "very happy" to "not very happy" people. I compare them by different categories (e.g. income, age, partner).

Then I wanted to do some interactive chart on a website. But I thought the individual data would be too big. So I used five categories (age, income, religiousness, health, number of friends) to group the data and run averages on each permutation of these categories. I exported this aggregated data (more than 2000 lines) to a CSV and imported it by D3.

On the website, people can enter their personal situation and see how the distribution of happiness changes according to the data they enter.

##I've learnt a lot about D3:
- graphics are drawn in a canvas. Text, scales and all charts are drawn on a specific canvas
- CSV files are loaded asynchronous. That means you need do your visualization for CSV data in the CSV loading function – or do some complicated function to wait for the loading.
- I still don't know how to do dynamic loading of new data (maybe with JSON?)
- the rotation of Text has to "translated" to the current coordinates
- I could only load the CSV file in D3 when running a local web server

##I've used JavaScript:
- I used a library for image sliders (TwentyTwenty)
- I copied code for tabs
- I copied code for 
- I don't know yet why my functions for drop-down buttons don't work in the external javascript file (i.e. need to be in the main file).

##I've exported files to Illustrator:
- the Pandas exports in eps format are sometimes different even if the png export would be exactly the same format