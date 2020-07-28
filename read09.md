# Functional Programming

**Functional programming is a programming style of building the structure and elements a program which treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data**

## Functional Programming Concepts:

- **Pure functions**
    - returns the same result if given the same arguments
    - does not cause any observable side effects
    - does not read external files
    - does not rely on a random number generator
- **Immutability**
    - unchangeable, its state cannot change after it's created
- **Referential transparency** 
    - consistently yields the same result for the same input
    - `pure functions + immutable data = referential transparency`
- **Functions as first-class entities**
    - functions are treated as values and used as data
    - refer to functions from constants and variables
    - pass functions as a parameter to other functions
    - return functions as result from other functions
- **Higher-order functions**
    - takes one or more functions as arguments
    - returns a function as its result
- **Filter**
    - filter a given collection by an attribute
- **Map**
    - transform a collection into a different collection
- **Reduce**
    - receive a function and a collection, and return a value created by combining the items

--------------------

# Code Refactoring for Performance and Readability

## Scenarios:

- **Using _`Hash functions`_**
- **Using _`friendly-words`_ package**

## Strategies:

- **Return early from functions**
i.e.

```
function showProfile(user) {
  if (user.authenticated === true) {
    // ..
  }
}

// Refactor into ->

function showProfile(user) {
  // People often inline such checks
  if (user.authenticated === false) { return; }
  // Stay at the function indentation level, plus less brackets
}
```

- **Cache variables — so functions can be read like sentences**
i.e.

```
function searchGroups(name) {
  for (let i = 0; i < continents.length; i++) {
    for (let j = 0; j < continents[i].length; j++) {
      for (let k = 0; k < continents[i][j].tags.length; k++) {
        if (continents[i][j].tags[k] === name) {
          return continents[i][j].id;
        }
      }
    }
  }
}

// Refactor into ->

function searchGroups(name) {
  for (let i = 0; i < continents.length; i++) {
    const group = continents[i]; // This code becomes self-documenting
    for (let j = 0; j < group.length; j++) {
      const tags = group[j].tags;
      for (let k = 0; k < tags.length; k++) {
        if (tags[k] === name) {
          return group[j].id; // The core of this nasty loop is clearer to read
        }
      }
    }
  }
}
```

- **Check for Web APIs before implementing your own functionality**
i.e.

```
function cacheBust(url) {
  return url.includes('?') === true ?
    `${url}&time=${Date.now()}` :
    `${url}?time=${Date.now()}`
}

// Refactor into ->

function cacheBust(url) {
  // This throws an error on invalid URL which stops undefined behaviour
  const urlObj = new URL(url);
  urlObj.searchParams.append('time', Date.now); // Easier to skim read
  return url.toString();
}
```
