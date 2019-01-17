# CURSO JAVASCRIPT ES6+

### INTRODUÇÃO
<h5>O ECMAScript 2015 é um padrão ECMAScript que foi ratificado em junho de 2015.</h5>

<p>ES2015 é uma atualização significativa para o JavaScript, e a primeira grande atualização desde que o ES5 foi padronizado em 2009. A implementação desses recursos nos principais mecanismos JavaScript está em andamento agora.

Consulte o <a href="http://www.ecma-international.org/ecma-262/6.0/index.html" target="blank">padrão ES2015 </a> para obter a especificação completa do ECMAScript 2015.</p>

<p>Este repositório trata-se de um curso de JavaScript ES6+ que aborda as principais feature do javaScript 2015 e as mais atuais. <br> No decorrer do curso iremos aprender não somente as novas features JS, mas trabalhares com babel, webpack e yarn em uma aplicação simples utilizando todos os recursos aprendidos no curso, é extremamente recomendado que ao iniciar o curso você já possua um conhecimento básico de lógica de programação e esteja familiarizado com terminal de controle de seu sistema operacional.</p>

<h4>Recursos do JavaScript ES6+ e Tópicos Extras.</h4>
<ul>
    <li><a href="https://github.com/lucaspedronet/curso-ecmas6-news-features#-ecmascript-2015-" target="blank">ECMAScript 2015</a></li>
    <li><a href="https://github.com/lucaspedronet/curso-ecmas6-news-features#-instala%C3%A7%C3%A3o-e-configura%C3%A7%C3%A3o-" target="blank">Instalação e Configuração</a></li>
    <li><a href="https://github.com/lucaspedronet/curso-ecmas6-news-features#-babel-" target="blank">Babel</a></li>
    <li><a href="#" target="blank">Classe</a></li>
    <li><a href="#" target="blank">Const & Let</a></li>
    <li><a href="#" target="blank">Array</a></li>
    <li><a href="#" target="blank">Arrow</a></li>
    <li><a href="#" target="blank">Valores padrões</a></li>
    <li><a href="#" target="blank">Desistruturação</a></li>
    <li><a href="#" target="blank">Rest & Spread</a></li>
    <li><a href="#" target="blank">Templete Literal</a></li>
    <li><a href="#" target="blank">Sintaxe curta objetos</a></li>
    <li><a href="#" target="blank">Webpack</a></li>
    <li><a href="#" target="blank">Import & Export</a></li>
    <li><a href="#" target="blank">Webpack devServer</a></li>
    <li><a href="#" target="blank">Async & Await</a></li>
    <li><a href="#" target="blank">Axios e Api</a></li>
    <li><a href="#" target="blank">App com es6+</a></li>
    <li><a href="#" target="blank">Adicionando repos</a></li>
    <li><a href="#" target="blank">Buscando Api</a></li>
    <li><a href="#" target="blank">Loading</a></li>
</ul>

<br>
<h2> ECMAScript 2015 </h2>
<p>
Fala galera tudo bem com vocês? Meu nome é Lucas Pedro estou cursando o 5ª período em Engenharia de Software e irei ministrar esse curso de javscript ES6+. Antes que possamos dar início às explicações e colocar a mão na	massa, é muito importante entender corretamente o que é o ECMAScript e qual a sua relação com o JavaScript. O ECMAScript (ES) é a especificação da linguagem de script que o JavaScript implementa. Isto é, a descrição de uma linguagem de script, sendo padronizado	pela Ecma International (http://www.ecmascript.org/index.php) —	associação criada em 1961 dedicada à padronização de	sistemas de	informação e comunicação — na especificação	ECMA-262. ECMAScript 2015 sofreu uma mudança significativa melhorando o desenvolvimento e trabalhando melhor os conceitos como paradigmo Orientado Objeto já concebido em outras liguagem como Java e PHP, vários outros recurso que ajudam a tornar o JS uma liguagem ainda mais poderesa.
Então sem mais delongas vamos dar início ao curso. </p> <br>
<p>
<h2> Instalação e Configuração </h2>

Para darmos inicio no curso teremos que baixar um gerenciado de dependências que facilitará a instalação de pacotes e bibliotecas, nesse caso será o chocolatey para Windows pois será o sistema que iremos trabalhar daqui pra frente, então acese o site do <a href="https://chocolatey.org/" target="blank">chocolatey</a> e siga as instruções de instalção: <br><br>
<b>Instalar com o PowerShell</b><br>

Precione as teclas em conjuto (windows + X) e escolha Windows PoweShell(admin) irá abrir uma janela, execute o seguinte comando: <b>Get-ExecutionPolicy.</b> Se ele retornar `Restricted`, execute `Set-ExecutionPolicy AllSigned` ou `Set-ExecutionPolicy Bypass -Scope Process`.
</p>
<p>Agora, execute o seguinte comando: (copiar texto de comando)</p>

`Set-ExecutionPolicy Bypass -Scope Process -Force; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))` precione enter e aguarde a instalação concluir, feito isso abra outro terminal e figite o comando `choco --version` para verificar o funcionamento do <b>chocolatey.</b> Agora vamos instalar o Yarn então mais uma vez em seu terminal digite `choco install yarn` esse comando também irá instalar o <a href="https://nodejs.org" target="blank">Node.js</a> caso não esteja instalado, caso queira instalar individualmente basta acessar o site (<a href="https://nodejs.org/en/" target="blank">https://nodejs.org/en/</a>). Agora teste o yarn e node digitando os camonado `yarn --version` e `node --version` ambos devem aparecer suas repectivas versões.<br><br>
<img src="node_yarn_version.PNG" alt="node e yarn" height="142" width="442"><br><br>

<h2> Babel </h2>
<p>
Configurando o Babel, depois de ter instalado o node e yarn em sua máquina vamos criar uma paste de nome <i>es6</i> que irá conter nosso projeto, em seguida abra seu terminal a partir dessa pasta e execute o seguinte comando: `yarn init` Pressione a tecla Entre até aparecer a mensagem <i>success saved packege.json</i> (As versoes mais recente do yarn pode pedir para que informe o nome do projeto nesse caso pode colocar o mesmo nome da pasta do projeto) esse comando criará um arquivo packege,json que gerenciará as dependências instaladas no projeto. Vamos precisar instalar algumas dependências e para isso precisamos da linha de comando do Babel instalada.
</p> 
<Ul>
    <li> yarn add @babel/cli [ Instalando a cli do babel (linha de comando do Babel). ]</li>
    <li>@babel/preset-env [ Instalando a preset-env. ]</li>
    
</ul>

<p>Vamos criar na raiz de nosso projeto um arquivo `.babelrc`  que vai conter o seguinte trecho de código:</p>

{
    "presets": ["@babel/preset-env"]
}

<h2> Classe </h2>
<h2> Const & Let </h2>
<h2> Array </h2>
<h2> Arrow </h2>
<h2> Desistruturação </h2>
<h2> Rest & Spread </h2>
<h2> Templete Literal </h2>
<h2> Sintaxe curta objetos </h2>
<h2> Webpack </h2>
<h2> Import & Export </h2>
<h2> Webpack devServer </h2>
<h2> Async & Await </h2>
<h2> Axios e Api </h2>
<h2> App com es6+ </h2>
<h2> Adicionando repos </h2>
<h2> Buscando Api </h2>
<h2> Loading </h2>