# learn-typescript

### Install
`npm install -g typescript`

### Compile
`tsc filename.ts`

### Autoload any changes
- Install **lite-server** package from npm
`npm install --save-dev lite-server`

- Update package.json script:
```json
{
...
  "scripts":{
    "start": "lite-server"
  }
...
}
```

## Key Features of TS
- Type Safety by declaring type
- Define Object type to create a variable of Object type
```ts
type User = {
  name: string;
  age: number;
  isAdmin: boolean;
  id: string | number;
}
```

- Interface type is another type similar to object type, it allows extensibility
```ts
interface User {
  name: string;
  age: number;
  isAdmin: boolean;
  id: string | number;
}

let student: User;

student = {
  name: 'Utkal',
  age: 10
}
```

- Alias Type allows to define custom types to wrap complex object structures (recommended)
```ts
// define a custom type that describes a function
type anyCustType = (a:number, b:number) => number;

// use the custom type to pass as a parameter
function someFunction(a:number, b:number, anotherFunction: anyCustType){
  ...
  //function logic goes here
  ...
}

// invoke function as required
someFunction(5,6, callFun);
```

- Merge Types
```ts

// first object type
type User = {
  name: string
};

// another object type
type Admin = {
  isAdmin: boolean
};

// declare a new type by merging both types
type AdminUser = User & Admin;

// use the type in following way
let admin: AdminUser;

admin = {
 name: 'Utkal',
 isAdmin: true
}
```

#### String Literals
- String Literals is a special type definition, that restricts value of the variable to specific pre-defined values
```ts
type User = 'abc' | 'some name' | 'another allowed name';

// OR
let User: 'abc' | 'some name' | 'another allowed name';
```

### Generic Types
- Add generic type and custom generic type to defer the types of variable for declaring later


