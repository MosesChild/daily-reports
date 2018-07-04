# Daily Activity

## 6/4/2018

### debugES6 project in VScode
Followed the instructions at [debugging-es6-in-visual-studio-code](https://medium.com/@drcallaway/debugging-es6-in-visual-studio-code-4444db797954)

## Purpose
- figure out how to use my own es6 modules in browser(should be available in all of the latest browsers!)
- to solidify es6 module style coding within node for html5-audio project.
- Understand launch.json(vs-code) and package.json(npm config) files.
- vs-code workflow - make debugger available on transpiled code at the src file!

## Conclusion
### In the browser
No significant work was necessary (other than using correct terminology at the index.html file.  Script tags must point to the main js file and have the parameter type="module"...

```
<script type="module" src="./src/app.js"></script>
```
Then es6 imports/exports work as expected with as many external module files as necessary.

### Importing npm modules to Browser
After the success of using es6 imports with my own module file, I thought I would look into also using npm modules...(much agreement that npm is where its at (for front-end too! )
All the resources agreed (plus my own experiments) you need to use some build tool. 

The established contenders are browserify and webpack and Rollup.

## 6/5/2018

Started this Daily Activity Log to better organize and direct my efforts to acheive my developing goals.

Investigated and solved ESLint problem...
- followed instruction to install globally
    - npm install -g eslint

Worked through sitepoint's [es6-babel-webpack](https://www.sitepoint.com/es6-babel-webpack/) 
tutorial.

Work was interrupted (10AM-) for most of the day by power interruption!

## 6/6/2018
Finished es6-babel-webpack tutorial...
Reviewed code and logs from last two projects to understand what I have learned and where I need to go...
### Next step...

Get transpiling setup (using webpack in vscode) that enables es6 & npm modules in the browser with debugging...

#### started project vscode-webpack-debug
* used webpack extension.
* debugged various problems with initial webpack.config parameters.
* got it to build with npm script.
* Got it to work with my own modules.
* Got it to work with npm modules.
* Created/Edited launch.json to work with index.html and app.js as separate configurations so that I could use vs-code debugging features. 

## 6/7/2018
* Investigated git repository for [webpack extension](https://github.com/remicass/vscode-exts/tree/master/webpack) to see how it works and if I might be able to fix my problems with it easily.
*  Looked at **Bower** (because it uses Bower) as I was unfamiliar with it.
    * Read Medium article to get latest word on it and was made aware that it is no longer relevant (unless you are currently using it.) Bower recommends that devs migrate to npm and Webpack.

* Started a new project: **ES6 template** that I can use to start my es6 projects and base a bash script or vscode extension on. I hope to see if I can make a bash script that will do all the setup work for a user.  
* Looked into webpack 4's zero-configuration.[easy instructions](https://www.valentinog.com/blog/webpack-4-tutorial/#webpack_4_as_a_zero_configuration_module_bundler)
    - still needs a webpack.config.js file for using loaders and also for using transpiler for debugger.
    * also valentino also uses the .babelrc file to "traditionally" use the babel loader, though he shows that you can do it within the package.json file.

## 6/8/2018
Configured html5 to es6 module style code (no transpiling.)

## 6/19/2018
Completed codecademy angular lesson to familiarize myself with it.
Checked top software-development articles this week.

* Studied [ES6 generator functions and reviewed iterators](https://codeburst.io/javascript-generator-yield-next-async-await-e428b0cb52e4)
* Discovered [Dev-to](https://dev.to/) community.
* Looked a bit into now defunct Dart (to create stand-alone apps that are platform independent.)  This dead-end ended up getting me looking into **PWA**'s or Progressive Web Apps.
	* Read blog and watched youtube video of Ada Rose Cannon which prompted me to look further into web-components as a way to possibly package my own helper library for my audio-components module.
	* Looked at some pre-packaged "practical collection of everyday Web Components" called [Bosonic](https://bosonic.github.io/)
		* Promising collection worth further investigation as it includes **tooltips, modals, dialogs dropdowns, accordians, etc _including transitions_** in short... bootstrap like capabilities in custom html components.
	* Looked into [Stencil](https://stenciljs.com/) (by iconic) to help me package my own web components.
		Watched video at stencil about iconic and web-components.  It made WC's look even more attractive (and I decided its finally time for me to transition to TypeScript...
		* Looked at [React-Native vs ionic-2 framework stackup](https://medium.com/swlh/react-native-vs-ionic-2-comparison-50aba900be6c) just to see the differences (because I have been planning on learning React-Native.
* Setup **AudioComponents**, as a git and github repo to house my multi-root audio component project.
	* Setup **Midi** & **Keyboard** folders in AudioComponents as Git and Github repos.
	* Created **exclude patterns** for .git/info/exclude for above projects.
	* Created working **keyboard.html** file (in AudioComponents) that leverages both keyboard and midi modules...
## 6/20/2018
Studied developers.google.com to start working with making my own custom Elements (as a prelude to learning to make **PWA**s.
* Created a **customElements** project to experiment with creating my own customElements.
	* After initial simple successes, created a "vert-fader" element that both encapsulated style and slotted in a title for a fader element.  This stylized vertical range-slider (custom Element) looks the same on all browsers...  More work needed to test to see if it works.

## 6/21/2018

Worked all day on **customElements** project.
Created vert-fader implementation with input/number display... But probably not ideal as it remakes inputs to deal with shadow-dom, but it works and looks ok...
See customElements for further documentation.

## 6/22/2018
Looked on stack-exchange to further compare two existing mobile platform frameworks:
* **React Native**
* **Ionic**

Then worked to create my own first Progressive Web Application (**VS-Code Projects/first-PWA**) with the tutorial [creating your first PWA](https://codelabs.developers.google.com/codelabs/your-first-pwapp/#1) from developers.google.

- Installed **Web Server for Chrome** which enables serving local files.

## 6/23/2018
Finished **first-PWA** project.
 * caching both app and data files seperately (cache-first network on return.)
 * included - manifest.json to make it available on homescream for Chrome,
 * tested on mobile device (by allowing chrome server to serve accross local network.

### Conclusions on first-PWA project.

This was an excellent tutorial, showing how easy it is to create multi platform PWA's... Also showed me the chrome server (excellent and easy for testing) the cache API and encouraged discovery and use of the indexDB api (and libraries) for production ready sites.

## 6/25/2018

### TypeScript 5 minute start ([typescript website walkthrough](https://www.typescriptlang.org/docs/handbook/typescript-in-5-minutes.html))
  * Global installed TypeScript compiler
  * Looked at 'interface' a term brought from other 'classic' oop languages.  It describes the variable names and static types required for a method to work.
  * also viewed compiled output... This in someways is a turn-off because it shows how class is just syntactic sugar on javascripts prototypal system...  It ends up with object instantiation (using 'new') a completely unnecessary construct in javascript.  My understanding of Eric Elliot and design patterns is to prefer construction over inheritance!
  * Still, type checking is cool, and Eric Elliot does advocate use of typescript partly just to get the functionality of 
	* parameter help based on the types of the DOM elements
  * Also cool...
	* symbol renaming.
	* handy-dandy symbol refactoring! Handy  Just right click on any text to turn it into a function in same scope or global scope.
	  * NOT just typescript, available in javascript (and probably other languages) in vscode!

### Read TypeScript [Handbook](https://www.typescriptlang.org/docs/handbook/basic-types.html)
#### Basic Types
* Looked at how basic types are declared.
  * generally easy... just add ':' + the variable type between the declaration and the assignment... like
    * let isDone: boolean = false;
	* let decimal: number = 6;
	* let color: string = "blue";
  * Arrays are similar but require both the type of contents and that it is an array...
   They can be declared and defined two ways...
    * let list: number[] = [1, 2, 3];
	* let list: Array<number> = [1, 2, 3];
	
* Mixed Type arrays are called **tuple**s and are declared...

```javascript
// Declare a tuple type
let x: [string, number];
// Initialize it
x = ["hello", 10]; // OK
// Initialize it incorrectly
x = [10, "hello"]; // Error
```

New concepts 
	Enum

### VS-Code [TypeScript walkthrough](https://code.visualstudio.com/docs/languages/typescript)
* Installed typeScript compiler.( npm install -g typescript )
* made HelloWorld.ts
* setup tsconfig.json (first by cut/paste, then with better 'tsc --init' which shows all of the possible options *commented out.*

Tried to do standard 'Run Build Task' from vscode **tasks** menu.
#### Ran into issues:
[The default Typescript build task v2.0.0 does not work with the bash-based integrated terminal #40907](https://github.com/Microsoft/vscode/issues/40907) Due to VS-code trying to make things easy for users, it creates default build and watch tasks for typescript... Unfortunately they don't work with WSL (windows subsystem linux.) 

I also wanted to be able to do debugging within vs-code across the tranpiled code which requires that typeScript also create source-maps (which the built in debugger must be configured to use.)

 This forced me to make my own build tasks.  

Created my own build tasks for **build** and **watch**.  This was done by editing the **.vscode/tasks.json** file to use the same switches as you would on the command line.

```javascript
    "tasks": [
        {
            "label": "tsc: build for WSL tsconfig.json",
            "type": "shell",
            "command": "tsc --sourceMap -p tsconfig.json",
            "presentation": {
                "reveal": "always",
                "panel": "new"
            },
            "problemMatcher": [
                "$tsc"
            ]
        },
        {
            "label": "tsc: watch for WSL tsconfig.json",
            "type": "shell",
            "command": "tsc --sourceMap -w -p tsconfig.json",
            "problemMatcher": [
                "$tsc-watch"
            ],
            "group": {
                "kind": "build",
                "isDefault": true
            }
        },
    ]
```

This solution leaves the original "type":"typescript" defaults (don't know how to remove them!) so if selecting a task from the task menu, make sure to use the ones in labelled as above "tsc: build for WSL tsconfig.json" rather than the defaults.

Also... This makes the "watch" task the default task, so if you run the default tsc task it will start watching the files for changes.  Change the default by moving the "group" attributes object (with "kind" and "isDefault") to the task you want as default.)

To make transpiled debugging work (again with WSL)...   you need a launch.json file:

```javascript
     "configurations": [
        {
            "type": "node",
            "request": "launch",
            "name": "Launch Program",
            "useWSL":true,
            "sourceMaps": true,
            "program": "${workspaceFolder}/greeter.js"
        }
	]
```

#### CodeLens
### Conclusions to VS-Code Walkthrough
More options are available for configuring where the output '.js' files are, for whether vs-code hides these derived files, using a local or specific TypeScript versions, etc... This can be found [here.](https://code.visualstudio.com/docs/languages/typescript)




* Notepad+++ working slowly and erraticly...
### Idea for project: 
#### Update Markdown project from FreeCodeAcademy to be a PWA.  A perfect candidate to practice PWA skills from last project.


### Started markup-pwa project
bootstrapped in 'VS-Code Projects' directory 

## 6/26/2018
Worked extensively to transport and update markdown code from my codepen to vscode.  Details can be found on Github [markdown-pwa](https://github.com/MosesChild/markdown-pwa)


## 6/27/2018
* Worked on markdown-pwa
* Read MDN's Server-side Introduction](https://developer.mozilla.org/en-US/docs/Learn/Server-side/First_steps/Introduction)
	* Static vs Dynamic sites.  

## 6/28/2018
Started day working on learning how to use slider in react-material components (for markdown-pwa.)  
Decided that it was time to really learn REDUX.
Worked on Redux creator **Dan Abramov** [Getting started with Redux](https://egghead.io/courses/getting-started-with-redux)
video lessons.  

Started redux-lessons project folder to go through examples.  Work was slow because he was in JS-bin and I was working in VS-Code.  This required I use a server so I used create-react-app to scaffold a my-app project inside the redux-lessons.
  
It was also a bit dated: a bunch of test-driven examples using 'expect' library (out of date, Abramov gave the code to jest!)

## 6/29/2018
Worked through Dan Abramov Redux lessons...

## 7/3/2018
Finished final Redux Lesson and documented my code (redux-lessons.)
Looked through other recommeded resources:  
* [devguides](http://devguides.io/redux/react) - great guide with minimalized explanations.

Decided that to cement my knowledge I must apply redux to a real react project...

### markdown-pwa
* Refactored code to separate version with collapsable.
* Removed material UI components and made simpler header.
* Created hideable element to replace collapsable.


	
