<h1> Desestruturação E Valores padrões</h1>

<p>
A passagem de parâmetro é bem simples 
</p>

<div><pre>
function subtracao(a, b){
  return a - b;
}
console.log(subtracao(1,2))

const soma = (a=1, b=2) => a + b

console.log(soma())
</pre></div>

<p>
Você declara um função que recebe algum parâmetro, que pode ser iniciado com algum valor ou não.
Vamos criar um objeto de nome usuário que conterá os atributos nome, idade, endereço este terá outros dois atributos que são respectivamente cidade e UF. 
</p>

<div><pre>
const usuario = {
  nome: 'Lucas Pedro',
  idade: 27,
  endereco: {
    cidade: 'Porto',
    UF: 'TO'
  }
}
</pre></div>

<p>
O objeto acima poderia ter seus atributos acessado da seguinte maneira:
</p>

<code> const name = usuario.nome</code>
<code> const idade = usuario.idade </code>
<code> const uf = usuario.endereco.UF </code>
<code> const cidade = usuario.endereco.cidade </code>

<p>
Entretanto com as novas feacture ECAMS6+ temos uma maneira mais fácil de acessa-los usando desestruturação de objetos, veja a seguir:
</p>

<div><pre>
const { nome, idade, endereco: { cidade, UF } } = usuario

const dados = {
    nome,
    idade,
    cidade,
    UF
}
</pre></div>

<p>
Assim podemos criar um outro objeto (poderia ser qualquer coisa array, variável e etc.) de nome dados que recebe os respectivos dados de cada usuário, repare que como os nomes do atributos de usuário são iguais ao do objeto dados, então não precisamos informar o nome dos atributos em que coincidirem.
</p>

<code> nome: nome;<code>

