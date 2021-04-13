## Movie Ratings
I love watching movies, but only if they are recommended by other audiences so I don't waste too much of my time.

So, I wrote this little app to help me search movies I am interested in, calculate average ratings from multiple trusted sources for each of them, and list them from high to low ratings.

#### Run
```
npm i
npm start
http://localhost:3000
```

On the home page, fill in the form with the keyword in the movie title, submit, and it will pull out the results for you.


#### Todo

sort by year, title, reverse sort ratings

load top 5 films/dramas currently on iPlayer, from a report in S3 bucket.

cache for iplayer, no need to call the api and recalculate for every request as the schedules don't change frequently

recently queried films can be retrieved from a sever side cache

iPlayer Poller Lambda function,  run once a day, queries appw/ibl, compute ratings, save the report in a S3 bucket.

Messenger, Lambda function, triggered by S3 upload and send iPlayer ratings to users by emails once a day.

user input validation ( both client and server side). 

limit the words/chars in comments


