# Triptease lightning talk ⚡💬 - Rendering performance improvements with React.memo()

This repo was made for a lightning talk, given at Triptease, by myself. It is to showcase the benefits of using 
React.memo() when using expensive to render functional components. 

By default, the Child component is not memoized. Try clicking the button in the parent. This causes the Parent to 
rerender, which in turn rerenders all of its children beneath it, including an expensive to render functional component.
It's slow! You can verify this by looking at the performance stats which get logged to the console (the important number
is actualTime which is the time taken to render the component in ms)

Uncomment the export in Child which turns it into a memoized component and try again. Although the initial mount render 
is still slow as it has to store the memoized value first time round. However on subsequent rerenders when you click the
button, it's waaaaay faster. It's just fetching the cached version of the component from the memo store.

Wooooo, hooray for memo!

# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `yarn start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.\
You will also see any lint errors in the console.

### `yarn test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `yarn build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `yarn eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).
