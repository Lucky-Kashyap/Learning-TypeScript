# Learning TypeScript

### Install TypeScript Using Command

- Install globally in system

      npm install -g typescript

- Check version

      tsc -v

- It will tell the typescript version

- TypeScript is a strongly typed programming language that builds on JavaScript, giving you better tooling at any scale.

- TypeScript is JavaScript with syntax for types.

- Create index.ts file

        console.log('Learning TypeScript');

        let num = 10;

        console.log(num);

- For running .ts file run command

        tsc index.ts

- It will convert .ts file to .js file

- TypeScript is all about static Typing

          let num =10;

          num = 'Hello';  // It will error

          // index.ts:9:1 - error TS2322: Type 'string' is not assignable to type 'number'.

          // num = 'Hello';

- We have to define type of variables

        let firstName:string = 'Lucky';

        console.log(firstName);

- For running file, we have to first compile .ts file & run .js file via node command

      tsc index.ts

      node index.js
