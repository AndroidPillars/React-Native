# 1.0.React Native

- React Native is a framework that builds a hierarchy of UI components to build the JavaScript code.
- It has a set of components for both iOS and Android platforms to build a mobile application with native look and feel.

# 1.1.React.js

- It is an open source JavaScript library to create user interfaces.
- Typically used for Web Development.
- ReactDOM.render(...) adds the web support.
- React itself is Platform agnostic.

# 1.2.DOM

 - DOM stands for Document Object Model. 
 - It is the structure representation of all nodes in HTML document. 
 - DOM provides a way for JavaScript to interact with every single node in an HTML document to manipulate it.

# 1.3.Why React Native

- With React Native Framework, you can render UI for both iOS and Android platforms.
- It is an open source framework, which could be compatible with other platforms like Windows or tvOS in the near future.
- React Native Development is comparatively simple, quick and efficient.
- React Native is a UI focused, which makes the apps load quickly and gives a smoother feel.
- Gaint Companies like Facebook, Instagram, Skype, Airbnb, Tesla, Walmart, Baidu Mobile and Bloomberg developed their apps using React Native Framework.

# 1.4.How React Native Works

 React Native is a seperate library which in the end is a collection of special React components it gives you, so a collection of components you can use in your React app and these components are special because React Native actually knows how to translate them, how to compile these components to native widgets for ios and Android. So React Native kind of is like React DOM, it knows how to talk to native platform, to Android and iOS and how to render native widgets and it gives a bunch of these widgets as React components so that you can build a user interface with these compilable components(i.e)you won't be able to use your regular divs and h1 and paragraph tags in React Native because there are no equivalents for that in Native Code. But beside giving you this components, React Native is a bit more than that, it also gives access to some native platform APIs, For example it helps us to use the device camera, common tasks you would want to do in Native Apps and in general React Native gives you to tools to connect javascript code to native platform code because you typically build a React Native app by mostly writting Javascript code or depending on the app you're building, by entirely writing Javascript. Now I say mostly, atleast that's a possibility because you can also write native code for iOS and Android and React Native gives you the tools to connect your Javascript code to that native code, though that's a bit more advanced and in many apps,You will never need that and therefore, React Native gives you full flexibility, it gives you a way of connecting Javascript to native code and it also gives you a lot of pre-built native features which are conveniently usable from inside your Javascript code. So if you then 
combine React Native and the features that gives you with React.js which knows how to update a user interface and how to control user 
interface, then you get everything you need to compile a real native mobile app and that's also what React Native gives you, it gives 
you everything you need to then take a Javascript code and compile that to a real native mobile app which you can ship to the App Store
for iOS and Google Play for Android. So you get a real native mobile app as a result at the end.

![look_behind](https://user-images.githubusercontent.com/48873155/75274660-3f78b480-5829-11ea-8470-8f613e8ae4a2.png)

__In Simple Terms,__
- A collection of "special" React components.
- Components compiled to Native Widgets.
- Native Platform APIs exposed to JavaScript.
- Connects Javascript and Native Platform Code.
- React.js + React Native = React Native Mobile Apps.

# 1.5.Behind the Scenes

- The JavaScript is the language we use to build React Native Apps.
- Here, Components are compiled to real native widgets, to real native elements, to real native code.
- JavaScript code where you manage your business logic will not be compiled. but, your views will be and that of course also means that 
you typically get a great performance when building React Native Apps.

![behind_scenes](https://user-images.githubusercontent.com/48873155/75210593-81f9ad00-57a7-11ea-8851-f21956cc0907.png)

# 1.6.Comparing React Components with other Platforms

![comparsion](https://user-images.githubusercontent.com/48873155/75272318-a85d2e00-5823-11ea-845c-8bd16ce853b4.png)

# 1.6.Learning React Native

- Getting started with React Native apps can be really hard work.
- Generally, expo makes working with React Native pretty simple and fun but it's important to understand.
- In React Native as a developer, we have to find out on which platform our code is running and then
adjust our styles and logic according to that platform.
- In React Native we have very little cross-platform styling of components -> So, We have to Style components on our own style or use third-party libraries.
- Only we have only a basic set of pre-built components -> So, We have to build components on our own or 
use third-party libraries.
- For Creating responsive designs where our app looks good on different device sizes and Orientations -> So, We have to write code that is flexible(i.e)Create responsive designs on our own.

# 1.7.Drawbacks

- New Versions every month.
- Breaking changes do happen.
- High Dependency on third-party packages that also change.
- Bugs/ Workarounds required.

# Requiremts

- JavaScript + React Knowledge

# Expo vs React Native CLI

- For Creating React Native app -> Two Options -> Expo CLI and React Native CLI.

# Expo CLI

- It is the third-party service which is completely free to use.
- It gives you a kind of "Managed App Development" work flow.
- Lots of Convenience & Utility Features: Simplifies Development.
- Adds in a ton of default config to use features common in apps, like icons, videos, better camera use, etc
- But, you are limited to the Expo Ecosystem.

# Advantages

- Setting up a project is easy and can be done in minutes
- You (and other people) can open the project while you're working on it
- Sharing the app is easy (via QR-code or link), you don't have to send the whole .apk or .ipa file
- No build necessary to run the app
- Integrates some basic libraries in a standard project (Push Notifications, Asset Manager,...)
- You can eject it to ExpoKit and integrate native code continuing using some of the Expo features, but not all of them
- Expo can build .apk and .ipa files (distribution to stores possible with Expo)

# Disadvantages

- You can't add native modules (probably a gamechanger for some)
- You can't use libraries that use native code in Objective-C/Java
- The standard Hello World app is about 25MB big (because of the integrated libraries)
- If you want to use: FaceDetector, ARKit o Payments you need to eject it to ExpoKit
- Ejecting it to ExpoKit has a trade-off of features of Expo, e.g. you cannot share via QR code
- When ejecting to ExpoKit you are limited to the react native version that is supported by ExpoKit at that point in time
- Debugging in ExpoKit (with native modules) is a lot more complicated, since it mixes two languages and different libraries (no official Expo support anymore)

# React Native CLI

- React Native CLI was managed by React Native Team and React Native community.
- Bare-bone Development, which means you get a native app, you need to install Android Studio and Xcode to build that app and you need
to configure and manage a lot on your own.
- Almost no Convenience or Utility Freatures(i.e) If you wanna to use some native device features like device camera, adding third party packages where the set up is quite complex.
- Defualt CLI to generate a project. Requires a lot of work to add in common Features.

# Advantages

- You can add native modules written in Java/Objective-C (probably the strongest feature)
- You will be having control over the builds.

# Disadvantages:

- Needs Android Studio and XCode to run the projects
- You can't develop for iOS without having a mac
- Device has to be connected via USB to use it for testing
- Fonts need to be imported manually in XCode
- If you want to share the app you need to send the whole .apk / .ipa file
- Does not provide JS APIs out of the box, e.g. Push-Notifications, Asset Manager, they need to be manually installed and linked with npm for example
- Setting up a working project properly (inlcuding device configuration) is rather complicated and can take time.

# Installation

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

# Documentation References

- https://expo.io/learn
- https://facebook.github.io/react-native/docs/getting-started

# Tools References

- https://git-scm.com/
- https://www.yelp.com/fusion



# Points to get Remember

```ruby
expo start		-> Start the Project
expo start --android	-> Start the Project in Android
```
- Visual Studio Code -> File -> Preferences -> Color Theme -> For Setting Theme
- View -> Extensions -> Material Icon Theme -> Install


# Common Errors

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
