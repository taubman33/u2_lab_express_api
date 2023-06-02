# SEIR 0508

### Express / Mongoose API From Scratch

## GAMEMDB - The GA Mongoose Express Movie Database (this name still needs work)

For this lab we are going to create our own backend server! 

1) Run your necessary installations to get the necessary files and folders for Mongoose and Express, then mkdir and touch the additional ones you will need. Feel free to look back at previous lessons to see what these will entail. You are _not_ expected to memorize every step of the process so far!

```sh
npm init -y
npm i ... ... ... ...
mkdir ... ... ... ...
touch ... ... ... ...
```

_note:_ you may have to run npm i, mkdir, and touch multiple times through these steps to ensure you have everything created in the correct order

2) Update your Scripts block in your package.json so that your server is able to run on Nodemon (which, hopefully you've installed. If not, do it now!)

3) In your config/db file, connect to a moviesDatabase using our standard Mongoose boilerplate

4) Create 3 schemas, Movies, Reviews and Actors. 

-  Your movies model should have a Title, Runtime, Rating, Year Released and a brief description. You can also include a link to a poster image for it, or try to upload an image file if you want a challenge! Think of what data types you'll want to use for each of these additional properties

- Your actors model should have properties for Name and Age, and one that says if they are Alive or not, plus any other properties you'll want to include. Again, try to add images using either method. What datatypes would we use for our other properties?

- Reviews should be owned by movies and have a score and a comment. Your score can be 1-5, or 0-100%, either way, it will need some kind of Constraint put on it to make sure it can only hold valid information.

- Use your Foreign Key references to connect your data! You will have the choice of which you want the parent and child to be. Should Actors own many movies? Or movies own any actors?

- Attach Reviews to movies using Foreign Key refs.

- Populate your db so that you have at least 5 of your parent data (movie or actor) and 10 of your child. Once you have Actors and Movies seeded, add at least 2 reviews to at least 3 of your movies.

- Attach all of the necessary boilerplate to your express server.js file. Your landing page (localhost:3001/) should be the index list of your top parent data. We will want endpoints that have index and show routes for all three collections


### Requirements

- At least 3 Collections with a relation. You can have either Actor->Movie->Review, or you can have Movie as a parent with both Actor and Review children. The choice is yours!
- Index and Show Routes for each of these routes


### Bonus I
- AAU I want to sort my reviews by ascending or descending order
- AAU I want to sort my movies by newest or oldest
- AAU I want to Create, Update, and Delete my Actors, Movies, and Reviews using either ThunderClient or a query.js file
- AAU I want an error message to display if I search for an Actor, Movie, or Review with an incorrect ID


### Bonus II

- AAU I want a Front End page that will allow me to pull, log, and render this information on screen using the Axios library to a url of localhost:3001 with all of our respective routes and endpoints
- As A Picky and Opinionated User I also want this page to have some style to it!

### Bonus III
- Using the Plants API HW as a reference, add in CRUD functionality to your back end, and test it with ThunderClient
- If you've gotten this far, we have a real challenge for you... use the Axios library to give your front end full CRUD as well!
