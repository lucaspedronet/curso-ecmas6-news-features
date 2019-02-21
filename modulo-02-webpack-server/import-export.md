<h1> Trabalhando com import & Expport </h1>

  <p>Em sequência vamos colocar o nosso webpack pra rodar, vá em seu terminal e digite <b>yarn dev</b>. Para testarmos esse webpack vamos começar a trabalhar com <em>import/export </em>e antes de mais nada alteraremos o arquivo <em>index.js</em> que atualmente recebe em seu script o <em>main.js</em> e vamos alterar para <em>bundle.js</em>.
  </p><br>

  <p>Vamos então criar um novo arquivo de nome funções.js que conterá as seguintes funções: </p>

  <img src="../assets/import-export-funcoes.PNG" name="img-importe-export" alt="img-import-export" height="321" width="636" >

  <div>
    <p>Então dentro do arquivo <i>main.js</i> vamos importa as funções que acabamos de criar em nosso arquivo <i>funcoes.js</i></p>
  
    <img src="../assets/import-export-funcoes-02.PNG" height="128" width="633"/>
  
    <p>Chamamos as funções entre chaves do arquivo <i><em>./funções</em></i> isso é bastante utilizado em bibliotecas como react e reac-native por exemplo, também conseguimos atribuir um default para alguma função, classe e etc porém apenas uma pode ser definida por arquivo. Bastando colocar a palavra default após o export ficando <b><em>export default function soma()</em></b>.
    </p>
  </div>

<div>
  <h4>Veja outros exemplos de import e export:</h4>

  <img src="../assets/import-export-funcoes-03.PNG" name="img-importe-export-03" alt="img-import-export-03" height="233" width="631" >

  <p>Quando definimos um export como <code>default</code> podemos importa-la sem a necessidade de usar as chaves entre ela e o mesmo pode ser renomeada para qualquer nome que desejar, foi o que aconteceu em somaFuncao, para obtermos os mesmos resultados sem utilizar default precisamos do <code>“as”</code> nesse caso deve ser passado entre chaves pois não estamos utilizando default, ficando da seguinte forma <code>import { sub as subtração } from “./funções”</code> .
  </p>
</div>

