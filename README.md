# Election-Analysis

## Project Overview

The purpose of this project is to analyse the election results of an election that took place in Colorado, USA. We will be analysing this election by looking at three counties of interest: Arapahoe, Denver, and Jefferson. The aim is to determine the vote count and vote share (as it relates to the total vote count) of each county. Using this data, we will determine which county has the highest voter turnout. This project will also show the vote recieved by each candidate running in the election as well as the share of the total vote each candidate received.

## Election Audit Results
In this election:
 - a total of 369,711 votes were cast over 3 counties.
 - Jefferson county had 38,855 votes cast accounting for 10.5% of the total votes.
 - Denver county had 306,055 votes cast accounting for 82.8% of the total votes.
 - Arapahoe county had 24,801 votes cast accounting for 6.7% of the total votes.
 - Denver county had the highest vote count
 - Charles Casper Stockham received 85,213 votes (23.0% of the total vote)
 - Dianna DeGette received 272,892 votes (73.8% of the total vote)
 - Raymon Anthony Doane received 11,606 votes (3.1% of the total vote)
 
 The election is summarized by the figure below which was obtained by writing the output of the code in our project to a text file.
 
 ![Election_results](https://user-images.githubusercontent.com/93050931/142780545-2a40c402-afd7-4923-aabf-c690c59fa7e1.PNG)

 
## Summary
The election commission will find this code very useful in future elections due to it's ease of adaptation to different datasets. The only line of code that one would need to modify to get the same results for a different election would be to change the file path  in the following:

file_to_load = os.path.join("Resources", "election_results.csv")

In this line, one would just need to replace 'election_results.csv' with the name of their .csv file of interest as well as make any changes to the folder name in the first argument of the os.path.join() function. For the code to run as intended however, the new .csv file would need to have the same data structure as the 'election_results.csv' file. If the new file were to be slightly different, one would need to make the following changes:

for row in reader:

        # Add to the total vote count
        total_votes = total_votes + 1

        # Get the candidate name from each row.
        candidate_name = row[2] ------------> candidate_name = row[updated index according to new .csv file]

        # 3: Extract the county name from each row.
        county_name = row[1] -------------> county_name = row[updated index according to new .csv file]

Alternatively, if one would like information other than candidate names and county names, this code could be modified to get that information instead. One would just want to change the variable name to a more fitting one and change the row index to the number which corresponds to the index of their column of interest in their dataset. By making the changes listed above, this code can be used to analyse a wide variety of information from any election data stored in a .csv file.

 
