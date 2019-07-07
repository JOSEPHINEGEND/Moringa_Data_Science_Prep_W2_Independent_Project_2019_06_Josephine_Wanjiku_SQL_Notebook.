# Moringa_Data_Science_Prep_W2_Independent_Project_2019_06_Josephine_Wanjiku_SQL_Notebook.
WEEK 2 SQL INDEPENDENT PROJECT 
# {SQL Programming}
#### {Project to assist a candidate to become the US president}, {June,2019}
#### By **{Josephine Wanjiku}**
## Description
{}The primary objective is to assist a candidate to become a US president. 

The winner is the candidate with the most grand-electors.

Grand electors are attributed at the state level in each of the 51 states.

In each of the 51 states, there is a given number of grand electors to win (roughly, but not exactly, proportional to the size of the state). 

The presidential candidate receiving the most local votes wins ALL the Grand Electors in that state.

Since the no. of grand electors is not proportional to the population, some states can be prioritized to increase the ROI of the campaign
*Assumptions:

 *There are only 2 candidates
 
 *No history (no trend of certain states to vote for a particular candidate or party)
 
 *Each vote is equally ‘expensive’ to get and
 
 *Some states grant more grand elector per capita
 
*Required:

 Identify the states that should be prioritized to win the election with a smart but simple algorithm.
 
 The main aim is to look for a strategy that makes sense and not to look for an overall optimum
## Setup/Installation Requirements
* We have been provided with two tables: 

 Grand electors per state
 
 Population per state
 
Data Cleaning and analysis steps:

Rank states by decreasing the number of grand electors per capita

The first states in the list are the most valuable i.e. you get a large number of grand-electors by convincing a small number of people to vote for you.

We will target all the states at the top of the list until the cumulative sum (also called running total) of grand electors won is larger than half the total number of Grand Electors in the country.

To do this we:

Join the two tables on the state key which appears in both

But first, convert all the States to upper case

Change the "District of Columbia" state to its short version "DC".

Compute ratio between the number of grand electors and the population and

Create a new column with the ratio

Order states by decreasing ratio of GrandElector per capita

Select all the states for which the running total of the GrandElectors in descending order is below or equal to the threshold.

Add the first state for which the running total is larger than the threshold.

Then filter our sorted list of states in order to keep only the (top) ones.

Those that are within the threshold we need to reach for winning the presidential election.

Other states can be ignored

This is our target list

Findings

The sum of all grand electors is 538

Half of the total of Grand Electors overall (in the whole country): 269

This is the threshold needed to reach for winning the presidential election.

Conclusion

Since the main objective was to assist the candidate to become a US president and the winner of the election is the candidate with the most grand-electors, we can conclude that from our analysis the candidate should target and maximize his resources such as campaigns in the 11 states above where he would easily meet the threshold to win the presidential election.

The country has 56 states, therefore, the target list for 11 states is fairly small but significant to achieve the main objective. It is nearly 20% of the total states. 

Recommendation

It would be a good recommendation to target the states to reach the threshold tactfully and win the presidential elections. 

## Known Bugs
{None. }
## Technologies Used
{Python; Pandas for data manipulation
SQL for selecting data and creating tables. 
Google Colab notebook for backend analysis}
## Support and contact details
{Email; josephinewanjiku748@gmail.com}
### License
*{MIT  See below for more details on licensing.}*
Copyright (c) {2019} **{Moringa School Data Science}**
