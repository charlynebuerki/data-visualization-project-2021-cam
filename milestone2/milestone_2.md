# Project of Data Visualization (COM-480)

| Student's name | SCIPER |
| -------------- | ------ |
| Charlyne Bürki | 261415 |
| Arnaud Dhaene  | 269883 |
| Marijn van der Meer | 247273 |

[Milestone 1](#milestone-1) • [Milestone 2](#milestone-2) • [Milestone 3](#milestone-3)

## Milestone 2 (7th May, 5pm)
**10% of the final grade**

### Introduction:
The goal of our project is to provide a platform for both Airbnb users and Airbnb listing owners (also known as hosts) in Switzerland. Since the tourism industry has been hit hard due to COVID-19 restrictions, our approach is twofold. In order to stimulate local tourism in Switzerland from this summer on, we aim to inform the Airbnb community about local Airbnb possibilities and give them more insight into different features. On the other hand, to allow listing owners to provide the best possible amenities to tourist and re-stimulate the private hospitality industry, we will show regional statistics and inputs about customer preferences. 

The entirety of our website will be accessible to both types of users. However, there will be two explicitly-labeled sections separate for users and owners. 

### Sketches and tools needed:
Before the interactive visualisations,  our site will exhibit general statistics pertaining to the three regions (Vaud, Geneva and Zurich) and Airbnb information. Because the goal is to stimulate Swiss tourism, the subsequent section will contain the de-confinement timeline outlined by the Federal Council's proposal (unfortunately, it’s not available in english). 

After that, we will have two buttons leading to the “insights for users” or “insights for hosts”.  Our main framework will contain 3 principle visualisation: 

### Visualisation 1: global insights about regional possibilities
![Map of listings](figures/fig1.png)

### Visualisation 2: 
![Map of listings](figures/fig2.png)

### Visualisation 3: further insights for owners 
![Map of listings](figures/fig3.png)
First, the user will be able to select from the menu which region to select. The data is presented in a way that separates the types of Airbnb listings into two categories: renting a room or renting a full place (house or apartment). These categories are further divided into subcategories based on price ranges. For each subcategory, we will show which amenities are available for that price range by grouping edges and showcasing which is more likely with regards to the edge width. This will allow Airbnb owners to identify which common amenities are found for their listing’s price range and what they should add to better respond to the client’s demands. 

tools needed:
items from the lecture on graphs (lecture 10), especially on edge groupings
the reference on Sankey flow diagrams, as visualised here.(https://www.d3-graph-gallery.com/sankey.html)  

We wish to finish the website with a testimonials section where some of our friends will leave comments on employing our website. 

### Visualisation 4: 
![Map of listings](figures/fig4.png)

## To go further: 
Some other ideas that we may include should we see that the visualisations are insufficient in providing ample information to the users and owners include :
* The introductory visualisation of the Airbnb activity as a scatterplot of listings. This visualisation would trace the Airbnb activity  of reviews in the three regions, distinguished by three colors. The user would be able to select a time point throughout the history, and be able to visualize the number of existing listings that were reviewed, indicating the Airbnb activity. Though not very quantitative, this visualisation could be an interesting qualitative visualisation that would draw attention and entice users to dig in deeper into the website. The inspiration comes from Europe’s Coronavirus Lockdown Nightmare introductory visualisation. 
* A complementary visualisation would be a bubble plot, plotting listing price vs the number of reviews obtained. For each listing, its “bubble” size would be proportional to the average score listed on Airbnb. This way, owners could observe whether a more expensive listing correlates to more reviews and whether this indicates a better rating. 

## Functional website:

The website skeleton is available [here](https://arnauddhaene.github.io/airbnb-visualized/). 
