# Heroku Deployment:-

 * We use the heroku login command to log in to the Heroku CLI.
 * The authentication is required for both the heroku and git commands to work correctly.
 * Heroku need the git, node.js and npm to work.
 * heroku create: will Create an app on Heroku, which prepares Heroku to receive your source code.
 * git push heroku master: will push/deploy my work to the heroku server.
 * heroku ps:scale web=1: to Ensure that at least one instance of the app is running.
 * heroku open: will send you to the url of your app after pushing it.
 * heroku logs --tail: to view information about your running app.
 * Control+C: to stop streaming the logs.
 ![Heroku](./Img/heroku.gif)


### commands on terminal to set up:

- `heroku login `
- `node --version`
- `npm --version`
- `git --version`
- `git clone https://github.com/heroku/node-js-getting-started.git`
- `cd node-js-getting-started  `
- `heroku create  `
- `git push heroku master  `
- `heroku ps:scale web=1  `
- `heroku open  `
- `heroku logs --tail `
- cnrtl+c
