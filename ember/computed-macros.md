# Computed Macros

You can make computed properties more reusable by turning them into helpers.

Take this computed property:
```
barcode: '',
upperCaseBarcode: Ember.computed('barcode', function(){
  return this.get('barcode').toUpperCase();
})
```

Create a helper with `ember g helper <some-name>`

```
import Ember from 'ember';

const { get, computed } = Ember;

export function uppper(key) {
  return computed(key, function(){
    let value = get(this,key);
    return value.toUpperCase();
  });
}

export default Ember.Helper.helper(uppper);
```

Now you can simply import it...
```
import { upper } from '../helpers/upper';
```
and use it where you like with:
```
upperCaseBarcode: upper('barcode');
```

Thanks to [emberdaily](http://www.emberdaily.com/2016/11/03/102-computed-macro/)
