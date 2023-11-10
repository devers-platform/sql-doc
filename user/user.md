# User

This is the documentation for `user` table.

This model is used to store user information.

## Table

| Column     | Type          | Description                                                                                                                       |
|------------|---------------|-----------------------------------------------------------------------------------------------------------------------------------|
| id         | `char(12)`    | Unique identifier of the user. Use nanoid as its format. **UNIQUE** **PRIMARY**.                                                  |
| name       | `char(16)`    | Name of the user.                                                                                                                 |
| email      | `char(64)`    | School email of the user. Should ended with `*hit.edu.cn`.                                                                        |
| role       | `bit(2)`      | Role of the user. <br />The number and role relationship is shown in [user-role.md](user-role.md)                                 |
| status     | `char(64)`    | Status of the user, where user shares their emotions, feelings, etc..                                                             |
| statusCode | `bit(4)`      | The code represents the status of the user.<br />The number and status relationship is shown in [user-status.md](user-status.md)  |
| password   | `char(64)`    | Password of the user. Hashed.                                                                                                     |
| createdAt  | `timestamptz` | The time when the user is created.                                                                                                |
| updatedAt  | `timestamptz` | The time when the user is updated (or we can say, the last time user's operation took place).                                     |
| deletedAt  | `timestamptz` | The time when the user is deleted (soft delete).                                                                                  |
| points     | `integer`     | The points of the user.                                                                                                           |
| avatar     | `bit(4)`      | The code represents the avatar of the user. <br />The number and avatar relationship is shown in [user-avatar.md](user-avatar.md) |
| bio        | `text`        | The bio of the user.                                                                                                              |
| schoolId   | `integer`     | The school ID of the user.                                                                                                        |
| major      | `bit(4)`      | The code represents the major of the user. <br />The number and major relationship is shown in [user-major.md](user-major.md)     |

```sql
CREATE TABLE users (
    id CHAR(12) UNIQUE PRIMARY KEY,
    name CHAR(16),
    email CHAR(64) CHECK (email ~* '^[A-Za-z0-9._%+-]+@*hit\.edu\.cn$'),
    role BIT(2),
    status CHAR(64),
    statusCode BIT(4),
    password CHAR(64),
    createdAt TIMESTAMPTZ DEFAULT current_timestamp,
    updatedAt TIMESTAMPTZ,
    deletedAt TIMESTAMPTZ,
    points INTEGER,
    avatar BIT(4),
    bio TEXT,
    schoolId INTEGER,
    major BIT(4)
);
```