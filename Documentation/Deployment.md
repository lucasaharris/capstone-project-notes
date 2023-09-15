# Deployment

## Server 
* DocuMentor is currently hosted on Heroku
* To push local changes to Heroku and restart the server: `git push heroku master`
* To stop the system: `heroku ps:scale web=0`

## File/Folder Structure
* To run the project locally for development : create a .env file in the root of the project following the .env.example file
  * <strong>This is where you will specify postgres username, password, access keys etc.</strong>
* To set environment variables when deploying to heroku: `heroku config:set <env variable>`

## Logging
* DocuMentor uses Coralogix for logging
* https://documentor.coralogix.com/#/login/user

## Troubleshooting
* see Heroku issues:
  *  https://help.heroku.com/946888
  *  https://help.heroku.com/948925

## Critical Pieces
* The app stores personally identifiable health information, and so must comply with HIPAA regulation
  * Security measures DocuMentor is taking:
      * Ensuring Pundit policies and scopes are used for every action.
      * Nesting most routes under /provider. There is a current_provider helper method available in all views and controllers. Using this to scope                 everything, and set foreign keys.
      * Using UUIDs on almost every model, for an extra layer of "security through obscurity" (URLs not traversible).




