import os
import csv
budget_data = os.path.join('budget_data.csv')
with open(budget_data, newline='') as csvfile:
    csvreader = csv.reader (csvfile, delimiter=',')
    print (csvreader)
    csv_header = next (csvreader)
    total_month_count = []
    total_month_count = 0
    net_total = []
    net_total = 0
    beginning_number = 0
    monthly_difference = []
    monthly_difference_list = []
    total_difference = []
    total_difference = 0
    date = []
    
    for row in csvreader:
        total_month_count = total_month_count + 1
        net_total = net_total + int(row[1])
        ending_number = int(row[1])
        monthly_difference = ending_number - beginning_number
        monthly_difference_list.append(monthly_difference)
        beginning_number = ending_number
        total_difference = total_difference + monthly_difference
        average_difference = total_difference / total_month_count
        greatest_increase = max(monthly_difference_list)
        greatest_decrease = min(monthly_difference_list)
        date.append(row[0])
        greatest_increase_date = date[monthly_difference_list.index(greatest_increase)]
        greatest_decrease_date = date[monthly_difference_list.index(greatest_decrease)]
    print("Financial Analysis")
    print("------------------------")
    print("Total Month: " + str(total_month_count))
    print("Total: " + "$" + str(net_total))
    print("Average Change: " + "$"+ str(average_difference))
    print("Greatest Increase in Profits: " + str(greatest_increase_date) + " ($"+str(greatest_increase)+")") 
    print("Greatest decrease in Profits: " + str(greatest_decrease_date) + " ($"+str(greatest_decrease)+")") 
