# Art House Box Office

This is the main repository.  There are two subrepos, client and server.

#### To install
First:  

    git clone https://github.com/art-house-box-office/app
    cd client && npm install
    cd ../server && npm install

###### MongoDB instance
You will need to have an available MongoDB instance running.  Once you have an available URI, insert it into the server's .env file in the appropriate location.

###### There are several environment variables required

in the client directory, create a file named .env-dev and add the following lines:

    API_URL=http://localhost:9000/api
    TOKEN_NAME=token

in the server directory, create a file named .env.dev , and add:


    APP_SECRET=SomethingSecret
    CDN_URL=http://localhost:5000
    MONGO_URI= ** insert your MongoDB URI here.
    PORT=9000


Once these files are in place, run the following command in the server directory, then in the client directory:

    npm run start:watch

Once the builds complete you can connect to http://locahost:5000 and either create a user or log in as Admin:password.


#### Acknowledgements:

- The [OMDb API - The Open Movie Database](http://www.omdbapi.com/), which we access using the [open-api-client package](https://www.npmjs.com/package/omdb-api-client), provides the movie data and poster imagery.
- Thanks to Al She for the team photo!
