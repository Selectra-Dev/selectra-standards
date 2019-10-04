SQL and MySQL
=

# Table of contents

1. [Naming convention](#naming-convention)

2. [User permissions](#user-permissions)

# Naming convention

- All databases, tables and table properties **MUST** follow `snake_case` naming convention

- Table names **MUST** be plural

- Table property names for foreign keys **SHOULD** be singular and without obvious `id``suffix

    > Instead of having for example `posts.user_id`, make it `posts.user`. It's obvious it links to users primary key (which is always `id`).

- Withing the same database, when using the same property names for different meanings, you **MUST** call them differently

    > For example, `offers.phone` (being stationary or mobile) and `contact.phone` (being contact's phone number) should be `offers.phone_type` and `contact.phone_number`.

- **MUST** be verbose

    > For example instead of `phone_num` (quantity or number?) use `phone_number`.

# User permissions

- Every project's database **SHOULD** have his own dedicated user with permissions restricted only to that database only
