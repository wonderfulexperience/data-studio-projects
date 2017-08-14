## Diary for the project "Swiss pension funds"

#2017-07-25

Entered the project pitch. Not clear how much I can do with the available data. Unfortunate that the Swiss statistics office doesn't offer individual data on pension funds, only aggregated. Contacted a Swiss asset management company to give more detailed information.

#2017-07-26

No reply from the asset management company. Using PDF data for costs and returns of pension funds for the last five years from a pension consultant company. Using Tableau to save files from PDF. Using Pandas to combine the data.

#2017-07-27
I worked on creating new visuals. I did some regression lines to show simple relationships between values.
The formula is as follows:
x_fit = np.arange(0,50) #creating just some values for x
y_fit = fit[1] + fit[0]*x_fit
ax.plot(x_fit, y_fit, color="violet", linewidth = 1, label = "Trend line")

I also did some charts where I filled the area of the graph.

This fills the values right of a line and below a line:
ax.fill_between([index_alloc,max(x_fit)], [index_return,index_return], alpha=0.2, color = "red")

This fills the values left of a line and above a line:
plt.axhspan(index_return, 7, 0, 0.335, facecolor='green', alpha=0.2)

Important hier is that "0.335" means 33.5% of the height of the chart

This fills the value of a diagonal throught the chart:
ax.fill_between([0,2], [0,2], [2,3], alpha=0.2, color = "red")

I also learned how to set the background color of a legend:
legend = ax.legend(frameon = 1)
frame = legend.get_frame()
frame.set_facecolor('white')

#2017-07-28
I plotted the differences of points to a diagonal line (red for plots above the line, green for dots below the line):

ax.plot([lower_costs_x,lower_costs_x],[lower_costs_x,lower_costs_y], color="green", linewidth = 0.4)
ax.plot([higher_costs_x,higher_costs_x],[higher_costs_x,higher_costs_y], color="red", linewidth = 0.4)

where (x,x) is the diagonal line, while (x,y) is the new point.

#2017-08-08
I used www.gifmaker.com to do an animation out of my png files.
I used multiple charts to make slides show longer on the animation.