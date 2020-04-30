# Apparently you can add pre to any script name and when you run the script it will run the pre-version first

```
"scripts": {
  "preinstall": "npx npm-force-resolutions",
  "prebuild": "rimraf dist",
  "build": "npm run build:server && npm run build:client",
  "pretest": "npm run gql",
  "test": "jest",
  "test:cov": "jest --coverage",
...
```
