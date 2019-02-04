<h1> Babel </h1>

<p>Configurando o Babel, depois de ter instalado o node e yarn em sua máquina vamos criar uma paste de nome <i>es6</i> que irá conter nosso projeto, em seguida abra seu terminal a partir dessa pasta e execute o seguinte comando: `yarn init` Pressione a tecla Entre até aparecer a mensagem <i>success saved packege.json</i> (As versoes mais recente do yarn pode pedir para que informe o nome do projeto nesse caso pode colocar o mesmo nome da pasta do projeto) esse comando criará um arquivo packege,json que gerenciará as dependências instaladas no projeto. Vamos precisar instalar algumas dependências e para isso precisamos da linha de comando do Babel instalada.
</p> 
<Ul>
    <li><code>$ yarn add @babel/cli</code> [ Instalando a cli do babel (linha de comando do Babel). ]</li>
    <li><code>$ @babel/preset-env</code> [ Instalando a preset-env. ]</li>
</ul>

<p>Vamos criar na raiz de nosso projeto um arquivo `.babelrc`  que vai conter o seguinte trecho de código:</p>
<code>
{<br/>
    "presets": ["@babel/preset-env"]<br/>
}<br/>

</code>
<p>
O babel possui vários preset-env ele vai identificar qual ambiente nós estamos utilizando para desenvolver se é um navegador (páginas web), Servidor nodejs (API Rest) ou Mobile(RN) e fará o trabalho de transpilar todo nosso código JSES6+ para um versão que seja compreendia pela maioria do navegadores e irá fazer isso da melhor forma possível.<br>
Vamos adicionar mais uma dependência ao babel: 
</p>

<div><pre>yarn add @babel/core<pre></div>

<p>
Agora ainda na raiz de nosso projeto vamos criar um arquivo index.html e main.js dentro do main.js adicione um <code>alert(‘Funcionou’)</code>.<br>
Feito isso vamos no arquivo packege.json e criar mais um objeto de nome “script” conforme figura abaixo:<br>
</p>

<div><pre>
"scripts": {
    "dev": "babel ./main.js -o ./bundle.js"<br>
  }
</pre></div>

<p>
O atributo <i>dev</i> vai pegar nosso arquivo <i>main.js</i> e transpilar todo o seu código em um novo arquivo chamado bunlde.js que seja compreendido por maioria dos navegadores, para realizar essa transpilação vá em seu terminal e digite <b>yarn dev.</b><br><br>
Note que foi criado um arquivo <em>budle.js </em>na raiz de seu projeto contendo o código convertido, mas perceba que nada mudou se comparado com main.js isso ocorre porque o <code>alert(‘Funcionou’)</code> é uma função reconhecida por versões anterios do ECS então ela é compreendida por todos os navegadores por isso não requer uma transpilação.
</p>