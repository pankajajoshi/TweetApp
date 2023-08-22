Explain what is an ODM/ Intro to Mongoose
ODM stand for Object Document Model. It translates the documents in Mongo into upgraded JavaScript Objects that have more helpful methods and properties when used in conjunction with express.

Rather than use the Mongo shell to create, read, update and delete documents, we'll use an npm package called mongoose. Mongoose will allow us to create schemas, do validations and make it easier to interact with Mongo inside an express app.

Mongoose Visual

Make a Schema
A schema will allow us to set specific keys in our objects. So if we have a key of name, we won't be able to insert other keys that don't match like firstNameor names. This helps keep our data more organized and reduces the chance of errors.

We can also specify the datatypes. We can set the datatype of nameto a string, ageto a number, dateOfBirthto a Date, bffto a Boolean etc.

Basic Set Up
In student_examples

mkdir intro_to_mongoose
cd intro_to_mongoose
touch app.js
npm init -yand go through the prompts
npm i mongoose dotenv
touch tweet.js .gitignore .env
code .

Remember Our MongoDB information is a secret so we need to set up Environment Variables
Update .gitignoreto include .env (always do this before you commit anything in .env)
lets add our connection string into the .env
update our app.jsto add our require('dotenv').config()to the very top of the file
this places every kvp in our .envinto a javascript object called process.env
