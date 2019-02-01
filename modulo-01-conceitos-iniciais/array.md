<h1> Array </h1>

<p>
Antigamente para realizar qualquer operação em um vetor/array e que fosse necessário manipular alguma informação, teriamos que utilizar um for ou até mesmo instalar bibliotecas de terceiros, com achegada do ECS6+ podemos fazer diversas operações nos arrays como por exemplo obter um valor, criar, comparar, buscar e converter dados e outros array a partir de algumas funções especificas, a primeira função que iremos ver será o <b>map()</b>.
</p>
<strong>MAP()</strong>
<code>
 const newArray = array.map(function(item){<br>
    return item * 2<br>
})<br><br>

const newArray2 = array.map(function(item, index){<br>
    return item * index<br>
})<br><br>

console.log(`Multiplicado por 2: ${newArray} Multiplicado pelo índece: ${newArray2}`)
</code>

