# Introdução ao PHP - SENAC - Registro/SP
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

# Criação do projeto
- Criar uma pasta dentro de \xamppz\htdocs\[pasta_projeto]
