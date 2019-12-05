# express_Sequelize_RESTfulAPI_ReturnData
An express app connecting to mySQL database and implementing RESTful API to return data from a GET request in Postman.

COMMAND PROMPT

(1) Run the following to navigate to your Desktop: 

    cd Desktop

(2) Create a new folder on Desktop: 

    mkdir Express

(3) Navigate to the Express directory: 

    cd Express

(4) Run the following command to install the Express generator globally onto your computer: 

    npm install express-generator -g

(5) Enter the following command to generate the Express starter app. This will set the view to use Handlebars and will name the app express_Sequelize_RESTfulAPI_ReturnData: 

    express --view=hbs express_Sequelize_RESTfulAPI_ReturnData

(6) Once the process is complete, navigate into the express_Sequelize_RESTfulAPI_ReturnData directory: 

    cd express_Sequelize_RESTfulAPI_ReturnData
    
(7) Now in the express_Sequelize_RESTfulAPI_ReturnData directory, run the following: 

    npm install

(8) Install Nodemon globally: 

    npm install -g nodemon
    
(9) Install Nodemon as a devDependency in the package.json file within the express_Sequelize_RESTfulAPI_ReturnData directory:

    npm install -save-dev nodemon
    
(10) Install mysql2:

    npm install --save mysql2

(11) Install sequelize: 

    npm install --save sequelize@5.15.1

(12) Open in VS code:

    code . 


VS CODE

(13) Navigate to the routes/index.js file and require mysql2 and models in routes/index.js file.: ![Require mySQL2 in index js file in routes folder (Sequelize_RESTfulAPI_ReturnData)](https://user-images.githubusercontent.com/35668707/70207793-c4a46f80-16f9-11ea-82a9-baea0c877dc5.JPG)

COMMAND PROMPT

(14) Create necessary sequelize folders and files in project.:

    sequelize init

(15)  Generate a model file for the actor table. (-h: IP/Hostname; -d: Database; -u: Username for database; -x: Password for database; -o: directory to place the models; -t: comma-seperated names of tables to import):  

    sequelize-auto -h localhost -d sakila -u root -x Password1! -o "./models" -t film,actor,film_actor
    
VS CODE

(16) Create a new folder in your "models" folder called rel. Create a file in your rel folder called associations.js and define the relationships between the "film" and "actor" models in this file.: ![In the models folder create a rel folder and a associations js file in the rel folder (Sequelize_RESTfulAPI_ReturnData)](https://user-images.githubusercontent.com/35668707/70207899-0fbe8280-16fa-11ea-82b1-4eb42827517c.JPG)

![Update associations js file in the rel folder (Sequelize_RESTfulAPI_ReturnData)](https://user-images.githubusercontent.com/35668707/70207971-4eecd380-16fa-11ea-879f-90aadd8d3d0e.JPG)

(17) In the models/index.js file add associations constant: ![Add associations constant to the models - index js file (Sequelize_RESTfulAPI_ReturnData)](https://user-images.githubusercontent.com/35668707/70208371-61b3d800-16fb-11ea-9537-76f426d19bb5.JPG)

(18) At the bottom of the models/index.js file add the call to associations function.: ![Add call to associations function in the models - index js file (Sequelize_RESTfulAPI_ReturnData)](https://user-images.githubusercontent.com/35668707/70208215-ec480780-16fa-11ea-8fdc-dd5e1a0f6fb2.JPG)

(19) Open config/config.json file and change settings to connect to the database.: ![Update database connection info in config - config json file (Sequelize_RESTfulAPI_ReturnData)](https://user-images.githubusercontent.com/35668707/70208457-a0e22900-16fb-11ea-843a-b12e682e0531.JPG)

(20) Open app.js file at the root of the project and include the './model" folder so that the models are available everywhere in the application.: ![Require models in app js file (Sequelize_RESTfulAPI_ReturnData)](https://user-images.githubusercontent.com/35668707/70208530-d1c25e00-16fb-11ea-854e-36ee790109ac.JPG)

(21) Add sequelize sync code above module.exports in the app.js file to ensure that the tables within the models in the project are the same as in the database.: ![Add models sequelize sync in app js file (Sequelize_RESTfulAPI_ReturnData)](https://user-images.githubusercontent.com/35668707/70208586-f8809480-16fb-11ea-9844-8c46e7e161ac.JPG)

(22) In the routes/index.js file require the models.: ![Require models in index js file in routes folder (Sequelize_RESTfulAPI_ReturnData)](https://user-images.githubusercontent.com/35668707/70208637-1e0d9e00-16fc-11ea-9441-5858e5e40502.JPG)

(23) In the routes/index.js file add get() route for /actors that will use the findAll() method.: ![Add get() route for actors in index js file in routes folder (Sequelize_RESTfulAPI_ReturnData)](https://user-images.githubusercontent.com/35668707/70208695-3e3d5d00-16fc-11ea-83ee-797fda6fb6c2.JPG)

COMMAND PROMPT

(24) Run nodemon in terminal to see DB sync'd up: 

    nodemon

POSTMAN

(25) Navigate to localhost3000/actors in Postman and perform a GET request to view data.: ![Perform a GET request for localhost3000 - actors in POSTMAN to view data (Sequelize_RESTfulAPI_ReturnData)](https://user-images.githubusercontent.com/35668707/70208776-67f68400-16fc-11ea-8b80-3e0ef0472232.JPG)

NODEMON NOTE

Sometimes nodemon crashes in Windows 10 and there is a simple fix:

(1) Open Task manager (press Ctrl+Alt+Delete)

(2) Select the 'Processes tab'

(3) Search for 'Node.js: Server-side JavaScript'

(4) Select it and click on 'End task' button

Now you can run npm start.

