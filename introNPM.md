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




