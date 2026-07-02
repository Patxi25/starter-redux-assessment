# Starter redux assessment: Doggiegram

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available scripts

In the project directory, you can run the following commands:

### `npm install`

Installs the project dependencies, including Redux packages such as @reduxjs/toolkit and react-redux.

### `npm run dev`

Runs the React app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

Runs an Express API at `http://localhost:3004` that exposes a single endpoint, `GET /api/suggestion`, which returns a dog suggestion at random.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Runs the test suites.

## AI Declaration

I did not use any AI tools for this assignment.

## Short-answer question

I had issues with inconsistent photo objects being stored in state, especially when adding new photos... I was dispatching incomplete payloads (like the image URL string), which caused newly added items to miss required fields like caption and isFavorite and the app would break... To solve this, I standardized the data model so every photo always had the same shape (id, imageUrl, caption, isFavorite). see commit 9a8d4b2

## Post submission reflection

1. Explain how you designed and implemented the Redux store for this project. What state did you choose to centralize, and why?

answer: it's based off of photos and search... photos slice holds the core application data, and search slice was added to manage the search term separately

2. Explain one key technical decision you made during your implementation. Why did you choose this approach over other possible solutions?

answer: A key decision was to store photos as normalized objects in Redux with a consistent schema to prevent runtime errors and be simple

3. AI use disclosure

Did you use any AI tools at any stage while preparing or developing this assessment?

answer: No
