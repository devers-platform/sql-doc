# Article

This is the documentation for `article` table.

This model is used to store article information.

## Table

| Column     | Type          | Description                                                                                                       |
|------------|---------------|-------------------------------------------------------------------------------------------------------------------|
| id         | `char(12)`    | Unique identifier of the article. Use nanoid as its format. **UNIQUE** **PRIMARY**.                               |
| title      | `char(16)`    | Title of the article.                                                                                             |
| statusCode | `bit(2)`      | Status of the article.<br />The number and status relationship is shown in [article-status.md](article-status.md) |
| authorId   | `char(12)`    | Unique identifier of the author user of the article. Use nanoid as its format.                                    |
| keyword    | `char(64)`    | The keywords of the article.                                                                                      |
| views      | `int`         | View numbers.                                                                                                     |
| likes      | `int`         | Like numbers.                                                                                                     |
| createdAt  | `timestamptz` | The time when the article is created.                                                                             |
| updatedAt  | `timestamptz` | The time when the article is updated.                                                                             |
| deletedAt  | `timestamptz` | The time when the article is deleted (soft delete).                                                               |

```sql
CREATE TABLE articles (
    id CHAR(12) UNIQUE PRIMARY KEY,
    title CHAR(16),
    statusCode BIT(2),
    authorId CHAR(12),
    keyword CHAR(64),
    views INT,
    likes INT,
    createdAt TIMESTAMPTZ,
    updatedAt TIMESTAMPTZ,
    deletedAt TIMESTAMPTZ
);
```