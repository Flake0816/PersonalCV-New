# Pensonal CV
Created a personal CV website based on Cyberlark David Resume Template to display all works during university study.

## How to Run the Project
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


## How to Deploy Pages
more see: https://javascript.plainenglish.io/deploying-any-app-to-github-pages-1e8e946bf890
### Install
1. Install 'gh-pages' respository
    ```shell
    sudo npm install gh-pages -g
    ```
2. Check 'gh-pages' version
    ```shell
    gh-pages -v (--version)
    ```

### Deploy 
1. Build the project
    ```shell
    npm run build
    ```

2. Build 'gh-pages'
    ```shell
    gh-pages -d build
    ```
