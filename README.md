# NxUiCore

🔎 **Smart, Extensible Build Framework**

## Quick Start & Documentation
[Nx Documentation](https://nx.dev/angular)
[10-minute video showing all Nx features](https://nx.dev/getting-started/intro)
[Interactive Tutorial](https://nx.dev/tutorial/01-create-application)

## Adding capabilities to your workspace
Nx supports many plugins which add capabilities for developing different types of applications and different tools.
These capabilities include generating applications, libraries, etc as well as the devtools to test, and build projects as well.
Below are our core plugins:
- [Angular](https://angular.io)
  - `ng add @nrwl/angular`
- [React](https://reactjs.org)
  - `ng add @nrwl/react`
- Web (no framework frontends)
  - `ng add @nrwl/web`
- [Nest](https://nestjs.com)
  - `ng add @nrwl/nest`
- [Express](https://expressjs.com)
  - `ng add @nrwl/express`
- [Node](https://nodejs.org)
  - `ng add @nrwl/node`

There are also many [community plugins](https://nx.dev/community) you could add.

## Generate an application
Run `ng g @nrwl/angular:app my-app` to generate an application.

## Generate a library
Run `ng g @nrwl/angular:lib my-lib` to generate a library.
Libraries are shareable across libraries and applications. They can be imported from `@nx-ui-core/mylib`.

## Development server
Run `ng serve my-app` for a dev server. Navigate to http://localhost:4200/. The app will automatically reload if you change any of the source files.

## Code scaffolding
Run `ng g component my-component --project=my-app` to generate a new component.

## Build
Run `ng build my-app` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests
Run `ng test my-app` to execute the unit tests via [Jest](https://jestjs.io).
Run `nx affected:test` to execute the unit tests affected by a change.

## Running end-to-end tests
Run `ng e2e my-app` to execute the end-to-end tests via [Cypress](https://www.cypress.io).
Run `nx affected:e2e` to execute the end-to-end tests affected by a change.

## Understand your workspace
Run `nx dep-graph` to see a diagram of the dependencies of your projects.

## Position Cache Nx
./node_modules/.cache/nx


## ☁ Nx Cloud

### Distributed Computation Caching & Distributed Task Execution
npx ng add @nrwl/nx-cloud 
Visit [Nx Cloud](https://nx.app/) to learn more.

## how to generate workspace
npx create-nx-workspace name-of-workspace --preset=angular --style=scss

npm run start

npm install concurrently or using run-many parallel projects
  - nx run-many --parallel --target=serve --projects=web,api
  - insert in scripts pacakge.json "serve:all": "concurrently \" npm run serve:api \" \" npm run serve:web \"",

## how to add project App
ng g app name-of-app --style=scss --routing=false

## how to add project Lib
npx nx add name-of-plugin

npx nx/ng g lib name-of-library --routing=true --style=scss

## how to add Services/Component
npx ng/nx g s name-of-services-dir/name-of-service --project=name-of-library/name-of-app

npx ng/nx g c name-of-component-dir/name-of-component --project=name-of-library/name-of-app --style=scss

## how to Run
npx nx run name-of-app:serve --open --port 4200 
