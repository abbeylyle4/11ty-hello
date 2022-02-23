---
title: Introduction to JavaScript and Open Web Components.
description: This is a post on My Blog about JavaScript and Web Components.
date: 2022-02-23
---
# 11ty Blog Posts

## Introduction to JavaScript and Open Web Components

Maybe you're also a beginner, or have no experience with JavaScript and are looking for a place to start. Welcome! We will be going through the steps for making sure that you have all you need to begin your web dev journey. 

_These steps will be most compatible with Mac users_

### What is JavaScript?

JavaScript first appeared in 1995 as a scripting language for the World Wide Web. It operates alongside HTML and CSS to increase interactivity and functionality on web pages. Nowadays, over 97% of websites use JavaScript to increase capabilities on their client-facing interfaces.

Now that you have a brief background, let's get started with getting all the tools we need.

### VS Code
VS code is a code editing software that comes in handy when learning JavaScript. It provides support for debugging and version control. It is a great option for beginners who are getting into web dev. 

You can get VS Code [here](https://code.visualstudio.com/Download)

### NodeJS
NodeJS is an open source platform and allows you to run server-side applications on your personal machine.

When [downloading](https://nodejs.org/en/download/), make sure that you download the LTS/"recommended for most users" option for a more reliable platform.

**Tip**: to double check that NodeJS has installed successfully, you can simply type `node` in your terminal window (for macOS users, you can navigate to it by searching 'terminal' in your launchpad)
![NodeJS](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/y6jj36msd5kkylkrjghr.png)
  

### npm
Luckily for you, npm (node package manager) is installed as a _package deal_ with NodeJS. Npm is the default package manager for NodeJS and allows you to use third party code in your own. It is one of the largest software registries, giving you a plethora of tools for your own code.

Similarly to NodeJS, you can ensure you have npm by typing `npm` in your terminal window. You will see a longer message this time showing some of the capabilities you have with npm!![npm](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/6qxrp0uql2cgxmb4l261.png)

### Git

Git is a version control service used for communicating and collaborating between different programmers creating code for one project.

You can get git [here](https://git-scm.com/downloads).
After completed, type `git` in terminal to ensure correct installation.

---


### Open Web Components
Now that we have all the necessary tools to begin, let's work on creating our own web component! First, we must create a new folder in Finder to host this project. Then, return to your terminal window and navigate to that folder you just created. You can do this by typing `cd "foldername"`. 
**Tip**: Make sure you are using the whole file path, typing just the destination folder can run an error.

Once in your folder, code `npm init @open-wc` and run the command. This initializes the process for us to create our first web component!
![open wc](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/mzogl69k19q38er44yc8.png)

From here, we answer the following prompts:
1. Scaffold a new project
2. Web component
3. Press `a` to select all options, then `enter` to run
4. Deny typescript
5. Pick a name for your first project! (I picked "hello-world")
![creating wc](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/6udxmnyy3y576p9wcv1t.png)  
6. Select yes to writing file structure to disk
7. Install dependencies with npm (this may take some time)
 
After receiving the message that we are all set up, simply follow the two commands to run your web server. You should be taken to your first web component!
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/t1ou9sje23z39w49smya.png)

---

### Understanding your Web Component

Once the web component is created, it is important to understand how it even operates using the `src/HelloWorld.js` file. In src files, you are able to edit code to enhance components of the websites as I mentioned at the beginning of this post. The src file looks something along the lines of this:

![src](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/n4rbe39eixl1eq2ss9up.png)
 
You can see at the beginning of the code, LitElement is being imported. Lit supports the building of fast and lightweight web components. In order to get more familiar with Lit, I recommend following this [tutorial](https://lit.dev/tutorial/). 


## Wikipedia API Contextualized and Leveraged

First, an **application programming interface** (API) is a connection between computers or between computer programs that allow applications to talk to each other. They are very versatile and basically act like a mutual friend between both systems. 

We will be walking through how APIs are visualized, how they work, and how the JSON response is used. The example that we will be contextualizing is Wikipedia's API and how we can leverage it using the Wikipedia query tag.

## Fetch
The main goal for us here is to communicate with Wikipedia's API so that we can render their content on our own projects! We can do this by using the `fetch` tag. It is "behind the scenes" of the web component. It is what starts the process to retrieve information through APIs. In this case, the `fetch` tag is used to communicate with Wikipedia to find the respective article so that it can be rendered on the page. In the source code of the Wikipedia query, it shows the `fetch` tag requesting the address which then leads to the JSON API response.
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/cqe45udiulbvjcoui1p9.png)

## APIs Visualized
The Wikipedia query tag communicates with Wikipedia's API service by searching for a Wikipedia article with the title specified. In this image of the Wikipedia query source code, you can see that the code is grabbing the Wikipedia article based on the search that the user will input. ![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/xw22bqe39ffvkgr95q6w.png)
To include the Wikipedia query in your own projects, the following syntax can be implemented. Below, we are specifying that the Wikipedia articles should be searched by the location specified by the user![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/zyb3c4o8au7w7dwqjyku.png)
**JSON Response and Display**
The JSON response is the default result of the fetch request because it is easily readable and easy to translate. When the JSON response is received, the web components are displayed on your own projects!

You can find more information about APIs [here](https://www.redhat.com/en/topics/api/what-are-application-programming-interfaces). For more information about the Wiki API, you can find its documentation [here](https://en.wikipedia.org/w/api.php)! For reference I have attached my own GitHub [repository](https://github.com/abbeylyle4/ip-project/blob/master/src/LocationFromIP.js).





