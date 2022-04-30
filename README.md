## php 




---
[Variavéis](https://github.com/JohnnyNF/php/blob/main/nomeCompleto.php)

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
- ## Switch



[Switch](https://github.com/JohnnyNF/php/blob/main/switch.php)
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
- Ele vai procurar se existe algo na array solicitada.
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

## Data/Hora

```
echo date('d/m/Y H:i:s');
```

- Para uma conversão de uma data inseri strtotime()

--- 

## Trabalhando com múltiplos arquivos

- Eu insiro o nome do arquivo nas funções. Ex: header.php, index.php, sobre.php e outros.


- **Require( )** ele impede o codigo de continuar.
- **Include( )** ele da um aviso mas continua.
-**Require_once** ele vai entender que já  tem um arquivo desses."**Sabendo que as tags head e body aparecem apenas uma vez num arquivo HTML, marque alternativa da função de requisição de arquivos que mais se encaixa com essa recomendação."**


---

## Trablhando com pastas diferentes
---

## Modulo 4: HTTP Requests
- action ="o que vai receber os dados", quando não especifica o action ele vai enviar para o proprio arquivo se for index vai enviar para o index 

- Method **POST** - Ele vai para a pagina e envia internamente esses dados. Ele não vai ver as informações sendo enviadas. 

- Method **GET** - Ele vai enviar pela URL e vai ficar visivel.

## Pegando informações do formulário 

- Função filter_input() ele tem 2 parâmetros o tipo de metodo que foi usado para enviar o metodo que foi usado foi GET o nome do campo que foi 'name'
ele vai pegar esse campo e vai fazer uam verificação se está preenchido ou não.

Em um novo arquivo com o nome "recebedor.php" digito essas infomarções:

```
$nome = filter_input(INPUT_GET, 'name');

Para verificar se o nome foi preenchido fazer uma condição

if($nome){
    echo "NOME: ".$nome;
}else {
    echo "NÃO FOI PREENCHIDO" .$nome;
}

echo 'NOME: '.$nome;
```

- A mesma coisa com a idade: 

**Os dois (&&) comercial significa "e"** 

```
$nome = filter_input(INPUT_GET, 'name');
$idade = filter_input(INPUT_GET, 'idade');

if($nome && $idade){
    echo "NOME: ".$nome;
    echo "IDADE: ".$idade;
}else {
    echo "NÃO FOI PREENCHIDO";
}

```

- E para voltar para a tela anterior se 'NÃO FOI PREENCHIDO' faço um redirecionamento 

- A função header vai trocar o header - cabeçalho da requisição e vou trocar a informação Location para o arquivo que eu quero

- Logo após inseri um comando **exit**. Ele vai cancelar a execução do restante do código abaixo.

```
$nome = filter_input(INPUT_GET, 'name');
$idade = filter_input(INPUT_GET, 'idade');

if($nome && $idade){
    echo "NOME: ".$nome;
    echo "IDADE: ".$idade;
}else {
    header("Location: ./index1.php");
    exit;
}   


```

## Validando informações do formulário

- Para validar um campo, vá até ele e inserio comando  **,FILTER_VALIDATE_EMAIL**.

- **SANITAZE** ele vai alterar os dados que foram enviados pra ficar em conformidade com oque espero **FILTER_SANITAZE_NUMBER_INT**.

- Tem também o **filter_var** quando por exemplo já tenho uma informação e quero validar a informação ou peguei uma informação de fora de um outro local ou preencheu uma variavel quero filtrar a validação. 

- Para evitar possiveis brechas **FILTER_SANNITIZE_SPECIAL_CHARS** Ele vai transformar em texto.

- FILTER_VALIDADE_INT - Numero inteiro
- FILTER_VALIDADE_EMAIL - Só vai validar o email
- FILTER_VALIDADE_IP - Verifica se o ip é correto
- FILTER_VALIDADE_URL- Verifica se foi um link real

```
$email = filter_input(INPUT_POST, 'e-mail', FILTER_VALIDATE_EMAIL);
$nome = filter_input(INPUT_POST, 'name', FILTER_SANITIZE_SPECIAL_CHARS);
$idade = filter_input(INPUT_POST, 'idade', FILTER_SANITIZE_NUMBER_INT);


if($nome && $email && $idade){
    echo "NOME: " .$nome;
    echo "<br/>";
    echo "IDADE: " .$idade;
    echo "<br/>";
    echo "EMAIL: " .$email;

}else {
   header('Location: ./index.php');
   exit;
}

```

## Sessões no PHP

- Sessões armazenar informações independente da pagina que eu esteja mandar uma informação a uma pagina a outra, uma sessãonão fica no computador do usuario ela fica no servidor.
Quando você acessa ele identifica que a sessão pertence a você e pega as informações.

- O comando usado vai ser **session_start()** se não existir uma sessão ele vai inicia e se existir ele vai recuperar.

```
<?php
session_start();
require('header.php');

?>

<form method="POST" action="recebedor.php">

    <label>
        Nome:
        <br/>
        <br/>
        <input type="text" name="name"/>
    </label>
    <br/>
    <br/>

    <label>
        E-mail:
        <br/>
        <br/>
        <input type="text" name="e-mail"/>
    </label>
    <br/>
    <br/>

    <label>
        Idade:
        <br/>
        <input type="text" name="idade" />
    </label>
    <br/>
    <br/>

    <input type="submit" value="Enviar" />

</form>
```
--- 

- Para salvar informações na sessões antes do **header()** preenchemos com a variavel **$_SESSION** - ELA É UMA ARRAY.

**Logo após inserir $_SESSION['aviso'] = 'Preencha os itens corretamen!';** Dentro dela vai ir inserir oque quer salvar por exemplo ['aviso]

```
<?php
session_start();

$email = filter_input(INPUT_POST, 'e-mail', FILTER_VALIDATE_EMAIL);
$nome = filter_input(INPUT_POST, 'name', FILTER_SANITIZE_SPECIAL_CHARS);
$idade = filter_input(INPUT_POST, 'idade', FILTER_SANITIZE_NUMBER_INT);

if($nome && $email && $idade){
    echo "NOME: " .$nome;
    echo "<br/>";
    echo "IDADE: " .$idade;
    echo "<br/>";
    echo "EMAIL: " .$email;

}else {
   $_SESSION['aviso'] = 'Preencha os itens corretamente!'; ===========> UM VALOR NA SESSION
    
   header('Location: ./index.php'); ====> MANDOU PRO INDEX 
   exit;
}

```

- Logo após vou fazer uma condição que vai fazer uam verificação se está corrreto com **if**
**Forma literaria SE SESSION AVISO EXISTIR VOU MOSTRAR A SESSION**
no documento que vocÊ deseja usar.
- Umas das maneirar de retirar o aviso seria.

```
<?php
session_start();
require('header.php');


if($_SESSION['aviso]) { =========> SE EXITIR A SESSÃO 
    echo $_SESSION['aviso']; ======> MOSTRAR SESSION 
    $_SESSION['aviso'] = '';  ====> MANEIRA DE RETIRAR O AVISO
}

?>

<form method="POST" action="recebedor.php">

    <label>
        Nome:
        <br/>
        <br/>
        <input type="text" name="name"/>
    </label>
    <br/>
    <br/>

    <label>
        E-mail:
        <br/>
        <br/>
        <input type="text" name="e-mail"/>
    </label>
    <br/>
    <br/>

    <label>
        Idade:
        <br/>
        <input type="text" name="idade" />
    </label>
    <br/>
    <br/>

    <input type="submit" value="Enviar" />

</form>
```
---
## Cookies no PHP 

- Para setar um cookie inserimos **setcookie()**.

 1º Parâmetro é o nome do cookie.  
 exemplo: 'nome'

2º Parâmetro o valor que vai ficar salvo esse cookie. Também seria a informação que vou armazenar dentro dele.
Exemplo : $nome ======> nome do usario 

3º Parâmetro quando é que esse cookie expira. 
Exemplo: time(valor em milisegundos) + (86400 * 30)

- 86400 = 1 dia em milisegundos
```
<?php
session_start();

$email = filter_input(INPUT_POST, 'e-mail', FILTER_VALIDATE_EMAIL);
$nome = filter_input(INPUT_POST, 'name', FILTER_SANITIZE_SPECIAL_CHARS);
$idade = filter_input(INPUT_POST, 'idade', FILTER_SANITIZE_NUMBER_INT);

if($nome && $email && $idade){
    
    $expiracao = time() + (86400 * 30);
    setcookie('name', $nome, $expiracao);
    
    echo "NOME: " .$nome;
    echo "<br/>";
    echo "IDADE: " .$idade;
    echo "<br/>";
    echo "EMAIL: " .$email;

}else {
   $_SESSION['aviso'] = 'Preencha os itens corretamente!';
    
   header('Location: ./index.php');
   exit;
}
```
### Para chamar o cookie

- Nós inserimos a variavel numa condição **SE $_COOKIE['']{}** e dentro dos colchetes eu insiro oque eu quero 'nome'

- E junto nessa condição para não ocorrer um erro inserimos **isset()** que significa = está setado essa variavel **SE** TIVER **SETADO** ELE ENTRA **SE NÃO**   ELE NÃO DA ERRO.

```
No INDEX ou NO ARQUIVO que queremos nos chamamos o cookie 

<a href ="">Home</a>

</br>
<?php
    if(isset($_COOKIE['name'])){
        $nome = $_COOKIE['name'];
        echo '<h2>'.$nome.'</h2>';
    }
?>
```

### APAGAR O COOKIE 
- Para apagar um cookie eu posso setar ele vazio ou preenchido tenho que setar ele com um tempo no passado.

setcookie('nome', '', time() - 3600);


```
Inserir em um arquivo para apagar o cookie 

setcookie('nome', '', time() - 3600);

header("Location: index.php");
exit;
```

## DIFERENÇA entre SESSION e COOKIE
A SESSÃO funciona enquanto o navegador tiver aberto quando você fecha o navegador ela é destruida o COOKIE não ele tem uma validade especifica ele fica salvo no computador e conseguimos mesmo desligando o pc e ligando novamente ele ainda vai estar lá desde que ele esteja no processo de validade 


---

## Lendo arquivos 
file _get_content = Vai pegar
## Escrevendo em arquivos 
o **file_put_contents()** ele vai fazer 2 coisas, se o arquivo existir ele vai criar e se existir ele vai substituir o arquivo são 2 parâmetros.
1º -  É o nome do arquivo
2º - É o conteudo 
```
$texto = 'Bonieky Lacerda';

file_put_contents('nome.txt', $texto); 

echo 'Arquivo criado com sucesso';

```

## Excluindo arquivos

- Para excluir insira **unlink('");**

Pode ser uma imagem, mp3, video,texto.

```
unlink('texto.txt');
echo 'Arquivo excluido com sucesso.'
```

## Movendo o arquivo e Renomeando arquivo 

- Para renomear inserimos **rename()**.

- Ele recebe dois parâmetros 

1º é o caminho até o arquivo que quero renomear o arquivo original insiro o nome do arquivo que eu quero.

2º é o nome que eu quero.

```
rename('texto.txt, 'pasta/teste2.txt');
```

Para mover o arquivo para uma pasta eu coloco no 2º parametro um diretório 

### copy - Vai copiar o arquivo que seria o primeiro o diretório que encotra o meu arquivo e segundo a minha copia de destino.

--- 

## Upload de arquivos(1/2)

- enctype = elepossibilita o tipo como o formulario agrega o conteudo para fazer o envio desses dados, quando são simplesmente dados, não precisa inserir o enctype, por qie ele vai enviar com o metodo tradiconal **form method="POST" action="recebedor.php"**. Agora quando tem arquivos inserimos **enctype="multipart/form-data"**

```
<form method="POST" action="recebedor.php" enctype="multipart/form-data">
    <input type="file" name="arquivo" />
    <input type="submit" value="Enviar" />
</form>
```
- Logo após no arquivo que vai receber os dados  e fazer oque for solicitado. 

- Para mostrar na tela inseri **print_r( $_FILES )**.

```
recebedor 

echo '<pre>';
print_r( $_FILE );
```
### Oque irá ser mostrado nessa tarefa.

```
Array
(
    [arquivo] => Array
        (
            [name] => BOLETO_237462003.pdf
            [full_path] => BOLETO_237462003.pdf
            [type] => application/pdf ----------------> Para inseri a maneira correta. Exemplo: Image eoutros tipos 
            [tmp_name] => C:\xampp\tmp\php142C.tmp
            [error] => 0
            [size] => 229262
        )

)
```
- Dependendo da configuração o arquivo pode ser deletado.

- Quando ele passa pela requisição/recebedor e é aceito o arquivo, faço um comando para ele ficar no meu sistema ou em outro lugar. ai inserimos uma função **move_upload_file()**. Essa função recebe dois parâmetros.

1º - é onde está o arquivo na pasta temporaria, a array;
```
                        // Arquivo é o item do array
move_uploaded_file($_FILE['arquivo])
```
 - Onde o arquivo se encontra temporario 
```
move_uploaded_file($_FILE['arquivo']['tmp_name'] )
```

2º - Aonde quero que o arquivo fique;

- Para inserir um nome que ja está la inseri uma variavel e pego as informações da array ['arquivo']['name'] e logo após concatena com a variavel.
```
$nome = $_FILE['arquivo'],['name'];
move_uploaded_file( $_FILE ['arquivo'] ['tmp_name'] , 'arquivos/'.$nome)
```

## Upload de arquivos(2/2)

Para deixar o arquivos unicos, precisamos de um hash para deixa-lo unico. 
Ao inves de pegar o nome colocamos a funções para deixar unico.

Essa função tem dois parâmetros:

- 1º O local que se encontra os arquivos  nesse caso 
**move-uploaded_file($_FILES['arquivo']['tmp_name'], 'diretório onde quero que fique/'** . **e o nome do arquivo ou deixar o nome que está no arquivo)** 

['arquivo'] = seria o item do array que se encontra

['tmp_name'] = a pasta temporaria do arquivo


```
echo '<prev>';
print_r($_FILES);

$nome = md5(time().rand(0, 1000));
move_uploaded_file($_FILES['arquivo']['tmp_name], 'arquivos/'.$nome);
```

- md5: É um hash.

- Exemplo para fazer um formulario e precisa de só imagens, como fazer? 

- Primeiro de tudo vou conferir se o type desse arquivo dentro da lista de type's que eu quero. Então usaria a função **in_array**

```
<?php 

echo '<prev>';
print_r($_FILES);

//Vai fazer uma verificação de arquivos que vão aceitar e depois na variavel $nome
//deixa-lo o arquivo unico.
//Junto com isso armazenar o local dos arquivos 'jow' com os arquivos temporarios 'tmp_name'.

if(in_array($_FILES['jow']['type'], array('iamge/jpeg','image/jpg', 'image/png'))){
    $nome = md5(time().rand(0,1000)).'.jpg';
    move_uploaded_file($_FILES['jow']['tmp_name'], 'arquivos/'.$nome);
}else {
    echo 'Arquivo não permitido!'
}
```

--- 

## Array Range

Função range podemos criar uma array já com valor dentro desse array.

- $variavel = range();

Função range tem dois parâmetros: 

1º - Eu insiro o item que vai começar.

2º - É o item que vai terminar.

E tem um 3º parâmetro.

O multiplicador ou a quantidade de item que vai pular.

```
$array = range('a', 'g');

 foreach($array as $item) {
     echo $item."<br/>";
 }
```
## Key_exists

Para evitar que aconteça o erro inesperado.

A função key_exists. Tem dois parâmetros:

- 1º - Oque você está procurando a chave chamada **nome da chave**.

- 2º E onde está procurando.

```
$array = [ 
    'nome' => 'Johnny',
    'idade' => '25',
    'empresa' =>'Comp',
    'cor' => 'Vermelho'
];

if(key_exists('idade', $array))
$idade = $array['idade'];
echo $idade;
```

