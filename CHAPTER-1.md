# React Native

## What is React Native?

- React Native is a seperate library which gives you a collection of special react components.
- React Native compiles these components to native widgets for Android and IOS.
- We can build Application in Android and IOS with single code base using JavaScript.

## React.js

- It is an open source JavaScript library to create user interfaces.
- Typically used for Web Development.
- ReactDOM.render(...) adds the web support.
- React itself is Platform agnostic.

# 1.2.DOM

 - DOM stands for Document Object Model. 
 - It is the structure representation of all nodes in HTML document. 
 - DOM provides a way for JavaScript to interact with every single node in an HTML document to manipulate it.

## Why React Native?

- Using React Native Framework, you can render UI for both iOS and Android platforms.
- It is an open source framework, which could be compatible with other platforms like Windows or tvOS in the near future.
- React Native Development is comparatively simple, quick and efficient.
- React Native is a UI focused, which makes the apps load quickly and gives a smoother feel.
- Gaint Companies like Facebook, Instagram, Skype, Airbnb, Tesla, Walmart, Baidu Mobile and Bloomberg developed their apps using React Native Framework.

## How React Native Works?

- React Native compiles special react components to native views but all the other javascript code where you manage your business logic is not compiled in to         native code.

![look_behind](https://user-images.githubusercontent.com/48873155/75274660-3f78b480-5829-11ea-8470-8f613e8ae4a2.png)


## Comparing React Components with other Platforms

![comparsion (1)](https://user-images.githubusercontent.com/48873155/75276479-39380780-582c-11ea-82f3-80b7c7b14320.png)

# 1.7.Learning React Native

- Getting started with React Native apps can be really hard work.
- Generally, expo makes working with React Native pretty simple and fun but it's important to understand.
- In React Native as a developer, we have to find out on which platform our code is running and then
adjust our styles and logic according to that platform.
- In React Native we have very little cross-platform styling of components -> So, We have to Style components on our own style or use third-party libraries.
- Only we have only a basic set of pre-built components -> So, We have to build components on our own or 
use third-party libraries.
- For Creating responsive designs where our app looks good on different device sizes and Orientations -> So, We have to write code that is flexible(i.e)Create responsive designs on our own.

# 1.8.Drawbacks

- New Versions every month.
- Breaking changes do happen.
- High Dependency on third-party packages that also change.
- Bugs/ Workarounds required.

# 1.9.Requirements

- JavaScript + React Knowledge

## Expo vs React Native CLI

- For Creating React Native app -> Two Options -> Expo CLI and React Native CLI.

## Expo CLI

- It is the third-party service which is completely free to use.
- It gives you a kind of "Managed App Development" work flow.
- Lots of Convenience & Utility Features: Simplifies Development.
- Adds in a ton of default config to use features common in apps, like icons, videos, better camera use, etc
- But, you are limited to the Expo Ecosystem.

![expo_works](https://user-images.githubusercontent.com/48873155/75275942-4accdf80-582b-11ea-91b5-1279381eda62.png)

## Advantages

- Setting up a project is easy and can be done in minutes
- You (and other people) can open the project while you're working on it
- Sharing the app is easy (via QR-code or link), you don't have to send the whole .apk or .ipa file
- No build necessary to run the app
- Integrates some basic libraries in a standard project (Push Notifications, Asset Manager,...)
- You can eject it to ExpoKit and integrate native code continuing using some of the Expo features, but not all of them
- Expo can build .apk and .ipa files (distribution to stores possible with Expo)

## Disadvantages

- You can't add native modules (probably a gamechanger for some)
- You can't use libraries that use native code in Objective-C/Java
- The standard Hello World app is about 25MB big (because of the integrated libraries)
- If you want to use: FaceDetector, ARKit o Payments you need to eject it to ExpoKit
- Ejecting it to ExpoKit has a trade-off of features of Expo, e.g. you cannot share via QR code
- When ejecting to ExpoKit you are limited to the react native version that is supported by ExpoKit at that point in time
- Debugging in ExpoKit (with native modules) is a lot more complicated, since it mixes two languages and different libraries (no official Expo support anymore)

## React Native CLI

- React Native CLI was managed by React Native Team and React Native community.
- Bare-bone Development, which means you get a native app, you need to install Android Studio and Xcode to build that app and you need
  to configure and manage a lot on your own.
- Almost no Convenience or Utility Freatures(i.e) If you wanna to use some native device features like device camera, adding third party packages where the set up   is quite complex.
- Defualt CLI to generate a project. 
- Requires a lot of work to add in common Features.

# Advantages

- You can add native modules written in Java/Objective-C (probably the strongest feature)
- You will be having control over the builds.

# Disadvantages

- Needs Android Studio and XCode to run the projects.
- You can't develop for iOS without having a mac.
- Device has to be connected via USB to use it for testing.
- Fonts need to be imported manually in XCode.
- If you want to share the app you need to send the whole .apk / .ipa file.
- Does not provide JS APIs out of the box, e.g. Push-Notifications, Asset Manager, they need to be manually installed and linked with npm.
- For example Setting up a working project properly (inlcuding device configuration) is rather complicated and can take time.

# 1.11.Installation

For Windows,

- Visit			-> https://expo.io/learn
- Install Node		-> https://nodejs.org/en/download/
- Cmd Prompt		-> __For Windows,__ npm install expo-cli --global __and For Mac__, sudo npm install expo-cli --global
- Required Folder 	-> Open Cmd Prompt -> expo init my-new-project -> Choose a template: expo-template-blank
- Enter the name as my-new-project ->  Use Yarn to install dependencies -> n (It will ask only for the First time)
- Project path		-> Cmd Prompt -> npm start
- In Mobile Device	-> Download Expo app from playstore -> Scan the QR Code
- ctrl+c			-> Close
- Now Install Visual Studio Code -> https://code.visualstudio.com/

# 1.12.Documentation References

- https://expo.io/learn
- https://facebook.github.io/react-native/docs/getting-started

# 1.13.Tools References

- https://git-scm.com/
- https://www.yelp.com/fusion



# 1.14.Points to get Remember

```ruby
expo start		-> Start the Project
expo start --android	-> Start the Project in Android
```
- Visual Studio Code -> File -> Preferences -> Color Theme -> For Setting Theme
- View -> Extensions -> Material Icon Theme -> Install


# 1.15.Common Errors

- warn Package react-native-gesture-handler has been ignored because it contains invalid configuration. Cannot find module 'react-native-gesture-handler\package.json',
```ruby
npm uninstall react-native-gesture-handler --save
npm install react-native-gesture-handler --save
```
- npm ERR! code ENOENT npm ERR! syscall spawn git npm ERR! path git,

Have to Install the Git

- Found 15 vulnerabilities
```ruby
npm audit fix --force
```
- For adding Navigation,

```ruby
expo install react-navigation react-native-gesture-handler@1.3.0 react-native-reanimated react-native-screens react-navigation-stack react-native-safe-area-context @react-native-community/masked-view
```
