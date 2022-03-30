# What I Learned Today
- Pandas officially stands for ‘Python Data Analysis Library’, THE most important Python tool used by Data Scientists today.
- The Pandas library one of the most preferred tools sfor data scintestic to do manipulation and analysis , next to matplotib for data visulazation and Numpy , the fundamental library for scintific , computing in python on which pandas was built .
- Data manipulation : The abiltiy to deal with data for analysis and  do some operation for the data mo matter how bid is it .

# What is Pandas and How does it work ?

Pandas is an open source Python library that allows users to explore, manipulate and visualise data in an extremely efficient manner. It is literally Microsoft Excel in Python.

# Why is Pandas so Popular ?
It is easy to read and learn
It is extremely fast and powerful
It integrates well with other visualisation libraries
It is black, white and asian at the same time

# What kind of data does Pandas take ?
Pandas can take in a huge variety of data, the most common ones are csv, excel, sql or even a webpage.

- To use pandas  -- > ` import pandas as pd `

- Data Frame : Data in a tabular form , and use it easily in python (like arrays or dectionaries )  panda give us the ability to deal with that data .

- To read data frrom cvs  file  ==>`df = pd.read_csv(file_path)`
- To get the default first data records  ==> `df.head(number of data records to get )`
- To get the default last data records  ==> `df.tail(number of data records to get )`
- To get the default specific data records ==> `df.iloc[2000]`  #2000 is the index of the record that i want to get 
- to slice over data frame ==>`df.iloc[5000:5001]`
- to get specific index from the slicing part of data ==>`df.iloc[5000:5001].iloc[3]`
- to get the type of object == >`type(df.iloc[5000:5001])`
- to get specific coloum from a slice of data frame == > 
 ```  
 all_vac = df['coloum_name']
 all_vac.iloc[4000:4005]
 ```

 - to get more one coloum ==>

```  
 all_vac = df[ ['coloum_name','another_coloum_name']]
 all_vac.iloc[4000:4005]
 ```

- to do sole mathematic operation 
```
some_valc = all_vac.iloc[4000:40001]['coloum_name']
some_valc.mean()
some_valc.median()
```
- to get the last item ==>   `df.iloc[-1]`

- to get data for a specific value ==>  
```
italy-data = df[df['location']=='Itay']
italy_date =df[df['date']=='2022-1-07]
italy-data
italy_date 
italy_data.describe()
```
















