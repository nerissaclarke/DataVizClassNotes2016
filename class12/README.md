# Class 12: Server Side Rendering & Web Apps!

## Housekeeping

 * Last Class?!?
 * Any Questions
 * Show N' Tell? Any cool maps?

## Today's Goals

 * Set up an Express.js app framework
 * Run it locally 
 * Go over D3 server-side
 * Push to a Github Repo
 * Log into Heroku
 * Connect your Github Repo
 * Deploy 
 * Enjoy the awesomeness 

###### Caveat

 1. We're walking through a simple framework for D3 + Express. *There are lots of other ways you could do this*, and this simple approach isn't ideal for complicated apps. Check out the Express.js site to learn about more of its features and frameworks.
 2. We're not going to go into the details of everything today. There's enough here for an entire course. Don't worry about understanding everything. Try to figure out where you add your code, how to add pages, and how to deploy.

### Getting Started

 What is [Node.js](https://nodejs.org/en/? Server side Javscript
 What is [Express.js](https://expressjs.com/? Web framework for Node
 What is [npm](https://www.npmjs.com/? A package manager for node modules

##### Setting up the Express framework

First, lets get an Express app framework downloaded and running

 1. Download this directory metis-app
 2. Download node, npm, git
  * ``brew install node npm git``` 
 3. Open up package.json
  * Change the name to your own. Make it distinct, as we'll try to use this when we push our app to heroku
  * (I'd also rename the directory name to that, though you don't need to)
 4. Run ```npm install```
 5. Run ```npm start```
 6. Go to localhost:5000

##### Running D3 server side
 * What does that mean?
 * Why do we do it?
 * Where do we write our D3?
 * What are the tradeoffs?
 * Trying different use cases
 	* Thinking about how you could build your site


##### Push to Github
Let's now go to Github and create a repo:
 * Go to your account
 * Click on Repositories 
 * Click on New
 * Enter in the name that matches your app


##### Deploy with Heroku

 * Go to [herkou](http://heroku.com)
 * Login in
 * Click on new app
 * Give it the same name you gave the other 

 * Connect using github
 * Don't enable automatic deploys

 * Deploy using Master branch
 * Go check it out! 

* Additional:
	* to view the log on herou: ```heroku logs --tail --app <APP_NAME>```

### Brainstorm
* What could you do with your site?
* Caveats around importing JSON
* Making it professional 

# Thanks!! Keep in touch! p.buffa@gmail.com



