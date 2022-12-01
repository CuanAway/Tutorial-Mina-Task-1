# Tutorial Mina Task 1

<p align="center">
  <img height="auto" width="auto" src="https://user-images.githubusercontent.com/38981255/203963845-a591e37b-5c2d-4c20-8f32-94db19c36a05.jpg">
</p>

Dokumen Official :

> [Task 1](https://docs.minaprotocol.com/zkapps/tutorials/hello-world)

> [Task 2](https://docs.minaprotocol.com/zkapps/tutorials/private-inputs-hash-functions)

> [Task 3](https://docs.minaprotocol.com/zkapps/tutorials/deploying-to-a-network)

> [Task 4](https://docs.minaprotocol.com/zkapps/tutorials/zkapp-ui-with-react)

> [Task 5](https://docs.minaprotocol.com/zkapps/tutorials/common-types-and-functions)

> [Task 6](https://docs.minaprotocol.com/zkapps/tutorials/offchain-storage)

> [Task 7](https://docs.minaprotocol.com/zkapps/tutorials/oracle)

> [Task 8](https://docs.minaprotocol.com/zkapps/tutorials/custom-tokens)

#Setup

First, install the [Mina zkApp CLI](https://github.com/o1-labs/zkapp-cli "Mina zkApp CLI"), if you haven’t already.

##Dependencies

You'll need the following installed to use the zkApp CLI:

 - NodeJS 16+ (or 14 using --experimental-wasm-threads)
 - NPM 6+
 - Git 2+
 
##Installation

```
npm install -g zkapp-cli

```
To confirm it is installed, run:

```
zk --version
```

#Create New Project
Now that you have the tooling installed, we can start building our application.

First, create a new project using:

```
zk project 01-hello-world
```

Let's change into this directory and list the contents to see what it created:

```
$ cd 01-hello-world
$ ls
LICENSE           build             jest.config.js    package-lock.json tsconfig.json
README.md         config.json       keys              package.json
babel.config.cjs  jest-resolver.cjs node_modules      src
```

#Preparing the project

First, delete the old files. Run:

```
rm src/Add.ts
rm src/Add.test.ts
rm src/interact.ts
```

And generate the new files for our project. Enter:

```
zk file src/Square
touch src/main.ts
```

```
cd
cd /01-hello-world/src/
nano index.ts
```

Paste this script :

```
import { Square } from './Square.js';
export { Square };
```
to save it push 'ctrl' 'x' 'y' and 'enter'
and then paste this code :

```
cd ..
```

To compile the TypeScript code into JavaScript, and run the JavaScript code, you'll type:

```
npm run build
node build/src/main.js
```

You can also combine these together into one line, such as:

```
npm run build && node build/src/main.js
```

This will run main if the build is successful.

#Write the zkApp Smart Contract

##Import

First, open src/Square.ts in your editor, then add the following at the top of the file:

```
cd src
nano Square.ts
```

and then paste this scripts :

```
import {
  Field,
  SmartContract,
  state,
  State,
  method,
  DeployArgs,
  Permissions,
} from 'snarkyjs';
```

push button 'ctrl' 'x' 'y' and 'enter' to save it.



