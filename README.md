# CURSO JAVASCRIPT ES6+

### INTRODUÇÃO
<h5>O ECMAScript 2015 é um padrão ECMAScript que foi ratificado em junho de 2015.</h5>

<p>ES2015 é uma atualização significativa para o JavaScript, e a primeira grande atualização desde que o ES5 foi padronizado em 2009. A implementação desses recursos nos principais mecanismos JavaScript está em andamento agora.

Consulte o <a href="http://www.ecma-international.org/ecma-262/6.0/index.html" target="blank">padrão ES2015 </a> para obter a especificação completa do ECMAScript 2015.</p>

<p>Este repositório trata-se de um curso de JavaScript ES6+ que aborda as principais feature do javaScript 2015 e as mais atuais. <br> No decorrer do curso iremos aprender não somente as novas features JS, mas trabalhares com babel, webpack e yarn em uma aplicação simples utilizando todos os recursos aprendidos no curso, é extremamente recomendado que ao iniciar o curso você já possua um conhecimento básico de lógica de programação e esteja familiarizado com terminal de controle de seu sistema operacional.</p>

<h4>Recursos do JavaScript ES6+ e Tópicos Extras.</h4>
<ul>
    <li><a href="https://github.com/lucaspedronet/curso-ecmas6-news-features#-ecmascript-2015-" target="blank">ECMAScript 2015</a></li>
    <li><a href="/ECMAScript 2015" target="blank">Babel</a></li>
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
Fala galera tudo bem com vocês? Meu nome é Lucas Pedro estou cursando o 5ª período em Engenharia de Software e irei ministrar esse curso de javscript ES6+. Antes que possamos dar início às explicações e colocar a mão na	massa, é muito importante entender corretamente o que é o ECMAScript e qual a sua relação com o JavaScript. O ECMAScript (ES) é a especificação da linguagem de script que o JavaScript implementa. Isto é, a descrição de uma linguagem de script, sendo padronizado	pela Ecma International (http://www.ecmascript.org/index.php) —	associação criada em 1961 dedicada à padronização de	sistemas de	informação e comunicação — na especificação	ECMA-262. ECMAScript 2015 sofreu uma mudança significativa melhorando o desenvolvimento e trabalhando melhor os conceitos como paradigmo Orientado Objeto já concebido em outras liguagem como Java e PHP, vários outros recurso que ajudam a tornar o JS uma ligugem ainda mais poderesa.
Então sem mais delongas vamos dar início ao curso. </p> <br>
<p>
Para darmos inicio no curso teremos que baixar um gerenciado de dependências que facilitará a instalação de pacotes e bibliotecas, nesse caso será o chocolatey para Windows pois será o sistema que iremos trabalhar daqui pra frente, então acese o site do <a href="https://chocolatey.org/" target="blank">chocolatey</a> e siga as instruções de instalção: <br>
Instalar com o PowerShell.exe
Com o PowerShell, há um passo adicional. Você deve garantir que <b>Get-ExecutionPolicy</b> não seja Restrito. Sugerimos usar Bypasspara ignorar a política para obter as coisas instaladas ou AllSignedpara um pouco mais de segurança.<br>

Execute <b>Get-ExecutionPolicy.</b> Se ele retornar `Restricted`, execute `Set-ExecutionPolicy AllSigned` ou `Set-ExecutionPolicy Bypass -Scope Process`.
</p>
<p>Agora, execute o seguinte comando:   (copiar texto de comando)</p>

`Set-ExecutionPolicy Bypass -Scope Process -Force; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1')) `

