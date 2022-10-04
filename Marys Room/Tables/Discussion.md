# Ongoing discussion

To have a discussion with someone one a particular note, make the tag `Discussion ::` tag and tag the person there in as well as the topic for discussion with `Dis_Topic ::`.
A new section can then be introduced to discuss the topic.
If the discussion have been resolved and create a new tag `Resolved ::` with the value `Yes` .
```dataview 
TABLE Dis_Topic as Discussion_Topic, Discussion as Discussant 
where (Discussion != None) AND (Resolved != string(Yes))  
```


```ad-danger
Make sure the tags are spelled excatly correctly, otherwise it won't show here.
```
