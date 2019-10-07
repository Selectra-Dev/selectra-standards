Laravel and Eloquent good practices and standards
=

# Table of contents

1. [Laravel](#laravel)

2. [Eloquent](#eloquent)

3. [Migrations](#migrations)

4. [Blade](#blade)

# Laravel

- **SHOULD** use contracts instead of facades

    > Facades are really nice feature but they encourage developers to build complex and unmaintainable code. Having dependencies injected explicitly we gain more control over our code.

- **MUST** use controller routes instead of closures

- **SHOULD** use [form requests](https://laravel.com/docs/master/validation#form-request-validation) whenever application is modifying something

- **SHOULD NOT** use policies to check if the user is allowed to make modifications

- **SHOULD NOT** use polymorphic relations

    > They're not using indexes. Please rethink twice before creating such relation.

- **SHOULD** separate migrations into multiple files if they are not related with each other

    > For example, in the case of moving a column from one table to another, it is always preferable to have 1 migration like `move_category_id_from_foo_table_to_bar_table`, rather than 3 migrations like `create_category_id_in_bar_table`, `copy_category_ids_from_foo_table_to_bar_table` and `remove_category_id_from_foo_table`.

- **SHOULD** separate seeders into multiple files

    > This way they're simpler to maintain. Migration file name should be self-explanatory.

- **SHOULD** use `selectra-dev/laravel-deploy` package

- **MUST NOT** use aliases in Laravel packages and portable code

- **MUST** name Traits in passive voice

    > For example CompilesLoops.

# Eloquent

- **SHOULD** use built-in authentication system

- **SHOULD** use built-in migration system

- **MUST** prefix external indexes properties

    > For example ZohoCRM that we use frequently (its properties should be prefixed with `zoho_`).

# Migrations

- **MUST NOT** implement no-create migrations in pre-release phase

    > If application is not deployed on production (meaning database is always re-created) don't create altering migrations but adjust **creating table** migration.

- **MUST** follow `create_{table_name}_table` pattern when writing **creating table** migration

- **MUST** follow `update_{index}_{table_name}_table` pattern when writing **updating table** migration

    > A **bulk** update that might contain `adding`, `removing` and `updating` columns. This also includes changing schema collation and manipulating indexes.

- **MUST** follow `add_{column_name}_to_{table_name}_table` pattern when writing **adding column** migration

- **MUST** follow `remove_{column_name}_from_{table_name}_table` pattern when writing **removing column** migration

- **MUST** follow `update_{index}_{column_name}_in_{table_name}_table` pattern when writing **updating column** migration

- **Updating table** migration **MUST** contain proper class documentation briefly listing what changes are done

    > Don't make other developers review the `up` and `down` methods code.

- **SHOULD** create independent migrations for each column

    > In some situations it's more convenient to have bulk **updating table** migration. By having multiple migrations it's easier to see what changed (you don't need to read bulk migration documentation).

# Blade

- **MUST** use translation directive everywhere, even if there is no translation for that sentence yet or application is not shipped internationally

    ```blade
    @lang('Lipsum ipsum dolor sit amet')
    ```

    > This way it's easier to digest whats more to translate.
