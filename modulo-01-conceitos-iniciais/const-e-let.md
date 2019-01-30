<h1> Const & Let </h1>

<p>
Se você utiliza o javaScript básico há algum tempo sabe que utilizamos a palavra reservada var nomeDaVariavel = “valor” para declarar/iniciar variáveis e com as novas feature de ECS6+ ganhamos mais duas novas maneiras de declaramos uma é a const e a outra é let.<br>
Uma constante não pode ter seu valor reatribuido, neste caso podemos multar seu valor e qual seria a diferencia entre multar e reatribuir valor de uma constante. Quando utilizamos a sintaxe de objetos conseguimos reatribuir os valores dos seus atributos vejamos:<br>
<code>
const a = 1<br>
a = 3 <br>
const objeto = { <br>
    nome: "Lucas",<br>
    idade: 25<br>
}<br>
objeto.idade = 25 <br>
console.log(objeto, a)<br>
</code>

</p>