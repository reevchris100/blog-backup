---
title: "How to Build and Deploy React App on Vercel"
seoTitle: "How to Build and Deploy React App on Vercel"
seoDescription: "How to build and deploy simple react app on Vercel using React and GitHub"
datePublished: Tue Mar 28 2023 12:59:53 GMT+0000 (Coordinated Universal Time)
cuid: clfs9mcrp000709kx997i2elz
slug: how-to-build-and-deploy-react-app-on-vercel
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1680007664313/1f46edbc-3bc6-4069-b9f1-f3647e7a7e5f.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1680008319749/767d0a1d-7b42-4c29-9dea-2734f929381d.png
tags: github, reactjs, application, deploy, vercel

---

### Prerequisites

* [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) installed.
    
* [GitHub Account](https://github.com/) created.
    
* [Vercel Account](https://vercel.com/docs/concepts/get-started) created.
    
* [Node and npm](https://nodejs.org/en/download) installed.
    

### Steps

1. Create an empty GitHub repository which can be public or private.
    
2. Create a simple React app
    
    ```javascript
    npx create-react-app vercel-react-app
    cd vercel-react-app
    ```
    
3. Set Github remote origin URL.
    
    ```bash
    git remote add origin https://github.com/gitname/vercel-react-app.git
    ```
    
4. Push the code changes to `master` branch.
    

```bash
git add .
git commit -m "Configure React app for deployment to Vercel"
git push origin master
```

1. Go to [Vercel](https://vercel.com/new) and import the project which is the above GitHub repository.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680008236753/f46a82f4-dfd7-43d4-bbac-70cd5797bc74.png align="center")

1. Click on deploy and wait for a few seconds for the deployment to be completed.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680008236753/f46a82f4-dfd7-43d4-bbac-70cd5797bc74.png align="center")
    
2. Now you can test the app deployed by hitting the below URL.
    
    [https://vercel-react-app-eight-ebon.vercel.app/](http://vercel-react-app-eight-ebon.vercel.app)