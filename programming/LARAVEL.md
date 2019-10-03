Laravel and Eloquent good practices and standards
=

# Table of contents

1. [Laravel](#laravel)

2. [Eloquent](#eloquent)

3. [Blade](#blade)

# Laravel

 **MUST** use contracts instead of facades.

 **MUST** use controller routes instead of `\Closure`.

 **SHOULD** use form request whenever application is modifying something.

 **SHOULD NOT** use policies to check if the user is allowed to make modifications.

 Don't use polymorphic relations.

 **SHOULD** separate migrations into multiple files if they are not related with each other.

    For example, in the case of moving a column from one table to another, it is always preferable to have 1 migration like `move_category_id_from_foo_table_to_bar_table`, rather than 3 migrations like `create_category_id_in_bar_table`, `copy_category_ids_from_foo_table_to_bar_table` and `remove_category_id_from_foo_table`.

- **SHOULD** separate seeders into multiple files 

- **SHOULD** use `selectra-dev/laravel-deploy` package

# Eloquent

- **SHOULD** use built-in authentication system

- **SHOULD** use built-in migration system

- Prefix zoho properties with `zoho_`

# Blade

- Use translation directive everywhere, even if there is no translation for that sentence yet

    ```blade
    @lang('Lipsum ipsum dolor sit amet')
    ```
