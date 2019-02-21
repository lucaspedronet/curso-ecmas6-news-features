### Configurndo o Webpack
<p>O que iremos fazer agora é <code>configurar o webpack</code>, este é uma espécie de serviço que irá nos disponibilizar uma forma de trabalhar com vários arquivos js na nossa aplicação, arquivos <i><em>js, css, json, html e etc</em></i> ou seja o webpack é um em pacotador de arquivos. Todos esses arquivos também serão transpilados para um único arquivo javascript <code>.bundle</code> com todas as informações. Abra o arquivo packege.json e faça a seguinte alteração no nome “dependencies” para <code>“devDepencies”:</code> 
</p>

<pre><div>"devDependencies": {
    "@babel/cli": "^7.2.3",
    "@babel/core": "^7.2.2",
    "@babel/plugin-proposal-object-rest-spread": "^7.2.0",
    "@babel/preset-env": "^7.2.3",
  },</div></pre>

<p>Feita modificação necessária devemos colocar o sinal de “–D” antes de todas as dependências que queiramos instalar somente em ambiente de desenvolvimento, então vamos começar instalando o webpack e webpack-cli, vá em nosso terminal e digite os seguintes comandos: 
</p>
<div>
 <ul>
 <li><b>yarn add webpack webpack-cli</b>: <label>[Instalando webpack e webpack-cli]</label></li>
 <li><b>webpack-cli</b>: <label>[ <i><em>é a linha de comandos do webpack.</em></i>]</label></li>
 <li><b>webpack</b>: <label>[ <i><em>Em essência, o webpack é um empacotador de módulos estáticos para aplicativos JavaScript modernos. </em></i>]</label></li>
 </ul>
</div>

<p>Agora vamos criar um arquivo de configuração do webpack esse arquivo vai ter o nome de <i><em>webpack.config.js</em></i> sendo este arquivo principal e ficará em nossa raiz e vai conter o seguinte código: 
</p>

<div><pre>module.exports = {
  mode: 'development'
  entry: './main.js',
  output: {
    path: __dirname,
    filename: 'bundle.js',
  },
  module: {
    rules: [
      {
        test: /\.js$/,
        exclude: /node_modules/,
        use: {
            loader: 'babel-loader',
        }
      }
    ]
  }
};</pre></div>

<div>
  <h4>Vamos conhecer um pouco mais sobre o código acima e suas propriedades.</h4>
  <p>
    <b><em>Entry</em></b>: [<em> Nos diz qual arquivo é o principal em nosso projeto. </em>]<br>
    <b><em>Output</em></b>: [<code>{ }</code> <em>Recebe os caminho para onde dever ir o arquivo compilado (igual ao babel fazia antes) </em>]<br>
    <b><em>Path</em></b>: [<em> Recebe o endereço onde ficará o arquivo após conversão e <b><em>__dirname</em></b> é uma variável global que representa a raiz do projeto. </em>]<br>
    <b><em>Filename</em></b>: [ <em> Recebe o nome desse arquivo que contém código copilado. </em> ]<br>
    <b><em>Module</em></b>: [<code>{ }</code> <em>Module tem uma propriedade que vai nos dizer como deve se comporta um arquivos baseado em sua extensão</em> ]<br>
    <b><em>Test</em></b>: [ <em>Utilizamos aqui uma expressão regular que nos diz qual extensão de arquivo deve ser considerada. </em>]<br>
    <b><em>Exclude</em></b>: [<em> Dizemos qual pastas ou arquivos queremos excluir. </em>]<br>
    <b><em>Use</em></b>: { }:
  </p>
</div>

<div>
  <h4>Voltamos ao terminal e vamos instalar mais uma dependência ao nosso package.json em ambiente de desenvolvimento.</h4>

  <b>yanr add babel-loader  –D</b><br>

  <p>E em nosso arquivo package.json no scriprs devemos alterar deixando da seguinte forma:</p>
  
  <div><pre>"scripts": {
    "dev": "webpack --module-development -w"
  }</pre></div>

  <p>Em sequência vamos colocar o nosso webpack pra rodar, vá em seu terminal e digite <b>yarn dev</b>. Para testarmos esse webpack vamos começar a trabalhar com <em>import/export </em>e antes de mais nada alteraremos o arquivo <em>index.js</em> que atualmente recebe em seu script o <em>main.js</em> e vamos alterar para <em>bundle.js</em>.
  </p><br>

  <p>Vamos então criar um novo arquivo de nome funções.js que conterá as seguintes funções: </p>
  <img src="../assets/import-export-funcoes.PNG" name="img-importe-export" alt="img-import-export" height="321" width="636" >

</div>

  <div>
    <p>Então dentro do arquivo <i>main.js</i> vamos importa as funções que acabamos de criar em nosso arquivo <i>funcoes.js</i></p>
  
    <img src="../assets/import-export-funcoes-02.PNG" height="128" width="633"/>
  
    <p>Chamamos as funções entre chaves do arquivo <i><em>./funções</em></i> isso é bastante utilizado em bibliotecas como react e reac-native por exemplo, também conseguimos atribuir um default para alguma função, classe e etc porém apenas uma pode ser definida por arquivo. Bastando colocar a palavra default após o export ficando <b><em>export default function soma()</em></b>.
    </p>
  </div>

<div>
  <p>
    Veja outros exemplos de import e export:
  </p>
  <img src="../assets/import-export-funcoes-03.PNG" name="img-importe-export-03" alt="img-import-export-03" height="233" width="631" >

  <p>Quando definimos um export como `default` podemos importa-la sem a necessidade de usar as chaves entre ela e o mesmo pode ser renomeada para qualquer nome que desejar, foi o que aconteceu em somaFuncao, para obtermos os mesmos resultados sem utilizar default precisamos do “as” nesse caso deve ser passado entre chaves pois não estamos utilizando default, ficando da seguinte forma <code>import { sub as subtração } from “./funções”</code> .
  </p>
</div>

### <a href="https://github.com/lucaspedronet/curso-ecmas6-news-features/blob/master/modulo-02-webpack-server/webpack-devserver.md" alt="Webpack-devServer" > Webpack devServer</a>
