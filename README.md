# The Complete Node.js Developer Course
## About
I'm learning NodeJS with "The Complete Node.js Developer Course", taught by Andrew Mead on Udemy.
### What is and Why should I use Node.js?
Following the definition of Wikipedia:
> Node.js is a packaged compilation of Google's V8 Javascript engine, the libuv platform abstraction layer, and a core library, which is itself primarily written in Javascript.
During the lesson, Andrew talked about that NodeJS isn't a Javascript Framework but instead a Runtime Environment based on Chrome's V8 Javascript Engine. The differences between blocking and non-blocking assignments is also clarified, let me give a brief resume about it.
#### Blocking
A Blocking operation is where further execution is impeded to be finished until the operation that came before be finished. 
#### Non-Blocking
Non-Blocking operation it's the opposite. While blocking prevents the operation, the non-blocking let all the operation pass and use them according the demand.
#### First Node.js script
A basic script to console 'Hello Node.js' in terminal.

```console.log('Hello Node.js');```

It's interesting how it's similar to Javascript code, it's because it is a command created to guide the engine to compile a console as result of something. Node.js, as Javascript, uses the same code because both use the same engine.
### Node.js Module System
Now we will start the Notes App, the first software developed during the course. It's a basic application, to be honest it's almost a CRUD. We will study it through three modules:
1. Node.js Module System
2. File System and Command Line Args
3. Debugging Node.js
Let's start the first one right now!
## Lesson 1 - Importing Nodejs Core Modules
In this section we'll work with the Module System or Core Modules of Nodejs. First lesson we learn about File System, the 'fs' command of Nodejs. We learned about the Require system and how to require a document or something that you need in the code.

### Codes with Module System
As a basic lesson, we didn't delve into the Module System. Just worked with File System and two variables from this command. We started with fs.writeFileAsync:
```
fs.writeFileAsync('fileName', 'dataYouWantToWrite');
```
It's a pretty basic code, but we could have an introduction of what is comming.
Then, with the file created and writted, the teacher give us a challenge: to write a new phrase without deleting or changing the last phrase added. The command is fs.appendFileSync:
```
fs.appendFileSync('fileName', 'dataYouWantToWrite);
```
Here was a little tricky, because I was trying to find some way to write a new line. I started to search about "append text in a new line node.js", and guess what? We do it in the same way as the lessons of PHP in faculty: using '\n' to jump to the next line. So it was easy, because I already knew about how to use special characters in your code.

## Lesson 2 - Importing Your Own Files
In this lesson we diver better in the Require system. More examples of what happen in the code when you use this to require another code or file from your folder. To exemplify we created two files: app.js and utils.js, app.js should use commands and code from utils.js. It was easy to handle, because the code is the same as the last lesson:

File: app.js:
```
require('./utils);
console.log(name);
```

File: utils.js:
```
const name = 'Victor';

module.exports = name
```

After this code, we can access the constant name from file utils.js to app.js. I have to be on alert with the spelling code, a simple misspelling can result in a huge problem. In the challenge I forgot to spell the 's' in the end of 'modules' and i spent a lot of time searching the error.

## Lesson 3 - Importing NPM Modules
Until now, we just make simple things with our own files that we created. But what if we could use a module that already exists? NPM Modules has a huge library of things to use that is much more easy than create your own things. I'm not saying that you will just use commands that other person made, you still doing your job. What I mean is: you can make your job easier by just focusing in things that correspond specifically to the project that you're working on.

### Installing NPM
First of all we have to install NPM, to do it you have to run a simple command line:
```
npm init
```
after this command line, a couple of files will be generated and you'll be able to apply packages on them.

### Applying Dependencies
To apply package you should run a command:
```
npm install >>package name<<
or
npm i >>package name<<
```
In the lesson we used the package 'validator' which validate a lot of informations from your code.

### Validating Email
Example of how to use the validator package just by using him to validate a string:
```
console.log(validator.isEmail('someone@example.com'))
```
the result should be 'true' as the passed string is a valid email shape.
Remember, you should use require to add the validator package in your code.

## Lesson 4 - Global NPM Modules and Nodemon
### What is Nodemon?
Following the definition of nodemon's page in npmjs.com:
> Nodemon is a tool that helps develop node.js based applications by automatically restarting the node application when file changes in the directory are detected.

Here we have a difference between nodemon and the others packages we just learned to use in this course: nodemon don't use Require to run in a code. If you watch, nodemon dependecie even exists in the package.json file. 

### How to use Nodemon?
After the installation using:
```
npm i nodemon -g
```

you can use the nodemon in the whole directory, that`s because you used the -g flag to inform that line is a Global command. After this you can use the following code to run a code with nodemon:
```
nodemon fileName.js
```

and that's it, your file will be runned with nodemon and every change in the file will reflect in the result instantly.