# React-Native

# Installation

For Windows,

- Visit			-> https://expo.io/learn
- Install Node		-> https://nodejs.org/en/download/
- Cmd Prompt		-> npm install expo-cli --global
- Required Folder 	-> Open Cmd Prompt -> expo init my-new-project name -> Choose a template: expo-template-blank
- Project path		-> Cmd Prompt -> npm start
- In Mobile Device	-> Download Expo app from playstore -> Scan the QR Code
- ctrl+c			-> Close

# Reference Website

- https://expo.io/learn
- https://facebook.github.io/react-native/docs/getting-started
- https://git-scm.com/

# Commands to get Remember

```ruby
expo start		-> Start the Project
expo start --android	-> Start the Project in Android
```


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

# React Component File

- Part 1 -> Import library we need to create component

```ruby
import React from "react";
import { Text, StyleSheet } from "react-native";
```
- Part 2 -> Create a component - function that returns some 'JSX'

```ruby
Normal Function:

const HomeScreen = function() {
  return <Text style={styles.text}>HelloWorld!!!</Text>;
};

Arrow Function:

const HomeScreen = () => {
  return <Text style={styles.text}>HelloWorld!!!</Text>; 
};

Inline Style:

const HomeScreen = () => {
  return <Text style={{fontSize: 30}}>HelloWorld!!!</Text>;  
};


Note: Semicolon is not necessary.
```

- Part 3 -> Create a Style sheet to create our component.

```ruby
const styles = StyleSheet.create({
  text: {
    fontSize: 30 
  } 
});
```

- Part 4 -> Export the Component so that we caan use it else where in our project.
```ruby
export default HomeScreen;
```

# Showing Custom Component

- Open App.js 
- import ComponentScreen from "./src/screens/ComponentScreen";
```ruby
  const navigator = createStackNavigator(
  {
    Home: HomeScreen,
    Components: ComponentScreen 
  },
  {
    initialRouteName: "Components",
    defaultNavigationOptions: {
      title: "App"
    }
  }
);
```
# Common Questions and Answers

- Primitive Elements -> Text, View, Image and Button,.. etc..
- 'JSX' -> <Text style={styles.text}>HelloWorld!!!</Text> -> It passes in to the react native bundler that one is using a 
  tool called babel to convert that in to javascript code.

- Reference: https://babeljs.io/

- createStackNavigator -> It is a tool Which is used to navigates from one screen to another screen.
- StyleSheet.create -> To Style the primitive elements.

# Rules of JSX

- If we place a Text inside a View, we should remove the semicolon of Text widget.
- We can declare a string global and re-use that as, const mTxtHello = 'Hi, How are you?' -> <Text>{mTxtHello}</Text> similary for         array, boolean and int.
- Similarly,  const mTxtHello = <Text>'Hi, How are you?'</Text> -> {mTxtHello}

# Common Errors

```ruby
return (
    <View>
    <Text style={styles.text}>HelloWorld!!!</Text>
    {mTxtHello}
    </View>
    );
```
 or
```ruby
return <View>
    <Text style={styles.text}>HelloWorld!!!</Text>
    {mTxtHello}
    </View>
```
# BoilerPlate Code

```ruby
import React from "react";
import { Text, StyleSheet, View } from "react-native";

const ListScreen = ()=>{
return<Text>List Screen</Text>
}

const styles = StyleSheet.create({});

export default ListScreen;
```
# Building List

- primitive Element -> FlatList Element
- It take in a array of records and turn it in to some list and display
- Props -> Props are configuration options we specify when we write it out a JSX element.
- Two Props 
- 1. Data -> Array of data  so that it will turn in to a collection of elements to show on the Screen.
- 2. RenderItem -> Function that will turn each individual item in to an Element.
- Note: Behaviour with out a key being provided gives warning. 
- For that we have to assign a key which it must be a string and also it should be unique.

# Button

- It has self closing Tag

# Touchable Opacity(i.e) Customizable Component

- Alternative widgets to Button

# Props

- It has lot of properties which we can navigate from one screen to another From React Naivgation Stack 
Navigator to Required Screens. 
- In Other words system to pass data from a parent to child.
- Work Flow: React Naivgation Stack Navigator -> props -> Navigator to Required Screens 

# State

- System to track a piece of data that will change over time. If that data changes, our app will 'rerender'.

# Notes on State

- We are using function-based state in a functional component. React also has class based components that have to access state.
- We never modify a state variable . React doesn't detect the change, Only use the 'setter' function.
- We can name the state variable anything we wish.
- We can track any kind of data that changes over time - a number, string, array of objects, ect
- When a component is rendered, all of its children get renendered to.
- A state variable can be passed to a child component ! At that time, the state variable is being used as props.

# Layout Systems

# Box Object Model

- Properties like Border, Margin, Padding and the Width and Height of some element. We
use this to affect the positioning of single element.
- Content -> Padding -> Border -> Margin
- Height  -> paddingTop -> borderTopWidth -> marginTop
- For Parent -> alignItems, justifyContent and flexDirection
- Short Cuts -> margin, marginVertical, marginHorizontal, padding, paddingVertical, paddingHorizontal and borderWidth

# Flex Box

- The Flex Box system is considered from how we layout some number of child elements that has own number of common parent. We use this to position mulitple elements with a common parent. 
- For Child  -> flex, alignSelf

# Position

- How to position a element inside of a child. One single child inside of a parent. We use 
this to override Box object model + Flex Box
- Apply box object model Class -> Is position 'absolute'
- No -> Apply all flex box rules, Considering siblings -> place element inside parent -> Apply top, left, right and bottom
- Yes -> Apply some flex box rules, ignore all siblings -> Apply top, left, right and bottom


