---
description: A estrutura de controle mais básica para testar condições verdadeiro/falso.
---

# If / Else \(se / senão\)

As estruturas de contrle

## if/else \(se/senão\)

O **if/else** \(se/senão\) serve para testar uma expressão, e ir para um bloco de código caso a expressão que você colocou seja verdadeira, ou caso você implemente o **else**, se a expressão não for verdadeira.

```php
<?php

$a = 0; 
$b = 1;

if($a > $b){ 
    print("a variável \$a é maior que a variável \$b."); 
} 
else { 
    print("a variável \$a NÃO É maior que a variável \$b."); 
}
?>
```

> **Importante:** eu usei o caractere de escape  **\(barra invertida\)** para que a saída do _print_ não interprete as variáveis e sim exiba o nome delas \($a e $b\).

## **elseif**

Quando você precisar testar mais um uma expressão de uma única vez, você pode **concatenar** mais de um **if** para testar duas ou mais expressões em uma mesma estrutura de controle.

```php
<?php

$a = 0;
$b = 1;

if($a > $b){
    print("a variável \$a É maior que a variável \$b.");
}
elseif ($a == $b){
    print("a variável \$a é IGUAL a variável \$b.");
}
else {
    print("a variável \$a NÃO É maior que a variável \$b.");
}

?>
```

> **Importante:** não abuse dos **if/elseif/else** em suas estruturas de controle. Caso você precise testar muitas expressões, utilize a estrutura de controle **switch/case**.

## Mesclando com HTML

Você pode utilizar as estruturas de controle do PHP, como o **if/else**, para exibir conteúdo **HTML**. O **PHP** irá mostrar o conteúdo que estiver dentro do bloco e não exibirá caso a expressão não seja satisfeita.

```php
<?php

$a = 0;
$b = 1;

if($a > $b){ ?>
    <p>a variável $a É maior que a variável $b.</p>
<?php } elseif ($a == $b){ ?>
    <p>a variável $a é IGUAL a variável $b.</p>
<?php } else { ?>
    <p>a variável $a NÃO É maior que a variável $b.</p>
<?php } ?>
```

No exemplo acima, não utilizamos mais o comando _print_, e o substituímos pelas _tags_ **P** do **HTML**. Como as _tags_ **P** interpretam de forma diferente os caracteres, e o **$** \(dólar\) não está dentro do contexto do PHP, não precisamos usar o caractere de escape **\** \(barra invertida\).

