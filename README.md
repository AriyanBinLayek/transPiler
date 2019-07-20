

<!--Babel -->

this is simple of example of babel transpiling from es6 to es5

npm install --save-dev babel-cli

After that has concluded, the babel-cli field will have been added to the devDependencies object in
the package.json file: {
"devDependencies": {

"babel-cli": "^6.26.0"

}
}

npm install --save-dev babel-preset-es2015

Once the command finishes running, our package.json file will
contain another dependency: "devDependencies": {

"babel-cli": "^6.26.0",

"babel-preset-es2015": "^6.24.1"

}


The scripts object allows us to run these commands from npm. We are going to
name the npm script transpile and it will run the command chain 

babelapp.js --out-file app.transpiled.js --source-maps

App.js is our input file. The --out-file command specifies the output file
for compilation. App.transpiled.js is our output file. Lastly, --
source-maps creates a source map file. This file tells the browser which line
of transpiled code corresponds to which lines of the original source. This allows
us to debug directly in the original source file, that is, app.js.


Now that we have everything set up, we can run our transpile script by typing
npm run transpile into the terminal window. This will transpile our code
from app.js into app.transpiled.js, creating or updating the file as
needed. Upon examination, we can see that the code in app.transpiled.js
has been converted into ES5 format. You can run the code in both files and see
that the output is the same.
Babel has many plugins and presets for different modules and JavaScript
releases. There are enough ways to set up and run Babel that we could write an
entire book about it. This was just a small preview for converting ES6 code to
ES5. For full documentation and information on Babel and the uses of each
plugin, visit the documentation.