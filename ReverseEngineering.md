# Unit 14 - Reverse Engineering Code

## Project Structure

The project is structured with multiple folders, each of them serving a specific purpose.

- `config/` : 
    - `config.json`: Json file with all config values that enable the app to run
    - `passport.js`: Setup passport for handling user authentication
    - `middleware/isAuthenticated.js`: Makes sure users aren't allowed to visit routes they aren't allowed to. 
- `models/` :
    - `index.js`: Connects to the database and imports the login data from user
    - `user.js`: Hashes passwords by using the `bcrypt` module, for storing passwords in the database more securely.
- `routes/`:
    - `api-routes.js`: List of all the routes in the app. These include: login, logout, and getting user data.
    - `html-routes.js`: Serves the appropriate html depending on the login status of the user.
- `package.json`: Information regarding the dependencies and script commands for running the application
- `package-lock.json`: Information on every single dependency used for the project and the respective version number.
- `server.js`: Sets up the server for the project. Uses `express` for routes and `passport` for authentication. Even logs information to the console depending on the activity being run.

## Adding changes

To make changes to the application, let's make sure it is running properly on your local machine:

- Create a `mysql` database called `passport_demo`.
- Edit the `config.json` file with credentials to successfully connect to the database.
- Make sure you are in the project directory and run `npm install` to install all the required dependencies to allow the project to run.
- Now run `node server.js` to run the project on your local machine.
- Open your browser and navigate to `http://localhost:8080` to access the app.

Now you can test the changes you make to the app and make sure your edits are valid!

