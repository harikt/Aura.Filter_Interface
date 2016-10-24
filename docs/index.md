# Aura.Filter_Interface

The interface has only one method `apply`. See below.

```php
interface FilterInterface
{
    /**
     *
     * Filter (sanitize and validate) the data.
     *
     * @param array|object $values The values to be filtered.
     *
     * @return bool True if all rules passed; false if one or more failed.
     *
     */
    public function apply(&$values);
}
```

It was purposefully kept simple for different implementations have different ways
to set the validation rules, and getting the failed result once the filter is applied.
