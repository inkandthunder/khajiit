# Khajiit

### Description

This is a personal-use generic Javascript development environment boilerplate.

### Status
|System|Status|
|--|--|
|Appveyor|[![Build status](https://ci.appveyor.com/api/projects/status/hnyhqrged5w252jd/branch/master?svg=true)](https://ci.appveyor.com/project/inkandthunder/ps-js-dev-env/branch/master)|
|Travis|![Travis Build Status](https://travis-ci.org/inkandthunder/ps-js-dev-env.svg?branch=master)|

### Features

* [Babel](https://babeljs.io/) for new JS features: [es2015](https://babeljs.io/docs/plugins/preset-es2015/), [stage-2](http://babeljs.io/docs/plugins/preset-stage-2/), [JSX](https://babeljs.io/docs/plugins/preset-react/) for React
* [Express server](https://github.com/expressjs/express/)
* [Webpack](https://webpack.github.io/) for bundling, middleware support, and hot reloading 
* [Travis CI](https://travis-ci.org/)
* [ESLint](https://github.com/eslint/eslint) for ES6
* Cache busting and bundle splitting
* Auto rebuild
* [Mocha](https://github.com/mochajs/mocha)
* [Localtunnel](https://github.com/localtunnel/localtunnel)
* [Appveyor CI](https://www.appveyor.com/)
* Mock data generator using [JsonServer](https://github.com/dreyacosta/JSONServer) and [Faker](https://github.com/Marak/faker.js)
* [Cheerio](https://github.com/cheeriojs/cheerio) for querying DOM with jQuery like syntax
* [Chai](https://github.com/chaijs/chai) assertion framework
* [Cross-env](https://github.com/kentcdodds/cross-env) environment scripting helper
* Polyfills
* [Rimraf](https://github.com/isaacs/rimraf)
* Up-to-date dependencies

### Instructions

1. **Install [Node 6](https://nodejs.org)**. Need to run multiple versions of Node? Use [nvm](https://github.com/creationix/nvm) or [nvm-windows](https://github.com/coreybutler/nvm-windows)
2. **Clone this repository.** - `git clone https://github.com/inkandthunder/khajiit.git` or [download the zip](https://github.com/inkandthunder/khajiit/archive/master.zip)
3. **Make sure you're in the directory you just created.** - `cd khajiit`
4. **Install Node Packages.** - `npm install`
5. **Run the app.** - `npm start -s`
This will run the automated build process, start up a webserver, and open the application in your default browser. When doing development with this kit, this command will continue watching files all your files. Every time you hit save the code is rebuilt, linting runs, and tests run automatically. Note: The -s flag is optional. It enables silent mode which suppresses unnecessary messages during the build.
6. Having issues? See below.

### Issues

1. Run `npm install` - If you forget to do this, you'll see this: `babel-node: command not found`.
2. Make sure you're running the latest version of Node. Or, use [Node 6.9.1](https://nodejs.org/en/download/releases/) if you're having issues on Windows. Node 7 has issues on some Windows machines.
3. Make sure files with names that begin with a dot (.babelrc, .editorconfig, .eslintrc) are copied to the project directory root. This is easy to overlook if you copy this repository manually.
4. Don't run the project from a symbolic link. It will cause issues with file watches.
5. Having linting issues? Delete any .eslintrc that you're storing in your user directory. Also, disable any ESLint plugin / custom rules that you've enabled within your editor. These will conflict with the ESLint rules defined in the course.
6. Seeing `Error: listen EADDRINUSE :::3000`? That means port 3000 is already in use on your machine. You probably have another instance of this project running on your machine in a different window. So find that window and kill the other instance using Ctrl+C.
7. Nothing above work? Delete your node_modules folder and re-run npm install.

## License

Copyright 2018 Scott DeHaan, et al.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the 'Software'), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
