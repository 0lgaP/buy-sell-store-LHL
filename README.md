Pokemon Black Market
=========

## Midterm Project

This project was completed in a team of three, working remotely and connecting via daily standups. This forked version of our final team effort focuses on my contributions. For the full project please checkout (Pokemon Black Market)[https://github.com/rosemaryku/buy-sell-store-LHL]<br>

My portion of this project focused on creating a dynamic home page with a filter function and search field. To create the styling I used a combination of bootstrap and my own CSS. We created a database using a googlesheet inorder to keep our data flxible, and seeded the database using this (file)[https://docs.google.com/spreadsheets/d/1Dl3u8Ljn4a8ZBeZEEJRMHPoSNVud7nUuDf5Bl6fWgss/edit?usp=sharing].
To keep our database organized and determine connections we created the (ERD)[https://drive.google.com/file/d/1PbDLUP3zLS19-jghNx1EasgC2OkrHiKr/view?usp=sharing] and adjusted it as the database developed.

## Front Page functionality

When you land on the Pokemon Black Market Homepage you are greeted by a plethera of colourful images and a dynamic attention grabbing carousel created through EJS & Bootstrap. <br>
The user can filter by preference values available in the dropdown, the default state is "Newest First". As the filter is selected, the carousel adjusts it's image order to accomodate the filter preference. <br>
The user can search by Pokemon name or partial and be redirected to a page containing only the search results. <br>
Each Pokemon card connects the user to the full details of the pokemon, and unlocks additional functionality like favourite and message. <br>
The footer is present at the bottem of the page and will take you back to the top of the page or to the github of our team mebers.

## Getting Started

1. Create the `.env` by using `.env.example` as a reference: `cp .env.example .env`
2. Update the .env file with your correct local information 
  - username: `labber` 
  - password: `labber` 
  - database: `midterm`
3. Install dependencies: `npm i`
4. Fix to binaries for sass: `npm rebuild node-sass`
5. Reset database: `npm run db:reset`
  - Check the db folder to see what gets created and seeded in the SDB
7. Run the server: `npm run local`
  - Note: nodemon is used, so you should not have to restart your server
8. Visit `http://localhost:8080/`

## Warnings & Tips

- Do not edit the `layout.css` file directly, it is auto-generated by `layout.scss`
- Split routes into their own resource-based file names, as demonstrated with `users.js` and `widgets.js`
- Split database schema (table definitions) and seeds (inserts) into separate files, one per table. See `db` folder for pre-populated examples. 
- Use the `npm run db:reset` command each time there is a change to the database schema or seeds. 
  - It runs through each of the files, in order, and executes them against the database. 
  - Note: you will lose all newly created (test) data each time this is run, since the schema files will tend to `DROP` the tables and recreate them.

## Dependencies

```sh
    "bootstrap": "^5.1.3",
    "chalk": "^2.4.2",
    "cookie-session": "^2.0.0",
    "dotenv": "^2.0.0",
    "ejs": "^2.6.2",
    "express": "^4.17.1",
    "jquery": "^3.6.0",
    "method-override": "^3.0.0",
    "moment": "^2.29.1",
    "morgan": "^1.9.1",
    "pg": "^8.5.0",
    "sass": "^1.35.1"
```
