<h1> Trabalhando com import & Expport </h1>

  <p>Em sequência vamos colocar o nosso webpack pra rodar, vá em seu terminal e digite <b>yarn dev</b>. Para testarmos esse webpack vamos começar a trabalhar com <em>import/export </em>e antes de mais nada alteraremos o arquivo <em>index.js</em> que atualmente recebe em seu script o <em>main.js</em> e vamos alterar para <em>bundle.js</em>.
  </p><br>

  <p>Vamos então criar um novo arquivo de nome funções.js que conterá as seguintes funções: </p>

  <img src="../assets/import-export-funcoes.PNG" name="img-importe-export" alt="img-import-export" height="321" width="636" >
  
  <div>
    <p>Então dentro do arquivo <code>main.js</code> vamos importa as funções que acabamos de criar em nosso arquivo <i><em>funcoes.js</em></i></p><br>
    <img src="../assets/import-export-funcoes-02.PNG" height="128" width="633">
    <p>Note que todas as funções do arquivo funcoes.js estão sendo importadas para dentro do <code>main.js</code> <b></i>import {soma, dev, mult, sub } from './funcoes'</i></b> onde desta maneira podemos utiliza-las, perceba que todas as funções importadas foram passada entre o abrir e fechar de uma chave, isso ocorrer porque tudo que quisermos exportar seja funções, objetos, variável, classes e etc, e não declararmos o <code>default</code> então devemos fazer o uso das chaves.</p>
    <p>Cada arquivo .js só pode ter apenas um propriedade <code>default</code> ou seja, em nosso exemplo do arquivo funcoes.js somente uma das funções poderia receber a propriedade default.</p>
  </div>
  <div>
  <h4>Veja outros exemplos de import e export:</h4>

  <img src="../assets/import-export-funcoes-03.PNG" name="img-importe-export-03" alt="img-import-export-03" height="233" width="631" >

  <p>Quando definimos um export como <code>default</code> podemos importa-la sem a necessidade de usar as chaves entre ela e o mesmo pode ser renomeada para qualquer nome que desejar, foi o que aconteceu em somaFuncao, para obtermos os mesmos resultados sem utilizar default precisamos do <code>“as”</code> nesse caso deve ser passado entre chaves pois não estamos utilizando default, ficando da seguinte forma <code>import { sub as subtração } from “./funções”</code> .
  </p>
</div>

