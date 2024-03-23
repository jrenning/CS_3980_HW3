## Homework Description

This homework involves setting up MongoDB and writing queries on the provided sample data.

The first query is one with the following requirements from the movies table:
- runtime greater than 200 minutes 
- In year 1983
- Sorted by runtime (increasing)
- Only return runtime, title, and year

The query for this and the results are shown below


```javascript

db.movies.find({runtime: {$gt: 200}, year: 1983}, {runtime: 1, title: 1, year: 1, _id: 0})
.sort({runtime: 1})
```

![Query 1](images/query_1.png)


*Note: for some reason the shell in Compass did not work for me, but it did work when I ran it separately so I just did it that way.*



The second query has the following requirements from the movies table:
- After 2014
- IMDB rating greater than 9

The query for this and the results are shown below.

```javascript
db.movies.find({year: {$gt: 2014}, "imdb.rating": {$gt: 9}})
```

![Query 2](images/query_2.png)


