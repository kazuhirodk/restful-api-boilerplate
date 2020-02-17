# restful-api-boilerplate
#### [![Build Status](https://travis-ci.org/kazuhirodk/restful-api-boilerplate.svg?branch=master)](https://travis-ci.org/kazuhirodk/restful-api-boilerplate) [![Coverage Status](https://coveralls.io/repos/github/kazuhirodk/restful-api-boilerplate/badge.svg?branch=master)](https://coveralls.io/github/kazuhirodk/restful-api-boilerplate?branch=master) [![Maintainability](https://api.codeclimate.com/v1/badges/8cc3280b4f8c66ee4fb2/maintainability)](https://codeclimate.com/github/kazuhirodk/restful-api-boilerplate/maintainability)
Restful API with NodeJS, Express, PostgreSQL, Sequelize, Travis, Mocha, Coveralls and Code Climate.
#### Reference: [@victorsteven Medium article](https://medium.com/@victorsteven/restful-api-with-nodejs-express-postgresql-sequelize-travis-mocha-coveralls-and-code-climate-f28715f7a014)

This is a simple Restful API boilerplate. The technologies used were the following:
- **NodeJS** - For writing Javascript server-side applications
- **Express** - A NodeJS framework
- **PostgreSQL** - An open source object-relational database
- **Sequelize** - An ORM(Object Relational Mapping) of PostreSQL
- **Travis** -A continuous integration service for Testing Applications
- **Coveralls** - A web service to help you track your code coverage over time.
- **Code Climate** - Provides automated code review for maintainability and test coverage.
- **Babel** - To convert ES6 javascript code to ES5

## Initial Setup
Install package dependencies
```
npm install
```
Build application
```
npm run build
```
Start application
```
npm run dev
```

Make sure you have PostgreSQL running locally.
Create the database
```
createdb books
createdb book_test
```
You can use any user for PostgreSQL database, just use `.env.example` template.
Next, run the migrations
```
sequelize db:migrate
```
This template already has a Book database by default, but you can utilize Sequelize to create a new one.

*example*
>sequelize model:create --name Book --attributes title:string, price:string, description:string

## Default endpoints
**POST** A BOOK
> http://localhost:8000/api/v1/books

*body example*
```
{
	"title": "First Awesome book",
	"price": "R$ 17,90",
	"description": "This is the awesome book"
}
```

**GET** ALL BOOKS
> http://localhost:8000/api/v1/books

**GET** A PARTICULAR BOOK
> http://localhost:8000/api/v1/books/:id

**UPDATE (PUT)** A PARTICULAR BOOK
> http://localhost:8000/api/v1/books/:id
*body example*
```
{
	"title": "First Awesome updated book",
	"price": "R$ 17,90",
	"description": "This is the awesome updated book"
}
```
**DELETE** A PARTICULAR BOOK
> http://localhost:8000/api/v1/books/:id


## Testing
```
npm run test
```
