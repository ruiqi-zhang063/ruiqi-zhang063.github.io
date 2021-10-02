Title: Homework 3 Explanation
Date: 10/01/2021   
Author: Ruiqi Zhang  
Slug: Homework 3
Category: Homework 3

# Homework 3 - Creating effective visualizations using best practices

#### Library: Altair

The reason I choose "Altair" is that this library is convenient. I want to achieve several interactive behaviors including multi-Line Tooltip, interactive average and interactive legend, and of these interactions can be implemented in "altair".

#### The first visualization

The first visualization is used to compare different counties malaria deaths or malaria incidence. The first parameter is a list of country name, representing the countries we want to compare. The second parameter is a string, inputing 'Deaths' means that we want to compare malaria deaths, while inpunting 'Incidence' means that we want to compare incidence.

The visualization has interactive behavior tied to the x position of the cursor. When the cursor is moved over, the most recent value will be displayed.

#### The second visualization

The second visualization is used to obtain the n countries with the highest number of deaths or infection rates in a given year. The first parameter is an int input, representing the year we are interested. The second parameter is an int input, meaning the number of countries we want to see. The third parameter is a string, inputing 'Deaths' means that we want to compare malaria deaths, while inpunting 'Incidence' means that we want to compare incidence.

The visualization uses an interval selection, which causes the chart to include an interactive brush (shown in grey). The brush selection parameterizes the red guideline, which visualizes the average value within the selected interval.

### The third visualization

The third visualization is used to obtain the specified country age group distribution about malaria deaths. The only parameter is a string, representing the country we are interested in.

The visualization has interactive legend. We can choose one category of the legend to see specific age group area.

