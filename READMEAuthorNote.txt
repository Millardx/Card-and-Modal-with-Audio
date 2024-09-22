# How to setup/migrate this project to your project.

-For backend and frontend files.. 
 In migrating the project you just need to follow the files structure and create the folders and file with their designated name.
 Then you need to copy their code and paste it to your newly created file in your project. 
 Make sure you follow structure so the imports wont messed up. 
After that you need to install the modules of the backend and and frontend 
    for backend copy this -  npm install cors@^2.8.5 express@^4.21.0 init@^0.1.2 mongoose@^8.6.3 multer@^1.4.5-lts.1 path@^0.12.7 serve-index@^1.9.1
                           - npm install --save-dev nodemon (for auto restarting the backend if something changes)
                           - add this script to package.json  "scripts": {
                                                                            "start": "node server.js",
                                                                            "dev": "nodemon server.js"
                            Also rename your main in package.json into "server.js"                                                         
                            This will have the exact version of the modules used in this project
    for frontend copy this - npm install axios@^1.7.7 react@^18.3.1 react-dom@^18.3.1 react-modal@^3.16.1 react-router-dom@^6.26.2 react-scripts@5.0.1 react-slick@^0.30.2 sass@^1.79.1 slick-carousel@^1.8.1
                    To install paste those command to you terminal inside their own folder like for backend and frontend 
                    You should inside the backend in terminal if youre trying to install the backend modules, works in frontend too
                    if encounter some issue in installation try to remove the version and try again . 
    Dont forget to copy this in public/index.html:
                            <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
                            <link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
                            <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@24,400,0,0" />
    Also this in src/index.js :
                            import "slick-carousel/slick/slick.css";
                             import "slick-carousel/slick/slick-theme.css";
# Setting up DB connection is simple you just need to replace this code in server.js:
    const dbUri = process.env.MONGO_URI || 'mongodb://localhost:27017/Card&Audio';
                                            "replace the "Card&Audio" with your new DB created in MONGO db or you can named it the same"

in running backend : npm run dev
in running the frontend : npm start 

At first you need to delete files in upload:    
        You might see errors in fetching in the console since theres no existing data that can fetch from your DB. 
        So you need to Upload first in the Admin Page 
                    In Edit Card any image type are allowed 
                    In Edit Modal only jpeg , jpg , png image type are allowed 
                    In Edit Audio only mp3, wav, ogg, m4a, flac audio types are allowed.

        If any issue in migrating on in trying this project ask the author of the code Millardx or GPT.