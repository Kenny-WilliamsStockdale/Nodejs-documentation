# Nodejs-documentation

## Node.js Reserved Keywords

### ```process.pid``` property returns the PID of the process.
``` JavaScript
  const { pid } = require('process');

  console.log(`This process is pid ${pid}`);
```
### ```process.argv``` property returns an array containing the command-line arguments passed when the Node.js process was launched. The first element will be process.execPath. The second element will be the path to the JavaScript file being executed. The remaining elements will be any additional command-line arguments.
``` JavaScript
  const { argv } = require('process');

  // print process.argv
  argv.forEach((val, index) => {
    console.log(`${index}: ${val}`);
  });
```
### ```process.env``` property returns an object containing the user environment.
``` JavaScript
  {
    TERM: 'xterm-256color',
    SHELL: '/usr/local/bin/bash',
    USER: 'maciej',
    PATH: '~/.bin/:/usr/bin:/bin:/usr/sbin:/sbin:/usr/local/bin',
    PWD: '/Users/maciej',
    EDITOR: 'vim',
    SHLVL: '1',
    HOME: '/Users/maciej',
    LOGNAME: 'maciej',
    _: '/usr/local/bin/node'
  }
```
### `process.platform`: Platform name, such as `darwin` for macOS. Property returns a string identifying the operating system platform on which the Node.js process is running.
``` JavaScript
  const { platform } = require('process');

  console.log(`This platform is ${platform}`);
```
### `process.release`: This Node's release URL. Returns an Object containing metadata related to the current release, including URLs for the source tarball and headers-only tarball.
#### Example:
``` JavaScript
  {
    name: 'node',
    lts: 'Erbium',
    sourceUrl: 'https://nodejs.org/download/release/v12.18.1/node-v12.18.1.tar.gz',
    headersUrl: 'https://nodejs.org/download/release/v12.18.1/node-v12.18.1-headers.tar.gz',
    libUrl: 'https://nodejs.org/download/release/v12.18.1/win-x64/node.lib'
  }
```
### `process.versions`: A list of versions of Google Chrome V8, zlib, uv, etc. Returns an object listing the version strings of Node.js and its dependencies. 
``` JavaScript
    const { versions } = require('process');

    console.log(versions)
```
#### Output example:
``` JavaScript
    { node: '11.13.0',
    v8: '7.0.276.38-node.18',
    uv: '1.27.0',
    zlib: '1.2.11',
    brotli: '1.0.7',
    ares: '1.15.0',
    modules: '67',
    nghttp2: '1.34.0',
    napi: '4',
    llhttp: '1.1.1',
    openssl: '1.1.1b',
    cldr: '34.0',
    icu: '63.1',
    tz: '2018e',
    unicode: '11.0' }
```
### `process.stdin()`: The standard input (for reading). The process.stdin property is an inbuilt application programming interface of the process module which listens for the user input. The stdin property of the process object is a Readable Stream. It uses on() function to listen for the event.
``` JavaScript
  // Node.js program to demonstrate the
  // process.stdin Property

  // Enter any texts ( User input)
  process.stdin.on('data', data => {
  console.log(`You typed ${data.toString()}`);
  process.exit();
  });

```
### `process.stdout()`: The Standard output (for writing). Similar to console.log but stream the output continuously. Both process.stdout and console.log in NodeJS have basic functionality to display messages on the console.
``` JavaScript
// for stdout
  <script>
      // For process.std.out 
      process.stdout.write("Hello");
      process.stdout.write("World");
      process.stdout.write("!!!");
  </script>
  // output: HelloWorld!!!

  // for console.log
  <script>
    // For console.log
    console.log("Hello");
    console.log("World");
    console.log("!!!");
  </script>
  //output:
  //Hello
  //World
  //!!! 
```
### `process.uptime()`: Time of how long this process is running. Measured in seconds. Use Math.floor() to get whole seconds.
``` JavaScript

```
### `process.memoryUsage()`: Resident set size, total heap and used heap memory usage
### `process.exit()`: Terminating this process
### `process.kill()`: Termination of another process