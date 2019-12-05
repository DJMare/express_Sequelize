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

(13) Navigate to the routes/index.js file and require mysql2 and models in routes/index.js file.: 

COMMAND PROMPT

(14) Create necessary sequelize folders and files in project.:

    sequelize init

(15)  Generate a model file for the actor table. (-h: IP/Hostname; -d: Database; -u: Username for database; -x: Password for database; -o: directory to place the models; -t: comma-seperated names of tables to import):  

    sequelize-auto -h localhost -d sakila -u root -x Password1! -o "./models" -t film,actor,film_actor
    

VS CODE
(16) Create a new folder in your "models" folder called rel. Create a file in your rel folder called associations.js and define the relationships between the "film" and "actor" models in this file.: 

(17) In the models/index.js file call the function from the models/rel/associations.js file.:

(18) At the bottom of the models/index.js file add the call to associations function.:

(19) Open config/config.json file and change settings to connect to the database.: 

(20) Open app.js file at the root of the project and include the './model" folder so that the models are available everywhere in the application.: 

(21) 

(22) Add sequelize sync code above module.exports in the app.js file to ensure that the tables within the models in the project are the same as in the database.: 

(23) In the views folder, create a actors.hbs file.: 

(24)  Add a get() route for /actors to the routes/index.js file.: 

COMMAND PROMPT

(27) Run nodemon in terminal to see DB sync'd up: 

    nodemon

POSTMAN

(28) Navigate to localhost3000/actors in Postman to view data.: 

NODEMON NOTE

Sometimes nodemon crashes in Windows 10 and there is a simple fix:

(1) Open Task manager (press Ctrl+Alt+Delete)

(2) Select the 'Processes tab'

(3) Search for 'Node.js: Server-side JavaScript'

(4) Select it and click on 'End task' button

Now you can run npm start.

