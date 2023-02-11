# A Guide to npm install: Types, Meanings, and Flags

## Introduction to NPM (Node Package Manager)

### Overview

Node Package Manager (NPM) is a package manager for the JavaScript programming language and is the default manager for the Node.js runtime environment. It provides a way to manage and distribute packages and collections of code for use in Node.js projects.

NPM was created in 2010 as a way to manage the packages used in Node.js projects and has since become the largest software registry in the world, with over one million packages available to download. It has become an essential tool for developers and is used by millions of developers around the world.

NPM makes it easy to install and manage packages, allowing developers to focus on writing code rather than worrying about dependencies. NPM also provides a way to share and distribute packages, making it possible for developers to reuse and share code with others.

Importance of NPM in the Node.js ecosystem

Some of the importance of the NPM in the Node.js ecosystem include:

* **Package Management**: NPM provides a centralized repository for packages that can be managed and installed easily. This makes it easy for developers to find and use packages as well as manage dependencies.
    
* **Sharing and collaboration**: NPM makes it easy for developers to share their packages with others and collaborate on the development of packages. This has created a thriving community of developers who contribute to packages written by others.
    
* **Version Management**: NPM provides version management for packages and hence making it easy to manage different versions of a package and also ensure compatibility.
    

Other importance includes:

* **Easy to use.**
    
* **Speed and scalability.**
    

## Types of NPM install

The NPM package provides various commands for installing, updating, and managing packages. The following commands are the various types of `npm install` :

* `npm install`: This is the most common type of `npm install`. It installs the packages specified in the **dependencies** section of the project's `package.json` file. By default, it installs the latest version of each package.
    
* `npm install --save`: This command installs the specified packages and adds them to the **dependencies** section of the `package.json` file.
    
* `npm install --save-dev`: This command installs the specified packages and adds them to the **devDependencies** section of the `package.json` file. These are specifically used for development purposes and are not required for the production environment.
    
* `npm install <package-name>@<version>`: This command installs a specific version of a package. The `@` symbol is used to specify the version number.
    
* `npm install <package-name>@<latest>`: This command installs the latest version of a package.
    
* `npm install <package-name> -g`: This command installs a package globally, making it available for all projects on the same machine.
    

## Explanations of the various flags that can be used with the `npm install` flag

Some of the most commonly used flags are:

* `g` or `global`: Installs the package globally, making it available for all projects on the same machine.
    
* `-save`: Adds the package to the **dependencies** section of the `package.json` file.
    
* `-save-dev`: Adds the package to the `devDependencies` section of the `package.json` file. These packages are typically used for development purposes and are not required for the production environment.
    
* `-only=production`: Installs only packages listed in the **dependencies** section of the `package.json` file, and not those listed in **devDependencies.**
    
* `-no-save`: Prevents the package from being added to the **dependencies** or **devDependencies** sections of the `package.json` file.
    
* `E` or `-save-exact`: Installs the exact version of the package specified in the `package.json` file, rather than the latest version.
    
* `-no-optional`: Installs only the required dependencies, and not the optional ones.
    
* `S` or `-save-optional`: Installs the optional dependencies and adds them to the **optionalDependendencies** section of the `package.json` file.
    
* `f` or `force`: Forces the installation of a package, even if it would normally be skipped due to compatibility issues.
    

## Example

Let's say we want to create a project that needs the following packages:

1. ***Mocha*** - Mocha is a test runner that helps us runs our test packages
    
2. ***Chai*** - Chai is an assertion library that helps us to test our functions.
    
3. ***Express*** -Is a Node.js framework that is used to build websites easily
    

To use the following packages, we can install them in the following ways:

* **Initialize npm**: Initializing npm, will create the `package.json` file. We can initialize NPM by running the following command:
    
    ```bash
    $  npm init -y
    ```
    
    Our output would be:
    
    ```json
    {
      "name": "<name-of-project>",
      "version": "<version-of-project>",
      "description": "",
      "main": "<default-run-file>", // usually index.js
      "scripts": {
        "test": "echo \"Error: no test specified\" && exit 1"
      },
      "keywords": [],
      "author": "",
      "license": "ISC"
    }
    ```
    
    Next, we install *Mochai* globally, this is because the test is written for other packages:
    
    ```bash
    $  npm install -g mocha
    ```
    
    When we run this command, nothing is changed in our `package.json` file.
    
* Next, we install Chai:
    
    ```bash
    $  npm install --save-dev chai
    ```
    
    Immediately we run this command, the devDependencies object is added to the `package.json` file, and it looks like this now:
    
    ```json
    {
        ........
        ........,
        "devDependencies": {
        "chai": "^4.3.7"
      }
    }
    ```
    
    As we explained previously, this is going to be for development only.
    

Lastly, we install `express` using the command below:

```bash
$  npm install express
```

This will create a dependency object in the `package.json` file:

```json
{
    ......
    ......,
    "dependencies": {
    "express": "^4.18.2"
  }
}
```

## Conclusion

In conclusion, npm install is a crucial command for developers working with JavaScript and Node.js. Understanding the different types of installations (local, global, and development), their meanings, and the available flags can greatly enhance one's productivity and streamline their workflow. By following the guidelines outlined in this guide, developers can easily manage dependencies, install packages, and control the configuration of their projects.

Thank you for reading 🙏🙏.

You can follow me on the following platforms:

Twitter 🐦: @[@nwokporo_ebuka](@nwokporo_ebuka)

LinkedIn ⚡: @[@chukwuebuka_nwokporo](@chukwuebuka_nwokporo)

GitHub 🚀: @[@ebukvick](@ebukvick)

Hashnode 📗: @[Nwokporo Chukwuebuka](@codeDaddy)