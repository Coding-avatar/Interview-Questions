<h1 id="top">TypeScript Last Minute Questionnaire</h1>
<h2>List of Topics</h2>
<ol type="a">
    <li>
        <details open>
            <summary><h3>TypeScript Basics & Fundamentals</h3></summary>
            <ol>
                <li><a href="#q1">Why use TypeScript over JavaScript?</a></li>
                <li><a href="#q2">What problems does TypeScript solve?</a></li>
                <li><a href="#q3">What are the main benefits of using static typing in TypeScript?</a></li>
                <li><a href="#q4">What are type annotations and why are they useful?</a></li>
                <li><a href="#q5">What is type inference in TypeScript?</a></li>
                <li><a href="#q6">How does TypeScript handle arrays, tuples, and enums?</a></li>
                <li><a href="#q7">What is the difference between any, unknown, and never types?</a></li>
                <li><a href="#q8">What is the difference between null and undefined in TypeScript?</a></li>
                <li><a href="#q9">What does the strict compiler option do?</a></li>
            </ol>
        </details>
    </li>
    <li>
        <details open>
            <summary><h3>Type System & Type Narrowing</h3></summary>
            <ol>
                <li><a href="#q10">What is the difference between interfaces and type aliases in TypeScript?</a></li>
                <li><a href="#q11">What are union and intersection types in TypeScript?</a></li>
                <li><a href="#q12">What is type narrowing, and how do type guards work?</a></li>
                <li><a href="#q13">What are literal types and discriminated unions in TypeScript?</a></li>
                <li><a href="#q14">What are keyof, typeof, and in in TypeScript?</a></li>
                <li><a href="#q15">What are index signatures in TypeScript?</a></li>
                <li><a href="#q16">What is structural typing in TypeScript?</a></li>
                <li><a href="#q17">What is declaration merging in TypeScript?</a></li>
            </ol>
        </details>
    </li>
    <li>
        <details open>
            <summary><h3>Advanced Types & Generics</h3></summary>
            <ol>
                <li><a href="#q18">What are generics in TypeScript, and why are they useful?</a></li>
                <li><a href="#q19">What are TypeScript utility types, and how are they used?</a></li>
                <li><a href="#q20">What are conditional and mapped types in TypeScript?</a></li>
                <li><a href="#q21">What is the infer keyword used for in TypeScript?</a></li>
                <li><a href="#q22">What are template literal types?</a></li>
                <li><a href="#q23">What are satisfies and as const in TypeScript?</a></li>
            </ol>
        </details>
    </li>
    <li>
        <details open>
            <summary><h3>Functions & Object Types</h3></summary>
            <ol>
                <li><a href="#q24">How does function overloading work in TypeScript?</a></li>
                <li><a href="#q25">What are optional and rest parameters in TypeScript?</a></li>
                <li><a href="#q26">What is the difference between readonly and const in TypeScript?</a></li>
                <li><a href="#q27">What is function type variance (covariance and contravariance)?</a></li>
                <li><a href="#q28">What are this types in TypeScript?</a></li>
            </ol>
        </details>
    </li>
    <li>
        <details open>
            <summary><h3>Object-Oriented Programming (OOP)</h3></summary>
            <ol>
                <li><a href="#q29">How does TypeScript support object-oriented programming (OOP)?</a></li>
                <li><a href="#q30">What is the difference between abstract classes and interfaces in TypeScript?</a></li>
                <li><a href="#q31">What is the difference between private, protected, and public modifiers?</a></li>
                <li><a href="#q32">What is the difference between implements and extends?</a></li>
                <li><a href="#q33">How do mixins work in TypeScript?</a></li>
            </ol>
        </details>
    </li>
    <li>
        <details open>
            <summary><h3>Practical Integration & Migration</h3></summary>
            <ol>
                <li><a href="#q34">How would you migrate a JavaScript project to TypeScript?</a></li>
                <li><a href="#q35">How do you use TypeScript with React?</a></li>
                <li><a href="#q36">How do you use TypeScript with Node.js?</a></li>
                <li><a href="#q37">How do you handle third-party JavaScript libraries that lack TypeScript definitions?</a></li>
            </ol>
        </details>
    </li>
    <li>
        <details open>
            <summary><h3>Configuration & Tooling</h3></summary>
            <ol>
                <li><a href="#q38">What is tsconfig.json, and why is it important?</a></li>
                <li><a href="#q39">How do you configure TypeScript with build tools like Webpack, Vite, or Babel?</a></li>
                <li><a href="#q40">How do you configure ESLint with TypeScript for better code quality?</a></li>
            </ol>
        </details>
    </li>
</ol>

<hr />
<h2>Answers Section</h2>

<!-- TypeScript Basics & Fundamentals -->
<h3 id="q1">1. Why use TypeScript over JavaScript?</h3>
<p><strong>Short Answer:</strong> TypeScript adds static typing and compile-time error checking, which helps developers detect bugs early and make codebases more predictable.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

TypeScript adds static typing and compile-time error checking, which helps developers detect bugs early and make codebases more predictable.

This ensures better maintainability and scalability.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q2">2. What problems does TypeScript solve?</h3>
<p><strong>Short Answer:</strong> TypeScript addresses JavaScript’s weaknesses in type safety, scalability, and readability.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

TypeScript addresses JavaScript’s weaknesses in type safety, scalability, and readability.

Enforcing clear type definitions prevents subtle runtime bugs and makes refactoring safer.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q3">3. What are the main benefits of using static typing in TypeScript?</h3>
<p><strong>Short Answer:</strong> Static typing improves code reliability, auto-completion, and developer productivity.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

Static typing improves code reliability, auto-completion, and developer productivity.

It helps with early detection of type errors and allows IDEs to provide richer tooling support.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q4">4. What are type annotations and why are they useful?</h3>
<p><strong>Short Answer:</strong> Type annotations allow developers to declare variable types explicitly.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

Type annotations allow developers to declare variable types explicitly.

This improves code readability and reduces runtime errors.

Here is an example:

```ts
let username: string = "DataCamper";
let age: number = 25;
let isAdmin: boolean = true;
```

In the above code, the compiler ensures that only the correct type can be assigned to each variable.

For example, if you try to assign a string to age, TypeScript will throw an error, which helps catch mistakes early.

Explicit typing is especially important for function parameters, return types, and API contracts, as it communicates expectations to other developers.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q5">5. What is type inference in TypeScript?</h3>
<p><strong>Short Answer:</strong> TypeScript can automatically infer types based on assigned values.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

TypeScript can automatically infer types based on assigned values.

This means you don’t always need to explicitly declare a type. TypeScript figures it out for you.

Here is an example:

```ts
let count = 10;  // inferred as number
count = "hello"; // Error: Type 'string' is not assignable to type 'number'
```

In this example, TypeScript infers that count must be a number based on its initial value, so assigning a string later causes a compile-time error. 

Best practices for type inference include:

Use explicit types for exported functions, classes, and interfaces to provide clear contracts.
Allow inference for local variables when the type is obvious.
Avoid using any unless absolutely necessary, as it bypasses TypeScript’s safety features.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q6">6. How does TypeScript handle arrays, tuples, and enums?</h3>
<p><strong>Short Answer:</strong> TypeScript allows developers to enforce strict types on arrays, tuples, and enums to improve clarity and prevent runtime errors.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

TypeScript allows developers to enforce strict types on arrays, tuples, and enums to improve clarity and prevent runtime errors.

Here is a typed array example:

```ts
let scores: number[] = [95, 80, 85];
scores.push(100); // OK
scores.push("A+"); // Error
```

Typed arrays ensure that all elements in the array follow the same type.

Here is a tuple example:

```ts
let user: [string, number] = ["Don", 25];
```

Tuples define fixed-length arrays with specific types for each position.

They are useful for structured data where the order and type of elements matter.

Here is an enum example:

```ts
enum Status {
  Active,
  Inactive,
  Pending,
}
let currentStatus: Status = Status.Active;
```

Enums provide named constants, improving readability and reducing invalid values.

They are especially useful for status codes, roles, and configuration options.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q7">7. What is the difference between any, unknown, and never types?</h3>
<p><strong>Short Answer:</strong> `any` disables type checking entirely, `unknown` is a safer alternative requiring type checking before use, and `never` represents values that can never occur.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

The following table highlights the key differences between the any, unknown, and never types in TypeScript:

<table border="1" cellpadding="6">
  <thead>
    <tr>
      <th>Type</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>any</code></td>
      <td>Disables type checking entirely, allowing any value.</td>
    </tr>
    <tr>
      <td><code>unknown</code></td>
      <td>Safer alternative to <code>any</code>; you must check the type before using it.</td>
    </tr>
    <tr>
      <td><code>never</code></td>
      <td>Represents values that never occur (e.g., functions that always throw).</td>
    </tr>
  </tbody>
</table>


Represents values that never occur (e.g., functions that always throw).

Here is an example:

```ts
function fail(): never {
  throw new Error("Something went wrong");
}
```

A tip would be to prefer unknown over any to maintain type safety while retaining flexibility.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q8">8. What is the difference between null and undefined in TypeScript?</h3>
<p><strong>Short Answer:</strong> The key differences between null and undefined are:</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

The key differences between null and undefined are:

undefined means a variable has been declared but not assigned a value.

null is an explicit value meaning no value.

TypeScript's strictNullChecks mode treats them as separate types, which prevents accidental null-related bugs.

Here is an example:

```ts
let a: string | null = null;
let b: string | undefined = undefined;
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q9">9. What does the strict compiler option do?</h3>
<p><strong>Short Answer:</strong> The strict flag enables all of TypeScript’s strict type-checking rules, such as:</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

The strict flag enables all of TypeScript’s strict type-checking rules, such as:

strictNullChecks: Prevents null and undefined values from being assigned to variables unless explicitly allowed, helping avoid runtime null reference errors.
noImplicitAny: Requires all variables to have explicit types or inferred types, preventing TypeScript from defaulting to any.

strictFunctionTypes: Enforces stricter rules for function type compatibility, catching mismatches in function parameter and return types.

strictBindCallApply: Ensures that the bind, call, and apply methods are used with the correct argument types for functions.

It ensures safer, more predictable code and catches subtle bugs early.


Let’s now look at some key TypeScript type system concepts commonly discussed in technical interviews.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<!-- Type System & Type Narrowing -->
<h3 id="q10">10. What is the difference between interfaces and type aliases in TypeScript?</h3>
<p><strong>Short Answer:</strong> Both interfaces and type aliases describe the shape of objects, but they serve slightly different purposes.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

Both interfaces and type aliases describe the shape of objects, but they serve slightly different purposes.

Interfaces can be extended using extends, which makes them ideal for hierarchical object models.

Type aliases can represent unions, intersections, primitives, and more complex composite types.

Here is an example:

```ts
interface Person {
  name: string;
  age: number;
}
```

```ts
type Employee = {
  name: string;
  department: string;
};
```

Use interfaces when defining object shapes or class contracts.

Use type aliases when you need flexible, composable types like unions or intersections.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q11">11. What are union and intersection types in TypeScript?</h3>
<p><strong>Short Answer:</strong> Union types allow a variable to hold multiple possible types, while intersection types combine multiple types into one.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

Union types allow a variable to hold multiple possible types, while intersection types combine multiple types into one.

Here is a union example:

```ts
let id: string | number;
id = ‘abc’; // OK
id = 123; // OK
```

Here is an intersection example:

```ts
type Admin = { name: string };
type Permissions = { canEdit: boolean };
type AdminUser = Admin & Permissions;
```

Union types are often used in function parameters.

Intersection types are common in complex object compositions.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q12">12. What is type narrowing, and how do type guards work?</h3>
<p><strong>Short Answer:</strong> Type narrowing lets TypeScript infer a more specific type based on control flow.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

Type narrowing lets TypeScript infer a more specific type based on control flow.

Here is an example:

```ts
function printId(id: string | number) {
  if (typeof id === "string") {
    console.log(id.toUpperCase());
  } else {
    console.log(id.toFixed());
  }
}
```

Type guards ensure safe runtime operations by verifying the type before performing specific actions.

You can use:

typeof: for primitives

instanceof: for classes

Custom type guards: using the param is Type syntax

Type guards improve type safety and reduce runtime errors.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q13">13. What are literal types and discriminated unions in TypeScript?</h3>
<p><strong>Short Answer:</strong> Literal types restrict a variable to a specific set of predefined values.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

Literal types restrict a variable to a specific set of predefined values.

Here is an example:

```ts
let direction: "up" | "down" | "left" | "right";
```

Discriminated unions combine literal types with object variants for pattern matching.

Here is an example:

```ts
type Shape =
  | { kind: "circle"; radius: number }
  | { kind: "square"; side: number };
```

```ts
function area(shape: Shape): number {
  if (shape.kind === "circle") return Math.PI * shape.radius ** 2;
  return shape.side ** 2;
}
```

Discriminated unions allow safe branching on object types and simplify logic in complex applications.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q14">14. What are keyof, typeof, and in in TypeScript?</h3>
<p><strong>Short Answer:</strong> These operators provide powerful type-level reflection.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

These operators provide powerful type-level reflection.

Keyof: gets the property names of a type

typeof: gets the type of a value

in: used in mapped types

Here is an example:

```ts
type Keys = keyof User; // "name" | "age"
const person = { name: "Alice", age: 25 };
type PersonType = typeof person; // { name: string; age: number }
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q15">15. What are index signatures in TypeScript?</h3>
<p><strong>Short Answer:</strong> Index signatures allow objects with dynamic keys.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

Index signatures allow objects with dynamic keys.

Here is an example:

```ts
interface Errors {
  [key: string]: string;
}
```

```ts
const messages: Errors = {
  email: "Invalid email",
  password: "Required"
};
```

These are used for dictionaries, map-like objects, or dynamic configuration patterns.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q16">16. What is structural typing in TypeScript?</h3>
<p><strong>Short Answer:</strong> Structural typing (duck typing) means types are compatible based on their structure, not their name.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

Structural typing (duck typing) means types are compatible based on their structure, not their name.

Here is an example:

```ts
interface Point { x: number; y: number; }
let p = { x: 10, y: 20, z: 30 };
let q: Point = p; // OK because structural match
```

This makes TypeScript flexible and works well with JavaScript patterns.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q17">17. What is declaration merging in TypeScript?</h3>
<p><strong>Short Answer:</strong> Declaration merging happens when TypeScript combines multiple declarations with the same name.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

Declaration merging happens when TypeScript combines multiple declarations with the same name.

Here is an example merging two interfaces:

```ts
interface User { name: string; }
interface User { age: number; }
const u: User = { name: "Rob", age: 30 }; // merged
```

This is useful when extending third-party types or augmenting libraries.


Here are advanced TypeScript interview questions and answers.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<!-- Advanced Types & Generics -->
<h3 id="q18">18. What are generics in TypeScript, and why are they useful?</h3>
<p><strong>Short Answer:</strong> Generics allow you to write reusable, type-safe functions and classes that work with multiple data types.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

Generics allow you to write reusable, type-safe functions and classes that work with multiple data types.

Here is a generic function example:

```ts
function identity<T>(value: T): T {
  return value;
}
```

```ts
let output = identity<string>("DataCamp");
let outputNumber = identity<number>(42);
```

Here is a generic class example:

```ts
class Box<T> {
  content: T;
  constructor(content: T) {
    this.content = content;
  }
  getContent(): T {
    return this.content;
  }
}
```

```ts
let stringBox = new Box("Hello");
let numberBox = new Box(123);
```

Best practices include:

Use descriptive names like <T>, <K, V>, or domain-specific names.

Avoid unnecessary complexity.

Use constraints (extends) to restrict acceptable types.

Generics improve code reusability by reducing duplication and enforcing consistent typing.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q19">19. What are TypeScript utility types, and how are they used?</h3>
<p><strong>Short Answer:</strong> TypeScript provides built-in utility types to manipulate and transform existing types efficiently.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

TypeScript provides built-in utility types to manipulate and transform existing types efficiently.

Here is an example:

```ts
interface Todo {
  title: string;
  description: string;
  completed: boolean;
}
```

```ts
type PartialTodo = Partial<Todo>; // all properties optional
type RequiredTodo = Required<Todo>; // all properties required
type TodoPreview = Pick<Todo, "title" | "completed">; // select specific properties
type TodoWithoutDescription = Omit<Todo, "description">; // exclude properties
```

These are especially useful when working with API responses, forms, or component props.

A tip would be to leverage utility types whenever possible to simplify code and enforce type consistency.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q20">20. What are conditional and mapped types in TypeScript?</h3>
<p><strong>Short Answer:</strong> Conditional types let you define logic within types based on relationships between them.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

Conditional types let you define logic within types based on relationships between them.

Here is an example:

```ts
type IsString<T> = T extends string ? "yes" : "no";
type Result1 = IsString<string>; // "yes"
type Result2 = IsString<number>; // "no"
```

Mapped types allow you to transform all properties of a type at once.

Here is an example:

```ts
type ReadonlyTodo = {
  readonly [K in keyof Todo]: Todo[K];
};
```

```ts
type OptionalTodo = {
  [K in keyof Todo]?: Todo[K];
};
```

The key differences are:

keyof extracts the property names of a type.
typeof gets the type of a variable or object. Combining them allows dynamic type manipulation and safer refactoring.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q21">21. What is the infer keyword used for in TypeScript?</h3>
<p><strong>Short Answer:</strong> infer lets you extract (infer) a type inside a conditional type.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

infer lets you extract (infer) a type inside a conditional type.

Here is an example:

```ts
type ReturnType<T> =
  T extends (...args: any[]) => infer R ? R : never;
```

```ts
type R = ReturnType<() => number>; // number
```

Often used in advanced utilities and generic type transformations.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q22">22. What are template literal types?</h3>
<p><strong>Short Answer:</strong> Template literal types construct string types using interpolation.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

Template literal types construct string types using interpolation.

Here is an example:

```ts
type Event = ${string}Changed;
let e: Event = "nameChanged"; // OK
```

This is useful for:

Event naming
CSS class patterns
API route patterns
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q23">23. What are satisfies and as const in TypeScript?</h3>
<p><strong>Short Answer:</strong> satisfies ensures a value satisfies a type but preserves its own literal type.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

satisfies ensures a value satisfies a type but preserves its own literal type. 

For example:

```ts
const config = {
  mode: "dark",
  version: 1
} satisfies { mode: string; version: number };
```

as const makes all properties read-only and literal. 

For example:

```ts
const directions = ["up", "down"] as const;
// type is readonly ["up", "down"]
```

Both satisfies and as const are useful in React, config objects, and discriminated unions.


In this section, we will explore TypeScript interview questions related to functions and objects.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<!-- Functions & Object Types -->
<h3 id="q24">24. How does function overloading work in TypeScript?</h3>
<p><strong>Short Answer:</strong> Function overloading allows you to define multiple function signatures for different argument types or patterns.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

Function overloading allows you to define multiple function signatures for different argument types or patterns.

Here is an example:

```ts
function add(a: number, b: number): number;
function add(a: string, b: string): string;
function add(a: any, b: any): any {
  return a + b;
}
```

```ts
let sumNumbers = add(5, 10); // 15
let sumStrings = add("Hello, ", "World"); // "Hello, World"
```

Best practices include:

Declare all possible overloads before the implementation.
Use type guards to handle multiple types safely.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q25">25. What are optional and rest parameters in TypeScript?</h3>
<p><strong>Short Answer:</strong> Optional and rest parameters make functions more flexible and expressive.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

Optional and rest parameters make functions more flexible and expressive.

Here is an example:

```ts
function greet(name: string, age?: number) {
  console.log(Hello ${name}, age: ${age ?? "unknown"});
}
```

```ts
function sum(...numbers: number[]) {
  return numbers.reduce((a, b) => a + b, 0);
}
```

The key rules for using optional and rest parameters are:

Use ? for optional parameters.

Use ... for rest parameters (variadic arguments).

These are often tested in interviews to evaluate how well you handle dynamic function inputs.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q26">26. What is the difference between readonly and const in TypeScript?</h3>
<p><strong>Short Answer:</strong> ```ts const applies to variables, while readonly applies to object properties.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

```ts
const applies to variables, while readonly applies to object properties.
```

Here is an example:

```ts
interface User {
  readonly id: number;
  name: string;
}
```

```ts
const user: User = { id: 1, name: "Bob" };
// user.id = 2; // Error: Cannot assign to 'id'
```

```ts
const { id, name } = user;
console.log(User ${name} has ID ${id});
```

Some best practices for using readonly and const are:

Use readonly for objects that should not be changed, such as data returned from an API.
Use const for variables that should not be reassigned.
Combine destructuring with type annotations for cleaner, self-documenting code.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q27">27. What is function type variance (covariance and contravariance)?</h3>
<p><strong>Short Answer:</strong> Function type variance describes how TypeScript decides if one function type can safely replace another, based on its parameter types and return types.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

Function type variance describes how TypeScript decides if one function type can safely replace another, based on its parameter types and return types.

Return types: Covariant

A function is allowed to return a more specific type than what the caller expects. For example:

```ts
type Animal = { name: string };
type Dog = Animal & { bark: () => void };
```

```ts
let f: () => Animal;
let g: () => Dog = () => ({ name: "Rex", bark() {} });
```

```ts
f = g; // OK: Dog is a subtype of Animal
```

Parameter types: Contravariant

A function is allowed to accept more general parameter types than expected. For example:

```ts
type Dog = { name: string; bark: () => void };
type Animal = { name: string };
```

```ts
type HandleDog = (dog: Dog) => void;
type HandleAnimal = (animal: Animal) => void;
```

```ts
let handleDog: HandleDog = d => console.log(d.bark());
let handleAnimal: HandleAnimal = a => console.log(a.name);

// A function that accepts an Animal is more general,
// so it can stand in for one that accepts a Dog
handleDog = handleAnimal; // OK
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q28">28. What are this types in TypeScript?</h3>
<p><strong>Short Answer:</strong> this types let methods return the same type as the class, useful for fluent APIs:</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

this types let methods return the same type as the class, useful for fluent APIs:

```ts
class Builder {
  setName(name: string): this {
    // ...
    return this;
  }
}
new Builder().setName("Test"); // chaining works
```


The following questions cover key TypeScript OOP concepts frequently discussed in technical interviews.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<!-- Object-Oriented Programming (OOP) -->
<h3 id="q29">29. How does TypeScript support object-oriented programming (OOP)?</h3>
<p><strong>Short Answer:</strong> TypeScript supports OOP principles such as classes, inheritance, and access modifiers.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

TypeScript supports OOP principles such as classes, inheritance, and access modifiers.

Classes define reusable blueprints for objects, and inheritance allows one class to extend another to share properties and behaviors.

Here is an example:

```ts
class Animal {
  constructor(public name: string) {}

  move(distance: number) {
    console.log(${this.name} moved ${distance}m.);
  }
}
```

```ts
class Dog extends Animal {
  bark() {
    console.log("Woof!");
  }
}
```

```ts
const dog = new Dog("Buddy");
dog.bark();       // Woof!
dog.move(10);     // Buddy moved 10m.
```

Access modifiers include:

public: accessible anywhere
protected: accessible in the class and its subclasses
private: accessible only within the declaring class
A tip would be to use access modifiers to ensure encapsulation, which prevents unintended modification of internal class logic or state.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q30">30. What is the difference between abstract classes and interfaces in TypeScript?</h3>
<p><strong>Short Answer:</strong> Both abstract classes and interfaces define contracts for objects or classes, but they serve different purposes.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

Both abstract classes and interfaces define contracts for objects or classes, but they serve different purposes.

Abstract classes can include shared implementation and abstract methods.

Interfaces only describe structure, not implementation.

Here is an example:

```ts
abstract class Shape {
  abstract getArea(): number; // must be implemented
}
```

```ts
class Circle extends Shape {
  constructor(public radius: number) {
    super();
  }

  getArea(): number {
    return Math.PI * this.radius ** 2;
  }
}
```

Best practices include:

Use abstract classes when you need shared logic across related classes.
Use interfaces for flexible type contracts and decoupled code design.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q31">31. What is the difference between private, protected, and public modifiers?</h3>
<p><strong>Short Answer:</strong> `public` makes properties accessible anywhere, `protected` allows access within the class and subclasses, and `private` restricts access solely to the declaring class.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

Here is a comparison of TypeScript’s access modifiers and what they control:

<table border="1" cellpadding="6">
  <thead>
    <tr>
      <th>Modifier</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>public</code></td>
      <td>Accessible anywhere.</td>
    </tr>
    <tr>
      <td><code>protected</code></td>
      <td>Accessible within the class and its subclasses.</td>
    </tr>
    <tr>
      <td><code>private</code></td>
      <td>Accessible only inside the declaring class.</td>
    </tr>
  </tbody>
</table>


Accessible only inside the declaring class.

Using the correct access modifier promotes encapsulation, which ensures that internal state and logic cannot be accessed or changed unexpectedly.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q32">32. What is the difference between implements and extends?</h3>
<p><strong>Short Answer:</strong> extends inherits behavior and properties, whereas implements enforces a contract but does not provide implementation</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

extends inherits behavior and properties, whereas implements enforces a contract but does not provide implementation

Here is an example:

```ts
interface Logger { log(msg: string): void; }
```

```ts
class Base { foo() {} }
```

```ts
class MyClass extends Base implements Logger {
  log(msg: string) {}
}
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q33">33. How do mixins work in TypeScript?</h3>
<p><strong>Short Answer:</strong> Mixins allow multiple reusable class components.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

Mixins allow multiple reusable class components.

Here is an example:

```ts
type Constructor<T = {}> = new (...args: any[]) => T;
```

```ts
function Timestamped<TBase extends Constructor>(Base: TBase) {
  return class extends Base {
    timestamp = Date.now();
  };
}
```

```ts
class User {}
const TimestampedUser = Timestamped(User);
```

Useful when you need multiple inheritance patterns.


These questions focus on real-world applications of TypeScript that often come up in interviews.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<!-- Practical Integration & Migration -->
<h3 id="q34">34. How would you migrate a JavaScript project to TypeScript?</h3>
<p><strong>Short Answer:</strong> Migrating a legacy JavaScript codebase to TypeScript should be incremental to minimize risk and disruption.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

Migrating a legacy JavaScript codebase to TypeScript should be incremental to minimize risk and disruption.

The recommended approach is:

Rename .js files to .ts.

Enable allowJs and checkJs in tsconfig.json.

Gradually add types, starting with core functions or modules.

Use any temporarily, then replace it with proper types as you refine the codebase.

 Example tsconfig.json for gradual migration:

{
  "compilerOptions": {
    "allowJs": true,
    "checkJs": true,
    "strict": true
  }
}

Gradual migration ensures stability and allows teams to benefit from type checking early without major rewrites.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q35">35. How do you use TypeScript with React?</h3>
<p><strong>Short Answer:</strong> Using TypeScript in React improves type safety for props and state, which helps prevent runtime errors.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

Using TypeScript in React improves type safety for props and state, which helps prevent runtime errors.

Here is an example:

```ts
interface Props {
  title: string;
}
```

```ts
const Header: React.FC<Props> = ({ title }) => <h1>{title}</h1>;
```

Defining prop types helps TypeScript catch missing or incorrectly typed props at compile time, which improves reliability and developer productivity.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q36">36. How do you use TypeScript with Node.js?</h3>
<p><strong>Short Answer:</strong> TypeScript enhances Node.js applications by adding type safety for API routes, configurations, and middleware.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

TypeScript enhances Node.js applications by adding type safety for API routes, configurations, and middleware.

Here is an example:

```ts
import express, { Request, Response } from "express";
const app = express();
```

app.get("/", (req: Request, res: Response) => res.send("Hello TypeScript"));

Typing Request and Response ensures correct parameter usage and prevents common runtime errors.

TypeScript makes Node.js APIs easier to maintain and refactor safely.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q37">37. How do you handle third-party JavaScript libraries that lack TypeScript definitions?</h3>
<p><strong>Short Answer:</strong> Some libraries don’t include built-in types. In these cases, you have two main options:</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

Some libraries don’t include built-in types. In these cases, you have two main options:

Option 1: Install community-maintained types

```bash
npm install --save-dev @types/library-name
```

Option 2: Create a custom declaration file

// custom.d.ts
```ts
declare module "legacy-library" {
  export function init(): void;
}
```

Tips include:

Always check @types before writing custom declarations.

Gradually add types for complex libraries to ensure compatibility.

Proper typing of third-party libraries increases confidence and reduces runtime bugs.


This section covers essential TypeScript configuration and tooling topics frequently discussed in technical interviews.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<!-- Configuration & Tooling -->
<h3 id="q38">38. What is tsconfig.json, and why is it important?</h3>
<p><strong>Short Answer:</strong> The tsconfig.json file is the central configuration for any TypeScript project.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

The tsconfig.json file is the central configuration for any TypeScript project. 

It defines compiler behavior, includes files, and enables features.

Here is an example:

{
  "compilerOptions": {
    "target": "ES2020",
    "module": "commonjs",
    "strict": true,
    "outDir": "./dist",
    "esModuleInterop": true,
    "forceConsistentCasingInFileNames": true,
    "noImplicitReturns": true,
    "noFallthroughCasesInSwitch": true
  },
  "include": ["src"],
  "exclude": ["node_modules", "dist"]
}

Key settings include:

target: JavaScript version for output

module: Module system (CommonJS, ESNext, etc.)

strict: Enables all strict type-checking options

outDir: Output folder for compiled code

esModuleInterop: Allows CommonJS module imports

Make sure you enable strict mode to catch potential bugs early and improve maintainability.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q39">39. How do you configure TypeScript with build tools like Webpack, Vite, or Babel?</h3>
<p><strong>Short Answer:</strong> TypeScript integrates seamlessly with modern build systems.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

TypeScript integrates seamlessly with modern build systems.

Common setups include:

Webpack: ts-loader for on-the-fly compilation

Vite: vite-plugin-ts for fast builds

Babel: @babel/preset-typescript for JS-heavy environments

Example Vite configuration:

```ts
import { defineConfig } from "vite";
import react from "@vitejs/plugin-react";
import tsconfigPaths from "vite-tsconfig-paths";
```

```ts
export default defineConfig({
  plugins: [react(), tsconfigPaths()],
  build: {
    target: "es2020"
  }
});
```

Align compiler and bundler settings, enable incremental builds, and use source maps for easier debugging.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q40">40. How do you configure ESLint with TypeScript for better code quality?</h3>
<p><strong>Short Answer:</strong> ESLint helps maintain consistent coding standards and catch errors early.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

ESLint helps maintain consistent coding standards and catch errors early.

Install required packages:

```json
npm install eslint @typescript-eslint/parser @typescript-eslint/eslint-plugin --save-dev
```

Example ESLint configuration:

{
  "parser": "@typescript-eslint/parser",
  "plugins": ["@typescript-eslint"],
  "extends": [
    "eslint:recommended",
    "plugin:@typescript-eslint/recommended"
  ],
  "rules": {
    "@typescript-eslint/no-explicit-any": "warn",
    "@typescript-eslint/explicit-function-return-type": "off"
  }
}
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />
