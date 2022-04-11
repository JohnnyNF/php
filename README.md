## php 




---
```
$nome = 'Johnny';
$sobrenome = 'Feijo'

$nomeCompleto = $nome;
$nomeCompleto .= $sobrenome;
```

  **o (ponto). antes do igual ele vai fazer o funcionamento de ser oque já tinha na variavel e vai adicionar a variavel que eu desejo**

---

- # if
**SE idade for menor que 18 ENTAO
-- Mostrar na tela "Menor de Idade"
CASO CONTRARIO 
-- Mostrar na tela "Maior de idade"** 

---

- # Operador ternario 

```
(CONDIÇÃO) ? RESULTADO POSITIVO : RESULTADO NEGATIVO;
           |
           -->Operador ternario

$idade = 6;

echo ($idade > 8) ? 'Maior de 5 anos': 'Menor de 5 anos';



$idade = 20;
}  else {
     echo 'Maior';
}
```
```
$idade = 12;

$menorDeIdade = ($idade < 18) ? true : false;

if($menorDeIdade) {
    echo 'TRUE';
} else {
    echo 'FALSE';
}
```
---
- ### loop for 

```
for($i = 0; $i < 20; $i++){  
    for($j = 0; $j < 20; $j++){
    if($j <= $i){
       echo '-'; 
    }
    }
    echo "<br/>";
}
```
- ### Switch

```
$tipo = 'foto';

switch($tipo) {
    case 'foto':
        echo 'Exibindo FOTO';
            break;
    case 'video':
        echo 'Exibindo VIDEO';
            break;
    case 'texto':
        echo 'Exibindo TEXTO';
            break;
}
```
---



- # Array
Primeiramente vamos criar uma $variável. Logo após vai atribuir para ela um par de chaves[ ]. E por fim dentro das chaves você armazena os valores que quiser, separados por virgulas. 

```
<?php

$arr=["primeiro valor", "segundo valor", "terceiro valor"];
print_r($arr);

?>
```
**Com a função print_r() ela imprimi a array no navegador:**

Array ( [0] => primeiro valor [1] => segundo valor [2] => terceiro valor )

Outra forma de declarar uma array é através da função array() onde inclui o valor dentro dos parenteses separados por virgula.

```
<?php
$arr=array("primeiro valor", "segundo valor", "terceiro valor");
print_r($arr);
?>
```
Também podemos fazer é cirar chaves personalizadas para array. Basta utilizar o => onde a esquerda é a chave e a direita o valor.

```
$arr=array( "nome"=>"Rafael","sobrenome"=>"Marques", "idade"=>"25");
print_r($arr);

echo "<br/><br/>";
echo "Nome: ".$arr["nome"]."<br/>";
echo "Sobrenome: <b>".$arr["sobrenome"]."</b><br/>";
echo "Idade: <b>".$arr["idade"]."</b>";
```

PHP Array Multidimensional (ou PHP Multi array)

São estruturas heterogêneas que permitem que você salve multiplos dados de tipos difirentes em um mesmo lugar. Dessa formar é permitido incluir uma ou mais arrays dentro de uma array.

```
<?php
$arr=array(
    array("Primeiro valor","Segundo valor"),
    array("Terceiro valor","Quarto valor")
);

print_r($arr);
echo "<br/>";
print_r($arr[0]);
echo "<br/>";
print_r($arr[1]);
?>
```

---
- # Function 
FUNÇÃO QUE VAI SOMAR...
- NUMERO 1 
- NUMERO 2

INTERNAMENTE:
- PEGAR O NUMERO 1 E ADICIONAR O NUMERO 2

RESULTADO:
- A SOMA DO NUMERO 1 E NUMERO 2 

O operador básico de atribuição é "=". A sua primeira inclinação deve ser a de pensar nisto como "é igual". Não. Isto quer dizer, na verdade, que o operando da esquerda recebe o valor da expressão da direita (ou seja, "é definido para").
```
function somar( $n1, $n2 ){
    $total = $n1 + $n2;
    return $total;
}

$soma = somar(10 , 20);
echo 'TOTAL: '.$soma;
```

- ## function

Parâmetros: Definição normal

function !nomedafunçao!(parâmetros que eu quero criando variaveis) {

}

```
function subSequente(){
    for($q=0;$q<=10;$q++){
        echo $q."<br/>";
    }

    echo "<hr/>";
}

subSequente();
subSequente();
```

```
function subSequente(){
    for($q=0;$q<=10;$q++){
        echo $q."<br/>";
    }

    echo "<hr/>";
}

subSequente();
subSequente();
```



