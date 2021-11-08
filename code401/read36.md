# Code 401 - Reading Notes

<!-- All references used were from Code 401 reading
assignment 36 -->

[comment]: <> (https://docs.amplify.aws/lib/auth/getting-started/q/platform/android/)

## Amplify and Cognito
The Amplify Auth category provides an interface for authenticating a user. t comes with default, built-in support for Amazon Cognito User Pool and Identity Pool.


### Setup
To start provisioning auth resources in the backend, go to your project directory and execute the command:
`amplify add auth`. 

```aidl
? Do you want to use the default authentication and security configuration?
    `Default configuration`
? How do you want users to be able to sign in?
    `Username`
? Do you want to configure advanced settings?
    `No, I am done.`
```

And then `amplify push` to sync to the cloud.


Add the dependency `implementation 'com.amplifyframework:aws-auth-cognito:1.28.3'`

Update code to reflect:

```aidl
// Add this line, to include the Auth plugin.
Amplify.addPlugin(new AWSCognitoAuthPlugin());
Amplify.configure(getApplicationContext());
```

Test in MainActivity's `onCreate()`:
```aidl
Amplify.Auth.fetchAuthSession(
    result -> Log.i("AmplifyQuickstart", result.toString()),
    error -> Log.e("AmplifyQuickstart", error.toString())
);
```

### Signup

The default CLI flow as mentioned in the getting started guide requires a username, password and a valid email id as parameters to register a user.

```aidl
AuthSignUpOptions options = AuthSignUpOptions.builder()
    .userAttribute(AuthUserAttributeKey.email(), "my@email.com")
    .build();
Amplify.Auth.signUp("username", "Password123", options,
    result -> Log.i("AuthQuickStart", "Result: " + result.toString()),
    error -> Log.e("AuthQuickStart", "Sign up failed", error)
);
```

#### Confirm and then SignIn User

[BACK TO HOME](../README.md)