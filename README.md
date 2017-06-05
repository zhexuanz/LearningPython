# Learning Python
The material below is broken down by modules


## List

* Append one element

`
ll.append( 'a' )
`
* Concatenate with another array

`
list1.extend( list2 )
`

* List grep
`
names = ['aet2000','ppt2000', 'aet2001', 'ppt2001']
filter(lambda x:'aet' in x, names)
`

* List and Dict Comprehension
`
cols = [ x for x in CNY.columns.tolist() if 'time' not in x ]
colsRename = {key:key+'_CNY' for key in cols}
`

## pandas

* Import dataframe from spreadsheet. The same command can also reads table from url. read_csv can directly reads csv without setting the 

`
df = pandas.read_table('data/abc.csv', sep = ',')
`

* Save dataframe to CSV with no index

`
df.to_csv('abc.csv', index=False)
`

* Create dataframe from list of list

```
df = pandas.DataFrame(listoflist)
df.columns = [ 'time', 'low', 'high', 'open', 'close', 'volume' ]  # gives column header
```

* Find the max of a column

`
val = pd['columnname'].max()
`

* Sort dataframe by a column value

`
df.sort_value( 'time', inplace = True ) 
`

* Add new column from a calculation using an existing column through lambda

`
df.newcolumn = df.existingcolumn.apply( lambda x: ( x/3 + 2 ) )
`

* Rename columns
`
df.rename(columns={'oldName1': 'newName1', 'oldName2': 'newName2'}, inplace=True)
`

## datetime

* Create a time datetime object

`
starttime = datetime.datetime(2017, 5, 28, 0, 0)
`

* Use timedelta to do time increment

`
endtime = startime + datetime.timedelta( seconds = 30 )
`

* Convert time stamp ( an integer format for time ) datetime object

`
datetime.datetime.fromtimestamp( 1495929600 )
`

* Convert time to an ISO formatted string

`
timeobj.isoformat() # this gives e.g. '2017-05-27T19:00:00'
`


## Time

*  Halt the program for a given time period (seconds)

`
time.sleep(5)
`


