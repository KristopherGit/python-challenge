# Module-2-Challenge

# python-challenge

# PyBank

1. Included in this program's file directories is a financial dataset [budget_data.csv] for a company. The dataset is comprised of two columns: Date and Profit/Losses.

2. The python script in the PyBank's folder includes the main.ipynb that calculates the following:

   i.) Total number of months included in the dataset.
   ii.) The net total amount of profit/losses over the entire period.
   iii.) The average of the changes in profit/losses over the entire period.
   iv.) The greatest increase in profits (including the date & total amount)
   over the entire period.

   The resulting analysis is summarized in the following:

   ## Financial Analysis

   Total Months: 86
   Total: $38382578
  Average  Change: $-2315.12
  Greatest Increase in Profits: Feb-2012 ($1926159)
  Greatest Decrease in Profits: Sep-2013 ($-2196167)

3. The final main.ipynb file executes to print the final analysis in terminal,
   as well as exporting to a text file called 'financial_analysis.txt'

# PyRamen

1.  The following program analyze's a company's business financial performance by cross-checking previous annual sales data with the current internal menu data which ultimately summarizes revenues & costs for the fiscal year. This program's goal is to analyze how well the business performed on a per-product basis, display which products are doing well, and which products may require review and need to be altered as required.

2.  This program begins by initializing an empty menu list object that reads & takes in the contents of the included 'menu_data.csv' and populates its it as a list object including an indexing of the menu list items, category, description, price and cost. (Ultimately the menu is filtered and category & description column data are excluded from the final list analysis). The initial menu list data is then converted to a dataframe to filter by column of crucial data & sorted back to a separate menu_list.

3.  Additionally, this program takes in further sales data from a 'sales_data.csv' file and populates a corresponding sales list object for analysis. Similarly, the sales list is also fed through a dataframe function to sort, sum, and summarize the data and stored in a separate finalized sales_list that can be analyzed further.

4.  Manipulation of the data is as follows:

    i.) An empty report dictionary is created to hold the summation data consolidated from the per-product results. The dictionary created as a 'report' contains the following field values tied to a unique 'sales_item' (menu_item) key pair in the following format:

                report[sales_item]["01-count"]
                report[sales_item]["02-revenue"]=price*quantity
                report[sales_item]["03-cogs"]=cost*quantity
                report[sales_item]["04-profit"]=(price-cost)*quantity

    ii.) Afterwards, both the sales_list & menu_list are run through a for-each style loop that matches & filters out only the sales items included on both so that a summarized nested dictionary of key-value pairs can be made of each sales_item and its associated sales '01-count', total yearly '02-revenue', total cost of goods and services '03-cogs' and finally annual '04-profit' can be viewed in a dictionary summarized format.

5.  Finally, the summarized 'report' dictionary is then printed and ultimately exported to a 'report_dictionary.txt' file for viewing/filing purposes.
