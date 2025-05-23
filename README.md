# Introdução ao PHP - SENAC - Registro/SP

## Aula 01

```php
<?php

$nomeJogo = "Aventura PHP";
$nomeJogador = "Haimon";

//Primeiro progarama PHP

echo "<h1>Bem-vindo(a), $nomeJogador ao Mundo dos Games!</h1>";
echo "<p>Iniciando nossa Jornada na Lógica de Programação em PHP</p>";
echo "<h2>Jogo: $nomeJogo</h2><hr>";

//Características de um personagem
$nomePersonagem = 'Hobhertos';
$nivel = 1;
$classe = 'Desenvolvedor';
$vidaMaxima = 100;
$vidaAtual = $vidaMaxima;
$manaMaxima = 50;
$manaAtual = $manaMaxima;
$forca = 2;
$inteligencia = 10;
$destreza = 5;
//Atributos derivados
$poderAtaque = $forca * 2;
$poderMagico = $inteligencia * 3;
$velocidade = $destreza * 1.5;

//Exibindo ficha tecnica
echo "<h2>Ficha Técnica do Personagem</h2>
	<div style='border: 1px solid #ccc; border-radius: 8px; padding: 1rem; width: 300px;'>
    	<h3>$nomePersonagem</h3>
        <p><strong>Classe:</strong> $classe</p>
        <p><strong>Nível:</strong> $nivel</p>
        <p><strong>Vida:</strong> $vidaAtual</p>
        <p><strong>Mana:</strong> $manaAtual</p>
        <hr>
        <p><strong>Força:</strong> $forca</p>
        <p><strong>Inteligência:</strong> $inteligencia</p>
        <p><strong>Destreza:</strong> $destreza</p>
        <hr>
        <p><strong>Poder de Ataque:</strong> $poderAtaque</p>
        <p><strong>Poder Mágico:</strong> $poderMagico</p>
        <p><strong>Velocidade:</strong> $velocidade</p>
    </div>
";


//Simular ataque
$danoCausado = $poderMagico;
$vidaInimigo = 100;
$vidaInimigoRestante = $vidaInimigo - $danoCausado;

echo "<h2>Resultado de Combate</h2>
	  <p>$nomePersonagem atacou e causou $danoCausado de dano!</p>
      <p>Vida do inimigo: $vidaInimigoRestante/100</p>
";

?>

```

## Aula 02

### Criação do projeto
- Criar uma pasta dentro de \xamppz\htdocs\pasta_projeto.

## Aprendendo a inserir o PHP no código HTML

`Arquivo 'index.php'`

```php
<!-- Sempre criar a sintaxe php -->
<?php

$salario = 3000;
$aluguel = 1200;
$contas = 600;
$mes = 'Maio';
$saldo = $salario - ($aluguel + $contas);

?>

<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aula 02 - Introdução ao PHP</title>
    <style>
        body{
            font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
            background: #f4f4f4;
            padding: 1.1rem;
        }
        .caixa{
            background: #fff;
            padding: 1.1rem;
            border-radius: 8px;
        }
    </style>
</head>
<body>
    
        <div class="caixa">
            <h1>Resumo Financeiro de <?= $mes?></h1>
            <p><strong>Salário:</strong> R$ <?php echo $salario;?></p>
            <p><strong>Aluguel:</strong> R$ <?php echo $aluguel;?></p>   
            <p><strong>Contas:</strong> R$ <?php echo $contas;?></p>   
            <p><strong>Saldo:</strong> R$ <?php echo $saldo;?></p>
        </div>

</body>
</html>

```

`Arquivo 'operadores.php'`

```php
<?php
//Operadores Relacionais


$a = 10;
$b = 20;
$c = 10;

// echo $a == $c. "\n";
// echo $a != $c. "\n";
// echo $a > $b. "\n";
// echo $a < $b;

echo "<h2>Variáveis</h2>";
echo "
    a = $a<br>
    b = $b<br>
    c = $c<br>
    <br>
";

echo "<h2>Operadores Relacionais</h2>";
echo '
== Comparação<br>
!= Diferente<br>
> Maior que<br>
>= Maior igual que<br>
< Menor que<br>
<= Menor igual que<br><br>
';
echo "a == c: ";
var_dump($a == $c);
echo "<br>";

echo "a > b: ";
var_dump($a > $b);
echo "<br>";

echo "a < c: ";
var_dump($a < $c);
echo "<br>";

echo "a != c: ";
var_dump($a != $c);
echo "<br>";

echo "a <=  b: ";
var_dump($a <= $b);
echo "<br>";

echo "a >= b: ";
var_dump($a >= $b);
echo "<br>";

//Condicionais simples e composta
echo "<h2>Condicionais Simples e Compostas</h2>";
$idade = 17;

echo "Idade: $idade<br>";

if($idade >= 18){
    echo 'Você é maior de idade<br>';
}else{
    echo 'Você é menor de idade<br>';
}

//Composta

$clima = 'sol';

if($clima == 'chuva'){
    echo 'Seria tao bom ficar em casa com essa chuva :(. Mas vá la e pegue seu guarda-chuvas';
}else if($clima == 'sol'){
    echo 'Tempo bom pra pegar o protetor solar e ir para a praia!';
}else{
    echo 'O clima ta bom pra ficar em casa e lavar a roupa.';
}

?>
```

## Exercícios - Operadores

`Arquivo 'media.php'`

```php
<?php

// abaixo de 5 reprovado
// abaixo de 6 exame
// maior igual a 6 aprovado

$nota1 = 4;
$nota2 = 5;
$nota3 = 5;
$media = ($nota1 + $nota2 + $nota3) / 3;

if($media < 5){
    echo "<strong>Reprovado.<br></strong>";
}else if($media < 6){
    echo '<strong>Exame.<br></strong>';
}else{
    echo '<strong>Aprovado.<br></strong>';
}

echo "Sua média: $media";

?>

```

`Arquivo 'conversor.php'`

```php

<?php
//Ler o valor em real e converter para dolar
$valor = 1;
$valorDolar = 5.60;
//Usando o 'number_format' passamos como parametro
//valor, quantidade de casas decimais, separador decimal, separador de milhar
$valorFinal = number_format($valor / $valorDolar, 2, ',', '.');


echo "Real para Dólar: U$ $valorFinal<br>";
$valorFinal = number_format($valorDolar * $valor, 2, ',', '.');
echo "Dólar para Real: R$ $valorFinal";

// '.' é usado para concatenar no php

echo '<br>Exemplo de '. 'concatenacao';

?>
```

```html

<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        body{
            background: black;
            color: #fff;
            font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
        }
    </style>
</head>
<body>

    

</body>
</html>


?>

```

## Aula 03

Nesta aula começamos a aprender a utilizar arrays, fazer depuração com 'var_dump()' e criar arrays dentro de array

```php

<?php

//Variaveis do tipo Array
$carros = ['Civic G10', 'Amarok', 'Tiggo 7 Pro'];

//O 'count' le o tamanho do array
// for($i = 0; $i < count($compras); $i++){
//     echo $compras[$i]. "<br>";
// }

//O 'var_dump' vai trazer informações para depuração como o tipo e a quantidade de elementos
var_dump($carros);

//Em vez de posições usando os numeros, é utilizado o apelido para aquela posição
$carro = [
    "modelo" => "Civic G10",
    "cor" => "Cinza",
    "marca" => "Honda",
    "ano" => 2025
];

var_dump($carro);

$estoque = [
    ["modelo" => "Civic G10", "cor" => "Cinza", "marca" => "Honda", "ano" => 2025, "foto" => "civic.png"],
    ["modelo" => "Amarok", "cor" => "Branco", "marca" => "Volkswagen", "ano" => 2019, "foto" => "amarok.png"],
    ["modelo" => "Tiggo 7 Pro", "cor" => "Branco", "marca" => "Caoacherry", "ano" => 2024, "foto" => "tiggo.jpg"]
];
echo '<br><br><br>';
var_dump($estoque);

echo '<br><br><br>';

//Dizendo para o 'estoque' que cada Array nele se chama 'item'
foreach($estoque as $item){
    echo "<strong>Modelo: </strong>".$item['modelo']. " - <strong>Cor: </strong>".
    $item['cor']. " - " . "<strong>Marca: </strong>". $item['marca']. " - " . "<strong>Ano: </strong>". $item['ano'] . " - " . "<strong>Foto: </strong>" .
     "<img src='".$item['foto']."'>" . "<br>";
}

?>
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aula 03</title>
    <style>
        body{
            background: black;
            color: white;
        }
        img{
            width: 400px;
        }
    </style>
</head>
<body>

    
</body>
</html>

```

## Exercícios

`Arquivo 'cadastro.php'`

```php
<?php
// nome, sobrenome, email e foto
// deve conter 5 clientes
$cliente = ["nome" => "Haimon", "sobrenome" => "Vieira", "email" => "haimon@mail.com", "foto" => "https://placehold.co/400"];

$clientes = [
    ["nome" => "Haimon", "sobrenome" => "Vieira", "email" => "haimon@mail.com", "foto" => "https://placehold.co/400"],
    ["nome" => "Roverto", "sobrenome" => "Larguei", "email" => "robs@mail.com", "foto" => "https://placehold.co/400"],
    ["nome" => "Vanvan", "sobrenome" => "Vonar", "email" => "vonar@mail.com", "foto" => "https://placehold.co/400"],
    ["nome" => "Leop", "sobrenome" => "Old", "email" => "leopold@mail.com", "foto" => "https://placehold.co/400"],
    ["nome" => "Niao", "sobrenome" => "Mi", "email" => "niaomi@mail.com", "foto" => "https://placehold.co/400"],
];

var_dump($clientes);

echo '<br>';

foreach($clientes as $item){
    echo "<strong>Nome: </strong>".$item['nome']. " - <strong>Sobrenome: </strong>".
    $item['sobrenome']. " - " . "<strong>E-mail: </strong>". $item['email']. " - " . "<strong>Foto: </strong>" . "<img src='".$item['foto']."'>" . "<br>";
}

?>


```

## Fazendo formulário

Arquivo `index.php`

```php

<?php

if(isset($_GET['msg']) && $_GET['msg'] == 'ok'){
    echo "<h2>Dados enviados com sucesso!</h2>";
}

?>

```

```html

<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Formulário</title>
    <style>
        body{
            padding: 0 2rem;
            font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
            font-size: 1rem;
        }
        input{
            all: unset;
            border: 1px solid #000;
            padding: .5rem;
        }
        input:focus{
            border: 2px solid black;
        }
        label{
            display: block;
            font-weight: 500;
            margin-top: 20px;
        }
        input[type="submit"]{
            display: block;
            margin-top: 20px;
            font-weight: 600;
            padding: .5rem 1rem;
            margin: 0 auto;
        }
    </style>
</head>
<body>

    <h1>Dados para Contato</h1>
    <!-- 'action' para onde vai as informacoes do formulario -->
    <!-- GET envia pela URL e o posto a informação é encapsulada -->
    <form action="recebimento.php" method="post">
        <label for="nome">Nome</label>
        <input type="text" name="nome" id="nome">
        <label for="email">E-mail</label>
        <input type="email" name="email" id="email">
        <label for="telefone">Telefone</label>
        <input type="tel" name="telefone" id="telefone">
        <input type="submit" value="Enviar">
    </form>
    
</body>
</html>

```

Arquivo `recebimento.php`

```php

<?php
//Aqui é tratado os dados que o formulário envia para o servidor

$nome = $_POST['nome'];
$email = $_POST['email'];
$telefone = $_POST['telefone'];

//Depois é enviado para o html e mostrar as informacoes

?>

```

```html

<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Recebimento</title>
    <style>
        body{
            font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
            font-size: 1rem;
            padding: 0 2rem;
        }
        a{
            text-decoration: none;
            border: 1px solid black;
            padding: .5rem;
            
        }
    </style>
</head>
<body>
    <h1>Recebimento do Formulário</h1>
    <hr>
    <p><strong>Nome: </strong><?= $nome?></p>
    <p><strong>E-mail: </strong><?= $email?></p>
    <p><strong>Telefone: </strong><?= $telefone?></p>
    <hr><br>
    <a href="index.php?msg=ok">Voltar</a>


</body>
</html>

```

# Exercício

Fazer um currículo

Arquivo `index.php`

```html

<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Currículo</title>
    <style>
        body{
            padding: 5rem;
            font-size: 1rem;
            font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
        }
        form{
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            border: 1px solid #000;
            padding: 2rem;
        }
        label{
            font-weight: 600;
            display: block;
            margin-bottom: 5px;
        }
        input{
            all:unset;
            border: 1px solid #000;
            padding: .5rem;
            margin-bottom: 10px;
        }
        input:focus{
            border: 2px solid #000;
        }
        .box:nth-child(1){
            grid-column: span 2;
        }
        textarea{
            font-size: 1rem;
            padding: .5rem;
            resize: none;
            width: 100%;
            height: 250px;
            grid-column: span 2;
        }
        input[type="submit"]{
            text-align: center;
            width: 100%;
            background: rgba(0, 0, 0, .5);
            color: white;
            font-weight: 600;
            grid-column: span 2;
        }
        .box:nth-child(5){
            grid-column: span 2;
        }
    </style>
</head>
<body>
    <h1 style="text-align: center;">Seu Currículo</h1>

    <form action="receber.php" method="post">

        <div class="box">
            <img src="https://placehold.co/200?text=Foto&font=roboto" alt="">
        </div>

        <div class="box">
            <label for="nomeCompleto">Nome completo</label>
            <input type="text" name="nome-completo" id="nomeCompleto">
        </div>

        <div class="box">
            <label for="telefone">Telefone</label>
            <input type="tel" name="telefone" id="telefone">
        </div>

        <div class="box">
            <label for="endereco">Endereço</label>
            <input type="text" name="endereco" id="endereco">
        </div>

        <div class="box">
            <label for="habilidade">Habilidades</label>
            <textarea name="habilidade" id="habilidade"></textarea>
        </div>

        <input type="submit" name="enviar" id="enviar" value="Enviar">

        
    </form>

</body>
</html>

```

Arquivo `receber.php`

```php

<?php

$nome = $_POST['nome-completo'];
$endereco = $_POST['endereco'];
$telefone = $_POST['telefone'];
$habilidades = $_POST['habilidade'];

?>

```

```html

<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Seu Currículo</title>
    <style>
        body{
            font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
            padding: 5rem;
            font-size: 1rem;
        }
        img{
            grid-column: span 2;
        }
        .box{
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            border: 1px solid #000;
            padding: 2rem;
        }
    </style>
</head>
<body>

    <div class="box">

        <img src="https://placehold.co/200?text=Foto&font=roboto" alt="">
        <p><strong>Nome: </strong> <?= $nome?></p>
        <p><strong>Telefone: </strong><?= $telefone?></p>
        <p><strong>Endereço: </strong><?= $endereco?></p>
        <p><strong>Habilidades: </strong><?= $habilidades?></p>

    </div>

    
    
</body>
</html>

```


## Aula 04

Nesta aula aprendemos a fazer formulario usando select, option, checkbox e como captar e tratar dados de um array enviado pelo formulario e mostra-lo.

`index.php`

```html



<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aula 04</title>
    <link rel="stylesheet" href="estilos.css">
</head>
<body>

    <h1 style="text-align: center; color: white;">Cadastro de Prefrências</h1>

    <form action="receber.php" method="post">

        <label for="nome">Nome</label>
        <input type="text" name="nome">

        <label for="genero">Gênero</label>
        <div class="grupo">
            <input type="radio" name="genero" value="masculino">Masculino
            <input type="radio" name="genero" value="femenino">Femenino
        </div>

        <label>Serviços Assinados</label>
        <div class="grupo">
            <input type="checkbox" name="servicos[]" value="Netflix">Netflix
            <input type="checkbox" name="servicos[]" value="Prime Video">Prime Video
            <input type="checkbox" name="servicos[]" value="Disney+">Disney+
            <input type="checkbox" name="servicos[]" value="Max (HBO)">Max (HBO)
        </div>

        <label>Estado</label>
        <select name="estado" id="estado">
            <option value="sp">sp</option>
            <option value="rj">rj</option>
            <option value="mg">mg</option>
            <option value="pr">pr</option>
        </select>

        <label>Data de Nascimento</label>
        <input type="date" name="nascimento">

        <input type="submit" value="Enviar">

    </form>
    
</body>
</html>

```

`receber.php`

```php

<?php

$nome = $_POST['nome'];
$genero = $_POST['genero'];
$servicos = $_POST['servicos'];
$estado = strtoupper($_POST['estado']);
$dataDeNascimento = $_POST['nascimento'];

$formatarData = date('d/m/Y', strtotime($dataDeNascimento));


?>


```

```html

<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Preferências</title>
    <link rel="stylesheet" href="estilos.css">
</head>
<body>

    <h1>Preferências</h1>

    <p><strong>Nome: </strong><?= $nome?></p>
    <p><strong>Gênero: </strong><?= $genero?></p>
    <p><strong>Serviços Assinados: </strong>
        <ul>
            <?php

                foreach($servicos as $servico){
                    echo "<li>" . htmlspecialchars($servico) . "</li>";
                }
            ?>
        </ul>
    </p>
    <p><strong>Estado: </strong><?= $estado?></p>
    <p><strong>Data de Nascimento: </strong><?= $formatarData?></p>




    
</body>
</html>

```

`estilos.css`

```css

body{
    font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
    font-size: 1rem;
    background: gray;
}

form{
    background: #fff;
    padding: 1.1rem;
    border-radius: 10px;
    width: 400px;
    margin: 0 auto;
}

label{
    display: block;
    font-weight: bold;
    text-transform: uppercase;
    margin-top: 10px;
}

input, select{
    width: 100%;
    padding: 0.9rem;
    margin-top: 5px;
    border-radius: 5px;
    border: 1px solid #ccc;
}

.grupo{
    margin-bottom: 10px;
    background: #ccc;
    padding: 5px;
    border-radius: 5px;
    animation: slideInLeft .8s;
}

select{
    text-transform: uppercase;
}

input[type="date"]{
    font-size: .8rem;
    font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
}

@keyframes slideInLeft{

    0%{
        transform: translateX(-50%);
        opacity: 0;
    }

    100%{
        transform: translateX(0);
        opacity: 1;
    }

}

```

## Exercício

Pasta `aula04/agendamento-odontologico`


`index.php`

```html

<!-- 
Agendamento Odontologico

-Nome cliente

Dentistas
- Álvaro da Silva
- Silvia Martins
- Lucio Otavio

Servicos
- Limpeza
- Clareamento
- Ortodontia
- Protse
-Canal

Data e hora(time) da consulta
-->

<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SorriDente</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>

    <h1>Bem vindo(a) a SorriDente!</h1>
    <p>Onde seu sorriso tem brilho!</p>


    <h2>Agende sua consulta agora! Preencha o formulário abaixo:</h2>

    <form action="receber.php" method="post">

        <div class="box">
            <label for="dentista">Conheça nossos dentistas</label>
            <select name="dentista" id="dentista">
                <option value="Álvaro da Silva">Álvaro da Silva</option>
                <option value="Silvia Martins">Silvia Martins</option>
                <option value="Lúcio Otavio">Lúcio Otavio</option>
            </select>
        </div>

        
        <div class="box">
            <label>Escolha o serviço</label>
            <input type="checkbox" name="servicos[]" value="Limpeza">Limpeza
            <input type="checkbox" name="servicos[]" value="Clareamento">Clareamento
            <input type="checkbox" name="servicos[]" value="Ortodontia">Ortodontia
            <input type="checkbox" name="servicos[]" value="Protese">Protese
            <input type="checkbox" name="servicos[]" value="Canal">Canal
        </div>

        
        <div class="box">
            <label for="">Escolha a data da sua consulta</label>
            <input type="date" name="data">
            <input type="time" name="hora">
        </div>

        <input type="submit" value="Enviar">

    </form>
    
</body>
</html>

```

`receber.php`

```php

<?php

$dentista = $_POST['dentista'];
$servicos = $_POST['servicos'];
$data = date("d/m/Y", strtotime($_POST['data']));
$horario = $_POST['hora'];

?>

```

```html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Consulta</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>

    <h1 style="text-align: center;">Sua Consulta</h1>
    <div class="consulta">
        <p><strong>Dentista: </strong><?= $dentista?></p>
        <p><strong>Serviço(s):</strong>
        <ul>
            <?php
            
                foreach($servicos as $servico){

                    if($servico == NULL){
                        echo "Sem serviços.";
                    }else{
                        echo "<li>" . htmlspecialchars($servico) . "</li>";
                    }
                }

            ?>
            </ul>
        </p>
        <p><strong>Data da Consulta</strong>
            <ul>
                <li><strong>Data: </strong><?= $data?></li>
                <li><strong>Horário: </strong><?= $horario?></li>
            </ul>
        </p>

    </div>

    <a href="index.php">Voltar ao Agendamento</a>


    
</body>
</html>

```

`styles.css`

```css

body{
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    padding: 5rem;
    background: #08979D;
    color: #fff;
}

h1{
    font-size: 3rem;
}
h2{
    margin-top: 10rem;
    text-align: center;
}

p{
    font-size: 1.1rem;
}

form{
    display: flex;
    flex-direction: column;
    gap: 1rem;
    padding: 1rem;
    background: #99c1b9;
    width: 50%;
    border-radius: 12px;
    margin: 0 auto;
}

select{
    padding: .5rem;
    border-radius: 8px;
    width: 50%;
    font-size: 1rem;
}

input[type="checkbox"]{

   font-size: 2em;
}

label{
    display: block;
    font-size: 1.2rem;
    font-weight: 600;
}

.box:nth-child(2){
   font-size: 1.1rem;
}

input[type="date"], input[type="time"]{

    font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
    font-size: .8rem;
    padding: .5rem;
    border-radius: 6px;

}

.consulta{
    background: #99c1b9;
    padding: 1rem;
    border-radius: 12px;
    width: 50%;
    margin: 0 auto;
    margin-bottom: 2rem;
}

ul{
    list-style-type: none;
}

a{
    margin-top: 2rem;
    text-decoration: none;
    color: #fff;
    border-radius: 8px;
    border: 1px solid #ccc;
    padding: .5rem;
    font-weight: bold;
    font-size: 1.2rem;
}

```
