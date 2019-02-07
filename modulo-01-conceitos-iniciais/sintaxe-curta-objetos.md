<h1> Sintaxe curta objetos </h1>

<p>Em muitos caso temos a necessidade de criar um objeto a partir de outras informações a partir de outros objetos e variáveis então veremos como faremos esse processo mais prático.
</p>

<br><code>// SEM SINTAXE CURTA DE OBJETOS </code><br>
<div><pre>
const nome = 'Lucas Pedro'
const idade = 23
const cidade = 'Porto Nacional'

const dados = {
  nome: nome,
  idade: idade,
  cidade: cidade
}
</pre></div>

<p>Perceba que existe uma redundância entre os nomes dos atributos do objetos e as variáveis, para corrigir isso as novas feacture ECAMS6+ elimina os nomes que coincidirem, veja como fica:
</p>

<code>// COM SINTAXE CURTA DE OBJETOS
const dados = {
  nome,
  idade,
  cidade
}