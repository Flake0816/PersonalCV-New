# Pensonal CV
Created a personal CV website based on Cyberlark David Resume Template to display all works during university study.

## How to Run
1. Install 'node' and 'npm' and check the version
    ```shell
    node -v (Provider-version: v16.18.0; Initial-version: v20.12.0; Current-version: v16.20.2)
    ```
    And
    ```shell
    npm -v (Provider-version: 8.19.2; Initial-version: 10.5.0; Current-version: 8.19.4)
    ```

2. Install all packages in the 'package.json'
    ```shell
    npm install --legacy-peer-deps
    ```
    Or
    ```shell
    npm i --save --legacy-peer-deps
    ```

3. Run the service and open the webpage
    ```shell
    npm start
    ```
   
4. Close the webpage
    ```shell
    ctrl + c
    ```


## How to Build
```shell
npm run build
```


## How to Deploy Git Pages
more see: <br>
https://javascript.plainenglish.io/deploying-any-app-to-github-pages-1e8e946bf890<br>
https://medium.com/@ninadkarlekar/deploying-your-react-project-on-github-pages-a-step-by-step-guide-f8b364fa75fa<br>
### Install
1. Install 'gh-pages' respository
    ```shell
    sudo npm install gh-pages -g
    ```
    Or
    ```shell
    npm install gh-pages --save-dev --legacy-peer-deps
    ```

    **Problem:**<br>
    ```shell
    Conflicting peer dependency: react@16.14.0
    npm ERR! node_modules/react
    npm ERR!   peer react@"^15.3.0 || ^16.0.0" from react-reveal@1.2.2
    npm ERR!   node_modules/react-reveal
    npm ERR!     react-reveal@"^1.2.2" from the root project
    ```
    **Solution:**<br>
    * Modified package.json: Set react and React-DOM to 16.14.0.
        ```shell
        {
            "dependencies": {
            "react": "16.14.0",
            "react-dom": "16.14.0",
            "react-reveal": "^1.2.2",
            // 其他依赖项
            }
        }
        ```
    * Remove node_modules and package-lock.json: make sure there are no version conflicts.
        ```shell
        rm -rf node_modules
        rm -rf package-lock.json
        ```
    * Reinstall dependencies: Make sure all packages use the correct version of React.
        ```shell
        npm install
        ```
    * Version verification: Check the correct version using the npm list.
        ```shell
        npm list react react-dom react-reveal
        ```
    **Result:**<br>
    Current versions of 'react' 'react-dom' 'react-reveal' : 
    ```shell
    cyberlark@0.1.0 C:\Z\GitHub\PersonalCV-New
    ├─┬ @testing-library/react@11.2.7
    │ ├── react-dom@16.14.0 deduped
    │ └── react@16.14.0 deduped
    ├─┬ cyberlark@0.1.0 -> .\
    │ ├── react-dom@16.14.0 deduped
    │ ├── react-reveal@1.2.2 deduped
    │ └── react@16.14.0 deduped
    ├─┬ react-dom@16.14.0
    │ └── react@16.14.0 deduped
    ├─┬ react-ga@3.3.1
    │ └── react@16.14.0 deduped
    ├─┬ react-reveal@1.2.2
    │ └── react@16.14.0 deduped
    ├─┬ react-zmage@0.8.5-beta.37
    │ ├── react-dom@16.14.0 deduped
    │ └── react@16.14.0 deduped
    └── react@16.14.0
    ```

2. Check 'gh-pages' version
    ```shell
    gh-pages -v
    gh-pages --version
    ```
    Or
    ```shell
    npm list gh-pages
    ```
    Current version: 
    ```shell
    cyberlark@0.1.0 C:\Z\GitHub\PersonalCV-New
    ├─┬ cyberlark@0.1.0 -> .\
    │ └── gh-pages@6.1.1 deduped
    └── gh-pages@6.1.1
    ```

### Configure
In the package.json file: 
   1. homepage: This is your GitHub Pages address, replaced with your own GitHub username and repository name, for example https://your-username.github.io/your-repo-name.
   2. predeploy: Run the build command to build your project and generate static files.
   3. deploy: Deploys the contents of the build folder to GitHub Pages using gh-pages.
```shell
{
    "name": "your-project-name",
    version: 1.0.0,
    "homepage": "https://Flake0816.github.io/PersonalCV-New", 
    // Replace with your GitHub username and repository name
    "scripts": {
        "start": "react-scripts start",
        "build": "react-scripts build",
        "predeploy": "npm run build", // Automatically runs build before deployment
        "deploy": "gh-pages -d build" // Deploy the build folder to GitHub Pages
    },
    "devDependencies": {
        "gh-pages": "^4.0.0"
    }
}
```


### Deploy
This command first runs npm run build to build the project, and then publishes the resulting build file to the gh-pages branch of GitHub Pages.
```shell
npm run deploy
```

### Access
The deployed git pages: https://flake0816.github.io/PersonalCV-New/