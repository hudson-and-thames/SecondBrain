# Novel Molecules

```dataview
TABlE Topics, Creator, Rating
FROM #molecule AND #novel 
Sort rating descending
```

# Recent Molecules Created

```dataview
TABLE number(string(date(today)- file.cday))  AS Days_Since_Creation, Creator
FROM #molecule 
where number(string(date(today)- file.cday)) <= 7
sort number(string(date(today)- file.cday)) asc
```


# Molecules created

```dataview
TABLE file.ctime AS Time_Created
FROM #molecule
sort Time_created asc
```
