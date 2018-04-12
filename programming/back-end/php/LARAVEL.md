Laravel and Eloquent good practices and standards
==

# Table of contents

* Laravel
* Eloquent
* Blade

# Laravel

- Use contracts instead of facades
- Use controller routes instead of `\Closure`
- Use form request whenever application is modifying something
- Don't use polymorphic relations
- Separate migrations into multiple files
- Separate seeders into multiple files 
- Indicate code completion by documenting available orm property
    ```php
    /**
     * Dummy class.
     *
     * @property int $id
     * @property float $amount
     * @property string $lead_source
     *
     * @package App\Models
     * @author Foo Bart <foo.bar@email.com>
     */
    class Dummy extends Model
    {
        /**
         * {@inheritdoc}
         */
        protected $attributes = [
            'id',
            'amount',
            'lead_source',
        ];
    }
    ```
- **SHOULD** Use `selectra-dev/laravel-deploy` package

# Eloquent

- **SHOULD** use built in authentication and migration
- Prefix zoho properties with `zoho_`

# Blade

- Use translation directive everywhere, even if there is no translation for that sentence yet
    ```blade
    @lang('Lipsum ipsum dolor sit amet')
    ```
