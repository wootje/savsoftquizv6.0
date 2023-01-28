## Removed the need for docker. Upload to the root of your web server, import SQL & you're good to go

Changes:
1. Removed Docker files
2. Added 'index.html' to the root directory that redirects you to the login page
3. Removed the need to manually enter your domain name in a file by setting relative paths:<br>
» var api_base_url="/api/public/";<br>
» var api_site_url="/api/public/index.php";

Savsoft Quiz v6.0 is an Opern Source and Free php based web application (script) to create and manage online quiz, test, exam on your website or server.


## Minimum Server Requirement
- PHP version 7.3 or newer is required
- tokenizer extension
- intl extension
- mysqli extension
- MySQL  version 5.1+



## Useful links

Open Source Version Demo: https://savsoftquiz.org/demo/application/dist/index.html <br>
Admin Login:<br>
Username: admin<br>
Password: admin<br><br>


User/student Login:<br>
Username:  user007<br>
Password:  123456<br><br>

 


## Installation Instructions

1) Upload zip file and extract.<br>
2) Open .env file (located at savsoftquizv6.0/api/ ) <br>
3) Update app base url and database credentials (update both database details, readDB and writeDB.) If you are using single database then use same credentials in both.<br>
4) Import database.sql file to both database (.sql file located in root folder of savsoftquizv6.0 )<br>
5) Upload all files to the root directory of your web server.
6) Open your web browser and go to the domain you host this software on.
7) Log in using the creadentials provided below.

Default admin logins:

username: admin

password:  admin

If you have any issue to login then read instructions at https://github.com/Techkshetra/savsoftquizv6.0/wiki/First-time-login-troubleshoot 

## Docker installation

The docker-compose file has two containers, mariadb and quiz (the app itself). 

First, clone this repo.

```$ git clone https://github.com/Techkshetra/savsoftquizv6.0.git
   $ cd savsoftquizv6.0/
```
Then edit docker-compose.yml with the following variables as you wish

```
     - DB_HOST=mariadb   # name of the mariadb container 
     - DB_USERNAME=exam
     - DB_NAME=exam
     - DB_PASSWORD=exam
     - DOMAINNAME=YOUR-DOMAINNAME
```

At last,  start the containers:

```
$ docker-compose up -d
```

populate database with file `database.sql`

```bash
$ mysql -u root -p --protocol tcp exam < database.sql
```

# Wiki - Documentation
https://github.com/Techkshetra/savsoftquizv6.0/wiki<br><br>

 

# Found any issue or bug?
Raise issue at https://github.com/Techkshetra/savsoftquizv6.0/issues/<br><br><br>



# Do you need more features?<br>
Try our Enterprise version demo at https://savsoftquiz.com/



Recommended hosting https://bitbullhost.com

The MIT License

Copyright 2021 TechKshetra Info Solutions Pvt. Ltd

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:
The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

