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


- ## function

Parâmetros: Definição normal

function !nomedafunçao!(parâmetros que eu quero criando variaveis) {

}

**Essa função recebe os parametros (n1 e n2) e logo após inserir uma nova variável, depois disso o return é a saida da função, então inseri a variável $total.**

- Agora utilizamos a função, vamos armazenar uma variável com descrição **$soma**. Logo após utilizamos a nossa função **somar()** os valores de **n1 e n2** ficariam assim **$soma = somar(10 , 5);** a variavel **$soma** vai armazenar a função. 
Agora imprimimos o valor da variavel que foi armazenada **echo "Total: ". $soma** .

```
function somar( $n1, $n2 ){
    $total = $n1 + $n2;
    return $total;
}

$soma = somar(10 , 20);
echo 'TOTAL: '.$soma;
```

- Tudo que for fazer dentro da função permanece na função inclusive definição de variáveis.

## Função de 3 parâmetros
- para deixar o parâmetro opcional em uma função definimos um valora padrão para ele.
```
function somar($n1, $n2, $n3 = 0){
   $total = $n1 + $n2 + $n3;
   return $total;
}

$x = somar(5, 3);
$y = somar(6, 7, 6);
$w = somar($x, $y);
echo $w; 
```
- o **n1** vai ser o valor atribuido unico nesse caso.

```
function somar($n1, $n2 =0, $n3 = 0){
   $total = $n1 + $n2 + $n3;
   return $total;
}

$x = somar(5, 3);
$y = somar(6, 7, 6);
$w = somar($x, $y);
echo $w;
```
- Para deixar esse **n1** em um tipo de dado especifico antes do nome da variavel inserir um tipo que vou receber da variavel se eu quero um **int=inteiro** quando definir um tipo de dado só vai executar se entrar algum determinado tipo de dado.
```
function somar(int $n1, int $n2=0, int $n3 = 0){
   $total = $n1 + $n2 + $n3;
   return $total;
}

$x = somar(5, 3);
$y = somar(6, 7, 6);
$w = somar($x, $y);
echo $w;
```
## Parâmetros: Referência ou Valor 

```
function somar($n1, $n2){
    $total = $n1 + $n2;
    return $total;
}

$x = 3;
$y = 2;
$soma = somar($x , $y);
echo "total ".$soma; 
```
- Quando mandei somar o meu **$x**, ele não mandou a variavel **$x** ele mandou o valor dessa variavel **$x**. Então eu passei um parâmetro por valor então eu mandei **3**, e no valor **y** foi o número **2**.

- Quando entrou na função o **3** assumiu o **n1** e o **2** assumiu o **n2**, retornoei o resultado que armazenei em **$soma** e imprimi ela.

## Variável por referência


## Função Anônimas

É quando não tem um nome, e no final tem que inserir ponto e virgula faz parte da definição da variavel


```
$variavel function (caracter $oque eu quero) {
 return $oque ue quero 
};

$o nome que vai receber = $variavel;

echo $o nome que vai receber();

```
Posso passar essa função para outra variavel qualquer e usar normalmente
```
$dizimo = function( int $valor) {
  return $valor * 0.1;
};

$funcao = $dizimo;
echo $dizimo(90);
```

## Funções Arrow 7.4 >

 - Nós inserimos fn() os parametros a arrow function só tem como fazer uma expressão dentro dela. Ela é inserida apenas quando tem uma função só sendo, executada. Coloque os parâmetros quanto quer que seja,logo após inseri um simbolo **=>** e depoiscoloque a expressão que estamos executando   

```
$dizimo = fn($valor) => $valor * 0.1;  

echo $dizimo(90);
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
---
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
---
 
```
function somar ($x1, $y1, &$total){
    $total = $x1 + $y1;
}

$x1 = 10;
$b3 = 8;
$w1 = 0;
somar($x1, $b3,$w1);
echo $w1;
```

## Funções Nativas de Matematica
 
- função absoluto **abs()**.

- função **pi()**.

- função **floor($variavel) - chão pra baixo**

- função **ceil($numero) - pra cima** ;

```
$numero = 12.45 
echo round($numero, 2)
```
```
$aleatorio = rand(3,9); **Vai vir numero aleatorio do que você deseja.**
```
```
$lista = [1,4,7,9,2];
echo max($lista);
```

---
## Funções Nativas string (1/2)
```
$nomeSujo = '   Johnny     ';
$nomeLimpo = trim($nomeSujo);

echo "Nome Sujo: ".strlen($nomeSujo)."<br/>"; 
echo "Nome Limpo: ".strlen($nomeLimpo);
```
length = extensão
-strlen = conta a quantidade de caractere.
trim = retira os espaços desnecessarios 

```
$nome = 'Bonieky Lacerda';

echo strtolower($nome);
```
- strtolower = para deixar o nome minusculo

- strtoupper = para letra maiuscula

```

$nome = 'Bonieky Lacerda';

$nomeAlterado = str_replace('Lacerda', 'Silva', $nome);

```
- Replace 

**procure por = Lacerda**

**Substitua por = Silva**

**Nessa variavel =$nome**


```
$nomeCompleto = 'Bonieky Lacerda';

$nome = substr($nomeCompleto, 0, 5); ==> a quantidade que eue quero pegar 

echo $nome;
```


## Funções Nativas de String (2/2)

- função explode tem 2 parâmetros, oque irá procurar para ser o divisor entre cada uma das palavras etc. No nosso caso é um espaço ''
o segundo parâmetro é propria string.

```
$nomeCompleto = 'bonieky lacerda leal';

$nome = explode('',$nomeCompleto);

print_r($nome);
```

- Exibir o numero formatado direitinho.  

```
$numero = 12913.12

echo number_format($numero,quantidade decimal que vai ter, 'terceiro parametro é optacional', 'quarto parametro simbolos para separar os milhares )
```

## Function Nativas Array (1/2)

```
$lista = ['nome1', 'nome2', 'nome3', 'nome4'];

echo "total".count($lista)
```

- Vai contar a quantidade ela vai dar um numero real

---
```
$lista = ['bonieky','pedro', 'paulo', 'josé', 'francisca','paula'];

$aprovados = ['bonieky', 'pedro', ''francisca];

$reprovados = array_diff($lista, quem eu quero fazer a comparação ---> $aprovados);

print_r($reprovados);
```

## array_diff
- Existe uma função do PHP, que ela vai pegar a difença entre o primeiro e o segundo e ela vai gerar um novo array, com os item que não estão na primeira lista. Os itens da primeira lista que não estão na segunda lista.
 

## array_filter
- Ele vai filtrar no array

```
$numeros = [10, 20, 24, 91, 18];

$filtrados = array_filter($numeros, function($item){
    if($item < 20) {
    return true;
    }else {
        return false;
    }
});

print_r($filtrados);
```

- Callback tem que criar uma função e mandar ele vai fazer um loop no parametro da função callback ele ira receber o numero especifico ele vai fazer um loop em cada um dos itens e ele vai receber a varivel item. e vamos ter que retornar true oyu false. 

- Nesse exercicos quero fazer também então quero gerar um novo array de filtrados só com os numeros que estão abaixo de 20 ou 30. Ai eu verifico.

## array_pop 
- Remove o ultimo array.

- Não precisa armazenar ele em variavel recebe o parâmetro por referencia ele vai fazer alteração no proprio item que mandar inserimos a variavel que desejamos e vai remover o ultimo item do array.

```
$numero = [10, 20, 24, 91, 18];

array_pop($numeros);

print_r($numero);
```

### array_shift 

- Remove o primeiro array.

```
$numero = [10, 20, 24, 91, 18];

array_shift($numeros);

print_r($numero);
```
### in_array
- Ele vai procurar se existe algo na varivel solicitada.
```
$numero = [10, 20, 24, 91, 18];

if(in_array(90, $numeros)) {
    echo 'EXITE';
}else {
    echo 'NÃO EXISTE';
}
```

### array_search

- Ele vai fazer um busca a posição que está o item especifico
```
$numero = [10, 20, 24, 91, 18];

$pos = array_search(91, $numeros);

echo $pos;
```

### sort

- E quando inserimos um **r** na frente dessa forma **rsort** 

- Ele vai ordenar o que está na array 

- Mantem o valor inseri **asort** associando 
```
$numero = [10, 20, 24, 91, 18];

sort($numeros);

echo "A chave 3 é ".$numero[3];

print_r($numeros);
```

### implode

- ele vai juntar tudo ele vai tranformar em uma string.

```
$nome = ['bonieky', 'johnny', 'rebeca'];

$nome = implode(' ', $nomes)
```

