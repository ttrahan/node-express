### Sample Node.js app deployment to Elastic Beanstalk

This example uses the sample Node.js application tutorial provided by Amazon [located
here](http://docs.aws.amazon.com/elasticbeanstalk/latest/dg/create_deploy_nodejs_express.html).

Instructions for using this sample:

1. **Fork this repo to your GitHub account**

1.  **Complete step 3 in the Amazon tutorial, "Configure Elastic Beanstalk"**
  * This will create a new Elastic Beanstalk application and environment for a
  sample Node.js application.

1.  **Update the file `.elasticbeanstalk/config.yml` with the application,
environment, and region you used in the previous step.**

1.  **Sign up or log in to your Shippable account (www.shippable.com)**

1.  **Enable the project for CI in Shippable**
  * [Instructions to enable your project](http://docs.shippable.com/ci_subscriptions/)

1.  **Add a Deploy Integration to your project for AWS**
  * This will allow AWS credentials stored in an Account Integration to be used for
  this deployment.
  * If you do not already have an Account Integration, create one with [these instructions](http://docs.shippable.com/int_overview/#adding-an-account-integration)
  * Assign the Account Integration to your project in the Deploy Integrations section of the [Project Settings page](http://docs.shippable.com/ci_projects/#enabling-integrations)

1.  **Make a change to the application code, commit and push it.**
  * For instance, change the title message on `routes/index.js`, commit it and
  push your change to your GitHub fork.


The push to GitHub will trigger a CI run on Shippable and execute the Instructions
in `shippable.yml`.  Upon a successful run, the new version of the app will be
deployed to Elastic Beanstalk.
