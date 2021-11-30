# Deep-links-universal (Universal Link)

## Project Base
Note: This project was created to complement the following repository: [UniversalLink](https://github.com/thaliees/ios-UniversalLinks).

### Apple-app-site-association file
Create the file called apple-app-site-association and add the following content:
`{`     
     `"applinks": {`     
          `"apps": [],`     
          `"details": [ { "appID": "TEAM_ID_HERE.BUNDLE_ID_HERE", "paths": ["*"] } ]`     
     `}`     
`}`

Where TEAM_ID_HERE is the team ID that Apple assigned you when you created your Apple developer account. You can find it in the Apple developer center and BUNDLE_ID_HERE is the app's bundle ID. In "paths", you can limit the paths value to specific folders or file names, the * means you have access to all routes.

This file MUST NOT HAVE EXTENSION! Now that the file is complete, you upload it to the web server.

## Deployment

This project is deployed on Heroku
1. Install the Heroku CLI
```
$ brew tap heroku/brew && brew install heroku
```
2. Login
```
$ heroku login
```
3. Add remote
```
$ heroku git:remote -a name_app_on_heroku_here
```
4. Deploy this project
```
$ git push heroku master
```