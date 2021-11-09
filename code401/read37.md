# Code 401 - Reading Notes

<!-- All references used were from Code 401 reading
assignment 37 -->

[comment]: <> (https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html)

[comment]: <> (https://docs.amplify.aws/lib/storage/getting-started/q/platform/android/)

## Simple Storage Service (S3)
Amazon Simple Storage Service (Amazon S3) is an object storage service that offers industry-leading scalability, data availability, security, and performance.

### Storage Classes

Amazon S3 offers a range of storage classes designed for different use cases. For example, you can store mission-critical production data in S3 Standard for frequent access, save costs by storing infrequently accessed data in S3 Standard-IA or S3 One Zone-IA, and archive data at the lowest costs in S3 Glacier and S3 Glacier Deep Archive.

You can store data with changing or unknown access patterns in S3 Intelligent-Tiering, which optimizes storage costs by automatically moving your data between four access tiers when your access patterns change.

### Data processing
To transform data and trigger workflows to automate a variety of other processing activities at scale, you can use the following features.

S3 Object Lambda – Add your own code to S3 GET requests to modify and process data as it is returned to an application. Filter rows, dynamically resize images, redact confidential data, and much more.

Event notifications – Trigger workflows that use Amazon Simple Notification Service (Amazon SNS), Amazon Simple Queue Service (Amazon SQS), and AWS Lambda when a change is made to your S3 resources.

### Access Points
Amazon S3 Access Points are named network endpoints with dedicated access policies that describe how data can be accessed using that endpoint. Access Points simplify managing data access at scale for shared datasets in Amazon S3. Access Points are named network endpoints attached to buckets that you can use to perform S3 object operations, such as GetObject and PutObject.

### AWS SDKs
AWS provides SDKs (software development kits) that consist of libraries and sample code for various programming languages and platforms (Java, Python, Ruby, .NET, iOS, Android, and so on). The AWS SDKs provide a convenient way to create programmatic access to S3 and AWS. Amazon S3 is a REST service. You can send requests to Amazon S3 using the AWS SDK libraries. which wrap the underlying Amazon S3 REST API and simplify your programming tasks. For example, the SDKs take care of tasks such as calculating signatures, cryptographically signing requests, managing errors, and retrying requests automatically.

### Amazon S3 REST API
The architecture of Amazon S3 is designed to be programming language-neutral, using AWS-supported interfaces to store and retrieve objects. You can access S3 and AWS programmatically by using the Amazon S3 REST API. The REST API is an HTTP interface to Amazon S3. With the REST API, you use standard HTTP requests to create, fetch, and delete buckets and objects.

To use the REST API, you can use any toolkit that supports HTTP. You can even use a browser to fetch objects, as long as they are anonymously readable.

The REST API uses standard HTTP headers and status codes, so that standard browsers and toolkits work as expected. In some areas, we have added functionality to HTTP (for example, we added headers to support access control). In these cases, we have done our best to add the new functionality in a way that matches the style of standard HTTP usage.

If you make direct REST API calls in your application, you must write the code to compute the signature and add it to the request.

### Getting Started
1. Run `amplify add storage`
2. Select:
```aidl
   ? Please select from one of the below mentioned services:
   `Content (Images, audio, video, etc.)`
   ? You need to add auth (Amazon Cognito) to your project in order to add storage for user files. Do you want to add auth now?
   `Yes`
   ? Do you want to use the default authentication and security configuration?
   `Default configuration`
   ? How do you want users to be able to sign in?
   `Username`
   ? Do you want to configure advanced settings?
   `No, I am done.`
   ? Please provide a friendly name for your resource that will be used to label this category in the project:
   `S3friendlyName`
   ? Please provide bucket name:
   `storagebucketname`
   ? Who should have access:
   `Auth and guest users`
   ? What kind of access do you want for Authenticated users?
   `create/update, read, delete`
   ? What kind of access do you want for Guest users?
   `create/update, read, delete`
   ? Do you want to add a Lambda Trigger for your S3 Bucket?
   `No`
```
3. Then, `amplify push` your changes.
4. Add to application build.gradle:
   1. `implementation 'com.amplifyframework:aws-storage-s3:1.28.3'`
   2. `implementation 'com.amplifyframework:aws-auth-cognito:1.28.3'`
5. Add to onCreate() of your application class:
   1. `Amplify.addPlugin(new AWSCognitoAuthPlugin());`
   2. `Amplify.addPlugin(new AWSS3StoragePlugin());`
6. Upload a file:
```aidl
Amplify.Storage.uploadFile(
"ExampleKey",
exampleFile,
result -> Log.i("MyAmplifyApp", "Successfully uploaded: " + result.getKey()),
storageFailure -> Log.e("MyAmplifyApp", "Upload failed", storageFailure)
```

[BACK TO HOME](../README.md)