## TypeScript<br/>in the Field
## **Magic or Menace?**

Note:
- Title
- Thank you
- Seeing TS More Often. Ranting, Raving
- Believe the hype?
- SO: Top 10 Most Popular Technologies; Top 5 Most Loved

---

## Your Guide<br/>to **TypeScript**

- Technical Co-Founder @ **Zippy Software**
- Sr Application Developer @ **U.S. Engineering**
- Application Architect @ **The Lead Group**

Note:
- Leading teams using TypeScript across the Lead Generation, Industrial Construction and Educational industries
- Small teams
- Collaboration

---

## **Playground** vs <strong class="text-yellow">Production</strong>

Note:
- Seen people pulling their hair out
- Seen the lightbulb that goes off when TypeScript "clicks"

---

## What Is<br/> **TypeScript?**

---

![IMAGE](assets/img/js-ts.jpg)

---

## JavaScript<br/>**that scales.**

"TypeScript is a typed superset of JavaScript that compiles to plain JavaScript."

---

## JavaScript<br/>**that scales.**

"TypeScript is a <strong class="text-yellow"><u>typed</u></strong> superset of JavaScript that compiles to plain JavaScript."

---

## JavaScript<br/>**that scales.**

"TypeScript is a typed <strong class="text-yellow"><u>superset</u></strong> of JavaScript that compiles to plain JavaScript."

---

## JavaScript<br/>**that scales.**

"TypeScript is a typed superset of JavaScript that <strong class="text-yellow"><u>compiles</u></strong> to plain JavaScript."


---

## Why Use TypeScript?
Note:
- Million Dollar Question
- You as a developer or as a team
- How would you defend to your boss?

---

![IMAGE](assets/img/38-percent.jpg)

---

## JavaScript<br/>**that <u>scales</u>.**

---

## **Magic** or <br/> Menace?

Note:
- What are the trade-offs?
- It is not always pain free.


---
## TypeScript<br/>**Does Not Exist**

Note:
- Compiled

---

@snap[north span-100]
## Where Did It Go?
@snapend

```ts
// TypeScript
type Hobby = 'running' | 'reading' | 'gaming' | 'painting' | 'other';

interface Person {
    name: string;
    phone: string;
    age: number;
    hobby: Hobby;
}

const callPerson = (person: Person): void => console.log(person.phone);
```

---

@snap[north span-100]
## Where Did It Go?
@snapend

```js
// JavaScript
"use strict";
const callPerson = (person) => console.log(person.phone);
```

---

## TypeScript<br/>**Watches Your Back**

---

#### EXAMPLE
## Increment<br/>**an Array**

---

```js
// JS
const increment = (num) => num + 1;
const incrementAll = (arr) => arr.map(increment);

let input = [1, 2, 3, 4, 5];

console.log(incrementAll(input)); // [2, 3, 4, 5, 6];
```
---

```js
// JS
input = ['a', 'b', 'c'];

console.log(incrementAll(input)); // ['a1', 'b1', 'c1'];
```
---
```ts
// TS
const increment = (num: number): number => num + 1;
const incrementAll = (arr: number[]): number[] => arr.map(increment);

let input = [1, 2, 3, 4, 5];

console.log(incrementAll(input)); // [2, 3, 4, 5, 6];

input = ['a', 'b', 'c']; // Compiler error
```
---

## Type **Inference**

---
@snap[north span-100]
## Type Inference
@snapend

```ts
// TS
let numArray = [1, 2, 3, 4, 5]; // number[]
let strArray = ['a', 'b', 'c']; // string[]

let num = 6;
let str = 'a';

numArray.push(num); // OK!
strArray.push(str); // OK!

numArray.push(str); // Nope! Compiler Error
strArray.push(num); // Nope! Compiler Error
```
---

## Fail **Early**

---

@snap[north span-100]
## Fail Early
@snapend

```ts
// TS
interface Person {
    name: string;
    phone: string;
}

const callPerson = (person: Person): void => console.log(person.phone);

const phone = '555-555-5555';

callPerson(phone);
```

---
@snap[north span-100]
## Fail Early
@snapend
![IMAGE](assets/img/tiny-error.png)

---

@snap[north span-100]
## Keep Your **Tools**
@snapend

@snap[west]
### JS
- ESLint
- Libraries
- Frameworks
- Tests
- `npm watch`

@snapend

@snap[east text-left]
### TS
- TSLint
- Libraries
- Frameworks
- Tests
- `tsc watch`
@snapend

---

## Magic or <br/> **Menace?**

Note:
- What are the trade-offs?
- It is not always pain free.

---

# Debugging

---

## **Pain-less** Errors

![IMAGE](assets/img/happy-error.png)

---

## **Painful** Errors

![IMAGE](assets/img/scary-error.png)

---

## **Types !==** Values

---

@span[north]
## Types !== Values
@spanend
```ts
interface Person {
    name: string;
    phone: string;
}

const person = { name: 'Jonathan', phone: '555-555-5555' };

console.log(typeof person === Person); // false
console.log(person instanceof Person); // Compiler Error

console.log('WTF');
```

---

## Expect<br/>**Resistance**

Note:
- Polarizing
- JavaScript that Scales.

---

## Implementation: <br/>**Plan** vs <span class="text-yellow">Reality</span>

![IMAGE](assets/img/your-plan.png)

Note:
- External libraries
- Refactoring
-

---

## Resist the Urge

Note:

- Not everything is a type, but you'll be tempted to think of them that way.
- Types can help communicate, but they don't encapsulate everything
- Tight coupling is still a concern that you need to carefully monitor for.

---

## **any**<br/>is the enemy

---

```typescript
const MyButtonComponent: React.FC<MyButtomComponentProps> = () => {
  const handleClick = (e) => {
    console.log(e);
  };

  return (
    <button onClick={handleClick}>
      My Button
    </button>
  );
};
```
---


```ts
const myType = 'foo';
```

---

## But <em>**should**</em> you <br/>use TypeScript?

Note:
- Million Dollar Question
- You as a developer or as a team
- How would you defend to your boss?

---

# **No.**

---

## **TypeScript**<br/> Changes The Way You Think

Note:
- Thinking in Types instead of thinking in Values
- Adopting new mental models, OOP vs FP, Dynamic vs Static Types
- Thinking categorically using generics

---

## Resources

- TypeScript Playground

---

# **Questions?**

---?image=assets/img/code.jpg&opacity=60&position=left&size=45% 100%

@snap[east span-50 text-center]

### Thank You!

**@jwondrusch**

@snapend

@snap[south-east span-50 text-center]
#### P.S. We're Hiring
@snapend

Note:
- 1:15
- Thank You to This Dot, Vin Solutions, and most of all to everyone here.
- We're currently hiring
