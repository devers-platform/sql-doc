# User Status

This is the documentation for `user` table field `statusCode`.

The `statusCode` field requires an integer value, representing the status of the user based on the following relations.

The `statusCode` field's type is `bit(4)`.

## Relations

| Status          | Integer | Bit  |
|-----------------|---------|------|
| Busy            | 0       | 0000 |
| Offline         | 1       | 0001 |
| Happy           | 2       | 0010 |
| We Got This     | 3       | 0011 |
| Exhausted       | 4       | 0100 |
| Low Mood        | 5       | 0101 |
| Thinking        | 6       | 0110 |
| Energetic       | 7       | 0111 |
| Zoning Out      | 8       | 1000 |
| Luck Come to Me | 9       | 1001 |
| Sleeping        | 10      | 1010 |
| Hardworking     | 11      | 1011 |
| Studying        | 12      | 1100 |
| Rushing Home    | 13      | 1101 |
| Mysterious      | 14      | 1110 |
| In Love         | 15      | 1111 |