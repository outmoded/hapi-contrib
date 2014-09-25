# Writing Tests for hapijs Modules

We want tests to be consistent from one repo to the next; one for readability and two to make it possible for [lab](https://github.com/hapijs/lab) to do "deep testing". Deep testing will allow the current module to test itself as well as all of the dependencies.

## Standards

1. Only create lab aliases for values the test actually uses. In other words, don't have `before` and `after` variables if the test never uses them.
2. Describing method tests should be appear like this; "methodName()" and _not_ "#methodName"
3. Any non-functional test should appear at the top of the test _outside_ of any `describe` bocks.
4. Tests should no longer have an outer `describe` block. See 3 above.

The full conversation can be found [here](https://github.com/hapijs/discuss/issues/24).
