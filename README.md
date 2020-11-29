# aws-cognito-spa-demo

A simple Single Page App powering by Vue.js and securing by AWS Cognito (Provided Hosted UI).

## Project setup
```
yarn install
```

### Compiles and hot-reloads for development
```
yarn serve
```

### Compiles and minifies for production
```
yarn build
```

### Lints and fixes files
```
yarn lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

## Deploy Infrastructure
```
aws cloudformation deploy --stack-name my-stack --template-file iac/cognito.yaml --parameter-overrides AppName=my-app
```

### Update .env
Create a `.env.local` file at the root containing, replace with the values provided by the stack outputs:
```
VUE_APP_COGNITO_USERPOOL_ID=REGION_XXXXXX
VUE_APP_COGNITO_APP_DOMAIN=XXXXX.auth.REGION.amazoncognito.com
VUE_APP_COGNITO_CLIENT_ID=XXXXXXXXXXXXXXXXXXX
```

Then create a User inside the created User Pool within the Cognito AWS console and finally visit http://localhost:8080
