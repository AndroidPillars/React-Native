# 3.0.Working with StyleSheet, Text, View, TextInput, Button, ScrollView and useState  

__Read the Documentation in__
- https://reactnative.dev/docs/components-and-apis

```ruby
import React, { useState } from "react";
import {
  StyleSheet,
  Text,
  View,
  TextInput,
  Button,
  ScrollView
} from "react-native";

export default function App() {
  const [enteredGoal, setEnteredGoal] = useState("");
  const [courseGoals, setCourseGoals] = useState([]);

  // Normal Function
  // function goalInputHandler(enteredText) {
  //   setEnteredGoal(enteredText);
  // }

  //Arrow Function
  const goalInputHandler = enteredText => {
    setEnteredGoal(enteredText);
  };

  const addGoalHandler = () => {
    setCourseGoals([...courseGoals, enteredGoal]);
  };

  return (
    <View style={styles.screen}>
      <View style={styles.container}>
        <TextInput
          style={styles.input}
          placeholder="Course Goal"
          onChangeText={goalInputHandler}
          value={enteredGoal}
        />
        <Button title="ADD" onPress={addGoalHandler} />
      </View>
      <ScrollView showsVerticalScrollIndicator={false}>
        {courseGoals.map(goal => (
          <View key={goal} style={styles.listItem}>
            <Text>{goal}</Text>
          </View>
        ))}
      </ScrollView>
    </View>
  );
}

const styles = StyleSheet.create({
  screen: {
    padding: 50.0
  },
  container: {
    flexDirection: "row",
    justifyContent: "space-between",
    alignItems: "center"
  },
  input: {
    width: "80%",
    borderColor: "black",
    borderWidth: 1,
    padding: 10
  },
  listItem: {
    padding: 10.0,
    marginVertical: 10.0,
    backgroundColor: "#ccc",
    borderColor: "black",
    borderWidth: 1
  }
});

```
# Working with FlatList

- The FlatList component displays the similar structured data in a scrollable list. 
- It works well for large lists of data where the number of list items might change over time. 
- The FlatList shows only those renders elements which are currently displaying on the screen, not all the elements of the list at once.
- The FlatList component takes two required props: data and renderItem.
- The data is the source of elements for the list, and renderItem takes one item from the source and returns a formatted component to render.
__Read the Documentation in__ https://reactnative.dev/docs/components-and-apis

```ruby
import React, { useState } from "react";
import {
  StyleSheet,
  Text,
  View,
  TextInput,
  Button,
  ScrollView,
  FlatList
} from "react-native";

export default function App() {
  const [enteredGoal, setEnteredGoal] = useState("");
  const [courseGoals, setCourseGoals] = useState([]);

  // Normal Function
  // function goalInputHandler(enteredText) {
  //   setEnteredGoal(enteredText);
  // }

  //Arrow Function
  const goalInputHandler = enteredText => {
    setEnteredGoal(enteredText);
  };

  const addGoalHandler = () => {
    setCourseGoals([...courseGoals, {id: Math.random().toString, value: enteredGoal}]);
  };

  return (
    <View style={styles.screen}>
      <View style={styles.container}>
        <TextInput
          style={styles.input}
          placeholder="Course Goal"
          onChangeText={goalInputHandler}
          value={enteredGoal}
        />
        <Button title="ADD" onPress={addGoalHandler} />
      </View>
      <FlatList
      keyExtractor = {(item, index) => item.id}
        data={courseGoals}
        renderItem={itemData => (
          <View style={styles.listItem}>
            <Text>{itemData.item.value}</Text>
          </View>
        )}
      />
    </View>
  );
}

const styles = StyleSheet.create({
  screen: {
    padding: 50.0
  },
  container: {
    flexDirection: "row",
    justifyContent: "space-between",
    alignItems: "center"
  },
  input: {
    width: "80%",
    borderColor: "black",
    borderWidth: 1,
    padding: 10
  },
  listItem: {
    padding: 10.0,
    marginVertical: 10.0,
    backgroundColor: "#ccc",
    borderColor: "black",
    borderWidth: 1
  }
});

```
