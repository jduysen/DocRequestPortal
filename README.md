# doc-request-portal

## Summary

This is a custom SPFx webpart that aims to improve the document request process in the organization

![alt text](https://github.com/jduysen/DocRequestPortal/blob/main/docrequest.gif?raw=true)

## Used SharePoint Framework Version

![version](https://img.shields.io/badge/version-1.11-green.svg)

## Used React Version

![version](https://img.shields.io/badge/version-15-blue.svg)


## Prerequisites

Set up environmnet (only need to run once) Install Node version 10.23 npm install -g gulp@3.9.1 npm install -g yo@3.1.0 npm install -g @microsoft/generator-sharepoint

Generate SPFx project: Create a folder where the project will live and open a command prompt in that location. yo @microsoft/sharepoint --skip-install (Go through the questions in the generator) Once generator is finished run "code ." to open the project in VSCode

Required for most spfx projects: npm i @pnp/sp npm i npm-force-resolutions npm i typescript@3.6.4 npm i @pnp/spfx-controls-react@1.19.0 npm i rimraf

Optional: npm install react-filepond filepond --save (if project requires file upload) npm i react-google-charts@2 (if project requires charts) npm i react-chartjs-2@2.11.1 (if project requires charts) npm i tableau-react (if project requires embedded tableau)

Optional but recommended: npm install spfx-fast-serve -g after install run: spfx-fast-serve

add "preinstall": "npx npm-force-resolutions" to package.json "scripts" add "resolutions": { "typescript": "3.6.4" },

rimraf node_modules npm install npm run serve(if using spfx-fast-serve) otherwise gulp serve

To Bundle and ship project (generate binary to be placed in app catelog on SP):

//gulp clean gulp build gulp bundle --ship gulp package-solution --ship Package will be in sharepoint/solution folder in your project.

## Solution

Solution|Author(s)
--------|---------
DocRequestPortal | James Duysen, TSB

## Version history

Version|Date|Comments
-------|----|--------
0.1|February 9, 2022|Beta



## Minimal Path to Awesome

- Clone this repository
- Ensure that you are at the solution folder
- in the command-line run:
  - **npm install**
  - **gulp serve**

> Include any additional steps as needed.

## Features

Has Request and My Assignments views where users can add new doc requests and assign users or view and complete their assignments by uploading documents.  Users can flag assignments and indicate N/A.  Request owners can download their completed requests.

## References

- [Getting started with SharePoint Framework](https://docs.microsoft.com/en-us/sharepoint/dev/spfx/set-up-your-developer-tenant)
- [Building for Microsoft teams](https://docs.microsoft.com/en-us/sharepoint/dev/spfx/build-for-teams-overview)
- [Use Microsoft Graph in your solution](https://docs.microsoft.com/en-us/sharepoint/dev/spfx/web-parts/get-started/using-microsoft-graph-apis)
- [Publish SharePoint Framework applications to the Marketplace](https://docs.microsoft.com/en-us/sharepoint/dev/spfx/publish-to-marketplace-overview)
- [Microsoft 365 Patterns and Practices](https://aka.ms/m365pnp) - Guidance, tooling, samples and open-source controls for your Microsoft 365 development
