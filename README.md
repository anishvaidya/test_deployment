# This is a simple tutorial to guide hosting of a react app on GitHub pages.

## To run the app locally: **npm run**
## To deploy the app: **npm run deploy**

## Steps:

- Create an empty repository on GitHub, with the name of your app ({app_name})
- Create a broiler plate for react app using: npm init react-app {app_name}
- Navigate to your app and install GH pages: npm install gh-pages --save-dev
- Set-up GH pages:
    - Add the following lines in your package.json file:
        ```
        "homepage": "http://{username}.github.io/{repo-name}"  
        "scripts": {
        //...
        "predeploy": "npm run build",
        "deploy": "gh-pages -d build"
        }
        ```
- Setup Git repo locally using the following steps: (use terminal or git bash, other terminals tested - VSCode terminal - did not work every time)
    ```
    git init
    git remote add origin git@github.com:{username}/{app_name}.git
    git add .
    git commit -m "Just checking my deployment"
    git push origin master
    ```
- Publish the app using: **npm run deploy**. You can see a new branch named gh-pages has been automatically created. It might take a few minutes for the latest version of the app to be deployed on the server.

### I hope this guide helps you in deploying your React apps on GitHub. Please feel free to fork this repo and add possible hosting solutions for apps using other frameworks like Angular.


