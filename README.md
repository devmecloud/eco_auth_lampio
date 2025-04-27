# Serverless Framework Node HTTP API on AWS

### Deployment

In order to deploy the example, you need to run the following command:

```
serverless deploy
```

After running deploy, you should see output similar to:

```
Deploying "authService" to stage "dev" (us-east-1)

✔ Service deployed to stack authService-dev  (91s)

endpoints:
  POST - https://s717qokuwe.execute-api.us-east-1.amazonaws.com/signUp
  POST - https://s717qokuwe.execute-api.us-east-1.amazonaws.com/confirmSignUp
  POST - https://s717qokuwe.execute-api.us-east-1.amazonaws.com/sign-in
functions:
  signUp: authService-dev-signUp (2.9 MB)
  confirmSignUp: authService-dev-confirmSignUp (2.9 MB)
  signIn: authService-dev-signIn (2.9 MB)
```
