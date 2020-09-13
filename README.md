You are an actuary looking at automobile claim settlement data. You have been asked to analyze
the dataset using R.

# Task 1) 

Read in the AutoSettlements_Messy.csv file in R. 
Name the resulting dataframe as AutoSett. 
Replace blanks with NAs, using the na.strings argument in the read.csv() function.
Determine the number of rows, the numbers of columns, and the data types for each column in
the Autosett data frame.

# Task 2) 

Filter the data to view the 60+ year old males that had a settlement. 
Hint: use the which() to handle NAs. Males are indicated by 1 in the Gender column.

# Task 3) 

Make a backup copy of the data frame, AutoSett, and name it AutoSettBackup. 
Changethe SETTNUM column to a factor data type, not an integer data type.

# Task 4) 
Fix the missing data (NAs) in the Gender column with the known information in the
table below. 
Hint: Use complete.cases() to isolate the missing data.

SETTNUM GENDER
21 2
47 2
1128 1
2018 1
2756 2

# Task 5) 

Fix the missing SEATBELT data by using a median of the known values. 
Hints: Use thena.rm = TRUE argument in the median function to calculate the median with stripping out the
NAs. 
Use !complete.cases. 


# Task 6) 

Fix the missing AGE data by using a mean of the known values within each occupation.
Hints: SETTNUM == 25 is missing AGE data. 
Calculate the mean AGE of the rows where Occupation is Engineering.

# Task 7) 

There’s messy data in the SETTLEMENT column. 
Fix the SETTLEMENT data for SETTNUM: 10, 37, 71. 

For SETTNUM == 10, remove the dollar ($) sign and the comma (,).

For SETTNUM == 37, remove the text “ dollars”. For SETTNUM == 71, remove the negative sign (-) since settlement amounts should be positive
