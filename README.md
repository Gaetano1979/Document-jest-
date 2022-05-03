# Document-jest
aggiungere jest al progetto angular

> nel package.json

```
"jest": {
    "preset": "jest-preset-angular",
    "globals": {
      "ts-jest": {
        "tsconfig": "<rootDir>/tsconfig.spec.json"
      }
    },
    "setupFilesAfterEnv": [
      "<rootDir>/setupJest.ts"
    ],
    "globalSetup": "jest-preset-angular/global-setup",
    "testPathIgnorePatterns": [
      "<rootDir>/node_modules/",
      "<rootDir>/dist/",
      "<rootDir>/src/test.ts",
      "<rootDir>/projects/nric/src/test.ts"
    ]
  }
```

il file dovrebbe risolturare in questo modo

```
{
  "name": "test-jest",
  "version": "0.0.0",
  "scripts": {
    "ng": "ng",
    "start": "ng serve",
    "build": "ng build",
    "test": "jest",
    "test:watch": "jest --watch",
    "lint": "ng lint",
    "e2e": "ng e2e"
  },
  "private": true,
  "dependencies": {
    "@angular/animations": "~11.2.14",
    "@angular/common": "~11.2.14",
    "@angular/compiler": "~11.2.14",
    "@angular/core": "~11.2.14",
    "@angular/forms": "~11.2.14",
    "@angular/platform-browser": "~11.2.14",
    "@angular/platform-browser-dynamic": "~11.2.14",
    "@angular/router": "~11.2.14",
    "rxjs": "~6.6.0",
    "tslib": "^2.0.0",
    "zone.js": "~0.11.3"
  },
  "devDependencies": {
    "@angular-devkit/build-angular": "~0.1102.18",
    "@angular/cli": "~11.2.19",
    "@angular/compiler-cli": "~11.2.14",
    "@types/jest": "^27.5.0",
    "@types/node": "^12.11.1",
    "codelyzer": "^6.0.0",
    "jest": "^27.5.1",
    "jest-preset-angular": "^11.1.2",
    "ts-node": "~8.3.0",
    "tslint": "~6.1.0",
    "typescript": "~4.1.5"
  },
  "jest": {
    "preset": "jest-preset-angular",
    "globals": {
      "ts-jest": {
        "tsconfig": "<rootDir>/tsconfig.spec.json"
      }
    },
    "setupFilesAfterEnv": [
      "<rootDir>/setupJest.ts"
    ],
    "testPathIgnorePatterns": [
      "<rootDir>/node_modules/",
      "<rootDir>/dist/",
      "<rootDir>/src/test.ts",
      "<rootDir>/projects/nric/src/test.ts"
    ]
  }
}
```

come prima cosa installiamo 
``` npm install -D jest jest-preset-angular @types/jest ```

poi creamo un file nella radice del progetto 
```
setup-jest.ts
```

poi all'interno del file mettiamo la import
```
import 'jest-preset-angular/setup-jest';
```
possiamo vediamo questa paggina
```
https://www.npmjs.com/package/jest-preset-angular
```
