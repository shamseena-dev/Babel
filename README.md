# Babel
Playing with BABEL :-)

## Notes for Installing BABEL

https://babeljs.io/docs/en/usage

## STEPS I FOLLOWED:
 
 #1. 
 npm install --save-dev @babel/core @babel/cli @babel/preset-env
 
 npm install --save @babel/polyfill
 
 #2 . Creating a config file named babel.config.js in the root of your project with this content: 
 
 const presets = [
  [
    "@babel/env",
    {
      targets: {
        edge: "17",
        firefox: "60",
        chrome: "67",
        safari: "11.1",
      },
      useBuiltIns: "usage",
    },
  ],
];

module.exports = { presets };

#3. npx babel src --out-dir lib  // i used 
-or -
./node_modules/.bin/babel src --out-dir lib

//get a message succesfully compiled 2 files
//2 new files in a new folder  lib appears

#4.  Plugins & Presets

 we also have other ES2015+ features in our code that we want transformed. Instead of adding all the plugins we want one by one, we can use a "preset" which is just a pre-determined set of plugins.
 
 //Now all ES6 would be converted to ES5 version in the app.js file in lib folder
 

npm install --save-dev @babel/preset-env

./node_modules/.bin/babel src --out-dir lib --presets=@babel/env
0r--
npx babel src --out-dir lib --presets=@babel/env  /////i used ////
