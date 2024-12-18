# Dart reduce method throws an error if the list is empty

This repository contains a bug report and solution for a common error encountered when using the `reduce` method in Dart. The `reduce` method is a powerful tool for aggregating elements in a list, but it can throw an error if the list is empty. This repository demonstrates this error and provides a solution to handle empty lists gracefully.

## Bug Report

The following Dart code snippet throws an error if the list `numbers` is empty:

```dart
List<int> numbers = [];
int sum = numbers.reduce((a, b) => a + b);
print(sum); // Throws an error
```

## Solution

To handle this error, check if the list is empty before using the `reduce` method. If the list is empty, return a default value. For example, if you are summing the elements of the list, return 0 as the default value:

```dart
List<int> numbers = [];
int sum = numbers.isEmpty ? 0 : numbers.reduce((a, b) => a + b);
print(sum); // Output: 0
```
