# Movies-ETL.
Overview:
 
 The purpose of this challenge was to create an automated ETL process for the classwork we did earlier. The script takes in data from Wikipedia and Kaggle. It then gets cleaned to a format that we have specified. It merges the data as well once cleaned. Once this is done, it is uploaded to a SQL database for future use 
 
 The challenge wanted us to have this process automated. This meant that we had to make several assumptions and use the try/except code for things to run properly. I looked at what the most probable mistakes would be, and gave the user an opportunity to fix them.
 
 Assumptions: 
 1) the path definition to wiki_movies_raw file is correct. If not, the user gets an error print out to tell them to change it.
 2) the path definition to kaggle_metadata file is correct. If not, the user gets an error print out to tell them to change it.
 3) the path definition to ratings file is correct. If not, the user gets an error print out to tell them to change it.
 4) The user needs to create a database called "movie_data" in pgAdmin to be able to have the script to run properly. If this is not done, then the user gets an error warning that tells them to fix this.
 5) The movies table needs to be cleared before the script is run for it to be able to upload into it. If this is not done, the user gets an error saying that they need to clear it
 6) I assumed that the Wikipedia and Kaggle information is accurate. Wikipedia is peer reviewed constantly, but could potentially have incorrect data. We used out best efforts to see which one would provide the cleanest data.
 7) The wiki and kaggle metadata will be in small enough files that they won't require batches, like the ratings data. If they do become to large, we will have to transfer them like the ratings data.
 8) We assume that the formats will not change going forward in the files.
 9) we can assume that all the data is matching up correctly from each of the files. for example: kaggle id and ratings id
 10) we also assume that any monetary number list, budget etc, has not been adjusted for inflation. This means that we are not judging apples to apples if we want to compare movies with those circumstances.



