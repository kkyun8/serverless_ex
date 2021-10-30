# serverless helloworld


aws lambda（node.js） serverless例

* 参考URL
  * https://serverless.co.jp/blog/25/
  * https://qiita.com/katsuhiko/items/de971929ffa750ec9b62





## deploy log

* 必要なIAM権限が多すぎて、管理者権限で実行した。


```bash
Serverless: Packaging service...
Serverless: Excluding development dependencies...
Serverless: Uploading CloudFormation file to S3...
Serverless: Uploading artifacts...
Serverless: Uploading service serverless-ex.zip file to S3 (847 B)...
Serverless: Validating template...
Serverless: Updating Stack...
Serverless: Checking Stack update progress...
CloudFormation - UPDATE_IN_PROGRESS - AWS::CloudFormation::Stack - serverless-ex-dev
CloudFormation - CREATE_IN_PROGRESS - AWS::ApiGateway::RestApi - ApiGatewayRestApi
CloudFormation - CREATE_IN_PROGRESS - AWS::Logs::LogGroup - HelloHogeLogGroup
CloudFormation - CREATE_IN_PROGRESS - AWS::IAM::Role - IamRoleLambdaExecution
CloudFormation - CREATE_IN_PROGRESS - AWS::Logs::LogGroup - HelloLogGroup
CloudFormation - CREATE_IN_PROGRESS - AWS::ApiGateway::RestApi - ApiGatewayRestApi
CloudFormation - CREATE_IN_PROGRESS - AWS::IAM::Role - IamRoleLambdaExecution
CloudFormation - CREATE_COMPLETE - AWS::ApiGateway::RestApi - ApiGatewayRestApi
CloudFormation - CREATE_IN_PROGRESS - AWS::Logs::LogGroup - HelloHogeLogGroup
CloudFormation - CREATE_COMPLETE - AWS::Logs::LogGroup - HelloHogeLogGroup
CloudFormation - CREATE_IN_PROGRESS - AWS::Logs::LogGroup - HelloLogGroup
CloudFormation - CREATE_COMPLETE - AWS::Logs::LogGroup - HelloLogGroup
CloudFormation - CREATE_IN_PROGRESS - AWS::ApiGateway::Resource - ApiGatewayResourceHello
CloudFormation - CREATE_IN_PROGRESS - AWS::ApiGateway::Resource - ApiGatewayResourceHello
CloudFormation - CREATE_COMPLETE - AWS::ApiGateway::Resource - ApiGatewayResourceHello
CloudFormation - CREATE_IN_PROGRESS - AWS::ApiGateway::Resource - ApiGatewayResourceHelloNameVar
CloudFormation - CREATE_IN_PROGRESS - AWS::ApiGateway::Method - ApiGatewayMethodHelloOptions
CloudFormation - CREATE_IN_PROGRESS - AWS::ApiGateway::Method - ApiGatewayMethodHelloOptions
CloudFormation - CREATE_COMPLETE - AWS::ApiGateway::Method - ApiGatewayMethodHelloOptions
CloudFormation - CREATE_IN_PROGRESS - AWS::ApiGateway::Resource - ApiGatewayResourceHelloNameVar
CloudFormation - CREATE_COMPLETE - AWS::ApiGateway::Resource - ApiGatewayResourceHelloNameVar
CloudFormation - CREATE_IN_PROGRESS - AWS::ApiGateway::Method - ApiGatewayMethodHelloNameVarOptions
CloudFormation - CREATE_IN_PROGRESS - AWS::ApiGateway::Method - ApiGatewayMethodHelloNameVarOptions
CloudFormation - CREATE_COMPLETE - AWS::ApiGateway::Method - ApiGatewayMethodHelloNameVarOptions
CloudFormation - CREATE_COMPLETE - AWS::IAM::Role - IamRoleLambdaExecution
CloudFormation - CREATE_IN_PROGRESS - AWS::Lambda::Function - HelloHogeLambdaFunction
CloudFormation - CREATE_IN_PROGRESS - AWS::Lambda::Function - HelloLambdaFunction
CloudFormation - CREATE_IN_PROGRESS - AWS::Lambda::Function - HelloHogeLambdaFunction
CloudFormation - CREATE_IN_PROGRESS - AWS::Lambda::Function - HelloLambdaFunction
CloudFormation - CREATE_COMPLETE - AWS::Lambda::Function - HelloHogeLambdaFunction
CloudFormation - CREATE_COMPLETE - AWS::Lambda::Function - HelloLambdaFunction
CloudFormation - CREATE_IN_PROGRESS - AWS::Lambda::Version - HelloHogeLambdaVersion0tdV1mIWnndksaKEu81MllGFaAV5mjnHFLjPts9E
CloudFormation - CREATE_IN_PROGRESS - AWS::Lambda::Version - HelloLambdaVersionGfI6Tqh27VxmFgFVqVVMxxkXoaae9zkEdMWS4f0ji5Q
CloudFormation - CREATE_IN_PROGRESS - AWS::Lambda::Permission - HelloHogeLambdaPermissionApiGateway
CloudFormation - CREATE_IN_PROGRESS - AWS::Lambda::Permission - HelloLambdaPermissionApiGateway
CloudFormation - CREATE_IN_PROGRESS - AWS::Lambda::Version - HelloHogeLambdaVersion0tdV1mIWnndksaKEu81MllGFaAV5mjnHFLjPts9E
CloudFormation - CREATE_IN_PROGRESS - AWS::Lambda::Permission - HelloHogeLambdaPermissionApiGateway
CloudFormation - CREATE_IN_PROGRESS - AWS::Lambda::Version - HelloLambdaVersionGfI6Tqh27VxmFgFVqVVMxxkXoaae9zkEdMWS4f0ji5Q
CloudFormation - CREATE_IN_PROGRESS - AWS::Lambda::Permission - HelloLambdaPermissionApiGateway
CloudFormation - CREATE_COMPLETE - AWS::Lambda::Version - HelloHogeLambdaVersion0tdV1mIWnndksaKEu81MllGFaAV5mjnHFLjPts9E
CloudFormation - CREATE_COMPLETE - AWS::Lambda::Version - HelloLambdaVersionGfI6Tqh27VxmFgFVqVVMxxkXoaae9zkEdMWS4f0ji5Q
CloudFormation - CREATE_COMPLETE - AWS::Lambda::Permission - HelloHogeLambdaPermissionApiGateway
CloudFormation - CREATE_COMPLETE - AWS::Lambda::Permission - HelloLambdaPermissionApiGateway
CloudFormation - CREATE_IN_PROGRESS - AWS::ApiGateway::Method - ApiGatewayMethodHelloGet
CloudFormation - CREATE_IN_PROGRESS - AWS::ApiGateway::Method - ApiGatewayMethodHelloNameVarGet
CloudFormation - CREATE_IN_PROGRESS - AWS::ApiGateway::Method - ApiGatewayMethodHelloGet
CloudFormation - CREATE_IN_PROGRESS - AWS::ApiGateway::Method - ApiGatewayMethodHelloNameVarGet
CloudFormation - CREATE_COMPLETE - AWS::ApiGateway::Method - ApiGatewayMethodHelloGet
CloudFormation - CREATE_COMPLETE - AWS::ApiGateway::Method - ApiGatewayMethodHelloNameVarGet
CloudFormation - CREATE_IN_PROGRESS - AWS::ApiGateway::Deployment - ApiGatewayDeployment1635599732742
CloudFormation - CREATE_IN_PROGRESS - AWS::ApiGateway::Deployment - ApiGatewayDeployment1635599732742
CloudFormation - CREATE_COMPLETE - AWS::ApiGateway::Deployment - ApiGatewayDeployment1635599732742
CloudFormation - UPDATE_COMPLETE_CLEANUP_IN_PROGRESS - AWS::CloudFormation::Stack - serverless-ex-dev
CloudFormation - UPDATE_COMPLETE - AWS::CloudFormation::Stack - serverless-ex-dev
Serverless: Stack update finished...
Service Information
service: serverless-ex
stage: dev
region: ap-northeast-1
stack: serverless-ex-dev
resources: 19
api keys:
  None
endpoints:
  GET - https://ap-northeast-1.amazonaws.com/dev/hello
  GET - https://ap-northeast-1.amazonaws.com/dev/hello/{name}
functions:
  hello: serverless-ex-dev-hello
  helloHoge: serverless-ex-dev-helloHoge
layers:
```
