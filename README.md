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

---

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


## array_keys e array_values 

array_keys

Ele ira mostrar as chaves do codigo 

$varivel = array_keys($array);

```
$array = [ 
    'nome' => 'Johnny',
    'idade' => '25',
    'empresa' =>'Comp',
    'cor' => 'Vermelho'
];

$chaves = array_keys($array);
```

array_values 

Ele ira mostrar os valores do codigo

$varivel = array_values($array);

```
$array = [ 
    'nome' => 'Johnny',
    'idade' => '25',
    'empresa' =>'Comp',
    'cor' => 'Vermelho'
];

$valores = array_values($array);
```

## Array_slice

- Array slice serve para cortar a array no meio ou onde quer que eu use.

- Ele não vai alterar o array original, ele vai criar um novo array com essa copia da array que eu quero pegar.

 Ele tem parâmetros :

- 1º - Vai inserir o array que eu quero fazer modificação 

- 2º - Por onder quer que comece esse corte. EXEMPLO: 
Quero que comece na posição 0 do array.

- 3º - É quantos itens que eu quero pegar. EXEMPLO = ['a', 'b']

```
<?php

$array = ['a','b','c','d','e','f'];

$retorno = array_slice($array, 0, 2);
print_r($retorno); =========> ver o resultado
```

com o  '-' voltamos a array 

## array_reduce 

O array_reduce tem 2 parâmetros:

- 1º Parâmetro eu mando a varivel solicitada.

- 2º Parâmetro vou mandar um nome de uma função para executar então crio uma função. 

Na prate reduce então criamos uma função com essa função inserimos 2 parâmetros

O $subtotal ele vem com = 0
```
$numero = [1, 2, 3, 4, 5];

function somar($subtotal, $item){
    $subtotal = $subtotal + $item;
    retutn $subtotal
}

$total = array_reduce($numero, 'somar');
```

NESSE EXEPLOC USAMOS ISSO:

Para contar o numero de sexo masculino fazemos uma condição

a função inserimos uma conta com o nome 'contar_m'
"SE O ITEM SEXO IGUAL A 'M' ENTÃO VAI AUMENTAR ++"
"SE É UM HOMEM  SUBTTOTAL VAI AUMENTAR UM"
```
<?php

$pessoas = [
    ['nome' => 'Fulano', 'sexo' => 'M', 'nota' => 9],
    ['nome' => 'Ciclano', 'sexo' => 'M', 'nota' => 7],
    ['nome' => 'Beltrano', 'sexo' => 'F', 'nota' => 10],
    ['nome' => 'Paulo', 'sexo' => 'M', 'nota' => 8],
    ['nome' => 'Cintia', 'sexo' => 'F', 'nota' => 9],
    ['nome' => 'Jessica', 'sexo' => 'F', 'nota' => 9]
];

function contar_m($subtotal, $item){
    if($item['sexo'] === 'M') {
        $subtotal++;
    } 
    return $subtotal;  
}

$total_m = array_reduce($pessoas, 'contar_m');

echo "Total de homens: ".$total

```

```
$pessoas = [
    ['nome' => 'Fulano', 'sexo' => 'M', 'nota' => 9],
    ['nome' => 'Ciclano', 'sexo' => 'M', 'nota' => 7],
    ['nome' => 'Beltrano', 'sexo' => 'F', 'nota' => 10],
    ['nome' => 'Paulo', 'sexo' => 'M', 'nota' => 8],
    ['nome' => 'Cintia', 'sexo' => 'F', 'nota' => 9],
    ['nome' => 'Jessica', 'sexo' => 'F', 'nota' => 9]
];

// Total de homens 
function contar_m($subtotal, $item){
    if($item['sexo'] === 'M') {
        $subtotal++;
    } 
    return $subtotal;  
}

$total_m = array_reduce($pessoas, 'contar_m');

// Soma das notas dos homens 

function soma_m($subtotal, $item){
    if($item['sexo'] === 'M'){
        $subtotal += $item['nota'];
    }
    return $subtotal;
}

$soma_m = array_reduce($pessoas, 'soma_m');

//media dos homens
$media_m = $soma_m / $total_m;

echo "Total de Homens: ".$total_m;"<br>";
echo "Soma das notas dos homens: ".$soma_m;"<br>";
echo "Media dos homens: ".$media_m."<br>"; 
```

---

## Descontruindo usando list 

Para descontruir uma array inserimos a função list($nome, $idade, $bebida, $cor) = $array;

- Ele vai pegar a array $array o primeiro item variavel nome, segundo item na variavel idade, terceiro item bebida, quarto item cor;

```
$array = ['Johnny', 90, 'cafe', 'azul'];

list($nome, $idade, $bebida, $cor) = $array;

echo $nome." tem ".$idade." anos e gosta de tomar ".$bebida. " com a cor".$cor; 
```


# Orientação a objetos

## Introdução

## Definindo Classes e Objetos 

- Uma CLASSE eu vou definir a propriedades daquele objeto.

Criando uma classe supor: Vamos criar uma CLASSES que vai ficar responsavel pelos posts, essa classe tem que saber quantos likes quantos comentarios e quais comentarios o post tem o tipo se é uma foto ou video e texto. 

Junto com isso as funções especificas supor no botão da mãozinha ele vai por o like, então ele vai aumentar a quantidade de likes naqueles posts.

o ato de só criar a clesse não executa ela ele tem uma ideia de posts criado.

A CLASSE é um modelo do veiculo. A classe é estatica. É a estrutura para a formação de objetos.

O OBJETO é dinâmico porque você efetua ações com ele atraés dos métodos estruturados na classe. Umas definição de objeto é a instacia de classe. Como na analogia podemos dizer que é você que da a vida a CLASSE. Porque classe sem instaciar objeto não sera utilizado.

```
class Post {
    public $likes = 0;     |
    public $coments = [];  |=====>CLASSE CRIADA
    public $author;        |
}
```

Agora criamos nosso objeto para criar um objeto usamos um comando **new** e depois associo esse objeto a uma variavel.
Falamos instaciar 

```
$post1 = new Post();
```
Agora definimos as propriedades usamos a -> para definir.

```
$post1 = new Post();
$post1 ->likes = 3;
```
```
$post2 = new Post();
$post2->$likes = 10;
```

## Propriedades tipadas ou Definindo Métodos e Propriedades

Propriedades é a classe são basicamente as caracteristicas que uma classe vai ter e por consequêcias o objeto tambem vai ter.

Exemplo criamos uma propriedade:
- Public=Publica  = Posso alterar informações eu posso acessar de fora.
- Protegidas=Protected=Ela não são acessiveis no lado de fora. Similar ao PRIVATE mas com algumas coisas diferentes 
- Privadas=Private=Ela não são acessiveis no lado de fora. Se for usar ela internamente no sistema com alguma propriedade interna. Usamos a propriedade privada quando você não quer dar  acesso aquela propriedade no mundo esterno 

### Agora vamos falar sobre metodos

O objeto tem caracteristicas e pode executar funções, tarefas ou atraves do proprio obejto.
Por exemplo vamos pegar um metodo especifico para aumentar a quantidade de likes:

- Inserimos o metodo na classe pois na classe que arquitetamos. 
- Inserimos uma função mas ela só vai ser utilizada na classe com o nome ¨aumentarLike¨.

- Para acessar a propriedade $likes, inseri ¨$this¨ significa ISTO uma ocisa que está proxima

- Para utilizar o methodo utilizamos a $variavel junto.

```
<?php

class Post {
    public $likes = 0;
    public $coments = [];
    public $author;

    public function aumentarLike() {
        $this->likes++;
    }
}

$post1 = new Post();
$post1->aumentarLike();

$post2 = new Post();
$post2->aumentarLike();

echo "Quantidade de likes Post 1: ".$post1->likes."<br/>";
echo "Quantidade de likes Post 2: ".$post2->likes."<br/>";
```


## Método Contrutor 

Uma classe vem com possibilidade de você ter uns metodos especificos para rodar automaticamente.

o metodo construtor seria, metodo __construct ele é um metodo que sempre quando você cria ele executa toda vez que cria um objeto novo.

Pra que serve o constutor __construct sempre quando precisar executar alguma coisa, no momento que o objeto é criado você usa o construtor 

```
<?php

class Post {
    public int $id;
    public int $likes = 0;
    public array $comments = [];
    public string $author;

    public function __construct($postId)
    {
        $this->id = $postId;
        // Consultar o bando de dados para pegar as informações do post $ID
        $this->likes =12;
    }

    public function aumentarLike()
    {
        echo 'abc';
        $this->likes++;
    }
}

$post1 = new Post( 25 );

$post2 = new Post(60);

echo "Post 1: ".$post1->likes."<br/>";
echo "Post 2: ".$post2->likes."<br/>";

```


## Encapsulamento 

-
-

```
class Post {
    public int $id;
    public int $likes = 0;
    public array $comments = [];
    public string $author;

    public function aumentarLike()
    {
        $this->likes++;
    }

    public function setAuthor($n){
        $this->author = $n;
        
    }

    public function getAuthor(){
        return $this->author;
    }
}

$post1 = new Post();
$post1->setAuthor('Johnny');

$post2 = new Post();
$post2->setAuthor('Fulano');

echo "Post 1: ".$post1->likes."likes - ".$post2->getAuthor()."<br/>";
echo "Post 2: ".$post2->likes."likes - ".$post2->getAuthor()."<br/>";

```

---
```
class Login {
    private $email;
    private $senha;

    public function getEmail(){
        return $this->email;
    }
    public function setEmail($e){
        $this->email = $e;
    }

    public function getSenha(){
        return $this->senha;
    }

    public function setSenha($s){
        $this->senha = $s;
    }

    public function logar(){
        if($this->email == "teste@teste.com" and $this->senha == "123456"):
            echo "Logado com sucesso!";
        else:
            echo "Dados invalidos";
        endif;
    }
}

$entrar = new Login;
$entrar->setEmail("teste@teste.com");
$entrar->setSenha("123456");
$entrar->logar();
echo "<br/>"; 
echo $entrar->getEmail();
```

## Método Estático 

É um metodo dentro da classe "Ele é independente" ou seja ele pode ser usado unicamente externamente.

- Para utilizar o metodo estático inserimos o **static**

Nós inserimos os   **: :**  para chamar-lo dentro da classe metodo estatico sem precisar instaciar o objeto.


## Entendendo Herança  

-
-
O exmplo embaixo é para ver o HERANÇA:
- Crio uma nova classe com o nome Foto, essa classe foto vai extender a classe Post.
- Dentro da classe Foto vai usar tudo que está na classse Post

```
class Post {
    private int $id;
    private int $likes = 0;

    public function setId($i){
        $this->id=$i;
    }
    public function getId(){
        return $this->id;
    }
    public function setLikes($li){
        $this->likes=$li;
    }
    public function getLikes(){
        return $this->likes;
    }
}

class Foto extends Post{
    private $url;

    public function __construct($id){
        $this->setId($id);
    }
    public function setUrl($u){
        $this->url=$u;
    }
    public function getUrl(){
        return $this->url;
    }
}

$foto = new Foto(20);
$foto->setLikes(12);
$foto->setUrl('abc');
echo "FOTO:".$foto->getID()."-".$foto->getLikes()." likes - ".$foto->getUrl();
```

<<<<<<< HEAD
## Entendendo Interfaces

Crio um guia para as minhas classes que vão utilizar esse guia **interace** ao inves de inserir chaves **{}**, nós inserimos o ;n interface.

Para implementar a interfaces **Database**.

```
<?php
interface Database{
   public function listaProdutos();

   public function adcionarProdutos();

   public function alterarProduto();
}

class MySqlDB implements Database{

   public function listaProdutos(){

   }
   public function adcionarProdutos(){
      echo "Adicionando com MySQL";
   }
   public function alterarProduto(){

   }

}

class OracleDB implements Database{
   public function listaProdutos(){

   }
   public function adcionarProdutos(){
      echo "Adicionando com Oracle";
   }
   public function alterarProduto(){

   }

}


$db = new MySqlDB();
$db->adcionarProdutos();


```

## Entendendo Polimorfismo

É simplesmente reescrever um metodo herdado, reescrevo o metodo andar
Em outras palavras Polimorfimos é substituir ou reecrever um metodo herdado da classe pai que é a classe Animal

```
class Animal{
    public function andar(){
        echo "O animal andou";
   }
}
class Cavalo extends Animal{
    public function andar(){
        echo "O cavalo andou";
   }
} 
$animal = new Cavalo();
$animeal->andar();
```

---

```
<?php
interface Forma {
   public function getTipo();
   public function getArea();
}

class Quadrado implements Forma{
   private $largura;
   private $altura;
   
   public function __construct($l,$a){
      $this->largura = $l;
      $this->altura = $a;
   }
   public function getTipo(){
      return "quadrado";
   }
   public function getArea(){
      return $this->largura * $this->altura;
   }
}

class Circulo implements Forma{
    private $raio;


   public function __construct($r){
      $this->raio = $r;  
   }
   public function getTipo(){
      return 'circulo';
   }
   public function getArea(){
      return pi()*($this->raio * $this->raio);
   }
}

$quadrado=new Quadrado(5,5);

$circulo=new Circulo(7); 

$objetos = [
   $quadrado,
   $circulo
];

foreach($objetos as $objeto){
   $tipo=$objeto->getTipo();
   $area=$objeto->getArea();
   echo "AREA: ".$tipo." : ".$area."<br/>";
}
```

```

```
=======
## Propriedade Private e Protected

A propriedade PRIVADA só pode ser acessada na classe mãe, ela só pode ser alterada pela classe que criou.
>>>>>>> d8ef86b93d86cdb8aca1c4acc293452dc06d415b


## Polimorfismo 
-
-
``` 
<?php

interface Forma {
   public function getTipo();
   public function getArea();
}

class Quadrado implements Forma{
   private $largura;
   private $altura;

   public function __construct($l,$a){
      $this->largura=$l;
      $this->altura=$a;
   }
   public function getTipo(){
      return 'quadrado';
   }
   public function getArea(){
      return $this->largura * $this->altura;
   }
}

class Circulo implements Forma{
   private $raio;
   
   public function __construct($r){
      $this->raio=$r;
   }
   public function getTipo(){
      return 'circulo';
   }
   public function getArea(){
      return pi() * ($this->raio * $this->raio);
   }
}

$quadrado = new Quadrado(5,5);
$circulo = new Circulo(7);

$objetos = [
   $quadrado,
   $circulo
];

foreach($objetos as $objeto){
   $tipo=$objeto->getTipo();
   $area=$objeto->getArea();
   echo "AREA: ".$tipo." : ".$area."<br/>";
}
```
--- 
## Namespace

Ele foi criado como uma forma de você encapsular classes, constante, enfim, dentro de um grupo para que você consiga usar classes com o memso nome dentro da mesma aplicação.

- É meio que cirar varias caixinhas e que eu consigo ter varias classes com o mesmo nome.

- Nós inserimos um **namespace** nos arquivos classes1.php e classes2.php.

```
<?php 

            // Arquivo classes1.php
namespace classes1;

class MinhaClasse {
    public function testar(){
        return 'Testando classe 1';
    }
    
}
```

```
<?php
        // Arquivo classes2.php
namespace classes2;

class MinhaClasse {
    public function testar(){
        return 'Testando classe 2';
    }
    
}
```

- Para usar essas classes no index.php crio

```
require 'classes1.php';
require 'classes2.php';

        // Insiro o nome da classe
$a = new classes1/MinhaClasse();
echo $a->testar();
```

- Para usar a classes Basic insiro...

```
    
require 'classes/matematica/basic.php';

    // O **as** significa como se fosse.
    //Ele tem que ser do mesmo nome que eu instaciei no objeto. Se fosse **as Dev**
    teria que instaciar com **new Dev**.

use classes\matematica\Basic as Basic;

$basico = new Basic();
```

## Injeção de Dependência

Ele inseri uma classe dentro de outra normalmente no construtor mas não necessariamente.

- Vou instanciar a classe que eu quero usar como no processo Basico

- Basicamente é inserir um objeto que eu quero de fora para dentro da minha classe 

```
class Basico1{
   public function somar($x,$y){
      return $x + $y;
   }
}

class Basico2 {
   public function somar($x,$y){
      $res = $x;
      for($q=0;$q<$y;$q++) {
         $res++;
      }
      return $res;
   }
}

class Matematica {
   private $basico;
   
   public function __construct($b) {
      $this->basico = $b;
   }
   public function somar($x,$y){
      return $this->basico->somar($x, $y);
   }

}

        //Inserir um objeto que eu quero de fora para dentro da classe

$basico = new Basico1();
$mat = new Matematica($basico); // Posso instanciar dentro dos parenteses (new Basic1)
echo $mat->somar(10,10);
```
## Autoload

Para fazer um auload nós usamos uma função chamada **spl_autoload_register**. Eu vou registrar um autoload.

- Crio uma outra função anonima e insiro pra dentro da **spl_autoload_register(function(){})** ele tem um parâmetro que vai ser chamado o nome que você inserir. **spl_autoload_register(function($class){});**.

- Para verificar se o arquivo existe fazemos uma validação...
```
<?php

spl_autoload_register(function($class){
      
      //Vai fazer uma verificação se o arquivo existe
   if(file_exists('classes/'.$class.'.php')){
    require 'classes/'.$class.'.php';
   }
});

$m = new Matematica();
echo $m->somar(10,20);
```

### Procedimento para o autoload __DIR__ vai inserir essa variavel global dir que vai pegar o proprio diretório do arquivo que estou que no caso é a raiz do projeto no final insiro a pasta com uma / no final. Exemplo:

**$baseDir=__DIR__.'/classes/';**

- Para trocar a barra \ para essa / inserimos na mesma função.
## No PHP a barra assim \ seguido de aspas '\' como fosse literalizando a propria aspa então inserimos '\\' para formar uma barra só

```
//Meu index.php

<?php

require 'autoload.php';

use \matematica\Basica;

$m = new matematica\Basica();
echo $m->somar(10,20);
```
### Autoload.php
```
// autoload.php
<?php

spl_autoload_register(function($class){
  $baseDir = __DIR__.'/classes/';
  
  $file = $baseDir.str_replace('\\', '/', $class).'.php';

  if(file_exists($file)) {
      require $file;
  }
});
```
### classes/fotos
upload.php

CRIO ESSAS PASTA NO DIRETÓRIO RAIZ;
### classes/matematica
Basica.php

```
// foto/Upload.php
<?php 
namespace foto;

class Upload {

}
```

```
// matematica/Basica.php
<?php 
namespace matematica;

class Basica{
    public function somar($x, $y){
        return $x + $y; 
    }
}
```


## Conectando ao banco de dados com PDO 

Para conectar no banco inserimos o código:

1º - Tipo de banco que vai ser usado. Exemplo: **mysql:**

2º - Ao nome do banco de dados que estou utilizando. Exemplo: **:dbname=test;**

3º - Aonde ele está funcionando **host=localhost**

Em um outro parâmetro inserimos os seguinte.

1º - Que vai fazer o user "root",""


```
$variavel = new PDO("mysql:dbname = test;host=localhost", "root","")
```

Para acessar o banco direto do codigo digitamos acessamos:
```
$variavel = new PDO("mysql:dbname = test;host=localhost", "root","")

$sql = $variavel->query('SELECT * FROM usuarios');


            //Fetch = Pegar os dados pra mim. ALL=Todos
$dados = $sql->fetchAll(); =======> Para inserir uma associação digitamos 
        $sql->fetchAll(PDO::FETCH_ASSOC)
 
```


