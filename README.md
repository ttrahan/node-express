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

1.  **[Enable the project for CI] in Shippable (http://docs.shippable.com/ci_subscriptions/)**

1.  **Replace the secure variables in `shippable.yml` with your own AWS credentials**
  * Read the [instructions to encrypt your secure variables](http://docs.shippable.com/ci_configure/#secure-variables)
  * Encrypt the variables as follows:
    * AWS_ACCESS_KEY_ID=_enter your AWS access key id here_
    * AWS_SECRET_ACCESS_KEY=_enter your AWS secret access key here_

1.  **Make a change to the application code, commit and push it.**
  * For instance, change the title message on `routes/index.js`, commit it and
  push your change to your GitHub fork.


The push to GitHub will trigger a CI run on Shippable and execute the Instructions
in `shippable.yml`.  Upon a successful run, the new version of the app will be
deployed to Elastic Beanstalk.
