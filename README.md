# \<yossh-challenge\>

This project is for the Yossh Coding Challenge I did found [here](https://www.notion.so/Expenses-Input-9b00e0d442a0451f901c07b46842855e).

## Run the application locally

1. Install the Polymer CLI: ` npm i -g polymer-cli`
2. Install Bower: `npm i -g bower`
3. In the root directory, install dependencies: `bower install`
4. In the root directory, run `polymer serve`

## Building the application for production

Assuming you installed the dependencies, you simply need to run `polymer build`.

This will create builds of the application in the `build/` directory, optimized to be served in production. You can then serve the built versions.

## Problem

Users need a way to easily record and view expenses.

## Solution

A simple one page application that allows people to record expenses and see them automatically update in an account ledger.

My solution focused on the front end (UX, CSS, responsive design, etc.).  I used Firebase's database as a service functionality for the back end.

## Assumptions

- No functionality for different users
- No authentication required
- Users don't need to see totals in this view
- Users want to see the amount of the expense in addition to the VAT

## Technical choices

I used **Polymer 2** as the front end framework because it is the framework I feel most comfortable using.  It's outdated (you can tell because it still uses Bower and HTML imports) so given more time I would use Polymer 3.

I used **Firebase** because it is the backend as a service app that I'm most familiar with.  It's very convenient for making demos.

I wrote the app as one large component to take advantage of Polymer syntactic sugar, although especially if the app were to grow more complex I would break it down into smaller components.

I chose to use two-way data binding because of the limited time and small scale of this app.  If the app were bigger I would have invested in implementing Redux or a similar solution.

I used vanilla CSS because I'm very familiar with it and because getting a preprocessor working did not seem like a good use of my time.

I decided to store the money value in pennies to avoid some of the floating point rounding errors.

## What I would improve given more time

- Add a delete button for expenses in case a mistake was made
- Use a library to manage currency storage and calculations to prevent rounding errors
- Use a library to keep track of dates accurately across browsers
- Add some color to the design
- Make the date picker component more closely match the other input fields
- Use Polymer 3 and lit-html instead of Polymer 2
- Break up the component into smaller reuseable components

