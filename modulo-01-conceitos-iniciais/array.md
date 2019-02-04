
<h1> Array </h1>

<p>
Antigamente para realizar qualquer operação em um vetor/array que houvesse a necessidade de manipular alguma informação, teriamos que utilizar um for ou até mesmo instalar alguma bibliotecas de terceiros, com achegada do ECS6+ podemos fazer diversas operações nos arrays como por exemplo obter um valor, criar, comparar, buscar e converter dados e outros array a partir de algumas funções específicas, a primeira função que iremos ver será o <b>map()</b>.
</p>
<strong>MAP()</strong><br>

<div><pre>
 const newArray = array.map(function(item){
    return item * 2
})


console.log(`Multiplicado por 2: ${newArray} Multiplicado pelo índece: ${newArray2}`)
</pre></div>

<div><pre>
const newArray2 = array.map(function(item, index){
    return item * index
})
</pre></div>