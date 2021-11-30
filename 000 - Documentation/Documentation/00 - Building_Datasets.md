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

The number of authors kept for each hole size is showed in the following chart:

![[Pasted image 20211129142954.png]]

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