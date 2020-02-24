---
title: Organize Your Life With 10 Simple rule
date: 2019-05-14T08:46:10.000+00:00
description: This is meta description
type: featured
image: images/featured-post/post-5.jpg
categories:
- Nature
tags:
- Fashion
- Nature

---
### Deployment of Project Pages From Your `gh-pages` branch

You can also tell GitHub pages to treat your `master` branch as the published site or point to a separate `gh-pages` branch. The latter approach is a bit more complex but has some advantages:

* It keeps your source and generated website in different branches and therefore maintains version control history for both.
* Unlike the preceding `docs/` option, it uses the default `public` folder.

#### Preparations for `gh-pages` Branch

These steps only need to be done once. Replace `upstream` with the name of your remote; e.g., `origin`:

##### Add the `public` Folder

First, add the `public` folder to your `.gitignore` file at the project root so that the directory is ignored on the master branch:

    echo "public" >> .gitignore
    

##### Initialize Your `gh-pages` Branch

You can now initialize your `gh-pages` branch as an empty [orphan branch](https://git-scm.com/docs/git-checkout/#git-checkout---orphanltnewbranchgt):

    git checkout --orphan gh-pages
    git reset --hard
    git commit --allow-empty -m "Initializing gh-pages branch"
    git push upstream gh-pages
    git checkout master
    

#### Build and Deployment

Now check out the `gh-pages` branch into your `public` folder using git’s [worktree feature](https://git-scm.com/docs/git-worktree). Essentially, the worktree allows you to have multiple branches of the same local repository to be checked out in different directories:oluptatem.