# Totality

With statically typed languages, type signitures should serve as documentation.

The following type signiture says the function should take an `int` and return an `int`.

```
int -> int
```

If the function throws an error, for instance it can't handle a zero input, it will be breaking this contract. So there are some ways to handle this.

Either:
  - Constrain the input e.g. `NonZeroInt -> int`.
  - Extend the output e.g. `int -> Maybe<int>`, you could get an int or nothing.

When you desgin with totality, you know what to expect from your functions.
