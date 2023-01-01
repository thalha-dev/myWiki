# NPM BASICS

##### To initialize nmp package

` npm init`

* -y flag to say yes to all feilds.
* generates an .json file in the root dir.

##### To install package dependencies with package.json file

`npm install`

##### To install packages as dev dependencies

`npm i <name> --save-dev`

`(or)` 

`npm i <name> -D`

##### Semantic Versioning

* `majorVersion:minorVersion:patchVersion`
* `^ma:mi:p`, cap symbol tells to update only minor and patch version.
* `npm i package@ma:mi:pa`, to install particular version.
* `npm update`, to update mi:pa.

##### To install packages 

`npm rm <name> `

`(or)` 

`npm uninstall <name>`

* If it is a dev dependency
`npm uninstall <name> -D`

### LIST OF PACKAGES AND ITS USES

* nodemon
    - used to run the project. 
    - by default looks for index.js file in root folder.
    - it is a dev dependency
    - `npm i nodemon` 

* uuid
    - used to generate unique user id everytime.
    - `npm i uuid` 
