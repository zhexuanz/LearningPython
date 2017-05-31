# Learning Python
The material below is broken down by modules


## List

* Append one element

`
ll.append( 'a' )
`
* Concatenate with another array

`
list1.append( list2 )
`


## pandas

* Create dataframe from list of list

```
df = pandas.DataFrame(listoflist)
df.columns = [ 'time', 'low', 'high', 'open', 'close', 'volume' ]  # gives column header
```

* Sort dataframe by a column value

`
df.sort_value( 'time', inplace = True )
`
* Save dataframe to CSV with no index

`
df.to_csv('abc.csv', index=False)
`
* Add new column from a calculation using an existing column through lambda

`
df.newcolumn = df.existingcolumn.apply( lambda x: ( x/3 + 2 ) )
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


