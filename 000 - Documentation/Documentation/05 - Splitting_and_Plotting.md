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
- Then the same chart of the previous notebook is stretched by using an **occurence of a new author as an event** instead of the years. ![[Pasted image 20211129155922.png]]
	- - located at  `myDATA/10-splitted_by_year//<HOLE_SIZE>_hole_size_splitted/trajectories_plt_by_events`


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