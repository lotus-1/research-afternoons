# Deploying and NPM  
## Cloud platforms:
(1) The hardware and operating environment of a server in an Internet-based datacenter. The system software components are called the "cloud stack".  

(2) The software infrastructure for a cloud computing service, which includes applications that let users create and manage their own accounts.

###  🔴 What is PasS ❓
(Platform As A Service) A cloud computing service that provides a comprehensive computing environment. PaaS includes the hardware, operating system, database and other necessary software for the execution of applications. It may include a complete development environment as well. PaaS is a step up from "infrastructure as a service" (IaaS), which provides only the servers and operating systems.  

PaaS is a fairly new technology stack that runs on top of IaaS and was created with the developer in mind. With the PaaS platform, everything is provided except the application code, users, and data. Typically, when using a PaaS, the vendor maintains the application server, databases, and all of the necessary operating system components, giving you time to focus on the application code. Since the vendor manages that platform for you, it is often hard to open up ports that are not specifically called for the application server, runtime, or database in use. PaaS also provides features that are specifically meant for applications, including the ability to scale the application tier up based upon the user demand of the application. In most platforms, this happens with little-to-no interaction from the developer.

Pro: PaaS provides a complete environment that is actively managed, letting you focus on your application code.

Con: Developers are often restricted to certain major/minor versions of packages available on the system so that the vendor can manage the platform effectively.


###  🔴 Why is it useful to be able to deploy your code to a cloud platform, rather than running it locally ❓
As developers, we often code applications on our local system and then, when we reach a work milestone, we move our code to the team’s development environment. Most developers wish they could develop on a daily basis with an infrastructure that resembles production as closely as possible. That goal can often be challenging due to the system administration overhead incurred to provide each developer with a cluster of machines.


###  🔴 What services are there that can provide you with a platform for your code ❓
![](https://upload.wikimedia.org/wikipedia/en/thumb/c/c7/Logo_Alpha7.jpg/220px-Logo_Alpha7.jpg)    


![](https://upload.wikimedia.org/wikipedia/commons/thumb/5/57/Box%2C_Inc._logo.svg/150px-Box%2C_Inc._logo.svg.png)

![](https://upload.wikimedia.org/wikipedia/en/a/a9/Heroku_logo.png)

![](https://upload.wikimedia.org/wikipedia/en/thumb/3/3e/CloudBolt_logo.png/150px-CloudBolt_logo.png)  

## Environment variables:

An environment variable is a dynamic value that the operating system and other software can use to determine information specific to your computer.

In other words, an environment variable is something that represents something else, like a location on your computer, a version number, a list of objects, etc.

Environment variables are surrounded by the percent sign (%), as in %temp%, to distinguish them from regular text.

**Two types of environment variables exist:**  
(1) User Environment Variables
User environment variables, as the name suggests, are environment variables that are specific to each user account.
This means that the value of an environment variable when logged in as one user can be different than the value of the same environment variable when logged in as a different user on the same computer.

(2)  System environment variables extend beyond just one user, applying to any user that might exist, or is created in the future. Most system environment variables point to important locations like the Windows folder.


![img](https://cdn-images-1.medium.com/max/1600/1*BIgXzxgolWVDBNq5F_eZpg.png)

###  🔴 What modules might you use to help manage environment variables ❓


Here are some examples of the module commands and a description of the resulting action:

module command    Description  
module help    displays the usage format of the module command  
module list    lists currently loaded modulefiles
module avail    lists available modules in the system
module switch  <old-module> <new-module>    first unloads module <old-module> then loads module <new-module>  
module display  <module-name>    lists the environment variables set up by the module <module-name>  
module load  <module-to-load>    loads module <module-to-load> (if there are no conflicts)    
module unload  <module-to-unload>    unloads module <module-to-unload>  


env2 :
allows you to store your environment variables in an env.json or a .env file which gets loaded when your app starts.

All the entries in the env file are exported as environment variables available as keys in the process.env object.

The format of a .env file is:

export DB_HOST=127.0.0.1
export DB_PORT=9200
export DB_USER=anon
export DB_PASS=password

## NPM:
NPM is the tool used by over 11,000,000 JavaScript developers around the world.

###  🔴 What are some common scripts to have in your package.json ❓

The package.json file is a key element in lots of app codebases based on the Node.js ecosystem.  
**Scripts**  
Defines a set of node scripts you can run

Example:
```
"scripts": {
  "dev": "webpack-dev-server --inline --progress --config build/webpack.dev.conf.js",  
  "start": "npm run dev",  
  "unit": "jest --config test/unit/jest.conf.js --coverage",  
  "test": "npm run unit",  
  "lint": "eslint --ext .js,.vue src test/unit",  
  "build": "node build/build.js"
}```  
These scripts are command line applications. You can run them by calling npm run XXXX or yarn XXXX, where XXXX is the command name. Example: npm run dev.

You can use any name you want for a command, and scripts can do literally anything you want.

###  🔴 What is the difference between package.json and package-lock.json ❓

package-lock.json: records the exact version of each installed package which allows you to re-install them. Future installs will be able to build an identical dependency tree.

package.json: records the minimum version you app needs. If you update the versions of a particular package, the change is not going to be reflected here.

### 🔴 What npm scripts do cloud platforms like heroku use ❓
** Terminal **  
$: npm run install    
** package.json **  
"install": "bash ./scripts/install.bash"  
** install.bash**  
** Install Dependencies **  
npm install  
...
