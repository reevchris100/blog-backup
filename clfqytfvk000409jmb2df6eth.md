---
title: "How to Build and Deploy React App to GitHub Pages"
seoTitle: "How to build and deploy React App to GitHub Pages"
seoDescription: "How to build and deploy React App to GitHub Pages in simple steps."
datePublished: Mon Mar 27 2023 15:09:42 GMT+0000 (Coordinated Universal Time)
cuid: clfqytfvk000409jmb2df6eth
slug: how-to-build-and-deploy-react-app-to-github-pages
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1679928368241/f8c95570-08ad-45de-8a23-0c8e56da758a.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1679929705728/8f809569-9313-4381-ab80-47a9e9ffc2e9.jpeg
tags: repository, github, reactjs, githubpages, pages

---

### Prerequisites

* [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) installed.
    
* [GitHub Account](https://github.com/) created.
    
* [Node and npm](https://nodejs.org/en/download) installed.
    

### Steps

1. Create an empty GitHub repository.
    
2. Create a simple React app
    
    ```javascript
    npx create-react-app simple-react-app
    cd simple-react-app
    ```
    
3. Install GitHub pages
    
    ```javascript
    npm install gh-pages --save-dev
    ```
    
4. Edit Package.json and add the homepage URL.
    
    ```json
    {
      "name": "my-app",
      "version": "0.1.0",
    +  "homepage": "https://gitname.github.io/simple-react-app",
      "private": true,	
    ```
    
5. Add deployment scripts as well to package.json.
    
    ```json
    "scripts": {
    +   "predeploy": "npm run build",
    +   "deploy": "gh-pages -d build",
        "start": "react-scripts start",
        "build": "react-scripts build",
    ```
    
6. Set Github remote origin URL.
    
    ```bash
    git remote add origin https://github.com/gitname/simple-react-app.git
    ```
    
7. Deploy or push the react app to GitHub Pages.
    
    ```javascript
    npm run deploy -- -m "Deploy the React app to GitHub Pages"
    ```
    
8. Save the source code of the react app in `master` branch and the react app code in `gh-pages` .
    

```bash
git add .
git commit -m "Configure React app for deployment to GitHub Pages"
git push origin master
```

1. Now you can test the app deployed by hitting the below URL.
    
    Page - [https://reevchris100.github.io/simple-react-app/](https://reevchris100.github.io/simple-react-app/)
    
    Repository - [https://github.com/reevchris100/simple-react-app/tree/master](https://github.com/reevchris100/simple-react-app/tree/master)