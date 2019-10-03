SQL and MySQL
=

# Table of contents

1. [Naming convention](#naming-convention)

2. [User permissions](#user-permissions)

# Naming convention 

- All databases, tables and table properties **SHOULD** follow *snake_case* naming convention.

- Table names **SHOULD** be plural.

- Table property names for foreign keys **SHOULD** be singular.

    > Instead of having for example `posts.user_id`, make it `posts.user`. It's obvious it links to users primary key (which is almost always `id`).

# User permissions

- Every project's database should have his own dedicated user with permissions restricted only to that database only.
