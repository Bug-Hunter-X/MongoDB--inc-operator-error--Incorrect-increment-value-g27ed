# MongoDB $inc Operator Error
This example demonstrates an uncommon error when using the `$inc` operator in MongoDB update operations. The error arises from providing a string value instead of a numerical value for the increment.

## Bug Description
The `$inc` operator is used to increment a numerical field in a MongoDB document.  Attempting to increment with a string will result in the string being appended, not a numerical increment.

## How to Reproduce
1. Create a MongoDB collection.
2. Insert a document with a numerical field (e.g., `field: 0`).
3. Use the incorrect `$inc` operation (string increment) to update the document.
4. Observe that the field is not numerically incremented.

## Solution
The correct approach is to always use a numerical value for the increment in the `$inc` operator. Ensure you're using integers or floating point numbers, not strings.