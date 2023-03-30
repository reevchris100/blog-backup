---
title: "How to Build and Deploy React App on Netlify"
seoTitle: "How to build and deploy react app to Netlify using GitHub"
seoDescription: "How to build and deploy react app to Netlify using GitHub in simple steps"
datePublished: Thu Mar 30 2023 07:21:54 GMT+0000 (Coordinated Universal Time)
cuid: clfusfec3000d09mma89ub51l
slug: how-to-build-and-deploy-react-app-on-netlify
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1680160997336/23d7cbfa-c6d5-4916-8ab5-079f0a91d386.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1680161019121/36905656-c008-4d5f-b0ef-05e7acb3da3d.jpeg
tags: github, reactjs, deploy, netlify, create-react-app

---

### Prerequisites

* [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) installed.
    
* [GitHub Account](https://github.com/) created.
    
* [Netlify Account](https://docs.netlify.com/get-started/) created.
    
* [Node and npm](https://nodejs.org/en/download) installed.
    

### Steps

1. Create an empty GitHub repository which can be public or private.
    
2. Create a simple React app
    
    ```javascript
    npx create-react-app netlify-react-app
    cd netlify-react-app
    ```
    
3. Set Github remote origin URL.
    
    ```bash
    git remote add origin https://github.com/gitname/netlify-react-app.git
    ```
    
4. Push the code changes to `master` branch.
    
    ```bash
    git add .
    git commit -m "Configure React app for deployment to Netlify"
    git push origin master
    ```
    
5. Go to [Netlify](https://www.netlify.com/) and import the project which is the above GitHub repository.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680160684962/3e6088aa-6e58-493e-8c56-2c0bed38d275.png align="center")
    
6. Click on deploy site and wait for a few seconds for the deployment to be completed.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680160711461/f6e5aea3-7f13-4aa3-b954-49f60253914f.png align="center")
    
7. Now you can test the app deployed by hitting the below URL.
    
    Netlify App - [https://master--spectacular-crumble-5461b7.netlify.app/](https://master--spectacular-crumble-5461b7.netlify.app/)  
    Repository - [https://github.com/reevchris100/netlify-react-app/tree/master](https://github.com/reevchris100/simple-react-app/tree/master)