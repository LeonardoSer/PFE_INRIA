## 00 - build_collaboration_df.ipynb

Retrived the dataset containing the **cumulative numer of collaboration** for computer scienze authors in French between **1990 and 2018**.

![[Pasted image 20211129140001.png]]

The relative csv is located at `myDATA/00-collaboration_df.csv`.

## 02 - build_publication_df.ipynb
Retrived the dataset containing the **numer of publications** for computer scienze authors in French between **1990 and 2018**.

![[Pasted image 20211129140011.png]]

The relative csv is located at `02-publication_df.csv`

## 05 - filtering_active_authors.ipynb

In the associated notebook are filtered out all inactive authors, so a dataset is built for each possible definition of **Inactivity**.  

An author is inactive if it has a hole in publications **greater** than a given value.
An author has a  hole in publication if he haven't published for **n consecutive years**. 
For example, given an **hole size = 3**, the author A1 is active but A2 is not.

![[Pasted image 20211129142426.png]]

The number of authors kept for each hole size is showed in the following chart, and also their differences in the number of authors:

![[Pasted image 20211129142954.png]]
![[Pasted image 20211206154905.png]]

The** output of the code are 28 csv ** located in the directory `/myata/05-filtered_by_hole_size/`

The distribution of new collaborators and new publicators for each year and hole size is located at `myDATA/05-filtered_by_hole_size`, it's shape is like:

![[Pasted image 20211130115415.png]]

## 08 - starting_pubblication_year.ipynb / 09 - ending_pubblication_year.ipynb

There are built two version of the **collabaration dataset** containing respectively a column with the **starting publication year** and the **ending publication year** for each author.

### starting year
Located at -> `myDATA/00-collaboration_df_with_starting_years.csv`.

![[Pasted image 20211129143829.png]]

#### distribution of the number of authors by starting year
![[Pasted image 20211129143843.png]]

## ending year
Located at ->  `myDATA/00-collaboration_df_with_ending_years.csv`.

![[Pasted image 20211129144053.png]]

####  distribution of the number of  authors by ending year

![[Pasted image 20211129144105.png]]

## 10 - splitting_collaborations.ipynb

Each hole lenght based dataset is **splitted in 28 subsets based on the starting year** of each author. 

- They are located at `myDATA/10-splitted_by_year/`

- Each hole size based dataset has an associate directory at `myDATA/10-splitted_by_year/<HOLE_SIZE>_hole_size_splitted/`

- The set of datasets associated with an hole size has a distribution chart showing the number of authors for each starting year, and it's located at `myDATA/10-splitted_by_year/<HOLE_SIZE>_hole_size_splitted/distribution_chart.png`. 
It's shape is the following:
	![[Pasted image 20211129145131.png]]
	
## 15 - plotting_splitted_data_by_year.ipynb

A chart containing the number of collaborations by year for each dataset built in the above described notebook is plotted here. Each one contains only the top 100 collaborative authors.

Each of them is located in the directory `myDATA/10-splitted_by_year/<HOLE_SIZE>_hole_size_splitted/trajectories_plt/` and they looks as follow:

![[Pasted image 20211129155946.png]]

## 16 - plotting_splitted_data_by_event.ipynb

- Firstly the same chart of the previous notebook is stretched by using an **occurence of a new author as an event** instead of the years.![[Pasted image 20211129155815.png]]

	- located at  `myDATA/10-splitted_by_year//<HOLE_SIZE>_hole_size_splitted/trajectories_plt_by_events`
- Then the same chart of the previous notebook is stretched by using an **occurence of a new collaboration as an event** instead of the years. ![[Pasted image 20211206164829.png]]
	- located at  `myDATA/10-splitted_by_year//<HOLE_SIZE>_hole_size_splitted/trajectories_plt_by_events`


## 20 - plotting_avg.ipynb

Same as the previous notebbok but, instead of the top 100 collaborative authors, here is plotted the average number of publications for each year.

Each of them is located int the directory  `trajectories_avg_plt` and look as follow:

![[Pasted image 20211129145843.png]]


## 21 - plotting_avg_by_event.ipynb

- Firstly are plotted the same averages of the previous notebook but all years associated with the same hole size, are collected in the same chart: ![[Pasted image 20211129150142.png]] 
	
	- They are located at `myDATA/10-splitted_by_year/<HOLE_SIZE>_hole_size_splitted/trajectories_avg_plt/averages_by_year.png`

### new author as event
- Then the same chart is stretched by using an **occurence of a new author as an event** instead of the years.	![[Pasted image 20211129150523.png]]
	
	- They are located at `myDATA/10-splitted_by_year/<HOLE_SIZE>_hole_size_splitted/trajectories_avg_plt/averages_by_num_authors.png`

### new collaboration as event
- lastly the same chart is stretched by using an **occurence of a new collaboration as an event** instead of the years.	![[Pasted image 20211129150611.png]]

	- They are located at `myDATA/10-splitted_by_year/<HOLE_SIZE>_hole_size_splitted/trajectories_avg_plt/averages_by_num_collaborations.png`

## 25 - plotting_functions._of_pubblications_df.ipynb
 Here are plotted:
 - The **number of new authors ** by year in the publication dataset ![[Pasted image 20211129151115.png]]
 - The **number of new publications** by year in the publication dataset ![[Pasted image 20211129151147.png]]
- The **number of new collaborations** by year in the collaboration dataset ![[Pasted image 20211206165358.png]]
## 35 - Ratios.ipynb
Here, both by year and using the occurence of a new collaboration as event, are plotted:
- The **Ratio** between the number of **new collaboration** and **new authors**.![[Pasted image 20211129151514.png]]
	- located at `myDATA/ratio_beetween_#_newCollaborations_and_#_newAuthors_by_newCollaborations.png` and `myDATA/ratio_beetween_#_newCollaborations_and_#_newAuthors_by_year.png`

- The **Ratio** between **total** number of **collaboration** and **authors**.![[Pasted image 20211129151404.png]]
	- located at `myDATA/ratio_beetween_#_collaborations_and_#_authors_by_newCollaborations.png` and `myDATA/ratio_beetween_#_collaborations_and_#authors_by_year.png`

## 40-fitting_avg_trajectories_by_starting_y
Tried to fit average trajectories stretched by new authors and new collaborations.

### stretched by new authors
![[Pasted image 20211206120207.png]]
### stretched by new collaboration
![[Pasted image 20211206120156.png]]

## 45-degree_distribution.ipynb
Plotted the degree distribution and it's log-log form both for the whole collaboration dataset and for each subset defined by the hole size

All results are located at `myDATA/40-degree_distribution/`

### whole data
![[Pasted image 20211206120415.png]]
### for hole size
![[Pasted image 20211206120458.png]]

## 46-fitting_degree_distribution.ipynb
Tried to fit the **whole degree distribution** with **powerlaw** lib 
![[Pasted image 20211206165926.png]]