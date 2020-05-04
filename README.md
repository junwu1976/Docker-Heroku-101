# Docker-Heroku-101
Guide for deploying Docker containers in Heroku

Before setting off on this guide please ensure you have a Heroku account

You'll also need the Heroku CLI tools which you can get from ![here](https://devcenter.heroku.com/articles/heroku-cli) or if you're on a mac and have Homebrew installed simply

```
brew tap heroku/brew && brew install heroku
```

 heroku login
Log in to Container Registry

You must have Docker set up locally to continue. You should see output when you run this command.

```
$ docker ps
```

Now you can sign into Container Registry.

```
$ heroku container:login
```
Push your Docker-based app

Build the Dockerfile in the current directory and push the Docker image.

```
$ heroku container:push web
````

Deploy the changes

Release the newly pushed images to deploy your app.

```
$ heroku container:release web
```

Note: Ensure your Dockerfile has a capital 'D' as the Heroku CLI tooks won't recognise it if you don't. Learn from my wasted few hours on this.

