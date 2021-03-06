# Asymptotic Explorer
Developed by James Skripchuk


# Blurb
Asymptotic Explorer is an online interactive explanation that aims to give a cursory introduction to Big O notation and asymptotic analysis. These mathematical tools are used extensively in the analysis of algorithms in order to give a ballpark estimate on the the complexity of an algorithm, and to compare algorithms against each other. Nothing like this interactive explanaition currently exists online, and there is an established learning need for CS students learning about algorithms to learn Big O notation. This was mainly created for Dr. Bart's Introduction to Algorithms class, CISC320.

# Instructions
The game details instructions for how to interact with the modules throughout the gameplay process. The main interactive elements are to play with the sliders to see how the Big O condition holds for various values of the constants; and then to test proving a Big O expression by yourself.

![Screenshot](/src/assets/screenshots/large.png)

# Video
https://youtu.be/-kcPXb6fq7E

# Important Files

These files are for coding your game:

* [src/scripts/game.ts](src/scripts/game.ts): The starting file of your game.

These files are for documenting your game:
 
* [egdd.md](egdd.md): The educational game design document describing this game in more depth.

These [package.json](package.json) settings are for configuring the metadata of your game and should be updated:

* `name`: This must be a lower-case version of your repository name on GitHub, without spaces.
* `description`: Give a quick, one sentence summary of your game.
* `game`:
    * `url`: Change this to be the EXACT name of your repository on GitHub.
    * `shortName`: Choose a short name for your game for [Progressive Web App](https://medium.com/@amberleyjohanna/seriously-though-what-is-a-progressive-web-app-56130600a093) packaging.
    * `name`: Choose a longer, complete name for your game.
* `repository`:
    * `url`: Change this URL to be a link to your GitHub repository.
* `homepage`: Change this URL to be a link to the final version of your game's EGDD.
* `contributors`: This should be an array (list) of strings, where each string is like `"Barney Rubble <b@rubble.com> (http://barnyrubble.tumblr.com/)"`.

You should edit the following images to create icons for your game, if it gets installed as a [Progressive Web App](https://medium.com/@amberleyjohanna/seriously-though-what-is-a-progressive-web-app-56130600a093):

* [src/assets/icons/icons-192.png](src/assets/icons/icons-192.png): This is a 192x192 pixel version of your game's icon.
* [src/assets/icons/icons-512.png](src/assets/icons/icons-512.png): This is a 512x512 pixel version of your game's icon.
* [src/assets/icons/favicon.ico](src/assets/icons/favicon.ico): The [Favicon](https://en.wikipedia.org/wiki/Favicon) for your game.
