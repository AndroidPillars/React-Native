# React-Native

# Installation

# For Windows,

- Visit			-> https://expo.io/learn
- Install Node		-> https://nodejs.org/en/download/
- Cmd Prompt		-> npm install expo-cli --global
- Required Folder 	-> Open Cmd Prompt -> expo init my-new-project name -> Choose a template: expo-template-blank
- Project path		-> Cmd Prompt -> npm start
- In Mobile Device	-> Download Expo app from playstore -> Scan the QR Code
- ctrl+c			-> Close

# React Component File

- Part 1 -> Import library we need to create component

import React from "react";

import { Text, StyleSheet } from "react-native";

- Part 2 -> Create a component - function that returns some 'JSX'

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

- Part 3 -> Create a Style sheet to create our component.

const styles = StyleSheet.create({

  text: {
  
    fontSize: 30
    
  }  
  
});

- Part 4 -> Export the Component so that we caan use it else where in our project.

export default HomeScreen;

# Showing Custom Component

- Open App.js 
- import ComponentScreen from "./src/screens/ComponentScreen";

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

return (

    <View>
    
    <Text style={styles.text}>HelloWorld!!!</Text>
    
    {mTxtHello}
    
    </View>
    
    );
    
