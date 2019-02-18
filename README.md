![CF](http://i.imgur.com/7v5ASc8.png) LAB 39
=================================================

## Lab 39: Socet.io Pub Sub

### Author: Ryan Gallaway

### Links and Resources

[![Build Status](https://www.travis-ci.com/rkgallaway/39-socket.io-pub-sub.svg?branch=master)](https://www.travis-ci.com/rkgallaway/39-socket.io-pub-sub)

* [repo](https://github.com/rkgallaway/39-socket.io-pub-sub)
* [travis](https://www.travis-ci.com/rkgallaway/39-socket.io-pub-sub)
* [back-end](http://xyz.com) (when applicable)
* [front-end](http://xyz.com) (when applicable)
* [Starter Sandbox](https://codesandbox.io/s/z6mpqy858m)

#### Documentation
* [swagger](http://xyz.com) (API assignments only)
* [jsdoc](http://xyz.com) (All assignments)

### Modules
#### `modulename.js`
##### Exported Values and Methods

This react application will be conneced to the Q server you build in Block 4. It will connect to the `database` queue and subscribe to `create`, `update`, and `delete` events. For each event, update the UI to indicate the collection that was affected, the event type, the time, and the ID of the record.  You may optionally display additional information.

You should give careful consideration to the visual layout of your application, color choices, animations, and overal usability.

### Notes - Q Server
* Deploy the server to Heroku and validate that you can connect and subscribe to events.
* Listen on `process.env.PORT`
  * Heroku will assign you a port
* Listen on a queue called `database`
* Montior the following events: `create`, `read`, `update`

### Notes - API Server
* Deploy the server to Heroku
* Listen on `process.env.PORT`
  * Heroku will assign you a port
* Alter your API server to connect to the Q server at startup
* Edit your models and make the following changes
  * Add "post" hooks for `save`, `delete` 
  * For each, publish a new event to the Q server
  * Make sure and publish separate events for `create` and `update`, not just `save`
  

### Notes - Connections
* Ensure that you can use `Postman` or `httpie` to hit your server properly.
  * Ensure that all write actions publish the appropriate event and payload into the queue.
  * You can use Postman and your original "logger" client to do this.
  * Once you are confident in the wiring, begin work on the react client.
### Setup
#### `.env` requirements
* `PORT` - Port Number
* `MONGODB_URI` - URL to the running mongo instance/db

#### Running the app
* `npm start`
* Endpoint: `/foo/bar/`
  * Returns a JSON object with abc in it.
* Endpoint: `/bing/zing/`
  * Returns a JSON object with xyz in it.
  
#### Tests
* How do you run tests?
* What assertions were made?
* What assertions need to be / should be made?

#### UML
Link to an image of the UML for your application and response to events
