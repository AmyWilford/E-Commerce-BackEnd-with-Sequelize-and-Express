# E-Commerce-BackEnd

## Table of Contents:

- [Description](#description)
- [Technologies-Used](#technologies-used)
- [Required Additional Technologies](#required-additional-technologies) 
- [Installation](#installation)
- [Usage](#usage)
- [Demo](#demo)
- [License](#license)

## Description:

The application uses Express.js and Sequelize to interact with a MySQL database, which together comprise the backe end of an e-commerce site. To interact with the application you will need insomnia to run HTTP requests on the application and view/edit database information.

## Technologies Used:

- MySQL 
- Node.js
- NPM Express
- NPM Mysql2
- NPM dotenv
- NPM Sequelize

## Required Additional Technologies:
- Insomnia

## Installation:

This application requires npm package dependencies.
For installation, in your terminal command line, run:
```
npm install
```
In order to access the database you will need to establish an environment variable file (.env) in the root of your file system. In this file include:
```
DB_NAME = 'ecommerce_db' | database name
DB_PASSWORD = '' | enter your password
DB_USER = '' | enter root user
``` 
Next, you will need to source the SQL database, in your terminal command line, run:
``` 
mysql -uroot -p
```
and enter your SQL login credentials. 
Once logged in, run the following in your terminal command line:
```
SOURCE db/schema.sql |to create the database
USE ecommerce_db;  | to set the databasea you want to use
quit | to exit SQL
```
Next, seed the database by running the following in your terminal command line:
```
npm run seed
```
Once the database is seeded you - you can access the application. To launch the server, in your terminal command line, run:
```
npm start
```
When successfully launched, you will see the following message in your terminal:
``` 
App listening on port 3001!
```

## Usage:

This application requires the use of Insomnia in order to view and interact with the database information. Once you have completed the installation steps listed above, open Insomnia and navigate to localhost:3001

To view information of this e-commerce sites backend database, you can run HTTP GET, POST, PUT, and DELETE requests from the following three end points:

- localhost:3001/api/categories --- to view all store categories
- localhost:3001/api/products --- to view all store products
- localhost:3001/api/tags --- to view all tags associated with products and categories

For POST & PUT requests - the req.body format is as follows:

Categories:
```
{
    "category_name": "test category"
}
```
Products:
```
{
    "product_name": "Basketball",
    "price": 200.00,
    "stock": 3,
    "tagIds": [1, 2, 3, 4]
}
```
Tags:
```
{
    "tag_name": "test-tag"
}
```

## Demo:

[View a video walk through of this application in use](https://drive.google.com/file/d/1wPuiH01ohV6w8u4t-gDgiyLQVpcYNPfM/view)

## License: 
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)