## php
---
FUNÇÃO QUE VAI SOMAR...
- NUMERO 1 
- NUMERO 2

INTERNAMENTE:
- PEGAR O NUMERO 1 E ADICIONAR O NUMERO 2

RESULTADO:
- A SOMA DO NUMERO 1 E NUMERO 2 

O operador básico de atribuição é "=". A sua primeira inclinação deve ser a de pensar nisto como "é igual". Não. Isto quer dizer, na verdade, que o operando da esquerda recebe o valor da expressão da direita (ou seja, "é definido para").


#### FUNCTION

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
Parâmetros: Definição normal

```
function !nomedafunçao!(parâmetros que eu quero criando variaveis) {
    $total = $n1 + $n2 
    Devolver a variavel que eu quero com o !return!
}
```

#### tudo que acontece dentro da função fica na função.

```
function a($x, $y){ 
    return $x + $y;
    }

    echo a(10, 15);
```    
**$x e $y são parâmetros. 10 e 15 são argumentos**
