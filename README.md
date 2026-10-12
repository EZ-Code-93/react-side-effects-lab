# React Side Effects Lab

## Overview
This lab demonstrates how to handle **side effects** in React using the `useEffect` hook. The app fetches and displays a random **programming joke** when the page loads and allows users to fetch a new joke with a button click.

## Setup

Run `npm install` to install dependencies.

Then, run `npm run dev` to start up the React app at `http://localhost:5173`.

In another tab, run `npm run test` to run the test suite.

Before you start building out the application, examine the current code and component hierarchy. This will tell you how components can pass data to each other as well as where that information should be stored.

## Deliverables

- **When our application loads**, make a `GET` request to `https://v2.jokeapi.dev/joke/Programming?type=single` to fetch a joke. Given your component tree, think about which component should be responsible for managing the joke data. Once the data is fetched, store it in state and render the joke on the page.

- **When the `New Joke` button is clicked**, make another `GET` request to `https://v2.jokeapi.dev/joke/Programming?type=single` to fetch a new joke. Update the state accordingly so that the new joke replaces the old one in the UI.

- **While waiting for the fetch request to resolve**, display a loading message to inform the user that a joke is being fetched.

- **If the API request fails**, handle the error gracefully by displaying a message instead of breaking the UI.

## Best Practices

- Use the `useEffect` hook to make API calls at the appropriate lifecycle phase.
- Manage component state using the `useState` hook.
- Keep components modular and reusable.
- Remove unnecessary console logs and commented-out code before submission.


Code Updated: Oct 12, 2026

=============
   UPDATES
=============
**App.jsx:**

Added code for joke functionality by implementing new state variables for joke and loading.
implemented useEffect to display initial joke on page load by calling a newly added fetchJoke function that sets laoding state to true while it fetches the joke from an API and updates the joke state once data is retrieved and resets loading state back to is initial state. function includes a .catch for error handling. Passed new props to JokeDisplay and fetchJoke function to FetchButton.

**FetchButton.jsx:**

Added event listener to button to invoke fetchJoke function upon button click.
passed fetchjoke function as prop to button function.

**JokeDisplay.jsx:**

Passed joke and loading as props to display function. Applied conditional logic to <div> to display loading message while data is retireved and to display joke otherwise.

