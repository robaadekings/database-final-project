# database-final-project


his database system provides a complete solution for managing library operations, including book tracking, member management, loan processing, and fine calculations. The system is built using MySQL and follows relational database best practices.



+-------------+       +-------------+       +---------------+
|   members   |       |    books    |       |   publishers  |
+-------------+       +-------------+       +---------------+
| PK: member  |------>| PK: book_id |<------| PK: publisher |
|    id       |       | FK: publish |       |      id       |
+-------------+       |    er_id    |       +---------------+
       ^              +-------------+
       |                    ^
       |                    |
       v                    v
+-------------+       +-------------+       +-------------+
|    loans    |       | book_authors|       |   authors   |
+-------------+       +-------------+       +-------------+
| PK: loan_id |<------| PK: book_id |------>| PK: author  |
| FK: book_id |       | PK: author  |       |     id      |
| FK: member  |       |     id      |       +-------------+
|    id       |       +-------------+
+-------------+
       |
       v
+-------------+       +-------------+
|    fines    |       |    staff    |
+-------------+       +-------------+
| PK: fine_id |       | PK: staff   |
| FK: loan_id |       |     id      |
+-------------+       +-------------+