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
