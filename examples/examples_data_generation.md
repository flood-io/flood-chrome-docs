---
title: Examples - Test Data Generation
---

# Examples - Test Data Generation

## Overview

With the help of the incredible open-source Faker library [link](https://github.com/Marak/faker.js) - we can generate test data for use in Flood Chrome test very easily and on-the-fly. The Faker library allows us to generate a wide variety of syntax-correct data such as randome names, numbers, strings, emails etc.

To start using Faker within your Flood Chrome script you will need to import the specific Faker library -for example for basic random data - we would use the following 'random' library:

```typescript
    import { random } from 'faker'
```

## Using Random Numbers

The simplest way to generate a random number using Faker is to declare the 'random' Faker object at the top of your Flood Chrome script:

```typescript
    import { random } from 'faker'
```

And then use the following in your Flood Chrome script step to generate a 5 digit random number between 0 and 99999:

```typescript
        //Generate a random phone number
        var randNumber = random.number(99999).toString()
```
