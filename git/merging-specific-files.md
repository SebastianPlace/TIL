# Merging specific files from one branch to another

You have some work on a branch which you'd like to merge into a new branch.

You may have a branch which consists of two features which you'd like to break-up.

For example the `feature/home-page` branch consists of two features. The 'collections' feature and the 'home-page' feature.

The collections branch needs the original home-page from the development branch.

First we branch the new collections branch from 'feature/home-page':
```
@feature/homepage

git checkout -b feature/collections
```

Next we can select the files we want to carry across from the development branch into the new collections branch:
```
git checkout app/routes/root.js app/controllers/root.js app/templates/home-page.hbs
```
