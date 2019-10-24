# League of Legends MapChecker

[Front End JavaScript](https://github.com/doubleyip/LeagueMapChecker)

[Back End NodeJS](https://github.com/doubleyip/apicallforlolmc)

### About the LoLMC App

League of Legends MapChecker is an app that displays detailed information about a League of Legends player.
This information is meant to let users review past games and analyze their results so they can improve their gameplay.

### What is League of Legends

League of Legends is a 10 player MOBA (Multiplayer Online Battle Arena) with 5 players on each side.
The goal of the game is to destroy the enemy nexus and there are various objectives each teams needs to take before they can attack the nexus.
Taking these objectives and killing other players gives gold which players can use to buy items to make themselves or their team stronger.

### How does the app work?

The LoLMC App takes data from Riot Games' API and extracts game information when given user name and region.
The Front End uses HTML/CSS and JavaScript with Bootstrap to organize and display game information including KDA (Kills/Deaths/Assists ratio),
CS (Creep Score) and Win rate. Some of this information is displayed as charts and graphs using the D3 framework. 

![Profile Page1](/images/pfpage1.png)
![Profile Page2](/images/pfpage2.png)

One of the goals of the project was to create a map that showed where players died so they can minimize mistakes in their play.
We did this through heat maps for individual games as well as another heat map aggregated over many games.

<img src="/images/map1.png" width="53%" height="53%">
<img src="/images/map2.png" width="40%" height="40%">

We originally used AJAX API calls directly to the Riot Games server to get player data. However, this could not be done without a chrome extension that enabled CORS 
or the Allow-Access-Origin exception. We solved this by creating a NodeJS server that made API calls in the Back End and then passed the returned JSON back to our JavaScript.
User accounts are created and accessed using PHP for SQL calls to our MySQL database.

### My Role

My role in the project was implementing the NodeJS server as well as the database. The NodeJS server used Express to streamline the process
of taking information from Riot's API and rendering it to our app. I used the Heroku Cloud to deploy both the actual app as well as the NodeJS server
to run the app. I also worked with the team to test and fix various bugs including overflowing decimals and other HTML/CSS/JavaScript display errors.
