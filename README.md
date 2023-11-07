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
- 
