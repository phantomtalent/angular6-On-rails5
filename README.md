# README
> Requirements:
    - nodejs
    - angular-cli
    - postgresql
    - rails

# description
this project was build with both the rails cli and the angular cli and is a example of how you could hook them together. in its current setup angular builds directly into the public folder over riding all off those files inside it to prevent the deletion of all files (for example you want to put non generated files in there) simply change the outputPath in the frontend/angular.json file to go one level deeper then public 
> example: `setting "outputPath": "../public"` too `"outputPath": "../public/build"` would mean you only had to add the root-route(in the config/routes.rb) to `root '/build/'`
# building your own version
## api
the api is the output of the basic `rails new command <name> --api -d postgresql` command with 3 seperate scaffolds commands ran

## frontend
this folder is the angular app with a few views to represent the data other then that it is the basic `ng new <name(frontend)> --routing`
command ran from the project root.

## db
the database is postgresql and requires some setup. If you decide to take the same steps to recreate this project for your self, keep in mind that i have added the `gem 'dotenv-rails'` to my gemfile so i could use a .env file. and made some changes to the config/database.yml file so the db would work when running rails db:create.

