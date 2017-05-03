# Abstractions

An abstraction encapsulates something complex, into one simple thing. This helps us reason about concepts in a more high-level way.

For instance you could abstract a function away from your code which is responsible for truncating a string. You pass the function a string and an int, it does some magic and returns a new string, truncated to the length specified.

You don't need to know how this function is implemented, it just works the same every time.

# Leaky Abstractions

A leaky abstraction is an abstraction which fails to encapsulate its implementation. Therefore to be able to work with the abstraction, one must have a knowledge of the underlying implementation.
