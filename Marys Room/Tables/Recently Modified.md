# Recently Modified
```dataview
TABLE file.mday AS Date_Last_Modified
where number(string(date(today)- file.cday)) <= 1
SORT file.mday DESC
```