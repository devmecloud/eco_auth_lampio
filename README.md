
# Serverless Framework Node HTTP API on AWS

## Step 1 : Clone source code

```
git clone https://github.com/devmecloud/eco_auth_lampio.git authServices
cd authServices
```

## Step 2 : Create app in Cognito AWS
Link : https://us-east-1.console.aws.amazon.com/cognito/v2/idp/set-up-your-application?region=ap-northeast-1
- Action create app with ``` application type ``` is ``` mobile``` in cognito

![image](https://github.com/user-attachments/assets/34fa750c-a479-460b-b942-bd8cf5c5f97a)


- And move to that link : http://us-east-1.console.aws.amazon.com/cognito/v2/idp/user-pools/ap-northeast-1_i4fGZtp92/applications/app-clients/7tm0cfs0nqidq5a7qg1t6egu10/quick-setup-guide?region=ap-northeast-1

![image](https://github.com/user-attachments/assets/e89db14f-f8b0-406f-be1f-eb272f7f4f8d)


- Copy ``` Client ID ``` change ```replace all``` in all source

![image](https://github.com/user-attachments/assets/47030cf2-c96d-4bdc-bd4d-70cec9e74ca6)


## Step 3 : Install package

```
npm install
```
## Step 4 : Two case

### If you run local then
```
aws configure
AWS Access Key ID [****************]: your_key
AWS Secret Access Key [****************]: your_key
Default region name [us-east-1]: us-east-1
Default output format [json]: json
```

```
cd authServices
sls deploy
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


### If you want push code on your github

```
Setting key aws in github
```


![image](https://github.com/user-attachments/assets/a9e868c0-3492-4256-840c-94be512afa8d)


```
cd authServices
rm rf .git
git init
git remote add origin your_link_github
git add .
git commit -m "Your commit"
git push origin master
```

After when push code, then check at Action in github


![image](https://github.com/user-attachments/assets/5390eebb-277a-4a79-b6de-e31a7403a1d3)


![image](https://github.com/user-attachments/assets/173dc476-d51d-46a2-8bd8-12c1f13523c4)



## Step 5 : Test function
- Check extension in vs code : https://marketplace.visualstudio.com/items?itemName=humao.rest-client
- Change link at attribute @host =  in file authService\test-rest-api\auh_services\regist_account.rest
- And action send request same below images

![image](https://github.com/user-attachments/assets/534add97-d81b-49dc-b2fd-7a0cfacd4f6b)



