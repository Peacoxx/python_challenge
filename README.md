# python challenge 
                                  **Original code being used leveraging module 3 cereal coding**
import os
import csv

# Construct the file path
csvpath = os.path.join('Users', 'pamala', 'Documents', 'GitHub', 'python_challenge', 'Pybank', 'Resources', '"budget_data.csv"')
with open(budget_data.csv) as csv_file:
    csv_reader = csv.reader(csv_file, delimiter=",")

                                                  **UPDATED CODING WITH HELP**
Kept receiving an error with the file path, used several resources and finally was able to get it to work with Chat GPT 
import os
import csv

# Construct the file path
csvpath = os.path.join('/', 'Users', 'pamala', 'Documents', 'GitHub', 'python_challenge', 'Pybank', 'Resources', 'budget_data.csv')

# Open the file and read the contents
try:
    with open(csvpath, newline='') as csvfile:
        csvreader = csv.reader(csvfile, delimiter=',')
        # Process each row in the CSV file
        for row in csvreader:
            print(row)  # This will print each row. You can replace this with your processing code.
except FileNotFoundError:
    print(f"File not found: {csvpath}")
except Exception as e:
    print(f"An error occurred: {str(e)}")
