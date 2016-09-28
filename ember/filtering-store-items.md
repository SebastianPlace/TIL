# Query the store without making a network request

```
const allActions = store.peekAll('action');
let allUserFavourites = allActions.filter((action) => {
  if (action.get('userId.id') === currentUserId && action.get('type') === 'favourite') {
    return true;
  }
});
```
