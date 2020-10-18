# [AWS CDK](https://aws.amazon.com/cdk/) on Scala

A [Giter8](http://www.foundweekends.org/giter8/index.html) template for deploying a web application implemented by Scala to AWS Fargate.

## Usage

### Recommended requirements

+ JDK 11
+ Node.js 14.x
+ Docker 19.03.x

### 1. Create a project with `sbt new`.  

```
$ sbt new NomadBlacky/aws-cdk-scala_fargate-simple-web-app.g8
```

### 2. Install `aws-cdk` CLI with `npm install`.

```
$ cd your-created-repository
$ npm install
```

### 3. Deploy the infrastructure and application with `cdk deploy`.

```
$ npx cdk deploy

(When the deployment is successful)
 ✅  WebServerStack

Outputs:
WebServerStack.FargateLoadBalancerDNSXXXXXXXX = WebSe-Farga-XXXXXXXXXXCC-0123456789.ap-northeast-1.elb.amazonaws.com
WebServerStack.FargateServiceURLXXXXXXXX = http://WebSe-Farga-XXXXXXXXXXXX-0123456789.ap-northeast-1.elb.amazonaws.com
```

### 4. Check the deployed web application.

Open the URL of `WebServerStack.FargateServiceURLXXXXXXXX` in `Outputs`.

### 5. (Optional) Clean up the deployed web application.

```
$ npx cdk destroy
```
