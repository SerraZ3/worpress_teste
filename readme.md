# Intrudução ao Wordpress

Essa material está sendo criando com intuito de facilitar o aprendizado dos membros da [Associação Empresa Junior de Computação da UESC (TecnoJr)](https://www.tecnojr.com.br/) e qualquer outro estudante da área de computação que tenha o desejo de aprender Wordpress

**Desenvolvido por:**
[Henrique A. Serra](https://github.com/SerraZ3/) :smile: :metal:

## Sumário

1. [Introdução](#introdução)
2. [Instalando o Wordpress](#instalando-o-wordpress)
3. [Criando Tema](#criando-um-tema)

**Conhecimentos prévios recomendados:** HTML, CSS e PHP.

## Introdução

### O que é o WordPress?

WordPress é uma ferramenta para criação de sites. Ele possibilita a criação de blogs, e-commerces, dentre diversos outros tipos de sites de forma dinâmica, ou seja, pode ser alterado por um painel administrativo.

Sistema de Gestão de Conteúdo, essa é a característa do WP. Esse tipo de sistema possibilita o usuário publicar, editar, modificar, organizar e deletar conteúdos.

### Como começar?

O WordPress possui um site, [WordPress.com](https://wordpress.com/), que oferece serviços gratuito de criação e hospedagem de blogs, uma ótima opção para quem não deseja investir em hospedagem ou dominio e que tem um pequeno site. Entretanto, seu dominio fica restrito a, por exemplo, *seublog.wordpress.com*. 

Você receberá acesso para postar e modificar seu site, porém, a costomização é muito limitada pois você apenas pode usar os layout fornecidos no site, não podendo realizar customizão própria. Além disso, não poderá instalar plugins, utilizar publicidade (programa de afiliados) ou um sistema de métricas, como o [Google Analytics](https://analytics.google.com/analytics/web/provision/?authuser=0#provision/SignUp/). Você não terá acesso FTP do servidor e terá que exibir obrigatoriamente no rodapé "Aloje seu blog com WordPress.com". 



Para aqueles que desejam ter maior liberdade existe também o [WordPress.org](https://wordpress.org/). Ele ofere os códigos do WordPress além de possuir diversos tema, plugins, dentre outras coisas que ajudam a estilizar e melhorar seu site. 


|              | <center>Wordpress.com</center> | <center>WordPress.org</center>|
|:------------:|:-------------------------|:-------------------------| 
|   Vantagens  |       left-aligned    |         $1600        | 
| Desvantagens | 1. teste <br> 2. teste <br> 3. teste |  1. teste <br> 2. teste |

## Instalando o Wordpress

Primeiro é necessário baixar o arquivo de instalação, você pode encontrar no site 	do [Wordpress.org](https://wordpress.org/) em "Get WordPress".

**AVISO:** É necessário o LAMP ou XAMPP em seu computador, pois o WordPress(WP) é feito em PHP e necessita do APACHE, além disso, precisa de conexão com Banco de Dado.

Após baixado, você deve colocar o arquivo .zip (ou .tar.gz) no seu diretório do localhost. Extraia o arquivo. Acesse a pasta extraida pelo navegador (localhost/"nome_pasta_wp"), ela irá te direcionar para uma pagina de instalação. Caso essa página não apareça você pode acessar pelo endereço **localhost/"nome_pasta_wp"/wp-admin/setup-config.php**.

Para continuar é preciso de algumas informações do seu Banco de Dados (BD).
1. Database name (nome do BD): Você deve criar um BD que será usado pelo WP. Após criar deve informá-lo no campo;
2. Username (Nome do usuário): Nome do usuário do BD;
3. Password (Senha): Senha do usuário BD;
4. Database Host (Endereço do BD): Como seu WP será local, pode colocar como "localhost" ou "127.0.0.1" (IP do localhost);
5. Table Prefix (Prefixo da tabela): Essa será o nome que o WP adotara para o inicio de toda tabela que será gerada por ele. Por convensão dexa-se o ultimo caracter como "_".
**OBS.:**Essas informações deverão ser modificadas caso haja transferencia para outro banco de dados.

Preenchido os campos com as devidas informações, você será redirecionado para uma página que possuirá um código. Copie esse código. Abra o arquivo **wp-config.php**, ele se encontra no diretório principal da sua pasta WP. Se não achar o arquivo com esse nome, você deve pegar o arquivo **wp-config-sample.php** e modificar para **wp-config.php**. Copie o codigo nesse no arquivo **wp-config.php** e salve.

Abrirá uma página de "Welcome"(bem-vindo). Você deve informar:
1. Site Title: Titulo que o site receberá (pode ser modificado depois);
2. Username: Usuário de acesso ao painel administrativo do WP;
3. Password: Senha do acesso ao painel administrativo do WP;<br>
3.1. Caso você coloque senha muito curta deve marcar esse radio button
4. Your email: Email para recuperação de acesso;
5. Search Engine Visibility: Caso você não deseje que os moteres de busca indiquem seu site (é possivel modificar depois).

Após preencher dados você terá concluido a instalação. :thumbsup:


## Criando um tema

Crie uma pasta em **"/wp-content/themes/"**. Essa pasta devera ter o nome do seu tema. O wordpress consegue identificar pastas e arquivos em locais ou com nomes específicos. A depender do local ou do nome ele realizará uma função preestabelecida. Nesse arquivo está a constituição básica de um tema.

### Constituição básica de um Tema:

* header.php: onde fica o código do cabeçalho;
* sidebar.php: onde fica o código da lateral da página;
* footer.php: onde fica o código do rodapé;
* index.php: código que mostra a página inicial;
* single.php: código que mostra o artigo na sua própria página;
* page.php: código que mostra o conteúdo de uma página estática;
* archive.php: o código nesta parte vai mostrar os artigos que estão no arquivo, nas categorias, tags, etc;
* functions.php: local onde ficam algumas funções que adicionam mais capacidades aos temas;
* 404.php: mostrará um texto para avisar que o conteúdo não foi encontrado;
* style.css: ficheiro onde fica o stylesheet do tema.

Para um tema funciona basta ter apenas os arquivos **style.css** e **index.php**. Entretanto seu tema não será robusto.

### style.css

Nesse arquivo ficará todas as configurações visuais do seu Tema. Além disso, possuirá as informações que o WP mostrará sobre seu Tema.

Crie um arquivo e nomei como **style.css** e depois abra-o.

#### Informações do seu Tema:

* Theme Name (\*): Nome do Tema.
* Theme URI: Página onde o publico pode conseguir mais informações sobreo Tema.
* Author (\*): Nome do Autor do Tema.
* Author URI: Link individual ou organizacional do Autor.
* Description (\*): Pequena descrição sobre o Tema.
* Version (\*): Versão do Tema. A cada atualização deve modificar.
* License (\*): Nome da licença, caso tenha.
* License URI (\*): Link que leva para a lincença.
* Text Domain (\*): Usado para traduzir seu tema para outras linhagens
* Tags: Palavras que representem caracteristicas do seu tema. Essas palavras ajudam na pesquisa. As palavras devem ser separadas de por virgula. Nesse formato "azul, blue, claro, calmo,..."
* Domain Path: ??. Defaults to /languages.
* Template: Serve para referenciar o Tema pai. Usado para quando você cria um Tema baseado em outro Tema. 

(\*) = Informações esseciais para o Tema.


#### Estilizando seu Tema:

O arquivo style.css funciona exatamente como qualquer outro arquivo .css. Você pode modificar qualquer atributo de qualquer tag, class ou id sem problema algum.

### index.php


## Apêndice

#### 1. FTP
