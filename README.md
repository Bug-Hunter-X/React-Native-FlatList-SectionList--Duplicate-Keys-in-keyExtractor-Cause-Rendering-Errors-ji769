# React Native FlatList/SectionList: Duplicate Keys in keyExtractor Cause Rendering Errors

This repository demonstrates a common, yet often difficult-to-diagnose, bug in React Native's FlatList and SectionList components. The issue arises from providing a `keyExtractor` function that generates duplicate keys for different items in the data array. This leads to unpredictable rendering behavior, such as missing items or the same item being rendered multiple times.  The error messages are often non-specific and can be confusing to debug.

## Bug Reproduction

The `bug.js` file shows the incorrect implementation of `keyExtractor`, leading to duplicate keys. This will cause the FlatList to render incorrectly.

## Solution

The `bugSolution.js` file demonstrates the correct implementation of `keyExtractor`, ensuring that unique keys are generated for each item. This fixes the rendering issue.

## Key Learning

Always ensure that the `keyExtractor` function in React Native's FlatList and SectionList components generates unique keys for each item in the data array.  Using a unique identifier like a UUID is a safe approach if your data doesn't have such a field.