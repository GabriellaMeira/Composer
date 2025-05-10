# Gerador de PDF com PHP e Composer

Este é um projeto prático desenvolvido em PHP com o objetivo de gerar arquivos PDF com qualquer conteúdo definido pelo usuário. Utiliza a biblioteca **mPDF** e gerenciador de dependências **Composer**.

## Tecnologias Utilizadas

- **PHP**
- **Composer**
- **mPDF**

## Requisitos

- PHP 7.4 ou superior
- Composer instalado

## Instalação

1. Clone o repositório:

   git clone https://github.com/seu-usuario/nome-do-projeto.git
   cd nome-do-projeto

Instale as dependências via Composer:

composer install

## Como usar
Edite o conteúdo do PDF dentro do arquivo principal do projeto (ex: index.php).

Execute o script via servidor local ou linha de comando.

Um arquivo PDF será gerado com o conteúdo definido.

## Exemplo básico

<?php
require_once __DIR__ . '/vendor/autoload.php';

$mpdf = new \Mpdf\Mpdf();
$mpdf->WriteHTML('<h1>Olá, mundo!</h1><p>Este é um PDF gerado com mPDF.</p>');
$mpdf->Output('arquivo.pdf', 'I');
