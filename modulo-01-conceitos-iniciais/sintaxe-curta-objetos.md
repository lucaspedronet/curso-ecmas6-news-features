<h1> Sintaxe curta objetos </h1>

<p>Em muitos caso temos a necessidade de criar um objeto a partir de outras informações, objetos e variáveis, veremos como fazer esse processo de modo bem mais prático, acompanhe o trecho de código asseguir.
</p>

<br><code>// <b>SEM</b> SINTAXE CURTA DE OBJETOS </code><br>

<div><pre>
const nome = 'Lucas Pedro'
const idade = 23
const cidade = 'Porto Nacional'

<span style="text-color={}">const </span> dados = {
  nome: nome,
  idade: idade,
  cidade: cidade
}
</pre></div>

<p>Perceba que objeto <em>dados</em> possui atributos cuja os nomes iguais as das constantes, cada atributo recebe respectivamente o valores da contante atribuido ao atributo correspondente, quando temos essa situação é possível deixar nosso código menos verboso, pois sempre que tivermos o nome do atributo igual ao de variável/constante/objeto podemos então retirar da variável que esta setando um valor no atributo. Veja como ficaria nosso exemplo com asaplicando essa nova feacture do ECAMS6+:
</p>

<code>// COM SINTAXE CURTA DE OBJETOS</code>
<div><pre>
const dados = {
  nome,
  idade,
  cidade
}
</div></pre>

<p>Desta maneira conseguimos aplicar a sintaxe curta de objetos, se dermos um <code>console.log(dados.nome)</code> teremos <code>// Lucas Pedro</code>
</p>