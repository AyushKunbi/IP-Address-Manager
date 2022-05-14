# IP-Address-Manager
Full Stack Web application 


Installation and Usage instructions

## Backend Setup
 Open a git bash / powershell terminal and cd to "backend" directory.
 On "backend" directory, You will need an environment file for the database configuration. Make a copy of the .env.example file and create a .env file by running    " cp .env.example .env" .
  open and edit the ".env" file to specify the db connection env.

    ex. 
        
        DB_CONNECTION=mysql
    
        DB_HOST=127.0.0.1
        
        DB_PORT=3306
        
        DB_DATABASE=MyDB
        
        DB_USERNAME=root
        
        DB_PASSWORD=
        
    Also add "AUDITING_ENABLED=true" to the .env file.
    
 after that run "composer install" (needs composer to be installed) to download dependencies.
  then run "php artisan migrate" to migrate all the needed tables to the db provided to env file.
  then run "php artisan serve" and it would serve it on your local (ex. http://127.0.0.1:8000)


* For Front-End
 Open a git bash / powershell terminal and cd to "frontend" directory.
 On "frontend" directory, run "npm install" to download dependencies. (Needs npm installed).
 Once installed, run "ng serve" and it would serve it also on your local (ex. http://localhost:4200/)

To access the site, please go to "http://localhost:4200/"


** Important Note **
- I have not added a register or any account management for this.
- To add a user, please use the ff. commands :
  
  On backend directory 
  run "php artisan tinker" and type "DB::table('users')->insert(['name'=>'demo_name','email'=>'demo@email.com','password'=>Hash::make('123456')])"
  
  If you run this command, you should be able to login using
 
  Email : demo@email.com
  
  Password : 123456
  
  ## Frontend setup
- Enter the frontend folder.
- Run the comman `$ npm install` to install all the dependencies.
- Run the command `$ ng serve` to run the project in 4200 port.
 
  ## Tech
 This project uses various other open source project to work properly.
 [Angular](https://angular.io/) - Frontend
 
 [Laravel](https://laravel.com/) - Backend
 
 [Bootstrap](https://getbootstrap.com/)     - For Responsive UI

 