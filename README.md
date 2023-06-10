# Smart Brain - Back end

This is the back end of my Smart Brain project. The server is built with Node.js and Express.js and is connected to a PostgreSQL database using Knex.js.

The server interacts with the Clarifai API using gRPC calls to detect faces from an image URL.

## Tech Stack

**Server:** Node, Express

**Database:** PostgreSQL


## Lessons Learned

In building this back end, I learned about the importance of organzing routes/controllers in your code in order to find bugs quicker. This was also the first time I made a project that connects to a database and got to learn SQL and use a JS Query Builder like Knex.js to run SQL queries in JavaScript. 

A challenge I faced while building this app was when I moved the Clarifai API calls from the front end to the back end. I was intially using fetch API calls but once I moved everything to the back end, I kept receiving empty objects as the response object. I did some research and learned that the Clarifai API works better with Node.js if you use gRPC rather than REST for communicating with it. After converting to gRPC, everything worked again.
