# Nodes per author

All Nodes
```dataview
TABLE length(rows) as Number
FROM #molecule OR #atom OR #source OR #particle OR #novel
WHERE Creator != None
GROUP BY Creator
```

---

Atoms Only
```dataview
TABLE length(rows) as Number
FROM #atom 
WHERE Creator != None
GROUP BY Creator
```

---

```dataview
TABLE Creator
FROM #molecule OR #atom OR #source OR #particle OR #novel
WHERE Creator != None
SORT Creator 
```
