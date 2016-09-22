# Invoke service methods directly from a component

[On ember guides](https://guides.emberjs.com/v2.8.0/components/triggering-changes-with-actions/#toc_invoking-actions-directly-on-component-collaborators)

Example:

app/services/favourites
```
import Ember from 'ember';

export default Ember.Service.extend({
  actions {
    showMsg(msg){
      console.log(msg);
    }
  }
});
```

app/components/addFavourite.js
```
import Ember from 'ember';

export default Ember.Component.extend({
  favourites: Ember.inject.service(),
});
```

app/templates/components/addFavourite.hbs
```
<span {{action "showMsg" target=favourites}}>Show Message</span>
```
