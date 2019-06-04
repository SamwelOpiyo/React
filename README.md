[![Build Status](https://travis-ci.org/SamwelOpiyo/React.svg?branch=master)](https://travis-ci.org/SamwelOpiyo/React)

# Beerbank

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

# CI/CD Setup.

## Generating a Github Token.

A github token is needed in order access and clone the repository containing infrastructure and application configuration/provisionment scripts.

Open https://github.com/settings/tokens and generate a new token. Ensure you check the *REPO* check box so that the token can have permissions to pull from private repositories.

## Environment Variables Setup.

Open https://travis-ci.org/{user/organization}/{repository}/settings for example https://travis-ci.org/SamwelOpiyo/Vue/settings and set the following environment variables:

* DOCKER_HUB_PASSWORD
* DOCKER_HUB_USER
* GITHUB_TOKEN
* GCP_MAIN_SERVICE_ACCOUNT :To get this value you will need the path of admin service account generated to run terraform. Use `base64 {path_to_SA} | paste -sd ''` to obtain it. For example in our case navigate to configurations repository, then run `base64 service_account_keys/main_service_account.json | paste -sd ''`.

## Activating Repository for CI/CD

Open https://travis-ci.org/{user/organization}/{repository} for example https://travis-ci.org/SamwelOpiyo/Vue and click on *Activate repository*.

# Project setup.

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.<br>
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.<br>
You will also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.<br>
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.<br>
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.<br>
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (Webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: https://facebook.github.io/create-react-app/docs/code-splitting

### Analyzing the Bundle Size

This section has moved here: https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size

### Making a Progressive Web App

This section has moved here: https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app

### Advanced Configuration

This section has moved here: https://facebook.github.io/create-react-app/docs/advanced-configuration

### Deployment

This section has moved here: https://facebook.github.io/create-react-app/docs/deployment

### `npm run build` fails to minify

This section has moved here: https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify
