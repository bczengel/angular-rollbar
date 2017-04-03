# Angular (2+) Rollbar Integration

This package provides an Angular 2+ service for logging to Rollbar.

## Installation

    npm install angular-rollbar

## Usage

### Bootstrap the module

```ts

NgModule({
    imports: [
        RollbarModule.forRoot({
            accessToken: 'YOUR ROLLBAR CLIENT TOKEN'
        })
    ]
})
export class MyAngularApp {}

```

### Use the service

Let the Angular DI do all the magic for you.

```
import { Component } from '@angular/core'
import { RollbarService } from 'angular-rollbar';

@Component(...)
export class MyComponent {

    constructor (rollbar: RollbarService) {
        rollbar.info('Logging to Rollbar!');
    }
}
```

## Development

We are using Angular CLI to make things a little bearable.

```sh
npm install
npm test
```

