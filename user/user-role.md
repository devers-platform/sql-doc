# User Role

This is the documentation for `user` table field `role`.

The `role` field requires an integer value, representing the role of the user based on the following relations.

The `role` field's type is `bit(2)`.

## Relations

| Role        | Integer | Bit |
|-------------|---------|-----|
| Guest       | 0       | 00  |
| User        | 1       | 01  |
| Admin       | 2       | 10  |
| Super Admin | 3       | 11  |
