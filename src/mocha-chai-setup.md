# Mocha Chai Setup - for integration testing

Assumes you are using Galvanize Express Generator, and that mocha is installed globally

## Steps

1. Create a "test" directory in the project root

1. Install dependencies:

  ``` sh
  $ npm install chai chai-http mocha --save -dev
  ```
  (chai-http 'mocks out' the app)

1. Add a "test" script to *package.json* (under "scripts"):
  ```json
  "test":"mocha"
  ```
1. Add new file called *mocha.opts* to the "test" directory and add the following flag so that mocha looks in all the directories within the "test" directory for tests:

  ```
  --recursive
  ```

1. Create a new folder called "integration" within the "test" directory.

1. Create a new file for each route resource that you are testing - i.e., *AUTHORS-routes.js* within the "integration" directory (*cars-routes.js* in this case).
