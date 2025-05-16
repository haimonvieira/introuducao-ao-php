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
- Criar uma pasta dentro de \xamppz\htdocs\[pasta_projeto].

## Aprendendo a inserir o PHP no código HTML

Arquivo 'index.php'

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

Arquivo 'operadores.php'

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

Arquivo 'media.php'

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
