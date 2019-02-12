### Configurndo o Webpack
<p>O que iremos fazer agora é <code>configurar o webpack</code>, este é uma espécie de serviço que irá nos disponibilizar uma forma de trabalhar com vários arquivos js na nossa aplicação, arquivos <i><em>js, css, json, html e etc</em></i>. Todos esses arquivos também serão transpilados para um único arquivo javascript `.bundle` com todas as informações. Abra o arquivo packege.json e faça a seguinte alteração no nome “dependencies” para <code>“devDepencies”:</code> 
</p>

<pre><div>
"devDependencies": {
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

<div><pre>
module.exports = {
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
};
</pre></div>