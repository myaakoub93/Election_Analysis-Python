# Election_Analysis

## Overview of Election Audit
Tom is part of the election team for Colorado Board, he has reached out to us to support him and report on the conclusion of the election and to audit the results for U.S. congressional precinct in Colorado. With our skills in Python we will need to indicate the total number of votes, the candidates and the numbers of votes they each received, and determine the winning candidate. The reason we are automating this process is to help the board with future auditing on the election. 


## Election-Audit Results
Below is an image showing the results for the election followed by a few summary to recap and conclude the results:

<img src="https://github.com/myaakoub93/Election_Analysis-Python/blob/main/Final%20Election%20Results.png" width="430" height="500" />   

1. **_How many votes were cast in this congressional election?_** <br /> The total number of votes that were cast in this congressional election were: 369,711
2. **_Provide a breakdown of the number of votes and the percentage of total votes for each county in the precinct._** <br /> As you can tell by the image above, the highest turnout was in Denver by a long shot with over 80% (306,055 of 369,711) of the votes coming out from there. Jefferson and Arapahoe both had very little turnout compared to Denver with each of them accounting for only only 10.5% and 6.7% respectively of all votes.
3. **_Which county had the largest number of votes?_** <br /> As mentioned Denver had the largest number of votes with over 80% (306,055 of 369,711) of them coming from here.
4. **_Provide a breakdown of the number of votes and the percentage of the total votes each candidate received._** <br /> Funny enough, similar to the county voting results there was a similar disparity in the results between the competition. With 73% of the votes going to Diana DeGette, she won the election with the popular vote total of 272,892 votes. She was followed by Charles Casper Stockham with 23% of the popular vote and Raymon Anthony Doane coming in last with a dissapointing 3.1% of the votes.
5. **_Which candidate won the election, what was their vote count, and what was their percentage of the total votes?_** <br /> With 73% of the votes going to Diana DeGette, she won the election with the a popular vote total of 272,892 votes. 

## Election-Audit Summary
The PyPoll code is built to be used for any election audit. However we need to consider the following:

- The format for CSV is crucial. The county name is the second coloumn and the candidate is in the third column of the CSV file. If that is not the case then the for loops must be adjusted to reflect the change. The following two lines must be adjusted to have the number in the brackets = (the column number - 1). That's because the CSV column index starts at 0 rather than 1. 

         # For each row in the CSV file.
      for row in reader:

        # Get the candidate name from each row.
        candidate_name = row[2]

        # 3: Extract the county name from each row.
        county_name = row[1]



- The second thing has to do with the file location. As you can see in the code below as an example, the file that the audit is referencing to is something on my computer specifically and for this to work elsewhere that would need to be adjusted to wherever the file is being referenced.

        Add a variable to load a file from a path.
        file_to_load = os.path.join("Resources", "election_results.csv")
        Add a variable to save the file to a path.
        file_to_save = os.path.join("analysis", "election_analysis.txt")   
