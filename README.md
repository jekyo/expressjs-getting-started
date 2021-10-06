# Tutorial: Deploying a basic Express app on Jekyo

### Prerequisites

Make sure you have [NodeJS](https://nodejs.org/en/download/), [npm](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm) and [git](https://github.com/git-guides/install-git) installed.

If it's your first time using **Jekyo**, you can **install** it by running the following command in your terminal:

`npm install -g jekyo`

### Sign in to Jekyo

You can sign in to Jekyo by running `jekyo user:signin`

```
➜  ~ jekyo user:signin 
Your email?: **************
Your password?: **********
You have successfully signed in!
```
If you don't have a Jekyo account, you can create one in the terminal by running `jekyo user:signup`. 

## Create an Express app skeleton

## Method 1

You can start your Express project by using `jekyo create`

Using the **arrows** on your keyboard, select expressjs and press **enter**.  
```
? Select template
  None Creates only the application
❯ expressjs A basic app skeleton using [Express](https://expressjs.com/)     
  nuxt-js A boilerplate SSR application using [Nuxt.js](https://nuxtjs.org/) 
```

When prompted, enter the desired name for your Express app. 

`Application name?: express-on-jekyo`

This will create a basic Express app in the current directory by cloning this [Express app skeleton](https://github.com/jekyo/expressjs-getting-started) repository.

```
Cloning source code... OK
Application created!
```
### Deploy the Express app on Jekyo

To deploy the app, first navigate to the newly created directory:

`cd express-on-jekyo`

Now you can deploy this app to Jekyo by running: 

`jekyo deploy`

After a while, you should see something like this:

```
➜  Fetching source code ... OK
➜  Building application, this might take a while ... OK
➜  Publishing application, this might take a while  ... OK
➜  Deploying application ... OK        
➜  Waiting for application to start ... OK
➜  Visit your app on: https://express-on-jekyo.jekyo.app ... OK
```

You can now browse to your Express app on https://express-on-jekyo.jekyo.app (replace 'express-on-jekyo' with your app name)

## Method 2

Clone the Jekyo repository containing an Express app skeleton by running: 

```
git clone https://github.com/ink16/expressjs-getting-started.git
```

**Alternatively**, you can follow [these instructions](https://expressjs.com/en/starter/generator.html) to create the same app yourself using _express-generator_, or [these instructions](https://expressjs.com/en/starter/hello-world.html) to create a single page 'hello world' app. 

Navigate to the cloned repository:

`cd expressjs-getting-started`

### Deploy the Express app on Jekyo

`jekyo create`

Select 'none' using the **arrows** on your keyboard and press **enter**. This will create an app using your current directory. 
```
? Select template (Use arrow keys)
❯ None Creates only the application
```

Name your app: 

`Application name?: express-on-jekyo`

Run `jekyo link` to link your local app to the remote Jekyo app. Select 'express-on-jekyo' using the **arrows** on your keyboard and press **enter**.

```
? Select application (Use arrow keys)
❯ express-on-jekyo
```

Now you can deploy this app to Jekyo by running: 

`jekyo deploy`

After a while, you should see something like this:

```
➜  Fetching source code ... OK
➜  Building application, this might take a while ... OK
➜  Publishing application, this might take a while  ... OK
➜  Deploying application ... OK        
➜  Waiting for application to start ... OK
➜  Visit your app on: https://express-on-jekyo.jekyo.app ... OK
```

You can now browse to your Express app on https://express-on-jekyo.jekyo.app (replace 'express-on-jekyo' with your app name)

## Pushing local changes to Jekyo 

Add the newly modified file(s) to the git index by using [git add](https://www.atlassian.com/git/tutorials/saving-changes)

`git add`

Create a [git commit](https://github.com/git-guides/git-commit)

`git commit -m "your commit message"`

Now, simply deploy your app again:

`jekyo deploy`

You will see your changes on your live app after a short while. 

