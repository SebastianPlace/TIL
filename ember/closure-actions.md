# Closure Actions

You can pass controller functions into components using the action helper.
In this example the `navigate` property on the component is being set the `someActionOnController` function found in the enclosing controller.

```
{{my-component item=model navigate=(action 'someActionOnController')}}
```

Calling it from `components/my-component`:

```
this.get('navigate')('back', item);
```
