Selectra’s MYSQL designing standards
=

# Table of contents

* Naming
* Permissions

# Naming 

- All databases, tables and table properties should follow *snake_case* naming standard
- Use plural table names
- Should use singular key names for foreign keys (because it's obvious to which key it links). Like, instead of having for example `post.user_id`, make it `post.user`.

# Permissions

- Every project's database should have his own dedicated mysql user with permissions restricted only to that database
