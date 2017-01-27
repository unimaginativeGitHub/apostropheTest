# apostropheTest
>Quick experiment with ApostropheCMS </br>
>*For TruQC Hack Day - January 2017*

**Note:** this project relies on a data directory that has been excluded from the repository - this also means no users or other MongoDB stored data will be preserved when pulling fresh from the repo.

## Infrastructure
* **Homebrew**

  `ruby -e "$(curl -fsSL https://raw.github.com/Homebrew/homebrew/go/install)`


* **MongoDB**

  `brew install mongo`

  **Note:** you can run MongoDB using a *local* db directory by creating a directory in your project called `data/db` and starting the MongoDB instance by running `mongod --dbpath data/db` from the project root directory.  You can also just follow the instructions in the tutorial and install mongo with homebrew and use the system default `/data/db` directory.

  You can check to see if mongo is running by navigating to `http://localhost:27017` <- mongo also prints out the port it's using on db startup.

  #### Handy Mongo Commands:
  * **Start MongoDB**:  `mongod`
  * **Start Mongo Shell**:  `mongo`


* **ImageMagick**

  `brew install imagemagick`

  **Use**: Apostrophe uses this to scale and crop images

* **Apostrophe Command Line Tools**

  `npm install apostrophe-cli -g`


## Tutorial

### Basic Hello World

* Create a simple test project

 >`apostrophe create test-project`

* Install dependencies, add an admin user and start the project

 >`cd test-project`<br/>
 >`npm install`<br/>
 >`node app.js apostrophe-users:add admin admin`<br/>
 >`node app.js`<br/>

* Navigate to default project location

 > http://localhost:3000/

## Gist

- MongoDB is used to store everything - including images and pdfs
- You write templates and pages in Nunjucks templating engine - a "a more sophisticated templating engine"

## Resources
* ApostropheCMS Home - http://apostrophecms.org/
* ApostropheCMS Docs - http://apostrophecms.org/docs/index.html
* ApostropheCMS Tutorials - http://apostrophecms.org/docs/tutorials/index.html
* MongoDB Docs - https://docs.mongodb.com/manual/
* Nunchucks Docs - http://mozilla.github.io/nunjucks/
