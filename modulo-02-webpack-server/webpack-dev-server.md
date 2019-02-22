## Webpack DevServer 

<div>
  <p>Vamos começar fazendo algumas alterações em nossa estrutura, primeiro criaremos duas pastas uma nome <i><em>src</em></i> e outra com <i><em>public</em></i>, depois de criar as pastas vamos adicionar todos os arquivos <code>.js</code> que serão monitorados pelo webpack-dev-server e nesse caso será o <code>main.js</code> já em <i>public</i> ficarão os arquivos que não serão monitorados ou seja o <i>index.htmls</i> </p><br>

  <img src="../assets/webpack-dev-server-00.PNG" alt="Estrutura de pastas" >    
</div>

<div>
  <p>Com a nova estrutura de pasta que acabamos de definir, vamos alterar o nosso arquivo <code>webpack.config.js</code> para receber essas novas configurações, veja abaxo o que deve ser feito.</p> <br>

  <img src="../assets/webpack-dev-server-01.PNG" alt="Configurnado webpack-dev-server" >
  
  <ul>
    <li><b><em>Entry<em><b>: [ <em><i>recebe um novo caminho já que o nosso arquivo <code>main.js<code> foi adicionado na pasta src.<i></em> ]</li>
    <li><b><em>Path</em></b>: [<em><i> recebe <code>+ ‘/public’</code> que é o novo caminho para index.html. ]</i></em> </li>
  </ul><br>
  
  <p>Em seguida vamos instalar nosso <b><em>webpack-dev-server</em></b> no modo de desenvolvimento <i>“-D”</i> em seu terminal execute o seguinte comando:<br><br>
  <b><em> $ yarn add webpack-dev-sever –D</em></b><br>
  Após instalar webpack-dev-sever vamos voltar em nosso arquivo <code>webpack.config.js</code> realizar a seguintes alterações:
  </p><br>

  <img src="webpack-dev-server-02.PNG" alt="Configurando webpack-dev-server contentBase" >  
  <p>Veja que adicionamos uma nova configuração devServe: {} que possui uma propriedade contentBase cuja valor é igual a __dirname + ‘/public’, esse propriedade nos permite dizer onde o arquivo build de nossa aplicação será salva e especificamos esse caminho dizendo __dirname + ‘/public’ ou seja estamos salvando em nossa pasta public que contém os arquivos estáticos do nosso projeto.</p>
</div>



