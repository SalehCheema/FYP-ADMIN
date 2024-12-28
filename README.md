                                                                                                  
                                   WELCOME TO [E-COMMERCE ADMIN PANEL]                                            
                                                                                                  
    Greetings,                                                                                    
                                                                                                  
    We extend our sincere appreciation for your interest in [T_Admin_Panel]. This repository            
    houses a robust e-commerce solution developed using the Flutter framework. Every line         
    of code here reflects our commitment to quality, efficiency, and scalability.                 
                                                                                                  
    We're dedicated to continuous improvement and we welcome feedback to make this                
    solution even more industry-leading. Dive in, explore, and let's innovate together.           
                                                                                                  
    Regards,                                                                                      
    Coding with T                                                                                 


### E-COMMERCE ADMIN PANEL 

This project is a comprehensive solution for managing various aspects of an e-commerce platform, including user management, product catalog, orders, media storage, and more.
Table of Contents

    Introduction
    Installation
    Configuration
    Usage
    Error Handling
    Deployment
    Support
    Contributing
    License

# Introduction
The project aims to provide a robust backend infrastructure for e-commerce applications, offering functionalities such as user authentication, product management, order processing, media storage, and more. It is built using Flutter for cross-platform compatibility and Firebase for backend services.
Developed by Coding with T, a leading software development company specializing in Flutter and Firebase solutions.

# Installation
To install and run this project locally, follow these steps:

    Clone the repository:
    bash


## Navigate to the project directory:
    cd projectname

## Install dependencies:
    flutter pub get

## Configuration
Before running the project, you need to configure Firebase services and set up environment variables:

    Create a Firebase project on the Firebase Console.
    Add your Flutter app to the Firebase project.
    Download and add the google-services.json file to your Flutter project's android/app directory.
    Enable Firebase services such as Authentication, Firestore, Storage, etc., as per your project requirements.
    Configure any necessary environment variables, API keys, or authentication tokens in your Flutter project.

# Usage
To use this project, follow these steps:

    Run the development server:
    flutter run
    Access the app on your preferred device or emulator.
    Use the app to manage users, products, orders, and other aspects of your e-commerce platform.

# Error Handling
While using the project, you may encounter the following errors:

    404 Not Found: This error occurs when the requested resource is not found. Ensure that the URL is correct and the resource exists.
    500 Internal Server Error: This error indicates a problem with the server. Check server logs for more information and try again later.
    Network Errors: Errors related to network connectivity issues. Verify internet connection and try again.
    Cross-Origin Resource Sharing (CORS) Errors: Occurs when making requests to a different domain. Configure CORS settings on the server or use a proxy.


    1. Target of URI doesn't exist: 'dart:html'

    This error occurs when you try to use dart:html library in a Flutter web project. However, dart:html is not supported in Flutter web. Instead, you should use the dart:html equivalent libraries provided by Flutter web.
    Solution: Use the dart:html equivalent libraries provided by Flutter web, such as dart:ui, html, and package:flutter/material.dart.

    2. Unsupported operation: Platform views are not supported.

    This error occurs when you try to use platform views, such as WebView, in a Flutter web project. However, platform views are not supported in Flutter web.
    Solution: Use Flutter web-specific packages for web views, such as flutter_inappwebview or webview_flutter.

    3. Failed assertion: line 1785 pos 12: 'owner._debugCurrentBuildTarget == this': is not true.

    This error occurs when you try to use a widget that is not designed to be used in a web project.
    Solution: Use widgets that are designed to be used in a web project, such as HtmlElementView, InteractiveViewer, and MouseRegion.

    4. Unhandled Exception: Null check operator used on a null value

    This error occurs when you try to access a null value using the ! operator.
    Solution: Always check if a value is null before using the ! operator. You can use the?. operator to safely access nullable values.

    5. Unhandled Exception: Concurrent modification during iteration: Instance of 'List<dynamic>'

    This error occurs when you try to modify a list while iterating over it.
    Solution: Use the List.asMap() method to iterate over a list and modify it at the same time.

    6. Unhandled Exception: NoSuchMethodError: The method '[]' was called on null.

    This error occurs when you try to access an index of a null list.
    Solution: Always check if a list is null before accessing its index. You can use the ?. operator to safely access nullable lists.

    7. Unhandled Exception: Failed assertion: line 1485 pos 12: 'data != null': is not true.

    This error occurs when you try to use a null ImageProvider with the Image widget.
    Solution: Always check if an ImageProvider is null before using it with the Image widget. You can use the ?. operator to safely access nullable ImageProviders.

    8. Unhandled Exception: type 'String' is not a subtype of type 'int' of 'index'

    This error occurs when you try to access an index of a string using an integer.
    Solution: Always convert an integer to a string before using it as an index of a string. You can use the .toString() method to convert an integer to a string.

    9. Unhandled Exception: type 'double' is not a subtype of type 'int' of 'index'

    This error occurs when you try to access an index of a list using a double.
    Solution: Always convert a double to an integer before using it as an index of a list. You can use the .toInt() method to convert a double to an integer.



# Deployment

## Setup Firebase Project
https://youtu.be/91fmyvqBoEo?si=Rnl6xd6te04VOjEt

## Firebase Hosting

### Prerequisites
Before deploying to Firebase Hosting, ensure you have the following:

- Firebase account
- Firebase CLI installed (if not, install it using `npm install -g firebase-tools`)
- Initialize Firebase in your project directory:
- 
- Navigate to your project directory and run: 
- # Step 1
- Select Firebase services:
- During initialization, choose Firebase Hosting as the service you want to use. 
- 
- Build your project for production:
- Before deploying, build your Flutter project for production:
- 
- Deploy to Firebase Hosting:
- Once your project is built, deploy it to Firebase Hosting using the Firebase CLI:
- 
- Access your deployed website:
- Firebase will provide you with a hosting URL where your website is deployed. You can access it via the provided URL.



######  Steps
1. **Configure Firebase Project**:
   ```bash
   flutterfire configure
      
2. **Install the Firebase CLI**:
   ```bash
   npm install -g firebase-tools   
   
3. **Init the Firebase**:
   ```bash
   firebase init
   
- Are you ready to proceed? Yes
- Which Firebase features do you want to set up for this directory? Press Space to select features, then Enter to confirm your choices. (firestore, hosting(configure file), Storage)

- === Project Setup
- Please select an option: Use an existing project
- Select a default Firebase project for this directory: Enter

- === Firestore Setup
- What file should be used for Firestore Rules? firestore.rules (Enter)
- File firestore.rules already exists. Do you want to overwrite it with the Firestore Rules from the Firebase Console? Yes
- What file should be used for Firestore indexes? firestore.indexes.json (Enter)
- File firestore.indexes.json already exists. Do you want to overwrite it with the Firestore Indexes from the Firebase Console? Yes

- === Hosting Setup
- What do you want to use as your public directory? build/web
- Configure as a single-page app (rewrite all urls to /index.html)? Yes
- Set up automatic builds and deploys with GitHub? No

- === Storage Setup
- What file should be used for Storage Rules? storage.rules
- File storage.rules already exists. Overwrite? Yes

4. **Release the Build**:
   ```bash
   flutter build web --release --no-tree-shake-icons
   
5. **Deploy the Build**:
   ```bash
    firebase deploy --only hosting

6. **Register Admin**

- Go to lib => features => authentication => controller => login_controller.dart
- Copy function name registerAdmin()
- Go to lib => features => authentication => screens => login => widgets => login_form.dart
- Find ElevatedButton() in the end
- Replace controller.emailAndPasswordSignIn() with controller.registerAdmin()
- `Modify Admin Credentials`
- Go to lib => utils => constants => text_strings.dart
- Change adminEmail and adminPassword 
- `Sign In`
- Run the code and press `Sign In` button
- `Modify SignIn buttton function`
- After Logged in 
- Go to lib => features => authentication => screens => login => widgets => login_form.dart
- Find ElevatedButton() in the end
- Replace controller.registerAdmin() with controller.emailAndPasswordSignIn()

# cPanel
######  Steps

    Create a new website or addon domain in cPanel:
        Log in to your cPanel account.
        Navigate to the "Domains" section and click on "Addon Domains" or "Create a New Website".
        Follow the on-screen instructions to set up your domain.

    Upload your project files to the public_html directory:
        Use FTP or cPanel's File Manager to upload your Flutter project files to the public_html directory of your domain.

    Configure necessary settings and permissions:
        Ensure that file permissions are correctly set for your files and directories.
        Configure any server-side settings required by your Flutter project.

    Access your website via the domain name:
        Once the files are uploaded and configured, you can access your website using your domain name in a web browser.

###### Additional Notes

    Make sure your cPanel hosting environment supports Flutter projects. Some hosting providers may require specific configurations or support for running Flutter web applications.
    It's recommended to test your website thoroughly after deployment to ensure everything is working as expected.

Feel free to reach out if you encounter any issues or need further assistance with deployment.

# Support
   For support, please contact [support@codingwitht.com] or visit [https://codingwitht.com/].
   
# Contributing
   Contributions to this project are welcome! To contribute, please follow our contributing guidelines.

# License
   This project is licensed under the Coding with T.
