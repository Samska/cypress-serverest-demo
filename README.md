[![Cypress Tests](https://github.com/Samska/cypress-serverest/actions/workflows/cypress.yml/badge.svg)](https://github.com/Samska/cypress-serverest/actions/workflows/cypress.yml)
[![Badge ServeRest](https://img.shields.io/badge/API-ServeRest-green)](https://github.com/ServeRest/ServeRest/)

# Cypress E2E and API tests in ServeRest application

This is a study project using Cypress for E2E and API testing in the application <https://serverest.dev> and <https://front.serverest.dev>.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

## Prerequisites

- Git
- Node.JS
- NPM

## Installing

1. Clone the repository
2. Install the dependencies:

`npm install` - Installs all dependencies included in `package.json`

## Running the scripts

`npm test` - Runs all project tests in headless mode

`npm open` - Opens the Cypress execution interface

`npm after-test` - Combines the reports generated by mochawesome and generates an html report

## Continuous integration

This project has continuous integration with GitHub Actions. The configuration file is located at the path `.github/workflows/cypress.yml`. Every time a push is made to the main branch, the pipeline is executed. With each execution, an artifact is generated with the test results and saved in that execution, as well as the results are published on the gh-pages and are available for consultation on this [page](https://samska.github.io/cypress-serverest/report.html).

## Folder structure

```
cypress-serverest-demo/          
 ├── .github/                               
 │    ├── workflows/                        
 │        ├── cypress.yml                           # Configuration for the tests on CI           
 ├── cypress/                                       # Cypress root folder                               
 │    ├── fixtures/                                 # Static data files used in tests
 │        ├── *.json                     
 │        ├── *.csv                     
 │        ├── *.png
 │    ├── screenshots/                              # Screenshots taken of the tests that are failing
 │        ├── api/
 │          ├── *.png
 │        ├── e2e/
 │          ├── *.png
 │    ├── support/                                  # Reusable code files to avoid repetition in the tests
 │        ├── api/
 │          ├── user-commands.js
 │        ├── e2e/
 │          ├── create-user-commands.js
 │        ├── e2e.js                                # Use this file to import any cypress custom command
 │    ├── tests/                                    # Project tests separated by test type folder     
 │        ├── api/
 │          ├── user.cy.js
 │        ├── e2e/
 │          ├── create-user.cy.js
 │    ├── videos/                                   # Recorded videos of the tests that are failing
 │        ├── api/
 │          ├── *.mp4
 │        ├── e2e/
 │          ├── *.mp4
 ├── node_modules/                                  # Where all of the project dependencies are stored
 ├── .gitignore                                     # Untracked folder and files
 ├── cypress.config.js                              # The main configuration file for cypress, set behaviors, timeout and other props here
 ├── package-lock.json                              # File that is auto generated when a package is installed via npm      
 ├── package.json                                   # Core file in node.js projects, used for dependency management, scripts, project metadata and configs
 ├── README.md                                      # README with project overview and instructions
```
