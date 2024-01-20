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

#### write a program to add two numbers?

- Using normal variables

      let num1 = 10;
      let num2 = 20;

      console.log(num1 + num2);

- Using function

      function sum(a,b){
        return a+b;
      }

      console.log(sum(12,15));

- If we run this code it works correct

      node index.ts

      // It shows 27

- If we pass

      sum(10,'Hello');

      // then it returns 10Hello

      // this is not correct

- So we need to define its type

      function sum(a:number,b:number):number{
        return a+b;
      }

      sum(10,20);
      sum(10,'Hi');  // It shows error

      // Argument of type 'string' is not assignable to parameter of type 'number'.

#### How to catch Errors & solve it?

- Duplicate function sum

      //@ts-ignore
      function sum(a:number,b:number):number{
        return a+b;
      }

      console.log(sum(12,19));

      console.log(sum(12,17));

#### TS Configuration File

- When there is error in ts file then not generate .js file

- for generating config file

      tsc --init

- Disable emitting files if any type checking errors are reported

      "noEmitOnError":true

- This command not generate .js file if erorr occur in ts file

      tsc --noEmitOnError index.ts

- convert function into fat Arrow Function

      const sum=(a:number,b:number):number=>{
        return a+b;
      }
