# 📘 Complete Guide to Lists, Data Types & Conditions in Dart

Your code is written in **Dart**, the programming language used mainly with **Flutter** for building mobile, web, and desktop apps.

---

# 1️⃣ The `main()` Function

```dart
void main() {
```

* `main()` is the **entry point** of every Dart program.
* The program starts running from here.
* `void` means this function does not return any value.

---

# 2️⃣ Data Types in Dart

Dart is a **strongly typed language**, which means every variable has a type.

### Common Data Types:

| Type     | Example    | Description          |
| -------- | ---------- | -------------------- |
| `int`    | 10         | Whole numbers        |
| `double` | 10.5       | Decimal numbers      |
| `String` | "Hello"    | Text                 |
| `bool`   | true/false | Boolean values       |
| `List`   | [1,2,3]    | Collection of values |

---

# 3️⃣ Understanding Lists in Dart

A **List** is a collection of ordered items.

### Example from your code:

```dart
List siblings_names = ["Faheem", "Abu bakar", "Najeeb"];
List<int> siblings_age = [23, 12, 34];
```

### 🔎 Difference Between These Two

#### ❌ Without Type (Not Recommended)

```dart
List siblings_names = ["Faheem", "Abu bakar", "Najeeb"];
```

* This is a **dynamic list**
* Can store any data type
* Not type-safe

#### ✅ With Type (Recommended)

```dart
List<String> siblings_names = ["Faheem", "Abu bakar", "Najeeb"];
List<int> siblings_age = [23, 12, 34];
```

* `List<String>` → Only strings allowed
* `List<int>` → Only integers allowed
* Safer and better practice

---

# 4️⃣ Accessing List Elements

Lists use **index numbers** starting from 0.

```dart
print(siblings_names[0]);  // Faheem
print(siblings_age[1]);    // 12
```

| Index | Value     |
| ----- | --------- |
| 0     | Faheem    |
| 1     | Abu bakar |
| 2     | Najeeb    |

---

# 5️⃣ Using `contains()` Method

```dart
if (siblings_names.contains("Najeeb")) {
```

* `contains()` checks if a value exists inside a list.
* Returns `true` or `false`.

### Example:

```dart
siblings_names.contains("Najeeb"); // true
siblings_names.contains("Ahmed");  // false
```

---

# 6️⃣ If-Else Statement

```dart
if (condition) {
   // runs if true
} else {
   // runs if false
}
```

In your code:

```dart
if (siblings_names.contains("Najeeb")) {
  siblings_names[1] = "Ali";
  print(siblings_names);
} else {
  print("Not Found");
}
```

### What Happens Here?

1. Checks if `"Najeeb"` exists
2. If yes:

   * Changes index 1 value to `"Ali"`
   * Prints updated list
3. If no:

   * Prints `"Not Found"`

---

# 7️⃣ Modifying Lists

Your code contains several useful list operations (commented). Let’s understand them:

---

## 🔹 1. Remove an Item

```dart
siblings_names.remove("Najeeb");
```

Removes specific value.

---

## 🔹 2. Add an Item

```dart
siblings_names.add("Nadeem");
```

Adds item at the end.

---

## 🔹 3. Add Multiple Items

```dart
siblings_names.addAll(["Alyan", "Ayaz"]);
```

Adds multiple values.

---

## 🔹 4. Sort List

```dart
siblings_names.sort();
```

Sorts alphabetically (for strings).

---

## 🔹 5. Update a Value Using Index

```dart
siblings_names[1] = "Ali";
```

Replaces value at index 1.

---

# 8️⃣ Output of Your Current Code

Since `"Najeeb"` exists:

Original list:

```dart
["Faheem", "Abu bakar", "Najeeb"]
```

After update:

```dart
["Faheem", "Ali", "Najeeb"]
```

This will be printed.

---

# 9️⃣ Best Practice Version of Your Code

Here’s the improved and recommended version:

```dart
void main() {
  List<String> siblingsNames = ["Faheem", "Abu Bakar", "Najeeb"];
  List<int> siblingsAge = [23, 12, 34];

  if (siblingsNames.contains("Najeeb")) {
    siblingsNames[1] = "Ali";
    print(siblingsNames);
  } else {
    print("Not Found");
  }
}
```

### Improvements:

✔ Used proper typing
✔ Used camelCase naming
✔ Clean and readable

---

# 🔟 Important Concepts Students Must Remember

### ✅ Lists are zero-indexed

### ✅ Use typed lists (`List<String>`)

### ✅ `contains()` returns boolean

### ✅ Use `add()`, `remove()`, `sort()` to manipulate lists

### ✅ Always write clean and readable code

---

# 🎯 Practice Exercises

Try these:

1. Add a new sibling to the list.
2. Remove the first sibling.
3. Print all siblings using a `for` loop.
4. Sort siblings in reverse order.
5. Check if age 12 exists in age list.

---

# 🚀 Final Summary

This program teaches you:

* Dart basic syntax
* Lists
* Data types
* Conditional statements
* List manipulation methods

Mastering these basics is essential before moving to:

* Loops
* Functions
* Classes & OOP
* Flutter app development
