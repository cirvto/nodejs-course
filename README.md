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

