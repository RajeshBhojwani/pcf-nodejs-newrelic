# Node JS application binding with newrelic

## It has configuration which is required to bind with newrelic service in PCF


## Important configuration to remember
 Add newrelic.js file in root folder. This will have configuration for license key. It has to be setup as env variable.
 
 Add "newrelic": "3.0.0" in package.json
 
 Add require('newrelic'); as the first line of the app's main module.
 
 Environment variable to be set before pushing the app to pcf. (License key has to be taken from PCF App->Services->newrelic-> credentials)
 Change key value in manifest.yml file 
 
 Bind the newrelic service from apps manager. Do cf restage to get the changes reflected.
 
 Check the newrelic Console to see if able to see the appname for transactions.
 

## Running
```npm install```
```node app.js```
```cf push```
