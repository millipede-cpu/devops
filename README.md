# Devops

A guide to database file set up with Node, Express, Cypress,PostgreSQL and steps to deploying web applications to Heroku

# What is Node.js?

Node.js is a platform for building the i/o applications which are server-side event-driven and made using JavaScript.

It is used to build server-side, input-output, event-driven apps. That's where the `server.js` file comes in.

# What is Express.js?

Express.js is a framework based on Node.js for which is used for building web-applications using approaches and principles of Node.js. You need to require Express in your `server.js` file such as `const express = require("express");`

# What is PostgreSQL ?

PostgreSQL is a powerful, open source object-relational database system. Creating a database requires typing some commands outside of typing `psql` into your terminal. You can connect to your database with `\connect your_database_name` or `\c your_database_name`

- `psql` command starts Postgres
- `\connect your_database_name` connects to your database
- `\include init.sql`command to run some SQL (Structured Query Language) directly from a file to save typing it all out
- `\q` command quits Postgres
- `\dt` command shows all the database tables, inlcuding new ones you created
- `\l` command lists all available databases

# Initial file setup

DevOps as a role in team projects requires the initial file setup for the repository. This can get confusing because a lot of folders and files are automatically made by using `npm install` for Cypress (Testing Framework to check your code is passing your tests) and Express

# Deploying to Heroku

- Set up an account on [Heroku](https://www.heroku.com)
- Create a new app from your dashboard
- Remember to include Heroku Postgres as an add-on and choose Hobby Dev as a free add-on option
- Remember to include these in your Heroku Config Vars, in the settings tab

`COOKIE_SECRET "longrandomstring"`

`DATABASE_URL postgres://(URI)`

`PGSSLMODE 'no-verify'`

- Check the connection.js inside the database folder of this repo to see the necessary additions to help with deployment, but this can sometimes stop your app from running locally, you can always comment them out though.

- In the deploy tab of Heroku, you can connect your Github to the correct repository ready for deployment. Scroll down to enable automatic deploys or choose to manually deploy once you have everything you need on the main branch.

- If you run into any issues with deployment you can check on your Heroku logs to try and see the issue.

- Once your app is deployed...make sure to check it all works first!

- Add the live link to your github repository and show it off to everyone!
