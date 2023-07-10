# cleancode-doc

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

### arguments (2 or fewer ideally)

## Class / Enum 

