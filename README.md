# Data Aggregation and Validation Engine

Each cycle of a CNC machine runs for 300+-5 secs. During this time multiple readings of 'Spindle Load' are taken. 
Our goal was to parse the given file which contained readings and store the mean, std, min, max for each of the reading of the cycle. 

So the next time when the machine is run, if the values recorded do not conform to the range that the previous values did, it can be inferred that there is an anomaly. 

16Jan2020.zip contains the CSV file which has the complete data of the machine, from which the desired parameter values were extracted. 

Final.ipynb is the Jupyter Notebook that reads the CSV file 16Jan2020.zip, extracts it into a Pandas dataframe and proceeds to analyse to give the final outputs which are stored in a list. Each of these lists is later stored locally in a Mongo database on the device it is run. 
