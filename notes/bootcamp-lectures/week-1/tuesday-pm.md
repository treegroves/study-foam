## Dependencies (libraries/packages) 
- code that your code needs to work
- Code is built on top of multiple dependencies
- `npm install <library>` to copy dependencies and put them into your projects
  - dependencies have their own dependencies 
  - 
### how to check a dependencies reliability
- look at `package.json` to view dependencies 
- look up dependences search npn 
- Check to see how popular the library is
  
### versions

    "Given a version number MAJOR.MINOR.PATCH, increment the:

        MAJOR version when you make incompatible API changes,
        MINOR version when you add functionality in a backwards compatible manner, and
        PATCH version when you make backwards compatible bug fixes.

    Additional labels for pre-release and build metadata are available as extensions to the MAJOR.MINOR.PATCH format."


### package lock
copy of .json make sure it's on github

### ways to install
`npm install 


### What not to commit
- don't commit node_modules 
- `.gitignore` file 
  - can use wildcards `node*`

### commands
`npm init -y` -npm initialise all
`npm install cowsay` install library
`npm install -D jest`

`npm test`