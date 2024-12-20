# MongoDB Aggregation Pipeline Bug: Incorrect $inc Operator Usage
This repository demonstrates a common error when using the `$inc` operator within the `$project` stage of a MongoDB aggregation pipeline.  The `$inc` operator is intended for updating existing fields, not creating new ones based on existing field values within the aggregation pipeline. The incorrect usage can lead to unexpected results or errors.

## Bug Description
The provided code attempts to increment the `count` field by 1 and store the result in a new field called `updatedCount`. However, this approach is flawed because `$inc` expects to modify an existing field, rather than create a new one. This will likely result in an error or unexpected behavior.

## Solution
The solution replaces the incorrect usage of `$inc` with the `$add` operator, which correctly performs the addition operation to create a new field. 
