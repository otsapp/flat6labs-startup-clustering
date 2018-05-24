# Industry footprint of Flat6Labs 
author: Oliver Tsappis, otsappis@googlemail.com
[HTML friendly version which doesn't include interactive bokeh and 3D plotly charts.]

## Brief overview
* Flat6Labs is a startup accelerator operating across the MENA region.
* Every startup invested in by the Flat6Labs fund impacts industries, people and markets around the world. 
* How can they measure these things to improve their business and help the startups in their portfolio?
* This project creates a visual map of startups, clustered by their industries to provide insights to support their business.
* This is simply an exploratory project, which raises more questions than it answers, so needs to be optimised and developed further to make useful conclusions.
###### Insights
* We find that Flat6Labs startups can be generalised e-commerce, tech and creative industries.
* Several startups operate in the white space between industries, which means their business models join industries in a relatively unique way and could mean a particularly innovate or disruptive idea. For example, Reform Studio operates somewhere between technology and creative industries using a socially responsible business model to disrupt the way we think about design and sourcing our home furniture.
* There is white space between creative industries and the rest, which could be exploited further by Flat6Labs investment strategy, or it could show trends in entrepreneurship in the region.

## Project files
* This project is presented in 2 different jupyter notebook files:
	* ind_footprint_interactive.ipynb: shows the project including interactive visualisations and focuses on story telling.
	* ind_footprint_dev.ipynb: shows the extra development stages used to get the results of ind_footprint_interactive.ipynb, use this one to follow in more detail how the insights were drawn.
* requirements.txt is a list of all packages used to write both notebooks.
* data/industry_complete.csv contains the raw csv containing the industry tags.

## Instructions
* Please open ind_footprint_interactive.ipynb using the nbviewer in a separate window (there’s a link in the top right of the notebook once open within github)
* ind_footprint_dev.ipynb was written using html friendly visualisations, so feel free to view within github.

## Background
###### What is Flat6Labs?
Flat6Labs is a leading startup accelerator operating in the MENA region, founded by Sawari Ventures in Cairo. Their aim is to push innovation in the Middle East & North Africa by supporting early stage startups and entrepreneurs with 3 tools:
1. Angel investment.
1. Acceleration program: If selected, local entrepreneurs are trained and connected to a network of experts and investors to improve performance of their startups.
1. Follow-on investment program. 
Their main objectives: 
* To give local entrepreneurs a platform to bring innovation to local and global markets for the greater good of MENA economies and people.
* Improve value of their angel & follow-on investment portfolios.

 
To create the largest impact and return possible, Flat6Labs must optimise their startup selection procedure and acceleration program. To do this effectively, they must understand the complex world in which they operate: industries, people, markets etc. This is especially important information for the selection committee and program managers. These people need to know the future potential of applicants and in what way to help startups already in the acceleration program. Being able to model, visualise and communicate these things would allow Flat6Labs to understand the entrepreneurial environment better and find opportunities to optimise their business:
* What types of problems are regional entrepreneurs trying to solve?
* What types of businesses are investors most excited about?
* What strengths, patterns or gaps are there in the investment strategy of Flat6Labs?
* Where can technology and recent innovation can be applied elsewhere, especially tech developed inside the Flat6Labs portfolio?
* What business models are having the largest impact in terms of investment, revenue, employment etc.?

One company that is already modelling this kind of data and is answering these types of questions for their clients is Quid, who've partly inspired this project. You can read more on how they do it here (non-technical): https://goo.gl/YeD1EH

The scope of this kind of research can be huge, but we will start by looking at industries the startups are currently operating in and dive a bit deeper from there.

## Objective
* To visualise the map of Flat6Labs' investment portfolio of startups in terms of their industries.
* Imply some answers to the questions: 
1. What types of problems are regional entrepreneurs trying to solve?
1. What patterns or gaps are there in the investment strategy of Flat6Labs?
1. Are there any potential market gaps the selection team should investigate?

## Data
* data/industry_complete.csv: a list of Flat6Labs startups, each tagged with their industries.
* The tags were authored by myself based on independent research. 
* Not all the startups are still currently operating, so the list shows the ideas that Flat6Labs have directly invested in
* Columns: 
	* name: names of the startups invested in by Flat6Labs since end 2017,
	* industry: tags that represent industries
* Each startup can have multiple entries.

## Approach
* Principle component analysis (PCA) will be used to generate coordinates to visualise the startups on a map, positioned according to their individual combination of industries. 
* K-means will be used to cluster the startups, pulling f
* We have the following industry footprints:
1. Level 1: This first footprint will show all Flat6Labs startups in 3 main clusters as an intro.
1. Level 2: The second footprint will break-down these 3 clusters into 8 clusters to give more detail.
    
## Model limitations
* It doesn't pick out some key industries very well, for example there are a few startups in film, but they get swallowed up into 'creative' and 'e-commerce' clusters.
* There are a few startups that are allocated to some clusters that don't follow the same logic as the majority.

## Future steps
* Modelling the clusters in 3d to show relationships between startups, most likely using plotly.
* Optimise the level 2 footprint using trial and error with multiple k-means arrangements.
* It would be interesting to use a network graph approach on top of the clustering algorithm, showing direct links between startups, perhaps defining the edges with a different set of data.
* Improve presentational elements eg. adjusting marker sizes to show number of employees or level of investment.

