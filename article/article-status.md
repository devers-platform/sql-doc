# Article Status

This is the documentation for `user` table field `statusCode`.

The `statusCode` field requires an integer value, representing the status of the user based on the following relations.

The `statusCode` field's type is `bit(4)`.

## Relations

| Status    | Integer | Bit |
|-----------|---------|-----|
| Draft     | 0       | 00  |
| Published | 1       | 01  |
| Deleted   | 2       | 10  |
| Blocked   | 3       | 11  |