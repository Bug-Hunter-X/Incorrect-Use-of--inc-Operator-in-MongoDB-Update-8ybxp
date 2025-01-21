# Incorrect Use of $inc Operator in MongoDB Update

This example demonstrates an incorrect use of the `$inc` operator in a MongoDB update operation.  Using a string value with `$inc` will not increment the field as expected, instead causing unexpected behavior.

**The bug:** The `$inc` operator should only be used with numeric values. Attempting to use a string will result in the update failing silently or causing unexpected results.

**Solution:** Always ensure that the value passed to `$inc` is a number (integer or floating-point).