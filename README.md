# aurizon
NodeJS ExpressJS MySql MongoDB TypeScript Mocha Chai 
Description
The what, why, and how:

Every good project needs a quality README with information about the app - what the app is for, how to use the app, how to install it, how to report issues, and how to make contributions so that other developers are more likely to use and contribute to the success of the project.

This is a command-line application that runs with Node.js that dynamically generates a README.md file based on input about your project. Check out the ExampleREADME.md in this repo as an example.

Table of Contents
Installation
Usage
Methodology
License
Installation
To generate your own README, git clone the repo down to your local so you have the Node project on your local.

Run npm install in order to install the following npm package dependencies as specified in the package.json:

inquirer will prompt you for your inputs from the command line.
axios will fetch your info from the GitHub API.
The application will start by running node index.js in the command line.

Answer the prompts in your command line to generate the README.

After answering all the prompts, your README file will be named 'ExampleREADME.md' and will be ready for you at the root of the repo.

The README has some automatically generated badges for your repo courtesy of shields.io and will include your profile picture & email from GitHub.

Usage
Gif demo of README-generator

When you run node index.js, the application uses the inquirer package to prompt you in the command line with a series of questions about your GitHub and about your project.

The application then takes your responses and uses axios to fetch your GitHub profile from the GitHub API, including your GitHub profile picture (avatar) and email. From there, the application will generate markdown and a table of contents for the README conditionally based on your responses to the Inquirer prompts (so, if you don't answer the optional questions, such as Installation, an Installation section will not be included in your README). The README will also include badges for your GitHub repo.

Finally, fs.writeFile is used to generate your project's README.md file. Check out the ExampleREADME.md in this repo as an example on the final output.

The lorem ipsum is generated thanks to Social Good Ipsum.

Methodology
The application utilizes modularization by separating the GitHub API call and generation of the markdown into separate modules: api.js and generateMarkdown.js, respectively, inside the utils folder.

The application also utilizes, as much as possible, syntax and paradigms introduced in ES6 and beyond, including:

Arrow functions,
const, let,
Template literals, and
async/await to handle inquirer, axios, and fs.writeFile promises.
License
