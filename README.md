# Pensonal CV
Created a personal CV website based on Cyberlark David Resume Template to display all works during university study.

## How to Run Project Locally
### 1. Run the project
* Install 'node' and 'npm' and check the version
    ```shell
    node -v (Provider-version: v16.18.0; Initial-version: v20.12.0; Current-version: v16.20.2)
    ```
    And
    ```shell
    npm -v (Provider-version: 8.19.2; Initial-version: 10.5.0; Current-version: 8.19.4)
    ```

* Install all packages in the 'package.json'
    ```shell
    npm install --legacy-peer-deps
    ```
    Or
    ```shell
    npm i --save --legacy-peer-deps
    ```

* Run the service and open the webpage
    ```shell
    npm start
    ```
   
* Close the webpage
    ```shell
    ctrl + c
    ```

### 3. Build
```shell
npm run build
```

### 4. Deploy
```shell
npm run deploy
```
more see: https://javascript.plainenglish.io/deploying-any-app-to-github-pages-1e8e946bf890


## How to Deploy Pages on the Github
### 1. Install
* Install 'gh-pages' respository
    ```shell
    sudo npm install gh-pages -g
    ```
* Check 'gh-pages' version
    ```shell
    gh-pages -v (--version)
    ```

### 2. Deploy 
* Build the project
    ```shell
    npm run build
    ```

* Build 'gh-pages'
    ```shell
    gh-pages -d build
    ```
