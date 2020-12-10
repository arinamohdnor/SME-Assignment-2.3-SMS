## CloudSchool

[![Codeship Status for hrshadhin/school-management-system](https://app.codeship.com/projects/09010350-b97f-0136-1477-5a7589b245e6/status?branch=master)](https://app.codeship.com/projects/312233)
[![license](https://img.shields.io/badge/license-AGPL-blue.svg)](https://www.gnu.org/licenses/agpl-3.0)
[![php](https://img.shields.io/badge/php-7.2-brightgreen.svg?logo=php)](https://www.php.net)
[![laravel](https://img.shields.io/badge/laravel-6.x-orange.svg?logo=laravel)](https://laravel.com)

    Username    | Password
    ------------|:-----------
    superadmin  | super99
    admin       | demo123

## Features
[:arrow_up: Back to top](#index)

|   Features  | 
|-----------------------|
| Academic Year manage  |
| Academic Calendar Setup |
| Institute Setup | 
| Class & Section Manage | 
| Subject & Teacher Manage | 
| Student Admission | 
| Student Attendance | 
| Exam & Grading Rules | 
| Marks & Result |
| Student Promotion |
| Employees Manage |
| Employees Attendance | 
| Employees Leave | 
| User & Role manage with permission grid(ACL) |
| User wise Dashboard | 
| Report Settings |
| Only 5 Reports | 
| Dynamic Front Website |
| Website Management Panel | 
| Photo Gallery | 
| Event Manage |
| Google Analytics | 
| User Notification |

## Installation
[:arrow_up: Back to top](#index)

#### Installing dependencies

- PHP >= 7.2
- OpenSSL PHP Extension
- PDO PHP Extension
- Mbstring PHP Extension
- Tokenizer PHP Extension
- XML PHP Extension
- Ctype PHP Extension
- JSON PHP Extension
- MySQL >= 5.6 `OR` MariaDB >= 10.1
- [hrshadhin/laravel-userstamps](https://github.com/hrshadhin/laravel-userstamps.git) [**Already Installed**]
- NodeJS, npm, webpack

#### Download and setup

 - Make sure you have git, npm, NodeJS, xampp (php, mysql and phpmyadmin) installed.
 - Clone the repo via Github Desktop or 
    ```
    $ git clone https://github.com/arinamohdnor/SME-Assignment-2.3-SMS.git
    ```
- Copy sample `env` file and change configuration according to your need in ".env" file and create Database
    ```
    $ cp .env.example .env
    ```
- Install php libraries
    ```
    $ composer install
    ```
 - Open xampp, turn on apache and mysql (make sure documentroot in httpd.conf in xampp/apache folder is set to {project directory}/public)
 - Setup application 
    - Method 1: By one command
         ```
         # setup cloudschool with out demo data
         $ php artisan fresh-install
       
         # setup cloudschool with demo data (preferred for our assignment)
         $ php artisan fresh-install --with-data 
          # OR
         $ php artisan fresh-install -d
         ```
    - Method 2: Step by step (not preferred)
        ```
        $ php artisan storage:link
        $ php artisan key:generate --ansi
      
        # Create database tables and load essential data
        $ php artisan migrate
        $ php artisan db:seed
      
        # Load demo data
        $ php artisan db:seed --class DemoSiteDataSeeder
        $ php artisan db:seed --class DemoAppDataSeeder
      
        # Clear all caches
        $ php artisan view:clear
        $ php artisan route:clear
        $ php artisan config:clear
        $ php artisan cache:clear
        ```
- Install frontend(css,js) dependency libraries and bundle them
    ```
    $ npm install
    $ npm run backend-prod
    $ npm run frontend-prod
    ```
    
- Go to http://localhost and you're done!

#### Use the app
[:arrow_up: Back to top](#index)

    Username    | Password
    ------------|:-----------
    superadmin  | super99
    admin       | demo123
