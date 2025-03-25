<h5 align="center">Template Repository</h5>
<h1 align="center">A Portable Node.js workspace</h1>

## Introduction

This repository serves as a template for quickly setting up a portable Node.js development environment. Whether you're starting a new project or need a clean, consistent development environment across multiple machines, this template will help you get up and running in no time.

### Features

- Pre-configured Node.js environment
- Portable setup for use on **windows** machines
- Easy-to-follow setup instructions
- Other workspace settings:
  - PHP server
  - PHP
  - prettier
  - cSpell checker
  - liveserver
  - live sass compiler

[![Version](https://img.shields.io/badge/NODE%20Version-20.6.1-blue.svg)](https://your-project-url)
[![Version](https://img.shields.io/badge/npm%20Version-10.2.0-blue.svg)](https://your-project-url)

**ON** _[15/10/2023](https://github.com/siMobin/Portable-NodeJS-Workspace)_...

## Getting Started

Follow these steps to set up your portable Node.js development environment using this template repository:
# Portable Node.js Project Template (Windows)

This is a fully self-contained, portable Node.js project setup for Windows. It does **not require global Node.js or npm**—everything is embedded in the project directory.

## 🚀 How to Use

### 1. Clone This Template for a New Project
Use PowerShell:

```powershell
& "D:\tools\git\bin\git.exe" clone https://github.com/c-wegner/Portable-NodeJS-Workspace.git D:\_projects\YourNewProject
cd D:\_projects\YourNewProject
2. Initialize Your Project
powershell
Copy
Edit
.\scripts\npm.cmd init -y
This creates a local package.json inside your project folder.

3. Install Dependencies
To install packages locally into the project (not globally):

powershell
Copy
Edit
.\scripts\npm.cmd install <package-name>
Example:

powershell
Copy
Edit
.\scripts\npm.cmd install express
4. Add Your Application Code
Create your main script file if not present:

powershell
Copy
Edit
New-Item -Path .\src\index.js -ItemType File
Then edit it, for example:

js
Copy
Edit
console.log("Hello from portable Node!");
5. Run Your Code Using Local Node
powershell
Copy
Edit
.\scripts\node.cmd src\index.js
📁 Folder Structure
pgsql
Copy
Edit
/YourProject
├── /node               ← Embedded Node.js binary
├── /node_modules       ← Local packages
├── /scripts            ← Local launch scripts (npm.cmd, node.cmd)
├── /src                ← Your app code
├── package.json
├── package-lock.json
└── README.md
♻️ Reusing This Template
Copy this folder to start a new project:

powershell
Copy
Edit
Copy-Item -Recurse -Path D:\_projects\portableNodeTemplate -Destination D:\_projects\YourNewProject
Inside the new project folder, run:

powershell
Copy
Edit
.\scripts\npm.cmd init -y
Start coding.

✅ Notes
Works entirely without touching system Node.js or npm.

Ideal for portable drives, isolated dev environments, and clean project setups.

You can embed a different Node.js version by replacing the node folder.
### Prerequisites

- **Git:** Install `Git` on your system if it's not already installed. You can download Git from _[git-scm.com](https://git-scm.com/)_.

- **Visual Studio Code:** Install `Visual Studio Code` on your system if it's not already installed. You can download it from _[code.visualstudio.com](https://code.visualstudio.com/download)_.

> [!IMPORTANT]  
> This portable workspace works on **vs code** only.

### Cloning the Repository

Clone this repository to your local machine:

```shell
git clone git@github.com:siMobin/Portable-NodeJS-Workspace.git
```

> [!WARNING]
> You may need a `ssh` key for that. You can try `HTTPS` then.

> [!IMPORTANT]  
> Delete `.git` folder before create a new repository using ***[this](https://github.com/siMobin/Portable-NodeJS-Workspace)*** template.

<h1 align="center">OR</h1>

<h4>Use <img src="https://img.shields.io/badge/Use this template-2ea043?logo=drop-down&logoColor=white&style=for-the-badge" height="25"/> to create an instant repository.</h4>

##

##

##

### Setting Up Your Project

check portable environment variable for **Node js** in `.vscode\settings.json`

```json
  "terminal.integrated.env.windows": {
    "PATH": "${env:PATH};${workspaceFolder}\\node"
  },
```

1. Change the working directory to your project folder:

2. Install project dependencies:

```shell
npm init
npm install `xxx` -save-dev
```

<!--
### Usage

Now you're all set to start your Node.js project within this portable environment. Use the following npm scripts to get started:

- **Start the development server:**

```shell
npm start
```

- **Multi-Dev:**

```shell
npm install npm-run-all
```

_settings:_

```json
{
  "dependencies": {
    "npm-run-all": "^4.1.5"
  },
  "name": "name",
  "version": "0.0.1-beta",
  "description": "",
  "main": "index.php",
  "scripts": {
    "start-admin": "php -S localhost:8000 -t x/",
    "start-user": "php -S localhost:8001 -t y/",
    "start-driver": "php -S localhost:8002 -t z/",
    "start": "npm-run-all --parallel start-x start-y start-z"
  },
  "author": "",
  "license": ""
}
``` -->

> [!IMPORTANT]  
> Before start your project check/setup `.gitignore` file.

##

### **Extra**

**update node**

```shell
nvm install x.x.x
```

**update npm**

```shell
npm update -g
```

_OR_

```shell
npm install npm@latest -g
```

**Clear npm cache**

```shell
npm cache clean --force
```
