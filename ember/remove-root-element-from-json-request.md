# Serialization

When added to a serializer, this method removes JSON root object on requests.

```
serializeIntoHash: function(hash, type, record, options) {
   Ember.merge(hash, this.serialize(record, options));
}
```
