# api documentation for  [shelljs (v0.7.7)](http://github.com/shelljs/shelljs)  [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-shelljs.svg)](https://travis-ci.org/npmdoc/node-npmdoc-shelljs)
#### Portable Unix shell commands for Node.js

[![NPM](https://nodei.co/npm/shelljs.png?downloads=true)](https://www.npmjs.com/package/shelljs)

[![apidoc](https://npmdoc.github.io/node-npmdoc-shelljs/build/screen-capture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-shelljs_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-shelljs/build..beta..travis-ci.org/apidoc.html)

![package-listing](https://npmdoc.github.io/node-npmdoc-shelljs/build/screen-capture.npmPackageListing.svg)



# package.json

```json

{
    "bin": {
        "shjs": "./bin/shjs"
    },
    "bugs": {
        "url": "https://github.com/shelljs/shelljs/issues"
    },
    "contributors": [
        {
            "name": "Nate Fischer",
            "email": "ntfschr@gmail.com",
            "url": "https://github.com/nfischer"
        },
        {
            "name": "Brandon Freitag",
            "email": "freitagbr@gmail.com",
            "url": "https://github.com/freitagbr"
        }
    ],
    "dependencies": {
        "glob": "^7.0.0",
        "interpret": "^1.0.0",
        "rechoir": "^0.6.2"
    },
    "description": "Portable Unix shell commands for Node.js",
    "devDependencies": {
        "ava": "^0.16.0",
        "codecov": "^1.0.1",
        "coffee-script": "^1.10.0",
        "eslint": "^2.0.0",
        "eslint-config-airbnb-base": "^3.0.0",
        "eslint-plugin-import": "^1.11.1",
        "nyc": "^10.0.0",
        "shelljs-changelog": "^0.2.0",
        "shelljs-release": "^0.2.0",
        "shx": "^0.2.0",
        "travis-check-changes": "^0.2.0"
    },
    "directories": {},
    "dist": {
        "shasum": "b2f5c77ef97148f4b4f6e22682e10bba8667cff1",
        "tarball": "https://registry.npmjs.org/shelljs/-/shelljs-0.7.7.tgz"
    },
    "engines": {
        "iojs": "*",
        "node": ">=0.11.0"
    },
    "files": [
        "commands.js",
        "global.js",
        "make.js",
        "plugin.js",
        "shell.js",
        "bin",
        "src"
    ],
    "gitHead": "95638cc773390920a446e383c40ed8104c7d211d",
    "homepage": "http://github.com/shelljs/shelljs",
    "keywords": [
        "shelljs",
        "bash",
        "unix",
        "shell",
        "makefile",
        "make",
        "jake",
        "synchronous"
    ],
    "license": "BSD-3-Clause",
    "main": "./shell.js",
    "maintainers": [
        {
            "name": "artur",
            "email": "arturadib@gmail.com"
        },
        {
            "name": "freitagbr",
            "email": "freitagbr@gmail.com"
        },
        {
            "name": "nfischer",
            "email": "ntfschr@gmail.com"
        }
    ],
    "name": "shelljs",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/shelljs/shelljs.git"
    },
    "scripts": {
        "after-travis": "travis-check-changes",
        "changelog": "shelljs-changelog",
        "codecov": "codecov",
        "gendocs": "node scripts/generate-docs",
        "lint": "eslint .",
        "posttest": "npm run lint",
        "release:major": "shelljs-release major",
        "release:minor": "shelljs-release minor",
        "release:patch": "shelljs-release patch",
        "test": "nyc --reporter=text --reporter=lcov ava --serial test/*.js",
        "test-no-coverage": "ava --serial test/*.js"
    },
    "version": "0.7.7"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module shelljs](#apidoc.module.shelljs)
1.  [function <span class="apidocSignatureSpan">shelljs.</span>ShellString (stdout, stderr, code)](#apidoc.element.shelljs.ShellString)
1.  [function <span class="apidocSignatureSpan">shelljs.</span>cat ()](#apidoc.element.shelljs.cat)
1.  [function <span class="apidocSignatureSpan">shelljs.</span>cd ()](#apidoc.element.shelljs.cd)
1.  [function <span class="apidocSignatureSpan">shelljs.</span>chmod ()](#apidoc.element.shelljs.chmod)
1.  [function <span class="apidocSignatureSpan">shelljs.</span>cp ()](#apidoc.element.shelljs.cp)
1.  [function <span class="apidocSignatureSpan">shelljs.</span>dirs ()](#apidoc.element.shelljs.dirs)
1.  [function <span class="apidocSignatureSpan">shelljs.</span>echo ()](#apidoc.element.shelljs.echo)
1.  [function <span class="apidocSignatureSpan">shelljs.</span>error ()](#apidoc.element.shelljs.error)
1.  [function <span class="apidocSignatureSpan">shelljs.</span>exec ()](#apidoc.element.shelljs.exec)
1.  [function <span class="apidocSignatureSpan">shelljs.</span>exit ()](#apidoc.element.shelljs.exit)
1.  [function <span class="apidocSignatureSpan">shelljs.</span>find ()](#apidoc.element.shelljs.find)
1.  [function <span class="apidocSignatureSpan">shelljs.</span>grep ()](#apidoc.element.shelljs.grep)
1.  [function <span class="apidocSignatureSpan">shelljs.</span>head ()](#apidoc.element.shelljs.head)
1.  [function <span class="apidocSignatureSpan">shelljs.</span>ln ()](#apidoc.element.shelljs.ln)
1.  [function <span class="apidocSignatureSpan">shelljs.</span>ls ()](#apidoc.element.shelljs.ls)
1.  [function <span class="apidocSignatureSpan">shelljs.</span>mkdir ()](#apidoc.element.shelljs.mkdir)
1.  [function <span class="apidocSignatureSpan">shelljs.</span>mv ()](#apidoc.element.shelljs.mv)
1.  [function <span class="apidocSignatureSpan">shelljs.</span>popd ()](#apidoc.element.shelljs.popd)
1.  [function <span class="apidocSignatureSpan">shelljs.</span>pushd ()](#apidoc.element.shelljs.pushd)
1.  [function <span class="apidocSignatureSpan">shelljs.</span>pwd ()](#apidoc.element.shelljs.pwd)
1.  [function <span class="apidocSignatureSpan">shelljs.</span>rm ()](#apidoc.element.shelljs.rm)
1.  [function <span class="apidocSignatureSpan">shelljs.</span>sed ()](#apidoc.element.shelljs.sed)
1.  [function <span class="apidocSignatureSpan">shelljs.</span>set ()](#apidoc.element.shelljs.set)
1.  [function <span class="apidocSignatureSpan">shelljs.</span>sort ()](#apidoc.element.shelljs.sort)
1.  [function <span class="apidocSignatureSpan">shelljs.</span>tail ()](#apidoc.element.shelljs.tail)
1.  [function <span class="apidocSignatureSpan">shelljs.</span>tempdir ()](#apidoc.element.shelljs.tempdir)
1.  [function <span class="apidocSignatureSpan">shelljs.</span>test ()](#apidoc.element.shelljs.test)
1.  [function <span class="apidocSignatureSpan">shelljs.</span>touch ()](#apidoc.element.shelljs.touch)
1.  [function <span class="apidocSignatureSpan">shelljs.</span>uniq ()](#apidoc.element.shelljs.uniq)
1.  [function <span class="apidocSignatureSpan">shelljs.</span>which ()](#apidoc.element.shelljs.which)
1.  object <span class="apidocSignatureSpan">shelljs.</span>config
1.  object <span class="apidocSignatureSpan">shelljs.</span>env

#### [module shelljs.config](#apidoc.module.shelljs.config)
1.  boolean <span class="apidocSignatureSpan">shelljs.config.</span>fatal
1.  boolean <span class="apidocSignatureSpan">shelljs.config.</span>noglob
1.  boolean <span class="apidocSignatureSpan">shelljs.config.</span>silent
1.  boolean <span class="apidocSignatureSpan">shelljs.config.</span>verbose
1.  [function <span class="apidocSignatureSpan">shelljs.config.</span>reset ()](#apidoc.element.shelljs.config.reset)
1.  [function <span class="apidocSignatureSpan">shelljs.config.</span>resetForTesting ()](#apidoc.element.shelljs.config.resetForTesting)
1.  number <span class="apidocSignatureSpan">shelljs.config.</span>maxdepth
1.  object <span class="apidocSignatureSpan">shelljs.config.</span>globOptions
1.  string <span class="apidocSignatureSpan">shelljs.config.</span>execPath



# <a name="apidoc.module.shelljs"></a>[module shelljs](#apidoc.module.shelljs)

#### <a name="apidoc.element.shelljs.ShellString"></a>[function <span class="apidocSignatureSpan">shelljs.</span>ShellString (stdout, stderr, code)](#apidoc.element.shelljs.ShellString)
- description and source-code
```javascript
function ShellString(stdout, stderr, code) {
  var that;
  if (stdout instanceof Array) {
    that = stdout;
    that.stdout = stdout.join('\n');
    if (stdout.length > 0) that.stdout += '\n';
  } else {
    that = new String(stdout);
    that.stdout = stdout;
  }
  that.stderr = stderr;
  that.code = code;
  // A list of all commands that can appear on the right-hand side of a pipe
  // (populated by calls to common.wrap())
  pipeMethods.forEach(function (cmd) {
    that[cmd] = shellMethods[cmd].bind(that);
  });
  return that;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.shelljs.cat"></a>[function <span class="apidocSignatureSpan">shelljs.</span>cat ()](#apidoc.element.shelljs.cat)
- description and source-code
```javascript
cat = function () {
  var retValue = null;

  state.currentCmd = cmd;
  state.error = null;
  state.errorCode = 0;

  try {
    var args = [].slice.call(arguments, 0);

    // Log the command to stderr, if appropriate
    if (config.verbose) {
      console.error.apply(console, [cmd].concat(args));
    }

    // If this is coming from a pipe, let's set the pipedValue (otherwise, set
    // it to the empty string)
    state.pipedValue = (this && typeof this.stdout === 'string') ? this.stdout : '';

    if (options.unix === false) { // this branch is for exec()
      retValue = fn.apply(this, args);
    } else { // and this branch is for everything else
      if (isObject(args[0]) && args[0].constructor.name === 'Object') {
        // a no-op, allowing the syntax 'touch({'-r': file}, ...)'
      } else if (args.length === 0 || typeof args[0] !== 'string' || args[0].length <= 1 || args[0][0] !== '-') {
        args.unshift(''); // only add dummy option if '-option' not already present
      }

      // flatten out arrays that are arguments, to make the syntax:
      //    'cp([file1, file2, file3], dest);'
      // equivalent to:
      //    'cp(file1, file2, file3, dest);'
      args = args.reduce(function (accum, cur) {
        if (Array.isArray(cur)) {
          return accum.concat(cur);
        }
        accum.push(cur);
        return accum;
      }, []);

      // Convert ShellStrings (basically just String objects) to regular strings
      args = args.map(function (arg) {
        if (isObject(arg) && arg.constructor.name === 'String') {
          return arg.toString();
        }
        return arg;
      });

      // Expand the '~' if appropriate
      var homeDir = getUserHome();
      args = args.map(function (arg) {
        if (typeof arg === 'string' && arg.slice(0, 2) === '~/' || arg === '~') {
          return arg.replace(/^~/, homeDir);
        }
        return arg;
      });

      // Perform glob-expansion on all arguments after globStart, but preserve
      // the arguments before it (like regexes for sed and grep)
      if (!config.noglob && options.allowGlobbing === true) {
        args = args.slice(0, options.globStart).concat(expand(args.slice(options.globStart)));
      }

      try {
        // parse options if options are provided
        if (isObject(options.cmdOptions)) {
          args[0] = parseOptions(args[0], options.cmdOptions);
        }

        retValue = fn.apply(this, args);
      } catch (e) {
<span class="apidocCodeCommentSpan">        /* istanbul ignore else */
</span>        if (e.msg === 'earlyExit') {
          retValue = e.retValue;
        } else {
          throw e; // this is probably a bug that should be thrown up the call stack
        }
      }
    }
  } catch (e) {
    /* istanbul ignore next */
    if (!state.error) {
      // If state.error hasn't been set it's an error thrown by Node, not us - probably a bug...
      console.error('ShellJS: internal error');
      console.error(e.stack || e);
      process.exit(1);
    }
    if (config.fatal) throw e;
  }

  if (options.wrapOutput &&
      (typeof retValue === 'string' || Array.isArray(retValue))) {
    retValue = new ShellString(retValue, state.error, state.errorCode);
  }

  state.currentCmd = 'shell.js';
  return retValue;
}
```
- example usage
```shell
...
shell.cp('-R', 'stuff/', 'out/Release');

// Replace macros in each .js file
shell.cd('lib');
shell.ls('*.js').forEach(function (file) {
shell.sed('-i', 'BUILD_VERSION', 'v0.1.2', file);
shell.sed('-i', /^.*REMOVE_THIS_LINE.*$/, '', file);
shell.sed('-i', /.*REPLACE_LINE_WITH_MACRO.*\n/, shell.cat('macro.js'), file);
});
shell.cd('..');

// Run external tool synchronously
if (shell.exec('git commit -am "Auto-commit"').code !== 0) {
shell.echo('Error: Git commit failed');
shell.exit(1);
...
```

#### <a name="apidoc.element.shelljs.cd"></a>[function <span class="apidocSignatureSpan">shelljs.</span>cd ()](#apidoc.element.shelljs.cd)
- description and source-code
```javascript
cd = function () {
  var retValue = null;

  state.currentCmd = cmd;
  state.error = null;
  state.errorCode = 0;

  try {
    var args = [].slice.call(arguments, 0);

    // Log the command to stderr, if appropriate
    if (config.verbose) {
      console.error.apply(console, [cmd].concat(args));
    }

    // If this is coming from a pipe, let's set the pipedValue (otherwise, set
    // it to the empty string)
    state.pipedValue = (this && typeof this.stdout === 'string') ? this.stdout : '';

    if (options.unix === false) { // this branch is for exec()
      retValue = fn.apply(this, args);
    } else { // and this branch is for everything else
      if (isObject(args[0]) && args[0].constructor.name === 'Object') {
        // a no-op, allowing the syntax 'touch({'-r': file}, ...)'
      } else if (args.length === 0 || typeof args[0] !== 'string' || args[0].length <= 1 || args[0][0] !== '-') {
        args.unshift(''); // only add dummy option if '-option' not already present
      }

      // flatten out arrays that are arguments, to make the syntax:
      //    'cp([file1, file2, file3], dest);'
      // equivalent to:
      //    'cp(file1, file2, file3, dest);'
      args = args.reduce(function (accum, cur) {
        if (Array.isArray(cur)) {
          return accum.concat(cur);
        }
        accum.push(cur);
        return accum;
      }, []);

      // Convert ShellStrings (basically just String objects) to regular strings
      args = args.map(function (arg) {
        if (isObject(arg) && arg.constructor.name === 'String') {
          return arg.toString();
        }
        return arg;
      });

      // Expand the '~' if appropriate
      var homeDir = getUserHome();
      args = args.map(function (arg) {
        if (typeof arg === 'string' && arg.slice(0, 2) === '~/' || arg === '~') {
          return arg.replace(/^~/, homeDir);
        }
        return arg;
      });

      // Perform glob-expansion on all arguments after globStart, but preserve
      // the arguments before it (like regexes for sed and grep)
      if (!config.noglob && options.allowGlobbing === true) {
        args = args.slice(0, options.globStart).concat(expand(args.slice(options.globStart)));
      }

      try {
        // parse options if options are provided
        if (isObject(options.cmdOptions)) {
          args[0] = parseOptions(args[0], options.cmdOptions);
        }

        retValue = fn.apply(this, args);
      } catch (e) {
<span class="apidocCodeCommentSpan">        /* istanbul ignore else */
</span>        if (e.msg === 'earlyExit') {
          retValue = e.retValue;
        } else {
          throw e; // this is probably a bug that should be thrown up the call stack
        }
      }
    }
  } catch (e) {
    /* istanbul ignore next */
    if (!state.error) {
      // If state.error hasn't been set it's an error thrown by Node, not us - probably a bug...
      console.error('ShellJS: internal error');
      console.error(e.stack || e);
      process.exit(1);
    }
    if (config.fatal) throw e;
  }

  if (options.wrapOutput &&
      (typeof retValue === 'string' || Array.isArray(retValue))) {
    retValue = new ShellString(retValue, state.error, state.errorCode);
  }

  state.currentCmd = 'shell.js';
  return retValue;
}
```
- example usage
```shell
...
}

// Copy files to release dir
shell.rm('-rf', 'out/Release');
shell.cp('-R', 'stuff/', 'out/Release');

// Replace macros in each .js file
shell.cd('lib');
shell.ls('*.js').forEach(function (file) {
  shell.sed('-i', 'BUILD_VERSION', 'v0.1.2', file);
  shell.sed('-i', /^.*REMOVE_THIS_LINE.*$/, '', file);
  shell.sed('-i', /.*REPLACE_LINE_WITH_MACRO.*\n/, shell.cat('macro.js'), file);
});
shell.cd('..');
...
```

#### <a name="apidoc.element.shelljs.chmod"></a>[function <span class="apidocSignatureSpan">shelljs.</span>chmod ()](#apidoc.element.shelljs.chmod)
- description and source-code
```javascript
chmod = function () {
  var retValue = null;

  state.currentCmd = cmd;
  state.error = null;
  state.errorCode = 0;

  try {
    var args = [].slice.call(arguments, 0);

    // Log the command to stderr, if appropriate
    if (config.verbose) {
      console.error.apply(console, [cmd].concat(args));
    }

    // If this is coming from a pipe, let's set the pipedValue (otherwise, set
    // it to the empty string)
    state.pipedValue = (this && typeof this.stdout === 'string') ? this.stdout : '';

    if (options.unix === false) { // this branch is for exec()
      retValue = fn.apply(this, args);
    } else { // and this branch is for everything else
      if (isObject(args[0]) && args[0].constructor.name === 'Object') {
        // a no-op, allowing the syntax 'touch({'-r': file}, ...)'
      } else if (args.length === 0 || typeof args[0] !== 'string' || args[0].length <= 1 || args[0][0] !== '-') {
        args.unshift(''); // only add dummy option if '-option' not already present
      }

      // flatten out arrays that are arguments, to make the syntax:
      //    'cp([file1, file2, file3], dest);'
      // equivalent to:
      //    'cp(file1, file2, file3, dest);'
      args = args.reduce(function (accum, cur) {
        if (Array.isArray(cur)) {
          return accum.concat(cur);
        }
        accum.push(cur);
        return accum;
      }, []);

      // Convert ShellStrings (basically just String objects) to regular strings
      args = args.map(function (arg) {
        if (isObject(arg) && arg.constructor.name === 'String') {
          return arg.toString();
        }
        return arg;
      });

      // Expand the '~' if appropriate
      var homeDir = getUserHome();
      args = args.map(function (arg) {
        if (typeof arg === 'string' && arg.slice(0, 2) === '~/' || arg === '~') {
          return arg.replace(/^~/, homeDir);
        }
        return arg;
      });

      // Perform glob-expansion on all arguments after globStart, but preserve
      // the arguments before it (like regexes for sed and grep)
      if (!config.noglob && options.allowGlobbing === true) {
        args = args.slice(0, options.globStart).concat(expand(args.slice(options.globStart)));
      }

      try {
        // parse options if options are provided
        if (isObject(options.cmdOptions)) {
          args[0] = parseOptions(args[0], options.cmdOptions);
        }

        retValue = fn.apply(this, args);
      } catch (e) {
<span class="apidocCodeCommentSpan">        /* istanbul ignore else */
</span>        if (e.msg === 'earlyExit') {
          retValue = e.retValue;
        } else {
          throw e; // this is probably a bug that should be thrown up the call stack
        }
      }
    }
  } catch (e) {
    /* istanbul ignore next */
    if (!state.error) {
      // If state.error hasn't been set it's an error thrown by Node, not us - probably a bug...
      console.error('ShellJS: internal error');
      console.error(e.stack || e);
      process.exit(1);
    }
    if (config.fatal) throw e;
  }

  if (options.wrapOutput &&
      (typeof retValue === 'string' || Array.isArray(retValue))) {
    retValue = new ShellString(retValue, state.error, state.errorCode);
  }

  state.currentCmd = 'shell.js';
  return retValue;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.shelljs.cp"></a>[function <span class="apidocSignatureSpan">shelljs.</span>cp ()](#apidoc.element.shelljs.cp)
- description and source-code
```javascript
cp = function () {
  var retValue = null;

  state.currentCmd = cmd;
  state.error = null;
  state.errorCode = 0;

  try {
    var args = [].slice.call(arguments, 0);

    // Log the command to stderr, if appropriate
    if (config.verbose) {
      console.error.apply(console, [cmd].concat(args));
    }

    // If this is coming from a pipe, let's set the pipedValue (otherwise, set
    // it to the empty string)
    state.pipedValue = (this && typeof this.stdout === 'string') ? this.stdout : '';

    if (options.unix === false) { // this branch is for exec()
      retValue = fn.apply(this, args);
    } else { // and this branch is for everything else
      if (isObject(args[0]) && args[0].constructor.name === 'Object') {
        // a no-op, allowing the syntax 'touch({'-r': file}, ...)'
      } else if (args.length === 0 || typeof args[0] !== 'string' || args[0].length <= 1 || args[0][0] !== '-') {
        args.unshift(''); // only add dummy option if '-option' not already present
      }

      // flatten out arrays that are arguments, to make the syntax:
      //    'cp([file1, file2, file3], dest);'
      // equivalent to:
      //    'cp(file1, file2, file3, dest);'
      args = args.reduce(function (accum, cur) {
        if (Array.isArray(cur)) {
          return accum.concat(cur);
        }
        accum.push(cur);
        return accum;
      }, []);

      // Convert ShellStrings (basically just String objects) to regular strings
      args = args.map(function (arg) {
        if (isObject(arg) && arg.constructor.name === 'String') {
          return arg.toString();
        }
        return arg;
      });

      // Expand the '~' if appropriate
      var homeDir = getUserHome();
      args = args.map(function (arg) {
        if (typeof arg === 'string' && arg.slice(0, 2) === '~/' || arg === '~') {
          return arg.replace(/^~/, homeDir);
        }
        return arg;
      });

      // Perform glob-expansion on all arguments after globStart, but preserve
      // the arguments before it (like regexes for sed and grep)
      if (!config.noglob && options.allowGlobbing === true) {
        args = args.slice(0, options.globStart).concat(expand(args.slice(options.globStart)));
      }

      try {
        // parse options if options are provided
        if (isObject(options.cmdOptions)) {
          args[0] = parseOptions(args[0], options.cmdOptions);
        }

        retValue = fn.apply(this, args);
      } catch (e) {
<span class="apidocCodeCommentSpan">        /* istanbul ignore else */
</span>        if (e.msg === 'earlyExit') {
          retValue = e.retValue;
        } else {
          throw e; // this is probably a bug that should be thrown up the call stack
        }
      }
    }
  } catch (e) {
    /* istanbul ignore next */
    if (!state.error) {
      // If state.error hasn't been set it's an error thrown by Node, not us - probably a bug...
      console.error('ShellJS: internal error');
      console.error(e.stack || e);
      process.exit(1);
    }
    if (config.fatal) throw e;
  }

  if (options.wrapOutput &&
      (typeof retValue === 'string' || Array.isArray(retValue))) {
    retValue = new ShellString(retValue, state.error, state.errorCode);
  }

  state.currentCmd = 'shell.js';
  return retValue;
}
```
- example usage
```shell
...
if (!shell.which('git')) {
shell.echo('Sorry, this script requires git');
shell.exit(1);
}

// Copy files to release dir
shell.rm('-rf', 'out/Release');
shell.cp('-R', 'stuff/', 'out/Release');

// Replace macros in each .js file
shell.cd('lib');
shell.ls('*.js').forEach(function (file) {
shell.sed('-i', 'BUILD_VERSION', 'v0.1.2', file);
shell.sed('-i', /^.*REMOVE_THIS_LINE.*$/, '', file);
shell.sed('-i', /.*REPLACE_LINE_WITH_MACRO.*\n/, shell.cat('macro.js'), file);
...
```

#### <a name="apidoc.element.shelljs.dirs"></a>[function <span class="apidocSignatureSpan">shelljs.</span>dirs ()](#apidoc.element.shelljs.dirs)
- description and source-code
```javascript
dirs = function () {
  var retValue = null;

  state.currentCmd = cmd;
  state.error = null;
  state.errorCode = 0;

  try {
    var args = [].slice.call(arguments, 0);

    // Log the command to stderr, if appropriate
    if (config.verbose) {
      console.error.apply(console, [cmd].concat(args));
    }

    // If this is coming from a pipe, let's set the pipedValue (otherwise, set
    // it to the empty string)
    state.pipedValue = (this && typeof this.stdout === 'string') ? this.stdout : '';

    if (options.unix === false) { // this branch is for exec()
      retValue = fn.apply(this, args);
    } else { // and this branch is for everything else
      if (isObject(args[0]) && args[0].constructor.name === 'Object') {
        // a no-op, allowing the syntax 'touch({'-r': file}, ...)'
      } else if (args.length === 0 || typeof args[0] !== 'string' || args[0].length <= 1 || args[0][0] !== '-') {
        args.unshift(''); // only add dummy option if '-option' not already present
      }

      // flatten out arrays that are arguments, to make the syntax:
      //    'cp([file1, file2, file3], dest);'
      // equivalent to:
      //    'cp(file1, file2, file3, dest);'
      args = args.reduce(function (accum, cur) {
        if (Array.isArray(cur)) {
          return accum.concat(cur);
        }
        accum.push(cur);
        return accum;
      }, []);

      // Convert ShellStrings (basically just String objects) to regular strings
      args = args.map(function (arg) {
        if (isObject(arg) && arg.constructor.name === 'String') {
          return arg.toString();
        }
        return arg;
      });

      // Expand the '~' if appropriate
      var homeDir = getUserHome();
      args = args.map(function (arg) {
        if (typeof arg === 'string' && arg.slice(0, 2) === '~/' || arg === '~') {
          return arg.replace(/^~/, homeDir);
        }
        return arg;
      });

      // Perform glob-expansion on all arguments after globStart, but preserve
      // the arguments before it (like regexes for sed and grep)
      if (!config.noglob && options.allowGlobbing === true) {
        args = args.slice(0, options.globStart).concat(expand(args.slice(options.globStart)));
      }

      try {
        // parse options if options are provided
        if (isObject(options.cmdOptions)) {
          args[0] = parseOptions(args[0], options.cmdOptions);
        }

        retValue = fn.apply(this, args);
      } catch (e) {
<span class="apidocCodeCommentSpan">        /* istanbul ignore else */
</span>        if (e.msg === 'earlyExit') {
          retValue = e.retValue;
        } else {
          throw e; // this is probably a bug that should be thrown up the call stack
        }
      }
    }
  } catch (e) {
    /* istanbul ignore next */
    if (!state.error) {
      // If state.error hasn't been set it's an error thrown by Node, not us - probably a bug...
      console.error('ShellJS: internal error');
      console.error(e.stack || e);
      process.exit(1);
    }
    if (config.fatal) throw e;
  }

  if (options.wrapOutput &&
      (typeof retValue === 'string' || Array.isArray(retValue))) {
    retValue = new ShellString(retValue, state.error, state.errorCode);
  }

  state.currentCmd = 'shell.js';
  return retValue;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.shelljs.echo"></a>[function <span class="apidocSignatureSpan">shelljs.</span>echo ()](#apidoc.element.shelljs.echo)
- description and source-code
```javascript
echo = function () {
  var retValue = null;

  state.currentCmd = cmd;
  state.error = null;
  state.errorCode = 0;

  try {
    var args = [].slice.call(arguments, 0);

    // Log the command to stderr, if appropriate
    if (config.verbose) {
      console.error.apply(console, [cmd].concat(args));
    }

    // If this is coming from a pipe, let's set the pipedValue (otherwise, set
    // it to the empty string)
    state.pipedValue = (this && typeof this.stdout === 'string') ? this.stdout : '';

    if (options.unix === false) { // this branch is for exec()
      retValue = fn.apply(this, args);
    } else { // and this branch is for everything else
      if (isObject(args[0]) && args[0].constructor.name === 'Object') {
        // a no-op, allowing the syntax 'touch({'-r': file}, ...)'
      } else if (args.length === 0 || typeof args[0] !== 'string' || args[0].length <= 1 || args[0][0] !== '-') {
        args.unshift(''); // only add dummy option if '-option' not already present
      }

      // flatten out arrays that are arguments, to make the syntax:
      //    'cp([file1, file2, file3], dest);'
      // equivalent to:
      //    'cp(file1, file2, file3, dest);'
      args = args.reduce(function (accum, cur) {
        if (Array.isArray(cur)) {
          return accum.concat(cur);
        }
        accum.push(cur);
        return accum;
      }, []);

      // Convert ShellStrings (basically just String objects) to regular strings
      args = args.map(function (arg) {
        if (isObject(arg) && arg.constructor.name === 'String') {
          return arg.toString();
        }
        return arg;
      });

      // Expand the '~' if appropriate
      var homeDir = getUserHome();
      args = args.map(function (arg) {
        if (typeof arg === 'string' && arg.slice(0, 2) === '~/' || arg === '~') {
          return arg.replace(/^~/, homeDir);
        }
        return arg;
      });

      // Perform glob-expansion on all arguments after globStart, but preserve
      // the arguments before it (like regexes for sed and grep)
      if (!config.noglob && options.allowGlobbing === true) {
        args = args.slice(0, options.globStart).concat(expand(args.slice(options.globStart)));
      }

      try {
        // parse options if options are provided
        if (isObject(options.cmdOptions)) {
          args[0] = parseOptions(args[0], options.cmdOptions);
        }

        retValue = fn.apply(this, args);
      } catch (e) {
<span class="apidocCodeCommentSpan">        /* istanbul ignore else */
</span>        if (e.msg === 'earlyExit') {
          retValue = e.retValue;
        } else {
          throw e; // this is probably a bug that should be thrown up the call stack
        }
      }
    }
  } catch (e) {
    /* istanbul ignore next */
    if (!state.error) {
      // If state.error hasn't been set it's an error thrown by Node, not us - probably a bug...
      console.error('ShellJS: internal error');
      console.error(e.stack || e);
      process.exit(1);
    }
    if (config.fatal) throw e;
  }

  if (options.wrapOutput &&
      (typeof retValue === 'string' || Array.isArray(retValue))) {
    retValue = new ShellString(retValue, state.error, state.errorCode);
  }

  state.currentCmd = 'shell.js';
  return retValue;
}
```
- example usage
```shell
...

## Examples

'''javascript
var shell = require('shelljs');

if (!shell.which('git')) {
  shell.echo('Sorry, this script requires git');
  shell.exit(1);
}

// Copy files to release dir
shell.rm('-rf', 'out/Release');
shell.cp('-R', 'stuff/', 'out/Release');
...
```

#### <a name="apidoc.element.shelljs.error"></a>[function <span class="apidocSignatureSpan">shelljs.</span>error ()](#apidoc.element.shelljs.error)
- description and source-code
```javascript
function error() {
  return common.state.error;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.shelljs.exec"></a>[function <span class="apidocSignatureSpan">shelljs.</span>exec ()](#apidoc.element.shelljs.exec)
- description and source-code
```javascript
exec = function () {
  var retValue = null;

  state.currentCmd = cmd;
  state.error = null;
  state.errorCode = 0;

  try {
    var args = [].slice.call(arguments, 0);

    // Log the command to stderr, if appropriate
    if (config.verbose) {
      console.error.apply(console, [cmd].concat(args));
    }

    // If this is coming from a pipe, let's set the pipedValue (otherwise, set
    // it to the empty string)
    state.pipedValue = (this && typeof this.stdout === 'string') ? this.stdout : '';

    if (options.unix === false) { // this branch is for exec()
      retValue = fn.apply(this, args);
    } else { // and this branch is for everything else
      if (isObject(args[0]) && args[0].constructor.name === 'Object') {
        // a no-op, allowing the syntax 'touch({'-r': file}, ...)'
      } else if (args.length === 0 || typeof args[0] !== 'string' || args[0].length <= 1 || args[0][0] !== '-') {
        args.unshift(''); // only add dummy option if '-option' not already present
      }

      // flatten out arrays that are arguments, to make the syntax:
      //    'cp([file1, file2, file3], dest);'
      // equivalent to:
      //    'cp(file1, file2, file3, dest);'
      args = args.reduce(function (accum, cur) {
        if (Array.isArray(cur)) {
          return accum.concat(cur);
        }
        accum.push(cur);
        return accum;
      }, []);

      // Convert ShellStrings (basically just String objects) to regular strings
      args = args.map(function (arg) {
        if (isObject(arg) && arg.constructor.name === 'String') {
          return arg.toString();
        }
        return arg;
      });

      // Expand the '~' if appropriate
      var homeDir = getUserHome();
      args = args.map(function (arg) {
        if (typeof arg === 'string' && arg.slice(0, 2) === '~/' || arg === '~') {
          return arg.replace(/^~/, homeDir);
        }
        return arg;
      });

      // Perform glob-expansion on all arguments after globStart, but preserve
      // the arguments before it (like regexes for sed and grep)
      if (!config.noglob && options.allowGlobbing === true) {
        args = args.slice(0, options.globStart).concat(expand(args.slice(options.globStart)));
      }

      try {
        // parse options if options are provided
        if (isObject(options.cmdOptions)) {
          args[0] = parseOptions(args[0], options.cmdOptions);
        }

        retValue = fn.apply(this, args);
      } catch (e) {
<span class="apidocCodeCommentSpan">        /* istanbul ignore else */
</span>        if (e.msg === 'earlyExit') {
          retValue = e.retValue;
        } else {
          throw e; // this is probably a bug that should be thrown up the call stack
        }
      }
    }
  } catch (e) {
    /* istanbul ignore next */
    if (!state.error) {
      // If state.error hasn't been set it's an error thrown by Node, not us - probably a bug...
      console.error('ShellJS: internal error');
      console.error(e.stack || e);
      process.exit(1);
    }
    if (config.fatal) throw e;
  }

  if (options.wrapOutput &&
      (typeof retValue === 'string' || Array.isArray(retValue))) {
    retValue = new ShellString(retValue, state.error, state.errorCode);
  }

  state.currentCmd = 'shell.js';
  return retValue;
}
```
- example usage
```shell
...
  shell.sed('-i', 'BUILD_VERSION', 'v0.1.2', file);
  shell.sed('-i', /^.*REMOVE_THIS_LINE.*$/, '', file);
  shell.sed('-i', /.*REPLACE_LINE_WITH_MACRO.*\n/, shell.cat('macro.js'), file);
});
shell.cd('..');

// Run external tool synchronously
if (shell.exec('git commit -am "Auto-commit"').code !== 0) {
  shell.echo('Error: Git commit failed');
  shell.exit(1);
}
'''

## Global vs. Local
...
```

#### <a name="apidoc.element.shelljs.exit"></a>[function <span class="apidocSignatureSpan">shelljs.</span>exit ()](#apidoc.element.shelljs.exit)
- description and source-code
```javascript
exit = function () {
<span class="apidocCodeCommentSpan">/*
 * this function will do nothing
 */
</span>    return;
}
```
- example usage
```shell
...
## Examples

'''javascript
var shell = require('shelljs');

if (!shell.which('git')) {
  shell.echo('Sorry, this script requires git');
  shell.exit(1);
}

// Copy files to release dir
shell.rm('-rf', 'out/Release');
shell.cp('-R', 'stuff/', 'out/Release');

// Replace macros in each .js file
...
```

#### <a name="apidoc.element.shelljs.find"></a>[function <span class="apidocSignatureSpan">shelljs.</span>find ()](#apidoc.element.shelljs.find)
- description and source-code
```javascript
find = function () {
  var retValue = null;

  state.currentCmd = cmd;
  state.error = null;
  state.errorCode = 0;

  try {
    var args = [].slice.call(arguments, 0);

    // Log the command to stderr, if appropriate
    if (config.verbose) {
      console.error.apply(console, [cmd].concat(args));
    }

    // If this is coming from a pipe, let's set the pipedValue (otherwise, set
    // it to the empty string)
    state.pipedValue = (this && typeof this.stdout === 'string') ? this.stdout : '';

    if (options.unix === false) { // this branch is for exec()
      retValue = fn.apply(this, args);
    } else { // and this branch is for everything else
      if (isObject(args[0]) && args[0].constructor.name === 'Object') {
        // a no-op, allowing the syntax 'touch({'-r': file}, ...)'
      } else if (args.length === 0 || typeof args[0] !== 'string' || args[0].length <= 1 || args[0][0] !== '-') {
        args.unshift(''); // only add dummy option if '-option' not already present
      }

      // flatten out arrays that are arguments, to make the syntax:
      //    'cp([file1, file2, file3], dest);'
      // equivalent to:
      //    'cp(file1, file2, file3, dest);'
      args = args.reduce(function (accum, cur) {
        if (Array.isArray(cur)) {
          return accum.concat(cur);
        }
        accum.push(cur);
        return accum;
      }, []);

      // Convert ShellStrings (basically just String objects) to regular strings
      args = args.map(function (arg) {
        if (isObject(arg) && arg.constructor.name === 'String') {
          return arg.toString();
        }
        return arg;
      });

      // Expand the '~' if appropriate
      var homeDir = getUserHome();
      args = args.map(function (arg) {
        if (typeof arg === 'string' && arg.slice(0, 2) === '~/' || arg === '~') {
          return arg.replace(/^~/, homeDir);
        }
        return arg;
      });

      // Perform glob-expansion on all arguments after globStart, but preserve
      // the arguments before it (like regexes for sed and grep)
      if (!config.noglob && options.allowGlobbing === true) {
        args = args.slice(0, options.globStart).concat(expand(args.slice(options.globStart)));
      }

      try {
        // parse options if options are provided
        if (isObject(options.cmdOptions)) {
          args[0] = parseOptions(args[0], options.cmdOptions);
        }

        retValue = fn.apply(this, args);
      } catch (e) {
<span class="apidocCodeCommentSpan">        /* istanbul ignore else */
</span>        if (e.msg === 'earlyExit') {
          retValue = e.retValue;
        } else {
          throw e; // this is probably a bug that should be thrown up the call stack
        }
      }
    }
  } catch (e) {
    /* istanbul ignore next */
    if (!state.error) {
      // If state.error hasn't been set it's an error thrown by Node, not us - probably a bug...
      console.error('ShellJS: internal error');
      console.error(e.stack || e);
      process.exit(1);
    }
    if (config.fatal) throw e;
  }

  if (options.wrapOutput &&
      (typeof retValue === 'string' || Array.isArray(retValue))) {
    retValue = new ShellString(retValue, state.error, state.errorCode);
  }

  state.currentCmd = 'shell.js';
  return retValue;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.shelljs.grep"></a>[function <span class="apidocSignatureSpan">shelljs.</span>grep ()](#apidoc.element.shelljs.grep)
- description and source-code
```javascript
grep = function () {
  var retValue = null;

  state.currentCmd = cmd;
  state.error = null;
  state.errorCode = 0;

  try {
    var args = [].slice.call(arguments, 0);

    // Log the command to stderr, if appropriate
    if (config.verbose) {
      console.error.apply(console, [cmd].concat(args));
    }

    // If this is coming from a pipe, let's set the pipedValue (otherwise, set
    // it to the empty string)
    state.pipedValue = (this && typeof this.stdout === 'string') ? this.stdout : '';

    if (options.unix === false) { // this branch is for exec()
      retValue = fn.apply(this, args);
    } else { // and this branch is for everything else
      if (isObject(args[0]) && args[0].constructor.name === 'Object') {
        // a no-op, allowing the syntax 'touch({'-r': file}, ...)'
      } else if (args.length === 0 || typeof args[0] !== 'string' || args[0].length <= 1 || args[0][0] !== '-') {
        args.unshift(''); // only add dummy option if '-option' not already present
      }

      // flatten out arrays that are arguments, to make the syntax:
      //    'cp([file1, file2, file3], dest);'
      // equivalent to:
      //    'cp(file1, file2, file3, dest);'
      args = args.reduce(function (accum, cur) {
        if (Array.isArray(cur)) {
          return accum.concat(cur);
        }
        accum.push(cur);
        return accum;
      }, []);

      // Convert ShellStrings (basically just String objects) to regular strings
      args = args.map(function (arg) {
        if (isObject(arg) && arg.constructor.name === 'String') {
          return arg.toString();
        }
        return arg;
      });

      // Expand the '~' if appropriate
      var homeDir = getUserHome();
      args = args.map(function (arg) {
        if (typeof arg === 'string' && arg.slice(0, 2) === '~/' || arg === '~') {
          return arg.replace(/^~/, homeDir);
        }
        return arg;
      });

      // Perform glob-expansion on all arguments after globStart, but preserve
      // the arguments before it (like regexes for sed and grep)
      if (!config.noglob && options.allowGlobbing === true) {
        args = args.slice(0, options.globStart).concat(expand(args.slice(options.globStart)));
      }

      try {
        // parse options if options are provided
        if (isObject(options.cmdOptions)) {
          args[0] = parseOptions(args[0], options.cmdOptions);
        }

        retValue = fn.apply(this, args);
      } catch (e) {
<span class="apidocCodeCommentSpan">        /* istanbul ignore else */
</span>        if (e.msg === 'earlyExit') {
          retValue = e.retValue;
        } else {
          throw e; // this is probably a bug that should be thrown up the call stack
        }
      }
    }
  } catch (e) {
    /* istanbul ignore next */
    if (!state.error) {
      // If state.error hasn't been set it's an error thrown by Node, not us - probably a bug...
      console.error('ShellJS: internal error');
      console.error(e.stack || e);
      process.exit(1);
    }
    if (config.fatal) throw e;
  }

  if (options.wrapOutput &&
      (typeof retValue === 'string' || Array.isArray(retValue))) {
    retValue = new ShellString(retValue, state.error, state.errorCode);
  }

  state.currentCmd = 'shell.js';
  return retValue;
}
```
- example usage
```shell
...

### Pipes

Examples:

'''javascript
grep('foo', 'file1.txt', 'file2.txt').sed(/o/g, 'a').to('output.txt');
echo('files with o\'s in the name:\n' + ls().grep('o'));
cat('test.js').exec('node'); // pipe to exec() call
'''

Commands can send their output to another command in a pipe-like fashion.
'sed', 'grep', 'cat', 'exec', 'to', and 'toEnd' can appear on the right-hand
side of a pipe. Pipes can be chained.
...
```

#### <a name="apidoc.element.shelljs.head"></a>[function <span class="apidocSignatureSpan">shelljs.</span>head ()](#apidoc.element.shelljs.head)
- description and source-code
```javascript
head = function () {
  var retValue = null;

  state.currentCmd = cmd;
  state.error = null;
  state.errorCode = 0;

  try {
    var args = [].slice.call(arguments, 0);

    // Log the command to stderr, if appropriate
    if (config.verbose) {
      console.error.apply(console, [cmd].concat(args));
    }

    // If this is coming from a pipe, let's set the pipedValue (otherwise, set
    // it to the empty string)
    state.pipedValue = (this && typeof this.stdout === 'string') ? this.stdout : '';

    if (options.unix === false) { // this branch is for exec()
      retValue = fn.apply(this, args);
    } else { // and this branch is for everything else
      if (isObject(args[0]) && args[0].constructor.name === 'Object') {
        // a no-op, allowing the syntax 'touch({'-r': file}, ...)'
      } else if (args.length === 0 || typeof args[0] !== 'string' || args[0].length <= 1 || args[0][0] !== '-') {
        args.unshift(''); // only add dummy option if '-option' not already present
      }

      // flatten out arrays that are arguments, to make the syntax:
      //    'cp([file1, file2, file3], dest);'
      // equivalent to:
      //    'cp(file1, file2, file3, dest);'
      args = args.reduce(function (accum, cur) {
        if (Array.isArray(cur)) {
          return accum.concat(cur);
        }
        accum.push(cur);
        return accum;
      }, []);

      // Convert ShellStrings (basically just String objects) to regular strings
      args = args.map(function (arg) {
        if (isObject(arg) && arg.constructor.name === 'String') {
          return arg.toString();
        }
        return arg;
      });

      // Expand the '~' if appropriate
      var homeDir = getUserHome();
      args = args.map(function (arg) {
        if (typeof arg === 'string' && arg.slice(0, 2) === '~/' || arg === '~') {
          return arg.replace(/^~/, homeDir);
        }
        return arg;
      });

      // Perform glob-expansion on all arguments after globStart, but preserve
      // the arguments before it (like regexes for sed and grep)
      if (!config.noglob && options.allowGlobbing === true) {
        args = args.slice(0, options.globStart).concat(expand(args.slice(options.globStart)));
      }

      try {
        // parse options if options are provided
        if (isObject(options.cmdOptions)) {
          args[0] = parseOptions(args[0], options.cmdOptions);
        }

        retValue = fn.apply(this, args);
      } catch (e) {
<span class="apidocCodeCommentSpan">        /* istanbul ignore else */
</span>        if (e.msg === 'earlyExit') {
          retValue = e.retValue;
        } else {
          throw e; // this is probably a bug that should be thrown up the call stack
        }
      }
    }
  } catch (e) {
    /* istanbul ignore next */
    if (!state.error) {
      // If state.error hasn't been set it's an error thrown by Node, not us - probably a bug...
      console.error('ShellJS: internal error');
      console.error(e.stack || e);
      process.exit(1);
    }
    if (config.fatal) throw e;
  }

  if (options.wrapOutput &&
      (typeof retValue === 'string' || Array.isArray(retValue))) {
    retValue = new ShellString(retValue, state.error, state.errorCode);
  }

  state.currentCmd = 'shell.js';
  return retValue;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.shelljs.ln"></a>[function <span class="apidocSignatureSpan">shelljs.</span>ln ()](#apidoc.element.shelljs.ln)
- description and source-code
```javascript
ln = function () {
  var retValue = null;

  state.currentCmd = cmd;
  state.error = null;
  state.errorCode = 0;

  try {
    var args = [].slice.call(arguments, 0);

    // Log the command to stderr, if appropriate
    if (config.verbose) {
      console.error.apply(console, [cmd].concat(args));
    }

    // If this is coming from a pipe, let's set the pipedValue (otherwise, set
    // it to the empty string)
    state.pipedValue = (this && typeof this.stdout === 'string') ? this.stdout : '';

    if (options.unix === false) { // this branch is for exec()
      retValue = fn.apply(this, args);
    } else { // and this branch is for everything else
      if (isObject(args[0]) && args[0].constructor.name === 'Object') {
        // a no-op, allowing the syntax 'touch({'-r': file}, ...)'
      } else if (args.length === 0 || typeof args[0] !== 'string' || args[0].length <= 1 || args[0][0] !== '-') {
        args.unshift(''); // only add dummy option if '-option' not already present
      }

      // flatten out arrays that are arguments, to make the syntax:
      //    'cp([file1, file2, file3], dest);'
      // equivalent to:
      //    'cp(file1, file2, file3, dest);'
      args = args.reduce(function (accum, cur) {
        if (Array.isArray(cur)) {
          return accum.concat(cur);
        }
        accum.push(cur);
        return accum;
      }, []);

      // Convert ShellStrings (basically just String objects) to regular strings
      args = args.map(function (arg) {
        if (isObject(arg) && arg.constructor.name === 'String') {
          return arg.toString();
        }
        return arg;
      });

      // Expand the '~' if appropriate
      var homeDir = getUserHome();
      args = args.map(function (arg) {
        if (typeof arg === 'string' && arg.slice(0, 2) === '~/' || arg === '~') {
          return arg.replace(/^~/, homeDir);
        }
        return arg;
      });

      // Perform glob-expansion on all arguments after globStart, but preserve
      // the arguments before it (like regexes for sed and grep)
      if (!config.noglob && options.allowGlobbing === true) {
        args = args.slice(0, options.globStart).concat(expand(args.slice(options.globStart)));
      }

      try {
        // parse options if options are provided
        if (isObject(options.cmdOptions)) {
          args[0] = parseOptions(args[0], options.cmdOptions);
        }

        retValue = fn.apply(this, args);
      } catch (e) {
<span class="apidocCodeCommentSpan">        /* istanbul ignore else */
</span>        if (e.msg === 'earlyExit') {
          retValue = e.retValue;
        } else {
          throw e; // this is probably a bug that should be thrown up the call stack
        }
      }
    }
  } catch (e) {
    /* istanbul ignore next */
    if (!state.error) {
      // If state.error hasn't been set it's an error thrown by Node, not us - probably a bug...
      console.error('ShellJS: internal error');
      console.error(e.stack || e);
      process.exit(1);
    }
    if (config.fatal) throw e;
  }

  if (options.wrapOutput &&
      (typeof retValue === 'string' || Array.isArray(retValue))) {
    retValue = new ShellString(retValue, state.error, state.errorCode);
  }

  state.currentCmd = 'shell.js';
  return retValue;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.shelljs.ls"></a>[function <span class="apidocSignatureSpan">shelljs.</span>ls ()](#apidoc.element.shelljs.ls)
- description and source-code
```javascript
ls = function () {
  var retValue = null;

  state.currentCmd = cmd;
  state.error = null;
  state.errorCode = 0;

  try {
    var args = [].slice.call(arguments, 0);

    // Log the command to stderr, if appropriate
    if (config.verbose) {
      console.error.apply(console, [cmd].concat(args));
    }

    // If this is coming from a pipe, let's set the pipedValue (otherwise, set
    // it to the empty string)
    state.pipedValue = (this && typeof this.stdout === 'string') ? this.stdout : '';

    if (options.unix === false) { // this branch is for exec()
      retValue = fn.apply(this, args);
    } else { // and this branch is for everything else
      if (isObject(args[0]) && args[0].constructor.name === 'Object') {
        // a no-op, allowing the syntax 'touch({'-r': file}, ...)'
      } else if (args.length === 0 || typeof args[0] !== 'string' || args[0].length <= 1 || args[0][0] !== '-') {
        args.unshift(''); // only add dummy option if '-option' not already present
      }

      // flatten out arrays that are arguments, to make the syntax:
      //    'cp([file1, file2, file3], dest);'
      // equivalent to:
      //    'cp(file1, file2, file3, dest);'
      args = args.reduce(function (accum, cur) {
        if (Array.isArray(cur)) {
          return accum.concat(cur);
        }
        accum.push(cur);
        return accum;
      }, []);

      // Convert ShellStrings (basically just String objects) to regular strings
      args = args.map(function (arg) {
        if (isObject(arg) && arg.constructor.name === 'String') {
          return arg.toString();
        }
        return arg;
      });

      // Expand the '~' if appropriate
      var homeDir = getUserHome();
      args = args.map(function (arg) {
        if (typeof arg === 'string' && arg.slice(0, 2) === '~/' || arg === '~') {
          return arg.replace(/^~/, homeDir);
        }
        return arg;
      });

      // Perform glob-expansion on all arguments after globStart, but preserve
      // the arguments before it (like regexes for sed and grep)
      if (!config.noglob && options.allowGlobbing === true) {
        args = args.slice(0, options.globStart).concat(expand(args.slice(options.globStart)));
      }

      try {
        // parse options if options are provided
        if (isObject(options.cmdOptions)) {
          args[0] = parseOptions(args[0], options.cmdOptions);
        }

        retValue = fn.apply(this, args);
      } catch (e) {
<span class="apidocCodeCommentSpan">        /* istanbul ignore else */
</span>        if (e.msg === 'earlyExit') {
          retValue = e.retValue;
        } else {
          throw e; // this is probably a bug that should be thrown up the call stack
        }
      }
    }
  } catch (e) {
    /* istanbul ignore next */
    if (!state.error) {
      // If state.error hasn't been set it's an error thrown by Node, not us - probably a bug...
      console.error('ShellJS: internal error');
      console.error(e.stack || e);
      process.exit(1);
    }
    if (config.fatal) throw e;
  }

  if (options.wrapOutput &&
      (typeof retValue === 'string' || Array.isArray(retValue))) {
    retValue = new ShellString(retValue, state.error, state.errorCode);
  }

  state.currentCmd = 'shell.js';
  return retValue;
}
```
- example usage
```shell
...

// Copy files to release dir
shell.rm('-rf', 'out/Release');
shell.cp('-R', 'stuff/', 'out/Release');

// Replace macros in each .js file
shell.cd('lib');
shell.ls('*.js').forEach(function (file) {
  shell.sed('-i', 'BUILD_VERSION', 'v0.1.2', file);
  shell.sed('-i', /^.*REMOVE_THIS_LINE.*$/, '', file);
  shell.sed('-i', /.*REPLACE_LINE_WITH_MACRO.*\n/, shell.cat('macro.js'), file);
});
shell.cd('..');

// Run external tool synchronously
...
```

#### <a name="apidoc.element.shelljs.mkdir"></a>[function <span class="apidocSignatureSpan">shelljs.</span>mkdir ()](#apidoc.element.shelljs.mkdir)
- description and source-code
```javascript
mkdir = function () {
  var retValue = null;

  state.currentCmd = cmd;
  state.error = null;
  state.errorCode = 0;

  try {
    var args = [].slice.call(arguments, 0);

    // Log the command to stderr, if appropriate
    if (config.verbose) {
      console.error.apply(console, [cmd].concat(args));
    }

    // If this is coming from a pipe, let's set the pipedValue (otherwise, set
    // it to the empty string)
    state.pipedValue = (this && typeof this.stdout === 'string') ? this.stdout : '';

    if (options.unix === false) { // this branch is for exec()
      retValue = fn.apply(this, args);
    } else { // and this branch is for everything else
      if (isObject(args[0]) && args[0].constructor.name === 'Object') {
        // a no-op, allowing the syntax 'touch({'-r': file}, ...)'
      } else if (args.length === 0 || typeof args[0] !== 'string' || args[0].length <= 1 || args[0][0] !== '-') {
        args.unshift(''); // only add dummy option if '-option' not already present
      }

      // flatten out arrays that are arguments, to make the syntax:
      //    'cp([file1, file2, file3], dest);'
      // equivalent to:
      //    'cp(file1, file2, file3, dest);'
      args = args.reduce(function (accum, cur) {
        if (Array.isArray(cur)) {
          return accum.concat(cur);
        }
        accum.push(cur);
        return accum;
      }, []);

      // Convert ShellStrings (basically just String objects) to regular strings
      args = args.map(function (arg) {
        if (isObject(arg) && arg.constructor.name === 'String') {
          return arg.toString();
        }
        return arg;
      });

      // Expand the '~' if appropriate
      var homeDir = getUserHome();
      args = args.map(function (arg) {
        if (typeof arg === 'string' && arg.slice(0, 2) === '~/' || arg === '~') {
          return arg.replace(/^~/, homeDir);
        }
        return arg;
      });

      // Perform glob-expansion on all arguments after globStart, but preserve
      // the arguments before it (like regexes for sed and grep)
      if (!config.noglob && options.allowGlobbing === true) {
        args = args.slice(0, options.globStart).concat(expand(args.slice(options.globStart)));
      }

      try {
        // parse options if options are provided
        if (isObject(options.cmdOptions)) {
          args[0] = parseOptions(args[0], options.cmdOptions);
        }

        retValue = fn.apply(this, args);
      } catch (e) {
<span class="apidocCodeCommentSpan">        /* istanbul ignore else */
</span>        if (e.msg === 'earlyExit') {
          retValue = e.retValue;
        } else {
          throw e; // this is probably a bug that should be thrown up the call stack
        }
      }
    }
  } catch (e) {
    /* istanbul ignore next */
    if (!state.error) {
      // If state.error hasn't been set it's an error thrown by Node, not us - probably a bug...
      console.error('ShellJS: internal error');
      console.error(e.stack || e);
      process.exit(1);
    }
    if (config.fatal) throw e;
  }

  if (options.wrapOutput &&
      (typeof retValue === 'string' || Array.isArray(retValue))) {
    retValue = new ShellString(retValue, state.error, state.errorCode);
  }

  state.currentCmd = 'shell.js';
  return retValue;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.shelljs.mv"></a>[function <span class="apidocSignatureSpan">shelljs.</span>mv ()](#apidoc.element.shelljs.mv)
- description and source-code
```javascript
mv = function () {
  var retValue = null;

  state.currentCmd = cmd;
  state.error = null;
  state.errorCode = 0;

  try {
    var args = [].slice.call(arguments, 0);

    // Log the command to stderr, if appropriate
    if (config.verbose) {
      console.error.apply(console, [cmd].concat(args));
    }

    // If this is coming from a pipe, let's set the pipedValue (otherwise, set
    // it to the empty string)
    state.pipedValue = (this && typeof this.stdout === 'string') ? this.stdout : '';

    if (options.unix === false) { // this branch is for exec()
      retValue = fn.apply(this, args);
    } else { // and this branch is for everything else
      if (isObject(args[0]) && args[0].constructor.name === 'Object') {
        // a no-op, allowing the syntax 'touch({'-r': file}, ...)'
      } else if (args.length === 0 || typeof args[0] !== 'string' || args[0].length <= 1 || args[0][0] !== '-') {
        args.unshift(''); // only add dummy option if '-option' not already present
      }

      // flatten out arrays that are arguments, to make the syntax:
      //    'cp([file1, file2, file3], dest);'
      // equivalent to:
      //    'cp(file1, file2, file3, dest);'
      args = args.reduce(function (accum, cur) {
        if (Array.isArray(cur)) {
          return accum.concat(cur);
        }
        accum.push(cur);
        return accum;
      }, []);

      // Convert ShellStrings (basically just String objects) to regular strings
      args = args.map(function (arg) {
        if (isObject(arg) && arg.constructor.name === 'String') {
          return arg.toString();
        }
        return arg;
      });

      // Expand the '~' if appropriate
      var homeDir = getUserHome();
      args = args.map(function (arg) {
        if (typeof arg === 'string' && arg.slice(0, 2) === '~/' || arg === '~') {
          return arg.replace(/^~/, homeDir);
        }
        return arg;
      });

      // Perform glob-expansion on all arguments after globStart, but preserve
      // the arguments before it (like regexes for sed and grep)
      if (!config.noglob && options.allowGlobbing === true) {
        args = args.slice(0, options.globStart).concat(expand(args.slice(options.globStart)));
      }

      try {
        // parse options if options are provided
        if (isObject(options.cmdOptions)) {
          args[0] = parseOptions(args[0], options.cmdOptions);
        }

        retValue = fn.apply(this, args);
      } catch (e) {
<span class="apidocCodeCommentSpan">        /* istanbul ignore else */
</span>        if (e.msg === 'earlyExit') {
          retValue = e.retValue;
        } else {
          throw e; // this is probably a bug that should be thrown up the call stack
        }
      }
    }
  } catch (e) {
    /* istanbul ignore next */
    if (!state.error) {
      // If state.error hasn't been set it's an error thrown by Node, not us - probably a bug...
      console.error('ShellJS: internal error');
      console.error(e.stack || e);
      process.exit(1);
    }
    if (config.fatal) throw e;
  }

  if (options.wrapOutput &&
      (typeof retValue === 'string' || Array.isArray(retValue))) {
    retValue = new ShellString(retValue, state.error, state.errorCode);
  }

  state.currentCmd = 'shell.js';
  return retValue;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.shelljs.popd"></a>[function <span class="apidocSignatureSpan">shelljs.</span>popd ()](#apidoc.element.shelljs.popd)
- description and source-code
```javascript
popd = function () {
  var retValue = null;

  state.currentCmd = cmd;
  state.error = null;
  state.errorCode = 0;

  try {
    var args = [].slice.call(arguments, 0);

    // Log the command to stderr, if appropriate
    if (config.verbose) {
      console.error.apply(console, [cmd].concat(args));
    }

    // If this is coming from a pipe, let's set the pipedValue (otherwise, set
    // it to the empty string)
    state.pipedValue = (this && typeof this.stdout === 'string') ? this.stdout : '';

    if (options.unix === false) { // this branch is for exec()
      retValue = fn.apply(this, args);
    } else { // and this branch is for everything else
      if (isObject(args[0]) && args[0].constructor.name === 'Object') {
        // a no-op, allowing the syntax 'touch({'-r': file}, ...)'
      } else if (args.length === 0 || typeof args[0] !== 'string' || args[0].length <= 1 || args[0][0] !== '-') {
        args.unshift(''); // only add dummy option if '-option' not already present
      }

      // flatten out arrays that are arguments, to make the syntax:
      //    'cp([file1, file2, file3], dest);'
      // equivalent to:
      //    'cp(file1, file2, file3, dest);'
      args = args.reduce(function (accum, cur) {
        if (Array.isArray(cur)) {
          return accum.concat(cur);
        }
        accum.push(cur);
        return accum;
      }, []);

      // Convert ShellStrings (basically just String objects) to regular strings
      args = args.map(function (arg) {
        if (isObject(arg) && arg.constructor.name === 'String') {
          return arg.toString();
        }
        return arg;
      });

      // Expand the '~' if appropriate
      var homeDir = getUserHome();
      args = args.map(function (arg) {
        if (typeof arg === 'string' && arg.slice(0, 2) === '~/' || arg === '~') {
          return arg.replace(/^~/, homeDir);
        }
        return arg;
      });

      // Perform glob-expansion on all arguments after globStart, but preserve
      // the arguments before it (like regexes for sed and grep)
      if (!config.noglob && options.allowGlobbing === true) {
        args = args.slice(0, options.globStart).concat(expand(args.slice(options.globStart)));
      }

      try {
        // parse options if options are provided
        if (isObject(options.cmdOptions)) {
          args[0] = parseOptions(args[0], options.cmdOptions);
        }

        retValue = fn.apply(this, args);
      } catch (e) {
<span class="apidocCodeCommentSpan">        /* istanbul ignore else */
</span>        if (e.msg === 'earlyExit') {
          retValue = e.retValue;
        } else {
          throw e; // this is probably a bug that should be thrown up the call stack
        }
      }
    }
  } catch (e) {
    /* istanbul ignore next */
    if (!state.error) {
      // If state.error hasn't been set it's an error thrown by Node, not us - probably a bug...
      console.error('ShellJS: internal error');
      console.error(e.stack || e);
      process.exit(1);
    }
    if (config.fatal) throw e;
  }

  if (options.wrapOutput &&
      (typeof retValue === 'string' || Array.isArray(retValue))) {
    retValue = new ShellString(retValue, state.error, state.errorCode);
  }

  state.currentCmd = 'shell.js';
  return retValue;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.shelljs.pushd"></a>[function <span class="apidocSignatureSpan">shelljs.</span>pushd ()](#apidoc.element.shelljs.pushd)
- description and source-code
```javascript
pushd = function () {
  var retValue = null;

  state.currentCmd = cmd;
  state.error = null;
  state.errorCode = 0;

  try {
    var args = [].slice.call(arguments, 0);

    // Log the command to stderr, if appropriate
    if (config.verbose) {
      console.error.apply(console, [cmd].concat(args));
    }

    // If this is coming from a pipe, let's set the pipedValue (otherwise, set
    // it to the empty string)
    state.pipedValue = (this && typeof this.stdout === 'string') ? this.stdout : '';

    if (options.unix === false) { // this branch is for exec()
      retValue = fn.apply(this, args);
    } else { // and this branch is for everything else
      if (isObject(args[0]) && args[0].constructor.name === 'Object') {
        // a no-op, allowing the syntax 'touch({'-r': file}, ...)'
      } else if (args.length === 0 || typeof args[0] !== 'string' || args[0].length <= 1 || args[0][0] !== '-') {
        args.unshift(''); // only add dummy option if '-option' not already present
      }

      // flatten out arrays that are arguments, to make the syntax:
      //    'cp([file1, file2, file3], dest);'
      // equivalent to:
      //    'cp(file1, file2, file3, dest);'
      args = args.reduce(function (accum, cur) {
        if (Array.isArray(cur)) {
          return accum.concat(cur);
        }
        accum.push(cur);
        return accum;
      }, []);

      // Convert ShellStrings (basically just String objects) to regular strings
      args = args.map(function (arg) {
        if (isObject(arg) && arg.constructor.name === 'String') {
          return arg.toString();
        }
        return arg;
      });

      // Expand the '~' if appropriate
      var homeDir = getUserHome();
      args = args.map(function (arg) {
        if (typeof arg === 'string' && arg.slice(0, 2) === '~/' || arg === '~') {
          return arg.replace(/^~/, homeDir);
        }
        return arg;
      });

      // Perform glob-expansion on all arguments after globStart, but preserve
      // the arguments before it (like regexes for sed and grep)
      if (!config.noglob && options.allowGlobbing === true) {
        args = args.slice(0, options.globStart).concat(expand(args.slice(options.globStart)));
      }

      try {
        // parse options if options are provided
        if (isObject(options.cmdOptions)) {
          args[0] = parseOptions(args[0], options.cmdOptions);
        }

        retValue = fn.apply(this, args);
      } catch (e) {
<span class="apidocCodeCommentSpan">        /* istanbul ignore else */
</span>        if (e.msg === 'earlyExit') {
          retValue = e.retValue;
        } else {
          throw e; // this is probably a bug that should be thrown up the call stack
        }
      }
    }
  } catch (e) {
    /* istanbul ignore next */
    if (!state.error) {
      // If state.error hasn't been set it's an error thrown by Node, not us - probably a bug...
      console.error('ShellJS: internal error');
      console.error(e.stack || e);
      process.exit(1);
    }
    if (config.fatal) throw e;
  }

  if (options.wrapOutput &&
      (typeof retValue === 'string' || Array.isArray(retValue))) {
    retValue = new ShellString(retValue, state.error, state.errorCode);
  }

  state.currentCmd = 'shell.js';
  return retValue;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.shelljs.pwd"></a>[function <span class="apidocSignatureSpan">shelljs.</span>pwd ()](#apidoc.element.shelljs.pwd)
- description and source-code
```javascript
pwd = function () {
  var retValue = null;

  state.currentCmd = cmd;
  state.error = null;
  state.errorCode = 0;

  try {
    var args = [].slice.call(arguments, 0);

    // Log the command to stderr, if appropriate
    if (config.verbose) {
      console.error.apply(console, [cmd].concat(args));
    }

    // If this is coming from a pipe, let's set the pipedValue (otherwise, set
    // it to the empty string)
    state.pipedValue = (this && typeof this.stdout === 'string') ? this.stdout : '';

    if (options.unix === false) { // this branch is for exec()
      retValue = fn.apply(this, args);
    } else { // and this branch is for everything else
      if (isObject(args[0]) && args[0].constructor.name === 'Object') {
        // a no-op, allowing the syntax 'touch({'-r': file}, ...)'
      } else if (args.length === 0 || typeof args[0] !== 'string' || args[0].length <= 1 || args[0][0] !== '-') {
        args.unshift(''); // only add dummy option if '-option' not already present
      }

      // flatten out arrays that are arguments, to make the syntax:
      //    'cp([file1, file2, file3], dest);'
      // equivalent to:
      //    'cp(file1, file2, file3, dest);'
      args = args.reduce(function (accum, cur) {
        if (Array.isArray(cur)) {
          return accum.concat(cur);
        }
        accum.push(cur);
        return accum;
      }, []);

      // Convert ShellStrings (basically just String objects) to regular strings
      args = args.map(function (arg) {
        if (isObject(arg) && arg.constructor.name === 'String') {
          return arg.toString();
        }
        return arg;
      });

      // Expand the '~' if appropriate
      var homeDir = getUserHome();
      args = args.map(function (arg) {
        if (typeof arg === 'string' && arg.slice(0, 2) === '~/' || arg === '~') {
          return arg.replace(/^~/, homeDir);
        }
        return arg;
      });

      // Perform glob-expansion on all arguments after globStart, but preserve
      // the arguments before it (like regexes for sed and grep)
      if (!config.noglob && options.allowGlobbing === true) {
        args = args.slice(0, options.globStart).concat(expand(args.slice(options.globStart)));
      }

      try {
        // parse options if options are provided
        if (isObject(options.cmdOptions)) {
          args[0] = parseOptions(args[0], options.cmdOptions);
        }

        retValue = fn.apply(this, args);
      } catch (e) {
<span class="apidocCodeCommentSpan">        /* istanbul ignore else */
</span>        if (e.msg === 'earlyExit') {
          retValue = e.retValue;
        } else {
          throw e; // this is probably a bug that should be thrown up the call stack
        }
      }
    }
  } catch (e) {
    /* istanbul ignore next */
    if (!state.error) {
      // If state.error hasn't been set it's an error thrown by Node, not us - probably a bug...
      console.error('ShellJS: internal error');
      console.error(e.stack || e);
      process.exit(1);
    }
    if (config.fatal) throw e;
  }

  if (options.wrapOutput &&
      (typeof retValue === 'string' || Array.isArray(retValue))) {
    retValue = new ShellString(retValue, state.error, state.errorCode);
  }

  state.currentCmd = 'shell.js';
  return retValue;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.shelljs.rm"></a>[function <span class="apidocSignatureSpan">shelljs.</span>rm ()](#apidoc.element.shelljs.rm)
- description and source-code
```javascript
rm = function () {
  var retValue = null;

  state.currentCmd = cmd;
  state.error = null;
  state.errorCode = 0;

  try {
    var args = [].slice.call(arguments, 0);

    // Log the command to stderr, if appropriate
    if (config.verbose) {
      console.error.apply(console, [cmd].concat(args));
    }

    // If this is coming from a pipe, let's set the pipedValue (otherwise, set
    // it to the empty string)
    state.pipedValue = (this && typeof this.stdout === 'string') ? this.stdout : '';

    if (options.unix === false) { // this branch is for exec()
      retValue = fn.apply(this, args);
    } else { // and this branch is for everything else
      if (isObject(args[0]) && args[0].constructor.name === 'Object') {
        // a no-op, allowing the syntax 'touch({'-r': file}, ...)'
      } else if (args.length === 0 || typeof args[0] !== 'string' || args[0].length <= 1 || args[0][0] !== '-') {
        args.unshift(''); // only add dummy option if '-option' not already present
      }

      // flatten out arrays that are arguments, to make the syntax:
      //    'cp([file1, file2, file3], dest);'
      // equivalent to:
      //    'cp(file1, file2, file3, dest);'
      args = args.reduce(function (accum, cur) {
        if (Array.isArray(cur)) {
          return accum.concat(cur);
        }
        accum.push(cur);
        return accum;
      }, []);

      // Convert ShellStrings (basically just String objects) to regular strings
      args = args.map(function (arg) {
        if (isObject(arg) && arg.constructor.name === 'String') {
          return arg.toString();
        }
        return arg;
      });

      // Expand the '~' if appropriate
      var homeDir = getUserHome();
      args = args.map(function (arg) {
        if (typeof arg === 'string' && arg.slice(0, 2) === '~/' || arg === '~') {
          return arg.replace(/^~/, homeDir);
        }
        return arg;
      });

      // Perform glob-expansion on all arguments after globStart, but preserve
      // the arguments before it (like regexes for sed and grep)
      if (!config.noglob && options.allowGlobbing === true) {
        args = args.slice(0, options.globStart).concat(expand(args.slice(options.globStart)));
      }

      try {
        // parse options if options are provided
        if (isObject(options.cmdOptions)) {
          args[0] = parseOptions(args[0], options.cmdOptions);
        }

        retValue = fn.apply(this, args);
      } catch (e) {
<span class="apidocCodeCommentSpan">        /* istanbul ignore else */
</span>        if (e.msg === 'earlyExit') {
          retValue = e.retValue;
        } else {
          throw e; // this is probably a bug that should be thrown up the call stack
        }
      }
    }
  } catch (e) {
    /* istanbul ignore next */
    if (!state.error) {
      // If state.error hasn't been set it's an error thrown by Node, not us - probably a bug...
      console.error('ShellJS: internal error');
      console.error(e.stack || e);
      process.exit(1);
    }
    if (config.fatal) throw e;
  }

  if (options.wrapOutput &&
      (typeof retValue === 'string' || Array.isArray(retValue))) {
    retValue = new ShellString(retValue, state.error, state.errorCode);
  }

  state.currentCmd = 'shell.js';
  return retValue;
}
```
- example usage
```shell
...

if (!shell.which('git')) {
shell.echo('Sorry, this script requires git');
shell.exit(1);
}

// Copy files to release dir
shell.rm('-rf', 'out/Release');
shell.cp('-R', 'stuff/', 'out/Release');

// Replace macros in each .js file
shell.cd('lib');
shell.ls('*.js').forEach(function (file) {
shell.sed('-i', 'BUILD_VERSION', 'v0.1.2', file);
shell.sed('-i', /^.*REMOVE_THIS_LINE.*$/, '', file);
...
```

#### <a name="apidoc.element.shelljs.sed"></a>[function <span class="apidocSignatureSpan">shelljs.</span>sed ()](#apidoc.element.shelljs.sed)
- description and source-code
```javascript
sed = function () {
  var retValue = null;

  state.currentCmd = cmd;
  state.error = null;
  state.errorCode = 0;

  try {
    var args = [].slice.call(arguments, 0);

    // Log the command to stderr, if appropriate
    if (config.verbose) {
      console.error.apply(console, [cmd].concat(args));
    }

    // If this is coming from a pipe, let's set the pipedValue (otherwise, set
    // it to the empty string)
    state.pipedValue = (this && typeof this.stdout === 'string') ? this.stdout : '';

    if (options.unix === false) { // this branch is for exec()
      retValue = fn.apply(this, args);
    } else { // and this branch is for everything else
      if (isObject(args[0]) && args[0].constructor.name === 'Object') {
        // a no-op, allowing the syntax 'touch({'-r': file}, ...)'
      } else if (args.length === 0 || typeof args[0] !== 'string' || args[0].length <= 1 || args[0][0] !== '-') {
        args.unshift(''); // only add dummy option if '-option' not already present
      }

      // flatten out arrays that are arguments, to make the syntax:
      //    'cp([file1, file2, file3], dest);'
      // equivalent to:
      //    'cp(file1, file2, file3, dest);'
      args = args.reduce(function (accum, cur) {
        if (Array.isArray(cur)) {
          return accum.concat(cur);
        }
        accum.push(cur);
        return accum;
      }, []);

      // Convert ShellStrings (basically just String objects) to regular strings
      args = args.map(function (arg) {
        if (isObject(arg) && arg.constructor.name === 'String') {
          return arg.toString();
        }
        return arg;
      });

      // Expand the '~' if appropriate
      var homeDir = getUserHome();
      args = args.map(function (arg) {
        if (typeof arg === 'string' && arg.slice(0, 2) === '~/' || arg === '~') {
          return arg.replace(/^~/, homeDir);
        }
        return arg;
      });

      // Perform glob-expansion on all arguments after globStart, but preserve
      // the arguments before it (like regexes for sed and grep)
      if (!config.noglob && options.allowGlobbing === true) {
        args = args.slice(0, options.globStart).concat(expand(args.slice(options.globStart)));
      }

      try {
        // parse options if options are provided
        if (isObject(options.cmdOptions)) {
          args[0] = parseOptions(args[0], options.cmdOptions);
        }

        retValue = fn.apply(this, args);
      } catch (e) {
<span class="apidocCodeCommentSpan">        /* istanbul ignore else */
</span>        if (e.msg === 'earlyExit') {
          retValue = e.retValue;
        } else {
          throw e; // this is probably a bug that should be thrown up the call stack
        }
      }
    }
  } catch (e) {
    /* istanbul ignore next */
    if (!state.error) {
      // If state.error hasn't been set it's an error thrown by Node, not us - probably a bug...
      console.error('ShellJS: internal error');
      console.error(e.stack || e);
      process.exit(1);
    }
    if (config.fatal) throw e;
  }

  if (options.wrapOutput &&
      (typeof retValue === 'string' || Array.isArray(retValue))) {
    retValue = new ShellString(retValue, state.error, state.errorCode);
  }

  state.currentCmd = 'shell.js';
  return retValue;
}
```
- example usage
```shell
...
// Copy files to release dir
shell.rm('-rf', 'out/Release');
shell.cp('-R', 'stuff/', 'out/Release');

// Replace macros in each .js file
shell.cd('lib');
shell.ls('*.js').forEach(function (file) {
  shell.sed('-i', 'BUILD_VERSION', 'v0.1.2', file);
  shell.sed('-i', /^.*REMOVE_THIS_LINE.*$/, '', file);
  shell.sed('-i', /.*REPLACE_LINE_WITH_MACRO.*\n/, shell.cat('macro.js'), file);
});
shell.cd('..');

// Run external tool synchronously
if (shell.exec('git commit -am "Auto-commit"').code !== 0) {
...
```

#### <a name="apidoc.element.shelljs.set"></a>[function <span class="apidocSignatureSpan">shelljs.</span>set ()](#apidoc.element.shelljs.set)
- description and source-code
```javascript
set = function () {
  var retValue = null;

  state.currentCmd = cmd;
  state.error = null;
  state.errorCode = 0;

  try {
    var args = [].slice.call(arguments, 0);

    // Log the command to stderr, if appropriate
    if (config.verbose) {
      console.error.apply(console, [cmd].concat(args));
    }

    // If this is coming from a pipe, let's set the pipedValue (otherwise, set
    // it to the empty string)
    state.pipedValue = (this && typeof this.stdout === 'string') ? this.stdout : '';

    if (options.unix === false) { // this branch is for exec()
      retValue = fn.apply(this, args);
    } else { // and this branch is for everything else
      if (isObject(args[0]) && args[0].constructor.name === 'Object') {
        // a no-op, allowing the syntax 'touch({'-r': file}, ...)'
      } else if (args.length === 0 || typeof args[0] !== 'string' || args[0].length <= 1 || args[0][0] !== '-') {
        args.unshift(''); // only add dummy option if '-option' not already present
      }

      // flatten out arrays that are arguments, to make the syntax:
      //    'cp([file1, file2, file3], dest);'
      // equivalent to:
      //    'cp(file1, file2, file3, dest);'
      args = args.reduce(function (accum, cur) {
        if (Array.isArray(cur)) {
          return accum.concat(cur);
        }
        accum.push(cur);
        return accum;
      }, []);

      // Convert ShellStrings (basically just String objects) to regular strings
      args = args.map(function (arg) {
        if (isObject(arg) && arg.constructor.name === 'String') {
          return arg.toString();
        }
        return arg;
      });

      // Expand the '~' if appropriate
      var homeDir = getUserHome();
      args = args.map(function (arg) {
        if (typeof arg === 'string' && arg.slice(0, 2) === '~/' || arg === '~') {
          return arg.replace(/^~/, homeDir);
        }
        return arg;
      });

      // Perform glob-expansion on all arguments after globStart, but preserve
      // the arguments before it (like regexes for sed and grep)
      if (!config.noglob && options.allowGlobbing === true) {
        args = args.slice(0, options.globStart).concat(expand(args.slice(options.globStart)));
      }

      try {
        // parse options if options are provided
        if (isObject(options.cmdOptions)) {
          args[0] = parseOptions(args[0], options.cmdOptions);
        }

        retValue = fn.apply(this, args);
      } catch (e) {
<span class="apidocCodeCommentSpan">        /* istanbul ignore else */
</span>        if (e.msg === 'earlyExit') {
          retValue = e.retValue;
        } else {
          throw e; // this is probably a bug that should be thrown up the call stack
        }
      }
    }
  } catch (e) {
    /* istanbul ignore next */
    if (!state.error) {
      // If state.error hasn't been set it's an error thrown by Node, not us - probably a bug...
      console.error('ShellJS: internal error');
      console.error(e.stack || e);
      process.exit(1);
    }
    if (config.fatal) throw e;
  }

  if (options.wrapOutput &&
      (typeof retValue === 'string' || Array.isArray(retValue))) {
    retValue = new ShellString(retValue, state.error, state.errorCode);
  }

  state.currentCmd = 'shell.js';
  return retValue;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.shelljs.sort"></a>[function <span class="apidocSignatureSpan">shelljs.</span>sort ()](#apidoc.element.shelljs.sort)
- description and source-code
```javascript
sort = function () {
  var retValue = null;

  state.currentCmd = cmd;
  state.error = null;
  state.errorCode = 0;

  try {
    var args = [].slice.call(arguments, 0);

    // Log the command to stderr, if appropriate
    if (config.verbose) {
      console.error.apply(console, [cmd].concat(args));
    }

    // If this is coming from a pipe, let's set the pipedValue (otherwise, set
    // it to the empty string)
    state.pipedValue = (this && typeof this.stdout === 'string') ? this.stdout : '';

    if (options.unix === false) { // this branch is for exec()
      retValue = fn.apply(this, args);
    } else { // and this branch is for everything else
      if (isObject(args[0]) && args[0].constructor.name === 'Object') {
        // a no-op, allowing the syntax 'touch({'-r': file}, ...)'
      } else if (args.length === 0 || typeof args[0] !== 'string' || args[0].length <= 1 || args[0][0] !== '-') {
        args.unshift(''); // only add dummy option if '-option' not already present
      }

      // flatten out arrays that are arguments, to make the syntax:
      //    'cp([file1, file2, file3], dest);'
      // equivalent to:
      //    'cp(file1, file2, file3, dest);'
      args = args.reduce(function (accum, cur) {
        if (Array.isArray(cur)) {
          return accum.concat(cur);
        }
        accum.push(cur);
        return accum;
      }, []);

      // Convert ShellStrings (basically just String objects) to regular strings
      args = args.map(function (arg) {
        if (isObject(arg) && arg.constructor.name === 'String') {
          return arg.toString();
        }
        return arg;
      });

      // Expand the '~' if appropriate
      var homeDir = getUserHome();
      args = args.map(function (arg) {
        if (typeof arg === 'string' && arg.slice(0, 2) === '~/' || arg === '~') {
          return arg.replace(/^~/, homeDir);
        }
        return arg;
      });

      // Perform glob-expansion on all arguments after globStart, but preserve
      // the arguments before it (like regexes for sed and grep)
      if (!config.noglob && options.allowGlobbing === true) {
        args = args.slice(0, options.globStart).concat(expand(args.slice(options.globStart)));
      }

      try {
        // parse options if options are provided
        if (isObject(options.cmdOptions)) {
          args[0] = parseOptions(args[0], options.cmdOptions);
        }

        retValue = fn.apply(this, args);
      } catch (e) {
<span class="apidocCodeCommentSpan">        /* istanbul ignore else */
</span>        if (e.msg === 'earlyExit') {
          retValue = e.retValue;
        } else {
          throw e; // this is probably a bug that should be thrown up the call stack
        }
      }
    }
  } catch (e) {
    /* istanbul ignore next */
    if (!state.error) {
      // If state.error hasn't been set it's an error thrown by Node, not us - probably a bug...
      console.error('ShellJS: internal error');
      console.error(e.stack || e);
      process.exit(1);
    }
    if (config.fatal) throw e;
  }

  if (options.wrapOutput &&
      (typeof retValue === 'string' || Array.isArray(retValue))) {
    retValue = new ShellString(retValue, state.error, state.errorCode);
  }

  state.currentCmd = 'shell.js';
  return retValue;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.shelljs.tail"></a>[function <span class="apidocSignatureSpan">shelljs.</span>tail ()](#apidoc.element.shelljs.tail)
- description and source-code
```javascript
tail = function () {
  var retValue = null;

  state.currentCmd = cmd;
  state.error = null;
  state.errorCode = 0;

  try {
    var args = [].slice.call(arguments, 0);

    // Log the command to stderr, if appropriate
    if (config.verbose) {
      console.error.apply(console, [cmd].concat(args));
    }

    // If this is coming from a pipe, let's set the pipedValue (otherwise, set
    // it to the empty string)
    state.pipedValue = (this && typeof this.stdout === 'string') ? this.stdout : '';

    if (options.unix === false) { // this branch is for exec()
      retValue = fn.apply(this, args);
    } else { // and this branch is for everything else
      if (isObject(args[0]) && args[0].constructor.name === 'Object') {
        // a no-op, allowing the syntax 'touch({'-r': file}, ...)'
      } else if (args.length === 0 || typeof args[0] !== 'string' || args[0].length <= 1 || args[0][0] !== '-') {
        args.unshift(''); // only add dummy option if '-option' not already present
      }

      // flatten out arrays that are arguments, to make the syntax:
      //    'cp([file1, file2, file3], dest);'
      // equivalent to:
      //    'cp(file1, file2, file3, dest);'
      args = args.reduce(function (accum, cur) {
        if (Array.isArray(cur)) {
          return accum.concat(cur);
        }
        accum.push(cur);
        return accum;
      }, []);

      // Convert ShellStrings (basically just String objects) to regular strings
      args = args.map(function (arg) {
        if (isObject(arg) && arg.constructor.name === 'String') {
          return arg.toString();
        }
        return arg;
      });

      // Expand the '~' if appropriate
      var homeDir = getUserHome();
      args = args.map(function (arg) {
        if (typeof arg === 'string' && arg.slice(0, 2) === '~/' || arg === '~') {
          return arg.replace(/^~/, homeDir);
        }
        return arg;
      });

      // Perform glob-expansion on all arguments after globStart, but preserve
      // the arguments before it (like regexes for sed and grep)
      if (!config.noglob && options.allowGlobbing === true) {
        args = args.slice(0, options.globStart).concat(expand(args.slice(options.globStart)));
      }

      try {
        // parse options if options are provided
        if (isObject(options.cmdOptions)) {
          args[0] = parseOptions(args[0], options.cmdOptions);
        }

        retValue = fn.apply(this, args);
      } catch (e) {
<span class="apidocCodeCommentSpan">        /* istanbul ignore else */
</span>        if (e.msg === 'earlyExit') {
          retValue = e.retValue;
        } else {
          throw e; // this is probably a bug that should be thrown up the call stack
        }
      }
    }
  } catch (e) {
    /* istanbul ignore next */
    if (!state.error) {
      // If state.error hasn't been set it's an error thrown by Node, not us - probably a bug...
      console.error('ShellJS: internal error');
      console.error(e.stack || e);
      process.exit(1);
    }
    if (config.fatal) throw e;
  }

  if (options.wrapOutput &&
      (typeof retValue === 'string' || Array.isArray(retValue))) {
    retValue = new ShellString(retValue, state.error, state.errorCode);
  }

  state.currentCmd = 'shell.js';
  return retValue;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.shelljs.tempdir"></a>[function <span class="apidocSignatureSpan">shelljs.</span>tempdir ()](#apidoc.element.shelljs.tempdir)
- description and source-code
```javascript
tempdir = function () {
  var retValue = null;

  state.currentCmd = cmd;
  state.error = null;
  state.errorCode = 0;

  try {
    var args = [].slice.call(arguments, 0);

    // Log the command to stderr, if appropriate
    if (config.verbose) {
      console.error.apply(console, [cmd].concat(args));
    }

    // If this is coming from a pipe, let's set the pipedValue (otherwise, set
    // it to the empty string)
    state.pipedValue = (this && typeof this.stdout === 'string') ? this.stdout : '';

    if (options.unix === false) { // this branch is for exec()
      retValue = fn.apply(this, args);
    } else { // and this branch is for everything else
      if (isObject(args[0]) && args[0].constructor.name === 'Object') {
        // a no-op, allowing the syntax 'touch({'-r': file}, ...)'
      } else if (args.length === 0 || typeof args[0] !== 'string' || args[0].length <= 1 || args[0][0] !== '-') {
        args.unshift(''); // only add dummy option if '-option' not already present
      }

      // flatten out arrays that are arguments, to make the syntax:
      //    'cp([file1, file2, file3], dest);'
      // equivalent to:
      //    'cp(file1, file2, file3, dest);'
      args = args.reduce(function (accum, cur) {
        if (Array.isArray(cur)) {
          return accum.concat(cur);
        }
        accum.push(cur);
        return accum;
      }, []);

      // Convert ShellStrings (basically just String objects) to regular strings
      args = args.map(function (arg) {
        if (isObject(arg) && arg.constructor.name === 'String') {
          return arg.toString();
        }
        return arg;
      });

      // Expand the '~' if appropriate
      var homeDir = getUserHome();
      args = args.map(function (arg) {
        if (typeof arg === 'string' && arg.slice(0, 2) === '~/' || arg === '~') {
          return arg.replace(/^~/, homeDir);
        }
        return arg;
      });

      // Perform glob-expansion on all arguments after globStart, but preserve
      // the arguments before it (like regexes for sed and grep)
      if (!config.noglob && options.allowGlobbing === true) {
        args = args.slice(0, options.globStart).concat(expand(args.slice(options.globStart)));
      }

      try {
        // parse options if options are provided
        if (isObject(options.cmdOptions)) {
          args[0] = parseOptions(args[0], options.cmdOptions);
        }

        retValue = fn.apply(this, args);
      } catch (e) {
<span class="apidocCodeCommentSpan">        /* istanbul ignore else */
</span>        if (e.msg === 'earlyExit') {
          retValue = e.retValue;
        } else {
          throw e; // this is probably a bug that should be thrown up the call stack
        }
      }
    }
  } catch (e) {
    /* istanbul ignore next */
    if (!state.error) {
      // If state.error hasn't been set it's an error thrown by Node, not us - probably a bug...
      console.error('ShellJS: internal error');
      console.error(e.stack || e);
      process.exit(1);
    }
    if (config.fatal) throw e;
  }

  if (options.wrapOutput &&
      (typeof retValue === 'string' || Array.isArray(retValue))) {
    retValue = new ShellString(retValue, state.error, state.errorCode);
  }

  state.currentCmd = 'shell.js';
  return retValue;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.shelljs.test"></a>[function <span class="apidocSignatureSpan">shelljs.</span>test ()](#apidoc.element.shelljs.test)
- description and source-code
```javascript
test = function () {
  var retValue = null;

  state.currentCmd = cmd;
  state.error = null;
  state.errorCode = 0;

  try {
    var args = [].slice.call(arguments, 0);

    // Log the command to stderr, if appropriate
    if (config.verbose) {
      console.error.apply(console, [cmd].concat(args));
    }

    // If this is coming from a pipe, let's set the pipedValue (otherwise, set
    // it to the empty string)
    state.pipedValue = (this && typeof this.stdout === 'string') ? this.stdout : '';

    if (options.unix === false) { // this branch is for exec()
      retValue = fn.apply(this, args);
    } else { // and this branch is for everything else
      if (isObject(args[0]) && args[0].constructor.name === 'Object') {
        // a no-op, allowing the syntax 'touch({'-r': file}, ...)'
      } else if (args.length === 0 || typeof args[0] !== 'string' || args[0].length <= 1 || args[0][0] !== '-') {
        args.unshift(''); // only add dummy option if '-option' not already present
      }

      // flatten out arrays that are arguments, to make the syntax:
      //    'cp([file1, file2, file3], dest);'
      // equivalent to:
      //    'cp(file1, file2, file3, dest);'
      args = args.reduce(function (accum, cur) {
        if (Array.isArray(cur)) {
          return accum.concat(cur);
        }
        accum.push(cur);
        return accum;
      }, []);

      // Convert ShellStrings (basically just String objects) to regular strings
      args = args.map(function (arg) {
        if (isObject(arg) && arg.constructor.name === 'String') {
          return arg.toString();
        }
        return arg;
      });

      // Expand the '~' if appropriate
      var homeDir = getUserHome();
      args = args.map(function (arg) {
        if (typeof arg === 'string' && arg.slice(0, 2) === '~/' || arg === '~') {
          return arg.replace(/^~/, homeDir);
        }
        return arg;
      });

      // Perform glob-expansion on all arguments after globStart, but preserve
      // the arguments before it (like regexes for sed and grep)
      if (!config.noglob && options.allowGlobbing === true) {
        args = args.slice(0, options.globStart).concat(expand(args.slice(options.globStart)));
      }

      try {
        // parse options if options are provided
        if (isObject(options.cmdOptions)) {
          args[0] = parseOptions(args[0], options.cmdOptions);
        }

        retValue = fn.apply(this, args);
      } catch (e) {
<span class="apidocCodeCommentSpan">        /* istanbul ignore else */
</span>        if (e.msg === 'earlyExit') {
          retValue = e.retValue;
        } else {
          throw e; // this is probably a bug that should be thrown up the call stack
        }
      }
    }
  } catch (e) {
    /* istanbul ignore next */
    if (!state.error) {
      // If state.error hasn't been set it's an error thrown by Node, not us - probably a bug...
      console.error('ShellJS: internal error');
      console.error(e.stack || e);
      process.exit(1);
    }
    if (config.fatal) throw e;
  }

  if (options.wrapOutput &&
      (typeof retValue === 'string' || Array.isArray(retValue))) {
    retValue = new ShellString(retValue, state.error, state.errorCode);
  }

  state.currentCmd = 'shell.js';
  return retValue;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.shelljs.touch"></a>[function <span class="apidocSignatureSpan">shelljs.</span>touch ()](#apidoc.element.shelljs.touch)
- description and source-code
```javascript
touch = function () {
  var retValue = null;

  state.currentCmd = cmd;
  state.error = null;
  state.errorCode = 0;

  try {
    var args = [].slice.call(arguments, 0);

    // Log the command to stderr, if appropriate
    if (config.verbose) {
      console.error.apply(console, [cmd].concat(args));
    }

    // If this is coming from a pipe, let's set the pipedValue (otherwise, set
    // it to the empty string)
    state.pipedValue = (this && typeof this.stdout === 'string') ? this.stdout : '';

    if (options.unix === false) { // this branch is for exec()
      retValue = fn.apply(this, args);
    } else { // and this branch is for everything else
      if (isObject(args[0]) && args[0].constructor.name === 'Object') {
        // a no-op, allowing the syntax 'touch({'-r': file}, ...)'
      } else if (args.length === 0 || typeof args[0] !== 'string' || args[0].length <= 1 || args[0][0] !== '-') {
        args.unshift(''); // only add dummy option if '-option' not already present
      }

      // flatten out arrays that are arguments, to make the syntax:
      //    'cp([file1, file2, file3], dest);'
      // equivalent to:
      //    'cp(file1, file2, file3, dest);'
      args = args.reduce(function (accum, cur) {
        if (Array.isArray(cur)) {
          return accum.concat(cur);
        }
        accum.push(cur);
        return accum;
      }, []);

      // Convert ShellStrings (basically just String objects) to regular strings
      args = args.map(function (arg) {
        if (isObject(arg) && arg.constructor.name === 'String') {
          return arg.toString();
        }
        return arg;
      });

      // Expand the '~' if appropriate
      var homeDir = getUserHome();
      args = args.map(function (arg) {
        if (typeof arg === 'string' && arg.slice(0, 2) === '~/' || arg === '~') {
          return arg.replace(/^~/, homeDir);
        }
        return arg;
      });

      // Perform glob-expansion on all arguments after globStart, but preserve
      // the arguments before it (like regexes for sed and grep)
      if (!config.noglob && options.allowGlobbing === true) {
        args = args.slice(0, options.globStart).concat(expand(args.slice(options.globStart)));
      }

      try {
        // parse options if options are provided
        if (isObject(options.cmdOptions)) {
          args[0] = parseOptions(args[0], options.cmdOptions);
        }

        retValue = fn.apply(this, args);
      } catch (e) {
<span class="apidocCodeCommentSpan">        /* istanbul ignore else */
</span>        if (e.msg === 'earlyExit') {
          retValue = e.retValue;
        } else {
          throw e; // this is probably a bug that should be thrown up the call stack
        }
      }
    }
  } catch (e) {
    /* istanbul ignore next */
    if (!state.error) {
      // If state.error hasn't been set it's an error thrown by Node, not us - probably a bug...
      console.error('ShellJS: internal error');
      console.error(e.stack || e);
      process.exit(1);
    }
    if (config.fatal) throw e;
  }

  if (options.wrapOutput &&
      (typeof retValue === 'string' || Array.isArray(retValue))) {
    retValue = new ShellString(retValue, state.error, state.errorCode);
  }

  state.currentCmd = 'shell.js';
  return retValue;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.shelljs.uniq"></a>[function <span class="apidocSignatureSpan">shelljs.</span>uniq ()](#apidoc.element.shelljs.uniq)
- description and source-code
```javascript
uniq = function () {
  var retValue = null;

  state.currentCmd = cmd;
  state.error = null;
  state.errorCode = 0;

  try {
    var args = [].slice.call(arguments, 0);

    // Log the command to stderr, if appropriate
    if (config.verbose) {
      console.error.apply(console, [cmd].concat(args));
    }

    // If this is coming from a pipe, let's set the pipedValue (otherwise, set
    // it to the empty string)
    state.pipedValue = (this && typeof this.stdout === 'string') ? this.stdout : '';

    if (options.unix === false) { // this branch is for exec()
      retValue = fn.apply(this, args);
    } else { // and this branch is for everything else
      if (isObject(args[0]) && args[0].constructor.name === 'Object') {
        // a no-op, allowing the syntax 'touch({'-r': file}, ...)'
      } else if (args.length === 0 || typeof args[0] !== 'string' || args[0].length <= 1 || args[0][0] !== '-') {
        args.unshift(''); // only add dummy option if '-option' not already present
      }

      // flatten out arrays that are arguments, to make the syntax:
      //    'cp([file1, file2, file3], dest);'
      // equivalent to:
      //    'cp(file1, file2, file3, dest);'
      args = args.reduce(function (accum, cur) {
        if (Array.isArray(cur)) {
          return accum.concat(cur);
        }
        accum.push(cur);
        return accum;
      }, []);

      // Convert ShellStrings (basically just String objects) to regular strings
      args = args.map(function (arg) {
        if (isObject(arg) && arg.constructor.name === 'String') {
          return arg.toString();
        }
        return arg;
      });

      // Expand the '~' if appropriate
      var homeDir = getUserHome();
      args = args.map(function (arg) {
        if (typeof arg === 'string' && arg.slice(0, 2) === '~/' || arg === '~') {
          return arg.replace(/^~/, homeDir);
        }
        return arg;
      });

      // Perform glob-expansion on all arguments after globStart, but preserve
      // the arguments before it (like regexes for sed and grep)
      if (!config.noglob && options.allowGlobbing === true) {
        args = args.slice(0, options.globStart).concat(expand(args.slice(options.globStart)));
      }

      try {
        // parse options if options are provided
        if (isObject(options.cmdOptions)) {
          args[0] = parseOptions(args[0], options.cmdOptions);
        }

        retValue = fn.apply(this, args);
      } catch (e) {
<span class="apidocCodeCommentSpan">        /* istanbul ignore else */
</span>        if (e.msg === 'earlyExit') {
          retValue = e.retValue;
        } else {
          throw e; // this is probably a bug that should be thrown up the call stack
        }
      }
    }
  } catch (e) {
    /* istanbul ignore next */
    if (!state.error) {
      // If state.error hasn't been set it's an error thrown by Node, not us - probably a bug...
      console.error('ShellJS: internal error');
      console.error(e.stack || e);
      process.exit(1);
    }
    if (config.fatal) throw e;
  }

  if (options.wrapOutput &&
      (typeof retValue === 'string' || Array.isArray(retValue))) {
    retValue = new ShellString(retValue, state.error, state.errorCode);
  }

  state.currentCmd = 'shell.js';
  return retValue;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.shelljs.which"></a>[function <span class="apidocSignatureSpan">shelljs.</span>which ()](#apidoc.element.shelljs.which)
- description and source-code
```javascript
which = function () {
  var retValue = null;

  state.currentCmd = cmd;
  state.error = null;
  state.errorCode = 0;

  try {
    var args = [].slice.call(arguments, 0);

    // Log the command to stderr, if appropriate
    if (config.verbose) {
      console.error.apply(console, [cmd].concat(args));
    }

    // If this is coming from a pipe, let's set the pipedValue (otherwise, set
    // it to the empty string)
    state.pipedValue = (this && typeof this.stdout === 'string') ? this.stdout : '';

    if (options.unix === false) { // this branch is for exec()
      retValue = fn.apply(this, args);
    } else { // and this branch is for everything else
      if (isObject(args[0]) && args[0].constructor.name === 'Object') {
        // a no-op, allowing the syntax 'touch({'-r': file}, ...)'
      } else if (args.length === 0 || typeof args[0] !== 'string' || args[0].length <= 1 || args[0][0] !== '-') {
        args.unshift(''); // only add dummy option if '-option' not already present
      }

      // flatten out arrays that are arguments, to make the syntax:
      //    'cp([file1, file2, file3], dest);'
      // equivalent to:
      //    'cp(file1, file2, file3, dest);'
      args = args.reduce(function (accum, cur) {
        if (Array.isArray(cur)) {
          return accum.concat(cur);
        }
        accum.push(cur);
        return accum;
      }, []);

      // Convert ShellStrings (basically just String objects) to regular strings
      args = args.map(function (arg) {
        if (isObject(arg) && arg.constructor.name === 'String') {
          return arg.toString();
        }
        return arg;
      });

      // Expand the '~' if appropriate
      var homeDir = getUserHome();
      args = args.map(function (arg) {
        if (typeof arg === 'string' && arg.slice(0, 2) === '~/' || arg === '~') {
          return arg.replace(/^~/, homeDir);
        }
        return arg;
      });

      // Perform glob-expansion on all arguments after globStart, but preserve
      // the arguments before it (like regexes for sed and grep)
      if (!config.noglob && options.allowGlobbing === true) {
        args = args.slice(0, options.globStart).concat(expand(args.slice(options.globStart)));
      }

      try {
        // parse options if options are provided
        if (isObject(options.cmdOptions)) {
          args[0] = parseOptions(args[0], options.cmdOptions);
        }

        retValue = fn.apply(this, args);
      } catch (e) {
<span class="apidocCodeCommentSpan">        /* istanbul ignore else */
</span>        if (e.msg === 'earlyExit') {
          retValue = e.retValue;
        } else {
          throw e; // this is probably a bug that should be thrown up the call stack
        }
      }
    }
  } catch (e) {
    /* istanbul ignore next */
    if (!state.error) {
      // If state.error hasn't been set it's an error thrown by Node, not us - probably a bug...
      console.error('ShellJS: internal error');
      console.error(e.stack || e);
      process.exit(1);
    }
    if (config.fatal) throw e;
  }

  if (options.wrapOutput &&
      (typeof retValue === 'string' || Array.isArray(retValue))) {
    retValue = new ShellString(retValue, state.error, state.errorCode);
  }

  state.currentCmd = 'shell.js';
  return retValue;
}
```
- example usage
```shell
...
'''

## Examples

'''javascript
var shell = require('shelljs');

if (!shell.which('git')) {
  shell.echo('Sorry, this script requires git');
  shell.exit(1);
}

// Copy files to release dir
shell.rm('-rf', 'out/Release');
shell.cp('-R', 'stuff/', 'out/Release');
...
```



# <a name="apidoc.module.shelljs.config"></a>[module shelljs.config](#apidoc.module.shelljs.config)

#### <a name="apidoc.element.shelljs.config.reset"></a>[function <span class="apidocSignatureSpan">shelljs.config.</span>reset ()](#apidoc.element.shelljs.config.reset)
- description and source-code
```javascript
reset = function () {
  objectAssign(this, DEFAULT_CONFIG);
  if (!isElectron) {
    this.execPath = process.execPath;
  }
}
```
- example usage
```shell
...

'''javascript
config.globOptions = {nodir: true};
'''

Use this value for calls to 'glob.sync()' instead of the default options.

### config.reset()

Example:

'''javascript
var shell = require('shelljs');
// Make changes to shell.config, and do stuff...
/* ... */
...
```

#### <a name="apidoc.element.shelljs.config.resetForTesting"></a>[function <span class="apidocSignatureSpan">shelljs.config.</span>resetForTesting ()](#apidoc.element.shelljs.config.resetForTesting)
- description and source-code
```javascript
resetForTesting = function () {
  this.reset();
  this.silent = true;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
