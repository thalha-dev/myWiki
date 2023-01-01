# NODE BASICS

##### To run repl

```node```, in terminal.

##### THINGS DIFFERENT IN NODEJS

* 'gloabal' object instead of 'window' object.
* CommonJs module instead of ES6 module.
* runs on server not in browser.
* the console is the terminal window.

##### OS MODULE FUNCTIONS

```javascript 
const os = require("os");

console.log(os.type());
console.log(os.version());
console.log(os.homedir());
console.log(os.uptime());
console.log(os.machine());
console.log(os.hostname());
console.log(os.cpus());
console.log(os.userInfo());
console.log(os.networkInterfaces());
console.log(os.tmpdir());
```
##### ALWAYS AVAILABLE VARIABLES

```javascript
console.log(__dirname);
console.log(__filename);
```

##### PATH MODULE FUNCTIONS
```javascript
const path = require("path");

console.log(path.dirname(__filename));
console.log(path.basename(__filename));
console.log(path.extname(__filename));
console.log(path.parse(__filename));

```

##### COMMONJS MODULES 

**To Create a module and export it** 

```javascript 
module.exports = { add, subtract, multiply, divide };

// OR

exports.add = ( a , b ) => a + b;
...

```

**To use an exported module** 


```javascript 
const math = require("./maths");
// OR
const { add , subtract } = require("./maths"); -- destructure
```

##### FILE MANIPULATION

* 'fs' module need to be required.
* 'path' module need to be required for get the path of file or dir.

```javascript
const fs = require("fs");
const path = require("path");

```

**Syncronous code** 

```javascript
fs.readFile(__dirname + "/files/stater.txt", "utf8", (err, data) => {
  if (err) {
    throw err;
  }
  console.log(data);
});

fs.readFile(path.join(__dirname, "files", "stater.txt"), (err, data) => {
  if (err) {
    throw err;
  }
  console.log(data);
  console.log(data.toString());
});

fs.writeFile(
  path.join(__dirname, "files", "reply.txt"),
  "Hellow THALHA ",
  (err) => {
    if (err) {
      throw err;
    }
    console.log("Write complete");
  }
);

fs.appendFile(
  path.join(__dirname, "files", "reply.txt"),
  `
    Hello how are you ? fine ? 
    `,
  (err) => {
    if (err) {
      throw err;
    }
    console.log("Append complete");
  }
);

fs.rename(
  path.join(__dirname, "files", "reply.txt"),
  path.join(__dirname, "files", "message.txt"),
  (err) => {
    if (err) {
      throw err;
    }
    console.log("Rename complete");
  }
);

process.on("uncaughtException", (err) => {
  console.error(`There was an uncaught error : ${err}`);
  process.exit(1);
});

```

**asyncronous code** 

```javascript
const fileOps = async () => {
  try {
    const data = await fsPromises.readFile(
      path.join(__dirname, "files", "stater.txt"),
      "utf8"
    );
    await fsPromises.unlink(path.join(__dirname, "files", "stater.txt"));

    console.log(data);
    await fsPromises.writeFile(
      path.join(__dirname, "files", "promiseWrite.txt"),
      data
    );
    await fsPromises.appendFile(
      path.join(__dirname, "files", "promiseWrite.txt"),
      "\n\nnice to meet you"
    );
    await fsPromises.rename(
      path.join(__dirname, "files", "promiseWrite.txt"),
      path.join(__dirname, "files", "promiseComplete.txt")
    );
    const newData = await fsPromises.readFile(
      path.join(__dirname, "files", "promiseComplete.txt"),
      "utf8"
    );
    console.log(newData);
  } catch {
    console.error(err);
  }
};

fileOps();

```

###### DIR

```javascript
const path = require("path");
const fs = require("fs");

if (!fs.existsSync("./new")) {
  fs.mkdir("./new", (err) => {
    if (err) {
      throw err;
    }
    console.log("dir created");
  });
}

if (fs.existsSync("./new")) {
  fs.rmdir("./new", (err) => {
    if (err) {
      throw err;
    }
    console.log("dir removed");
  });
}

```

###### STREAM

```javascript
const path = require("path");
const fs = require("fs");
const rs = fs.createReadStream(path.join(__dirname, "files", "lorem.txt"), {
  encoding: "utf8",
});
const ws = fs.createWriteStream(path.join(__dirname, "files", "newLorem.txt"));

rs.on("data", (dataChunk) => {
  ws.write(dataChunk);
});

// effecient way
rs.pipe(ws);

```
```javascript
console.log("hello")
```
