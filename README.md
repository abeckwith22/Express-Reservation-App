# Reservation App

#### Part One: Setting Up

- [x] Create a project folder, Git repository, and ***package.json***.
- [x] Create a database, ***lunchly***.
- [x] Read in the sample data in ***data.sql***.
- [x] Install the required node modules through `npm i`.
- [x] Start the server with ***nodemon***
- [x] Take a tour of the site at ***http://localhost:3000*** -- you should be able to see the list of customers, view a customer detail page, and add a customer. Add a reservation is not yet complete, so expect errors if you try to create a new reservation.

#### Part Two: Look at the code

There's lots of existing sample code.
- [x] **app.js** - application logic; can be imported from other files/tests.
- [x] **models**/ - Model objects as classes, to "abstract" database handling.
- [x] **routes.js** - Routes for the web interface.
- [x] **server.js** - Functionality to start the server (this is the file that is run to start it).
- [x] **templates**/ - Jinja templates, rendered with the JS "Nunjucks" library
- [x] **seed.py** - File to create sample data (you don't need to use this, but may find it interesting as an example of how to create realistic fake data.)

#### Part Three: Class (Static) Methods
- [x] Take a look at `get(id)` method of the ***Customers*** classes. These methods are meant to be called on the class. They look up the corresponding sutomer in the database, and return a JS instance of the correct class. Find where this code is being used in the handlers and make sure you understand it.

#### Part Five: Full Name

In several templates, we show customer names as `{{ firstName }} {{ lastName }}`. This is slightly tedious, that we have to write out both fields, but also might be inflexible for future data changes: what if we added a middle name field later? What if we added a prefix field for labels like “Ms.” or “Dr.”?

- [x] Add a function, `fullName`. to the Customer class. This should (for now) return first and last names joined by a space.
- [x] Change the templates to refer directly to this.

#### Part Six: Saving Reservations

We've already written a ***.save()*** method for customers. This either adds a new customer if they're new, or updates the existing record if there are changes.
- [x] We don't yet have a similar method for reservations, but we need one in order to save reservations. Write this.