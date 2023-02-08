# React Simple Project using mkcert to create a self signed certificate

This project is just a React simple project using mkcert to create a self signed certificate.

The final result will make possible to access a web site in your own PC so that you get the lock icon in your project:

![Before log in](/screenshots/screenshot-7.png)

## Getting Started

Read the links in the acknowlegements section bellow to get an idea about mkcert.

You can get an idea of how https certificates work with this tutorial:
[Secure Web Site using certificates](/docs/DPL-2012-2013-doc10-UT-2-https.pdf)

## Prerequisites

You need a working environment with:
* [Git](https://git-scm.com) - You can install it from https://git-scm.com/downloads.
* [Node.js](https://nodejs.org) - Install node.js from https://nodejs.org/es/download/. It's advisable to install the LTS version.
* [ReactJS](https://es.reactjs.org/) - A JavaScript Library to create User Interfaces.

## General Installation instructions

Clone this project in your PC:

```
git clone https://github.com/tcrurav/using-mkcert.git
```

You need a node.js working environment. The LTS is recommended: https://nodejs.org/es/

Once you have cloned the project customize your environment files.

```
cd bicycles-cert
copy .env.example .env
```

Now install all dependencies.

```
cd bicycles-cert
npm install
```

Install chocolatey using the instructions in the following page: https://chocolatey.org/install

Now open Visual Studio Code with administrative rights and create the Certificate Authority (CA):

![Creating CA](/screenshots/screenshot-2.png)

In your certificate manager you can see your created CA:

![checking CA](/screenshots/screenshot-4.png)

Now create a new certificate signed with your CA valid for the domain "localhost".

![Creating Site Certificate](/screenshots/screenshot-3.png)

Move the 2 files created to server/.cert:

![Creating Site Certificate](/screenshots/screenshot-8.png)

In this last screenshot above you can see where the created cert files are used in `server/server.js`.

Now it's time to Build the project.

```
cd bicycles-cert
npm run build
```

Now you can see a new folder called `build`.

Run your project:

```
cd bicycles-cert
node server/server.js
```

Now you will see the final output so that you get the lock icon in your project:

![Before log in](/screenshots/screenshot-7.png)

Enjoy!!!

## Built With

* [Visual Studio Code](https://code.visualstudio.com/) - The Editor used in this project
* [Node.js](https://nodejs.org/) - Node.js® is a JavaScript runtime built on Chrome's V8 JavaScript engine.
* [ReactJS](https://es.reactjs.org/) - A JavaScript Library to create User Interfaces.
* [mkcert](https://github.com/FiloSottile/mkcert) - mkcert is a simple tool for making locally-trusted development certificates. It requires no configuration.

## Acknowledgments

* Thank you to my student <strong>Kevin</strong> (https://github.com/KRodVal) who has told me about mkcert and given the first instructions to start with it.
* https://github.com/FiloSottile/mkcert. mkcert is a simple tool for making locally-trusted development certificates. It requires no configuration.
* https://gist.github.com/PurpleBooth/109311bb0361f32d87a2. A very complete template for README.md files.
