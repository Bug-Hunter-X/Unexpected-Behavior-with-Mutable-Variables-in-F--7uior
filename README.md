# F# Mutable Variable Swap Bug

This example demonstrates a common pitfall in F# when working with mutable variables.  The `swap` function intends to exchange the values of `x` and `y`, but due to pass-by-reference semantics, it modifies the original variables directly.

**Issue:** The `swap` function doesn't create copies of the input variables; instead, it alters `x` and `y` in place.

**Solution:**  To properly swap values, you need to return new values from the function, avoiding direct modification of input variables.  This can be achieved using tuples or records.