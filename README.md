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

(5) Enter the following command to generate the Express starter app. This will set the view to use Handlebars and will name the app express_Sequelize_ProvideDataToTheFrontEnd: 

    express --view=hbs express_Sequelize_ProvideDataToTheFrontEnd

(6) Once the process is complete, navigate into the express_Sequelize_ProvideDataToTheFrontEnd directory: 

    cd express_Sequelize_ProvideDataToTheFrontEnd
    
(7) Now in the express_Sequelize_ProvideDataToTheFrontEnd directory, run the following: 

    npm install

(8) Install Nodemon globally: 

    npm install -g nodemon
    
(9) Install Nodemon as a devDependency in the package.json file within the express_Sequelize_ProvideDataToTheFrontEnd directory:

    npm install -save-dev nodemon
    
(10) Install mysql2:

    npm install --save mysql2

(11) Install sequelize: 

    npm install --save sequelize@5.15.1

(12) Open in VS code:

    code . 


VS CODE

(13) Navigate to the routes/index.js file.: ![Open index js file (Sequelize_ProvideDataToTheFrontEnd)](https://user-images.githubusercontent.com/35668707/69693911-08b5c580-10a5-11ea-9d4e-4d77582c6d9d.JPG)

(14) Require mysql2 and models in routes/index.js file.: ![Require mysql2 in index js file (Sequelize_ProvideDataToTheFrontEnd)](https://user-images.githubusercontent.com/35668707/69693937-2551fd80-10a5-11ea-8444-143e164d0700.JPG)

COMMAND PROMPT

(15) Install Sequelize CLI commands globally onto your computer: 

    npm install -g sequelize-cli

(16) Create necessary sequelize folders and files in project.:

    sequelize init
    

VS CODE

(17) Open config/config.json file and change settings to connect to the database.: ![Open config json file and update database connection info  (Sequelize_ProvideDataToTheFrontEnd)](https://user-images.githubusercontent.com/35668707/69693968-49154380-10a5-11ea-8b03-56684274763d.JPG)

COMMAND PROMPT

(18) Install mysql2 globally so sequelize CLI will be able to connect to the database.:

    npm install -g mysql2
    
(19) Install sequelize-auto tool to generate model files: 

    npm install -g sequelize-auto

(20) Generate a model file for the actor table. (-h: IP/Hostname; -d: Database; -u: Username for database; -x: Password for database; -o: directory to place the models; -t: comma-seperated names of tables to import):  

    sequelize-auto -h localhost -d sakila -u root -x Password1! -o "./models" -t actor
    
VS CODE

(21) Open app.js file at the root of the project and include the './model" folder so that the models are available everywhere in the application.: ![Require models i app js file (Sequelize_ProvideDataToTheFrontEnd)](https://user-images.githubusercontent.com/35668707/69694016-7104a700-10a5-11ea-8dcf-628c0935961d.JPG)

(22) Add sequelize sync code above module.exports in the app.js file to ensure that the tables within the models in the project are the same as in the database.: ![Add models sequelize sync in app js file (Sequelize_ProvideDataToTheFrontEnd)](https://user-images.githubusercontent.com/35668707/69694065-9d202800-10a5-11ea-8830-caa893b3c989.JPG)

(23) In the views folder, create a actors.hbs file.: ![In views create actors hbs file (Sequelize_ProvideDataToTheFrontEnd)](https://user-images.githubusercontent.com/35668707/69694296-3cddb600-10a6-11ea-98b3-e4a273fe3940.JPG)

(24)  Add a get() route for /actors to the routes/index.js file.: ![Add get() route for actors in index js file (Sequelize_ProvideDataToTheFrontEnd)](https://user-images.githubusercontent.com/35668707/69694340-61399280-10a6-11ea-9ea2-fa549f98ea92.JPG)

COMMAND PROMPT

(27) Run nodemon in terminal to see DB sync'd up: 

    nodemon

POSTMAN

(28) Navigate to localhost3000/actors in Postman to view data.: ![Open in Postman (Sequelize_ProvideDataToTheFrontEnd)](https://user-images.githubusercontent.com/35668707/69844588-e48bed00-123a-11ea-8fd3-9e2858c8bb24.JPG)

NODEMON NOTE

Sometimes nodemon crashes in Windows 10 and there is a simple fix:

(1) Open Task manager (press Ctrl+Alt+Delete)

(2) Select the 'Processes tab'

(3) Search for 'Node.js: Server-side JavaScript'

(4) Select it and click on 'End task' button

Now you can run npm start.

