# serverless-test

## Get Started

### Deploy to  serverless app and aws lambda

1. yarn run/ npm start
2. serverless deploy

### Deploy to other stages

If you want to deploy to different stage instead of using dev
- serverless deploy --stage "stage-name"

### Deploy offline for testing

1. yarn add -D serverless-offline/ npm install serverless-offline --save-dev

2. Edit serverless.yml

   - add plugins: serverless-offline

   - add events under each function

     ```
     ...
     plugins:
       - serverless-offline
     
     functions:
       hello:
         handler: handler.hello
         events:
           - http:
               path: /hello
               method: get
     ...
     ```

3. serverless offline

## Reference

[使用 Node.js + serverless framework + AWS Lambda 打造可擴展、更穩定而且更經濟的架構 | by 李至青 | Visually Lab | Medium](https://medium.com/visuallylab/使用-node-js-serverless-framework-aws-lambda-打造可擴展-更穩定而且更經濟的架構-6a54b51b8988)

[AWS Lambda Tutorial: Lambda + Serverless = HAPPY - YouTube](https://www.youtube.com/watch?v=71cd5XerKss)
