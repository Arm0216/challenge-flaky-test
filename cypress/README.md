### Installation
**You must follow these steps for installing dependencies and run localHos.**

1. Project Dependencies
    * `cd` to root directory of the project
    * Install Node modules:
   ```
   npm install
   ```
2. Start local server:
    ```
   npm start
   ```

###Opening Cypress GUI
* `cd` to root directory of the project
* start local server
* open Cypress GUI:
    ```
   npx cypress open
   ```
### Running Tests from the CLI
* `cd` to root directory of the project
* start local server

Run tests headlessly:
```
npx cypress run

```

### The cause of the issue.
Wait was not fixed, that's why test was not stable.

### How did I solve that.
I added default wait in the ```cypress.json``` file which helped to solve the problem

### Another solution.
I can add timout directly on the part of the code which have issue with waits.

For example: ```cy.get('li', {timeout:time}).should('contain', 'Some Name - some@email.com - core - git-it')```
