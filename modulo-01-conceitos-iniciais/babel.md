<h1> Babel </h1>

<p>Configurando o Babel, depois de ter instalado o <i><em><b>node e yarn</b></em></i> em sua máquina vamos criar uma pasta de nome <i>es6</i> que irá conter nosso projeto, em seguida abra seu terminal a partir dessa pasta e execute o seguinte comando: <code>yarn init</code> Pressione a tecla Entre até aparecer a mensagem <i><em>success saved packege.json</em></i> (As versoes mais recente do yarn pode pedir para que informe o nome do projeto nesse caso pode colocar o mesmo nome da pasta do projeto) esse comando criará um arquivo packege,json que gerenciará as dependências instaladas no projeto. Vamos precisar instalar algumas dependências, para isso iremos precisar do <i><em><b>babel-cli</b></em></i> instalado em nossa máquina, é simplesmente uma linha de comando que Babel utiliza para instalar suas dependências e etc.
</p> 
<Ul>
    <li><code>$ yarn add @babel/cli</code> <i><em>[ Instalando a cli do babel (linha de comando do Babel). ]</em></i></li>
    <li><code>$ yarn add @babel/preset-env</code> [ Instalando a preset-env. ]</li>
</ul>

<p>Vamos criar na raiz de nosso projeto um arquivo `.babelrc`  que vai conter o seguinte trecho de código:</p>
<div><pre>
{
  "presets": ["@babel/preset-env"]
}
</pre></div>

<p>
O babel possui vários <i><em><b>preset-env</b></em></i> ele é o responsável por identificar qual ambiente estamos utilizando para desenvolver o projeto, se é um navegador (páginas web), servidor nodejs (API Rest) ou mobile(RN) e fará o trabalho de transpilar todo nosso código JSES6+ para uma versão que seja compreendia pela maioria dos navegadores e irá fazer isso da melhor forma possível.
</p>

<h4>Vamos adicionar mais uma dependência ao babel: </h4>

<pre>yarn add @babel/core</pre>

<p>Ainda na raiz de nosso projeto vamos criar um arquivo <i><em><b>index.html</b></em></i> e <i><em><b>main.js</b></em></i> dentro do <i><em><b>main.js</b></em></i> adicione um <code>alert(‘Funcionou’)</code>.<br>
Feito isso vamos no arquivo packege.json e criar mais um objeto de nome <i><em><b>“script”</b></em></i> conforme figura abaixo:<br>
</p>

<div><pre>
"scripts": {
    "dev": "babel ./main.js -o ./bundle.js"<br>
  }
</pre></div>

<p>
O atributo <i><em><b>dev</b></em></i> vai pegar nosso arquivo <i>main.js</i> e transpilar todo o seu código em um novo arquivo chamado bunlde.js que seja compreendido por maioria dos navegadores, para realizar essa transpilação vá em seu terminal e digite <b>yarn dev.</b><br><br>


<i><em><b>Note</b></em></i> que foi criado um arquivo <em>budle.js</em>na raiz de seu projeto contendo o código convertido, mas perceba que nada mudou se comparado com main.js isso ocorre porque o <code>alert(‘Funcionou’)</code> é uma função reconhecida por versões anterios do ECS então ela é compreendida por todos os navegadores por isso não requer uma transpilação. Então vamos adicionar uma classe que é um feacture da versão mais recente no ECS6+ acompanhe na imagem abaixo, dentro do main.js reescreva o código da seguinte forma:
</p>

<div><pre>
class teste {
    static metodo (){
        alert('Funcionou')
    }
}
</div></pre>

<p>Agora abra seu arquivo budle.js e veja como ficou! </p>

<div><pre>
/*#__PURE__*/
function () {
  function teste() {
    _classCallCheck(this, teste);
  }

  _createClass(teste, null, [{
    key: "metodo",
    value: function metodo() {
      alert('Funcionou');
    }
  }]);

  return teste;
}();
</div></pre>

