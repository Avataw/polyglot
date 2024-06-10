---
marp: true
theme: uncover
paginate: skip
class: invert
---

# Perks of being a Polyglot

How to improve your typescript code by learning other languages.

---

## About me

- I'm [Andre](https://www.linkedin.com/in/andre-wru/) :D
- Senior Software Engineer at Interhyp
- Fullstack with more experience in the frontend
- I love all sorts of languages!

---

## Learning from other languages

> Learning another language is not only learning different words for the same things, but learning another way to think about things.
> &mdash; Flora Lewis

---

## Usage according to Stackoverflow

- 64% Javascript
- 39% Typescript
- 13% Rust
- 2% Elixir

---

## Popularity by subreddit size

- 2.4m Javascript
- 296k Rust
- 129k Typescript
- 30k Elixir

---

## Java

### 3 billion devices run Java every day!

---

### Just kidding :p

Java inspired me to dabble with Kotlin though.

---

## Kotlin

[Kotlin](https://kotlinlang.org/) was developed by Jetbrains as an easily implementable, interoperable replacement for Java.

---

### Copy Java & Paste Kotlin

> TODO

---

### Kotlin - Comfort functions

Example:

Given a team of pokémon, calculate the total sum of all levels.

```typescript
const team = [
  { name: "Pikachu", level: 20, trainer: "Ash" },
  { name: "Charmander", level: 12, trainer: "Gary" },
  { name: "Snorlax", level: 42, trainer:: "Ash" }
]
 ```

 ---

### In Typescript

 ```typescript
team.reduce((acc, { level }) => acc + level, 0)

// result: 76
 ```

---

### In Kotlin

```kotlin
team.mapNotNull{ it.level }.sum()
```

So comfy :D

---

### Now let's spice it up a bit...

Given a team of pokémon, group them by their trainer.

```typescript
const team = [
  { name: "Pikachu", level: 20, trainer: "Ash" },
  { name: "Charmander", level: 12, trainer: "Gary" },
  { name: "Snorlax", level: 42, trainer: "Ash" }
]
 ```

 ---

### In Typescript

 ```typescript
const result = team.reduce((acc, pokemon) => {
  acc[pokemon.trainer] = acc[pokemon.trainer]?.concat(pokemon) ?? [pokemon];
  return acc
}, {})

 ```

---

### This works!

```json
{
  "Ash": [
    {
      "name": "Pikachu",
      "level": 20
    },
    {
      "name": "Snorlax",
      "level": 42
    }
  ],
  "Gary": [
    {
      "name": "Charmander",
      "level": 12
    }
  ]
} 
```

---

### Now in Kotlin


### Extension Methods
