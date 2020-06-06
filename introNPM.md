# ZTM_NPM

Install node.js on machine from website. Open repository in GitBash. Here are some commands: 

```gitattributes
Rob@RobPC MINGW64 ~/Documents/coding/zeromasterywebdev/JS/zeroMastery/bground_gen/background_generator (master)
$ npm -v                                                                                                                
6.14.4

Rob@RobPC MINGW64 ~/Documents/coding/zeromasterywebdev/JS/zeroMastery/bground_gen/background_generator (master)
$ node -v
v12.16.3

```

If you need update version, for node go to website. For NPM: 

```gitattributes
Rob@RobPC MINGW64 ~/Documents/coding/zeromasterywebdev/JS/zeroMastery/bground_gen/background_generator (master)
$ npm install npm@latest -g
```

If you get permission errors, need to run as administrator for apple use sudo command, need a different one for windows: 

```gitattributes

Rob@RobPC MINGW64 ~/Documents/coding/zeromasterywebdev/JS/zeroMastery/bground_gen/background_generator (master)
$ sudo npm install react      

```

To initiate NPM: 


```
Rob@RobPC MINGW64 ~/Documents/coding/zeromasterywebdev/JS/zeroMastery/bground_gen/background_generator (master)
$ npm init

This utility will walk you through creating a package.json file.
It only covers the most common items, and tries to guess sensible defaults.

See `npm help json` for definitive documentation on these fields
and exactly what they do.

Use `npm install <pkg>` afterwards to install a package and
save it as a dependency in the package.json file.

Press ^C at any time to quit.
version: (1.0.0)
description:
entry point: (script.js)
test command:
git repository: (https://github.com/robhami/background_generator.git)
keywords:
author:
license: (ISC)
About to write to C:\Users\Rob.000\Documents\coding\zeromasterywebdev\JS\zeroMastery\bground_gen\background_generator\package.json:

{
  "name": "background_generator",
  "version": "1.0.0",
  "description": "",
  "main": "script.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "repository": {
    "type": "git",
    "url": "git+https://github.com/robhami/background_generator.git"
  },
  "author": "",
  "license": "ISC",
  "bugs": {
    "url": "https://github.com/robhami/background_generator/issues"
  },
  "homepage": "https://github.com/robhami/background_generator#readme"
}


Is this OK? (yes)

```

Adds .json file to directory: 

```
{
  "name": "background_generator",
  "version": "1.0.0",
  "description": "",
  "main": "script.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "repository": {
    "type": "git",
    "url": "git+https://github.com/robhami/background_generator.git"
  },
  "author": "",
  "license": "ISC",
  "bugs": {
    "url": "https://github.com/robhami/background_generator/issues"
  },
  "homepage": "https://github.com/robhami/background_generator#readme"
}
```

### Downloading packages ###

If download locally, only saves package to project folder. If download globally (using -g) can use package outside of folder anywhere on computer. 


```gitattributes

Rob@RobPC MINGW64 ~/Documents/coding/zeromasterywebdev/JS/zeroMastery/bground_gen/background_generator (master)
$ npm install -g live-server

```
To run package: 

```gitattributes
Rob@RobPC MINGW64 ~/Documents/coding/zeromasterywebdev/JS/zeroMastery/bground_gen/background_generator (master)
$ live-server
Serving "C:\Users\Rob.000\Documents\coding\zeromasterywebdev\JS\zeroMastery\bground_gen\background_generator" at http://127.0.0.1:8080
Ready for changes
GET /favicon.ico 404 1.955 ms - 150
```
liverserver creates a server and watches for changes. i.e.  with change css it detects it and changes it: 

```gitattributes
CSS change detected C:\Users\Rob.000\Documents\coding\zeromasterywebdev\JS\zeroMastery\bground_gen\background_generator\style.css

```

use ctrl + C to quit live-server.

To locally install package: 

```gitattributes

Rob@RobPC MINGW64 ~/Documents/coding/zeromasterywebdev/JS/zeroMastery/bground_gen/background_generator (master)
$ npm install lodash 

```

This adds new line in json file: 

```
"dependencies": {
    "lodash": "^4.17.15"
```

Also adds folder called node_modules.

Can use lodash as follows by adding to script.js file at top: 

```
var _ = require('lodash');

console.log(_);

```

You need to install and run browserify: 

```gitattributes

Rob@RobPC MINGW64 ~/Documents/coding/zeromasterywebdev/JS/zeroMastery/bground_gen/background_generator (master)
$ npm install -g browserify
C:\Users\Rob.000\AppData\Roaming\npm\browserify -> C:\Users\Rob.000\AppData\Roaming\npm\node_modules\browserify\bin\cmd.js
+ browserify@16.5.1
added 146 packages from 117 contributors in 46.115s

Rob@RobPC MINGW64 ~/Documents/coding/zeromasterywebdev/JS/zeroMastery/bground_gen/background_generator (master)
$ browserify script.js>bundle.js

```

This creates a bundle.js file in folders. Change index.html to point to bundle.js instead of script.js: 

```
<script type="text/javascript" src="bundle.js"></script>
```

Add lodash method to script.js,need to use the _ to call lodash:

```
var array = [1,2,3,4,5,6,7,8];

console.log('answer:', _.without(array, 3));
```

Then add it to the bundle.js file using terminal: 

```
Rob@RobPC MINGW64 ~/Documents/coding/zeromasterywebdev/JS/zeroMastery/bground_gen/background_generator (master)
$ browserify script.js>bundle.js
```

This then shows without method console.log in console: 

```
answer: Array(7)
0: 1
1: 2
2: 4
3: 5
4: 6
5: 7
6: 8
length: 7__proto__: Array(0)
```

Packages will add weight to project, be careful. 

Also now have dependancies, so app always needs access to the packages. It also adds an extra layer of complexity. json file will tell you what packages your project depends on. Can also update versions in json. 

version numbers are called semver: Semantic Versioning. Each number has a meaning: 

right most number is patch release. Middle number is minor release. Left most number isthe major release: 

e.g. "^4.17.4"

Even if lodash package gets deleted can still use and when do npm install locally it add them back into local folders. 

There is another type dependancy- dev dependancy: Packages only needed for development and testing. So have a separate section for dev dependancies in JSON file. 

If we do the following: 

```
Rob@RobPC MINGW64 ~/Documents/coding/zeromasterywebdev/JS/zeroMastery/bground_gen/background_generator (master)
$ npm run test

> background_generator@1.0.0 test C:\Users\Rob.000\Documents\coding\zeromasterywebdev\JS\zeroMastery\bground_gen\background_generator
> echo "Error: no test specified" && exit 1
```


This is because that is what is defined in json file: 

```

 "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  
```

Can edit this as follows: 

```
 "scripts": {
    "build": "browserify script.js > bundle.js && live-server"
  },
  
```

This can now be run to automate browserify transfer from script.js to bundle.js and start live-server: 

```gitattributes

Rob@RobPC MINGW64 ~/Documents/coding/zeromasterywebdev/JS/zeroMastery/bground_gen/background_generator (master)
$ npm run build

> background_generator@1.0.0 build C:\Users\Rob.000\Documents\coding\zeromasterywebdev\JS\zeroMastery\bground_gen\background_generator
> browserify script.js > bundle.js

```

Inportant to keep packages up to date. If you go to json file in github. Go to security alerts to see where issues are.
