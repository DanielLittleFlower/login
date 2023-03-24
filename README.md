# Login and Registration App (Flutter + Dart)
This is a Flutter-based mobile application that allows users to register an account and login. The app uses HTTP requests to communicate with a server-side API for authentication and registration purposes. The app uses the shared_preferences package to store user data locally.

## Features
The app has the following features:

1. A splash screen with the app logo displayed for 2 seconds before redirecting to the login screen.
2. A login screen that allows users to enter their email and password. The app checks the user's input against the API and logs in the user   if the input is correct. If the input is incorrect, an error message is displayed.
3. A two-step registration process that allows users to enter their name, email, password, and address. The app sends the user's data to the API for registration. If registration is successful, the user is logged in automatically. If registration fails, an error message is displayed.
4. A home screen that displays a welcome message to the user after successful login.
5. Google login integration that allows users to sign in to their account using their Google credentials.

## Prerequisites

1. Flutter SDK installed on your machine.
2. A server-side API that handles authentication and registration requests.
3. Basic knowledge of Flutter and Dart programming languages.
4. A Firebase app with Google Sign-In enabled. Follow the official [FlutterFire documentation](https://firebase.flutter.dev/docs/overview/) for instructions on how to set up Firebase for your app.

## Getting started

1. Clone the repository to your local machine using the following command:

`git clone https://github.com/DanielLittleFlower/simple-login-registration-flutter-dart.git`

2. Open the project in your preferred code editor.

3. Run `flutter pub get` to install the dependencies.

4. Update the API URL in `LoginScreen` and `RegisterScreen` classes to match your server-side API.

5. Run the app using `flutter run`.

## Usage
The app consists of three screens: `SplashScreen`, `LoginScreen`, and `RegisterScreen`.

## SplashScreen
The `SplashScreen` is the first screen that is displayed when the app is launched. The screen displays the app logo for 2 seconds and then redirects to the `LoginScreen`.

## LoginScreen
The `LoginScreen` allows users to enter their email and password to login to their account. The screen consists of two `TextField` widgets for email and password inputs, respectively, and a `RaisedButton` widget for submitting the form. If the user's input is incorrect, an error message is displayed using an 'AlertDialog'.

## RegisterScreen
The `RegisterScreen` allows new users to create an account. The registration process is divided into two steps:

Step 1
Users enter their `name`, `email`, and `password` in the first step of the registration process. The screen consists of three `TextField` widgets for name, email, and password inputs, respectively, and a `RaisedButton` widget for submitting the form. If all the required fields are filled, the user is taken to the second step of the registration process.

Step 2
Users enter their address in the second step of the registration process. The screen consists of one `TextField` widget for address input and two buttons: a Back button that takes the user back to the first step of the registration process and a Register button that registers the user by sending their information to the backend server. If registration is successful, the user is logged in automatically. If registration fails, an error message is displayed using an AlertDialog.

## HomePage
The `HomePage` is displayed after a successful login. The screen displays a welcome message to the user.

## Google Login Integration
The app also includes a Google login feature. Users can sign in to their account using their Google credentials. The following packages are used for the Google login integration:

`google_sign_in` package for signing in with Google.
`firebase_auth` package for handling authentication with Firebase.
`flutter_signin_button` package for displaying the Google sign-in button.

To use the Google login feature, the user can tap on the "Sign in with Google" button on the `LoginScreen`. 
The app will authenticate the user with Google and if successful, will sign in the user. 
Once signed in, the user will be redirected to the `HomePage`.

To use the Google login feature, you will need to set up Firebase for your app and add the `google-services.json` file to your project. 
For more information on how to set up Firebase for your Flutter app, refer to the official [FlutterFire documentation](https://firebase.flutter.dev/docs/overview/).

In addition, you will need to enable Google Sign-In for your Firebase project. Follow these steps to enable Google Sign-In for your Firebase project:

Go to the Firebase console and select your project.

1. In the left sidebar, click on "Authentication" and then select the "Sign-in method" tab.
2. Click on "Google" and then click on the "Enable" toggle.
3. Enter the authorized domains for your app (e.g., "myapp.com"). This is optional but highly recommended for security reasons.
4. Save your changes.
5. Once you have enabled Google Sign-In for your Firebase project, you can use the google_sign_in and firebase_auth packages in your Flutter app to handle authentication with Google. You can also use the flutter_signin_button package to display the Google sign-in button.

## Laravel Login and Registration API
For the server-side API that handles authentication and registration requests for this mobile application, please refer to the [Laravel Login and Registration API repository](https://github.com/DanielLittleFlower/login-registration-api)

### Contributing
Contributions are welcome! If you would like to contribute to this project, please fork the repository and submit a pull request.

### License
This project is licensed under the MIT License.
