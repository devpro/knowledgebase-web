---
title: "TypeScript"
date: 2019-09-13T10:24:07+02:00
draft: false
weight: 70
---

See [typescriptlang.org](https://www.typescriptlang.org/).

## Learn

### Documentation

- [typescriptlang.org/docs](https://www.typescriptlang.org/docs/home.html)
- [github.com/Microsoft/TypeScript](https://github.com/Microsoft/TypeScript)

### Versions

- [TypeScript 3.7](https://www.typescriptlang.org/docs/handbook/release-notes/typescript-3-7.html)

### Quickstart

#### 5 minutes tutorial

- TypeScript must be known globally on your machine: `npm install -g typescript`

- Create a new folder and initiate TypeScript configuration: `tsc --init`

  - Review the fille name `tsconfig.json` that has been generated

- Create a file named `greeter.ts`

  {{< highlight typescript >}}
  class Student {
      fullName: string;
      constructor(public firstName: string, public middleInitial: string, public lastName: string) {
          this.fullName = firstName + " " + middleInitial + " " + lastName;
      }
  }

  interface Person {
      firstName: string;
      lastName: string;
  }

  function greeter(person : Person) {
      return "Hello, " + person.firstName + " " + person.lastName;
  }

  let user = new Student("Jane", "M.", "User");

  document.body.innerHTML = greeter(user);
  {{< /highlight >}}

- Run the compiler: `tsc`

  - Review the generated file `greeter.js`
  - You can also have the compiler run with the watch option: `tsc --watch`

- Create a `greeter.html` file and open the file in a browser:

  ```html
  <!DOCTYPE html>
  <html>
      <head><title>TypeScript Greeter</title></head>
      <body>
          <script src="greeter.js"></script>
      </body>
  </html>
  ```
