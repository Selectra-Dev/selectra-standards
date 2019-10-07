Laravel
=

Laravel's ecosystem standardization.

# Table of contents

1. [Laravel](#laravel)

2. [Eloquent](#eloquent)

3. [Migrations](#migrations)

4. [Seeders](#seeders)

5. [Blade](#blade)

# Laravel

- **MUST** use controller routes instead of closures

    > Closures can't be cached and it's hard to reflect them.

- **SHOULD** use [form requests](https://laravel.com/docs/master/validation#form-request-validation) whenever application is modifying something

- **SHOULD** prefer [contracts](https://laravel.com/docs/master/contracts) to [facades](https://laravel.com/docs/master/facades)

    > Facades are really nice feature but they encourage developers to build complex and unmaintainable code. Having dependencies injected explicitly we gain more control over our code.

- **SHOULD** prefer [policies](https://laravel.com/docs/master/authorization#authorizing-actions-using-policies) to [gates](https://laravel.com/docs/master/authorization#gates)

- **SHOULD** use [`selectra-dev/laravel-deploy`](https://github.com/Selectra-Dev/laravel-deploy) package

    > This repository holds common useful laravel tools.

- **MUST** name Traits in passive voice

    > For example CompilesLoops. This is Laravel's naming convention and it should be maintained for consistency.

- **SHOULD** use built-in authentication system

- **SHOULD** use built-in migration system

- **MUST** prefix external indexes properties

    > For example ZohoCRM that we use frequently (its properties should be prefixed with `zoho_`).

- **MUST NOT** use [aliases](https://laravel.com/docs/master/facades#facade-class-reference) in Laravel packages and portable code

# Eloquent

- **SHOULD NOT** use [polymorphic relations](https://laravel.com/docs/master/eloquent-relationships#polymorphic-relationships)

    > They're not using indexes. Please rethink twice before creating such relation.

# Migrations

- **SHOULD** separate migrations for independent tables

    > But in the case of moving a column from one table to another, it is always preferable to have one migration like `move_category_id_from_foo_table_to_bar_table`, rather than 3 migrations like `create_category_id_in_bar_table`, `copy_category_ids_from_foo_table_to_bar_table` and `remove_category_id_from_foo_table`.

- **SHOULD** separate migrations for independent columns

    > In some situations it's more convenient to have bulk **updating table** migration. By having multiple migrations it's easier to see what changed (you don't need to read bulk migration documentation).

- **MUST NOT** implement no-create migrations in pre-release phase

    > If application is not deployed on production (meaning database is always re-created) don't create altering migrations but adjust **creating table** migration.

- **MUST** follow `create_{table_name}_table` pattern when writing **creating table** migration

- **MUST** follow `update_{index}_{table_name}_table` pattern when writing **updating table** migration

    > A **bulk** update that might contain `adding`, `removing` and `updating` columns. This also includes changing schema collation and manipulating indexes.

- **MUST** follow `add_{column_name}_to_{table_name}_table` pattern when writing **adding column** migration

- **MUST** follow `remove_{column_name}_from_{table_name}_table` pattern when writing **removing column** migration

- **MUST** follow `update_{index}_{column_name}_in_{table_name}_table` pattern when writing **updating column** migration

- Bulk **updating table** migration **MUST** contain proper class-scope documentation briefly listing what changes are done

    > Don't force other developers review the `up` and `down` methods code themselves.

# Seeders

- **SHOULD** separate seeders into multiple files

    > This way they're simpler to maintain. Migration file name should be self-explanatory.

# Blade

- **MUST** use translation directive everywhere, even if there is no translation for that sentence yet or application is not shipped internationally

    ```blade
    @lang('Lipsum ipsum dolor sit amet')
    ```

    > This way it's easier to digest whats more to translate.
