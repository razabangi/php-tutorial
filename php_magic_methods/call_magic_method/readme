##### __call Magic Method

```php
<?php

class Str
{
    private string $text;

    public $helper = [
        'length' => 'strlen',
        'upper' => 'strtoupper',
        'lower' => 'strtolower'
    ];

    public function __construct(string $text)
    {
        $this->text = $text;
    }

    public function __call($method, $arguments)
    {
        if (!in_array($method, array_keys($this->helper))) {
            return "Choose correct method example: [length, upper, lower]";
        }

        array_unshift($arguments, $this->text);

        return call_user_func_array($this->helper[$method], $arguments);
    }
}

$a = new Str("hello world");
// echo $a->raza();
// echo $a->upper() . PHP_EOL;
// echo $a->length() . PHP_EOL;
// echo $a->lower() . PHP_EOL;
```