import os
import csv
election_data = os.path.join('election_data.csv')
with open(election_data, newline='') as csvfile:
    csvreader = csv.reader (csvfile, delimiter=',')
    print (csvreader)
    csv_header = next (csvreader)

    candidatelist =[]
    unique_candidate =[]
    candidates = []
    votes = []
    percent = []
    individual_vote_count = []
    max_votes_count = []
    winner = []
    for row in csvreader:
        votes.append(row[0])
        candidatelist.append(row[2])
        votes_count = len(votes)
    for x in set(candidatelist):
        unique_candidate.append(x)
        percent.append(round(int(candidatelist.count(x))/int (votes_count),2)*100)
        individual_vote_count.append(candidatelist.count(x))
        max_votes_count = max(individual_vote_count)
        winner = unique_candidate[individual_vote_count.index(max_votes_count)]
    print("Election Result")   
    print("-----------------------------")
    print ("Total Votes: " + str(votes_count))
    print("-----------------------------")
    print("Candidates: " + str(unique_candidate))
    print("-----------------------------")
    for i in range(len(unique_candidate)):
        print(unique_candidate[i] + ":" +str(percent[i])+"% (" + str(individual_vote_count[i])+")" )
    print ("winner is: " + str(winner))
   
