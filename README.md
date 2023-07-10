# cleancode-doc

- [cleancode-doc](#cleancode-doc)
  - [Naming](#naming)
    - [Use meaningful variable names](#use-meaningful-variable-names)
    - [Boolean variables are often required to answer specific questions, such as:](#boolean-variables-are-often-required-to-answer-specific-questions-such-as)
    - [Use searchable names](#use-searchable-names)
    - [Use consistent subfix](#use-consistent-subfix)
  - [Use Mapping to reduce Switch](#use-mapping-to-reduce-switch)
  - [Reusability](#reusability)
  - [Functions](#functions)
    - [do one thing](#do-one-thing)
    - [arguments (2 or fewer ideally)](#arguments-2-or-fewer-ideally)
  - [Class / Enum](#class--enum)

## Naming

clearly and descriptively = readability and maintainability

### Use meaningful variable names
```
originalAccountList
modifiedAccountList
totalAccounts
```

### Boolean variables are often required to answer specific questions, such as:
```
isActive
canSwitchUser
hasChildren
```

### Use searchable names
constants to be searchable
  ```
  const SESSION_DURATION_MS = 15 * 60 * 1000
  ```

### Use consistent subfix
```
xxxList
xxxSet
xxxMap
```

## Use Mapping to reduce Switch
```
Map widgetMap = {
  "Line": LineChart,
  "Bar": BarChart
}
```

## Reusability
quality and consistency = efficiency and productivity

## Functions

### do one thing
**Bad:**
```
createFile(name: string, temp: boolean) {
  if (temp) {
    fs.create(`./temp/${name}`);
  } else {
    fs.create(name);
  }
}
```
**Good:**
```
createTempFile(name: string) {
  createFile(`./temp/${name}`);
}

createFile(name: string) {
  fs.create(name);
}
```
### arguments (2 or fewer ideally)
**Bad:**
```
createMenu(title: string, body: string, buttonText: string, cancellable: boolean) {}
```
**Good:**
```
Type MenuOptions = { title: string, body: string, buttonText: string, cancellable: boolean }
createMenu(options: MenuOptions) {}
```
## Class / Enum 

