<h1>ARROW FUNCTION</h1>
<p>
Arrow function é uma maneira mais simples de escrever funções e com algumas vantagens a mais sobre as tradicionais funções, acompanhe o exemplo abaixo.
</p>
<code>
const array = [1,2,3,7,5,1, "Lucas", 1.33]

const somaArray = array.map(function soma(item){
    return item + 2
})

</code>
<p>
Acima temos a forma tradicional sem função de seta, com uma função de nome soma que retorna a soma de cada item da interação ao número 2.
</p>

<code>
const somaArray = array.map(function(item) {
    return item + 2
})

</code>

<p>
Transformamos a função soma em uma função anônima removendo seu nome “soma”.
</p>

<code>
const somaArray = array.map((item) => {
    return item + 2
})
</code>

<p>
Aqui removemos a palavra reservada function e adicionamos o sinal de e igualdade “=” e em seguida o sinal de maior “>” após o parâmetro de função, formando assim o símbolo da arrow e transformando nossa antiga função soma em uma nova função de arrow function. Ainda conseguimos reduzir um pouco mais essa função, veja no exemplo.
</p>´

<code>
const somaArray = array.map(item => item + 2)
</code>

<p>
No caso acima temos a função arrow ainda mais otimizada pois como existia apenas uma única linha de código em no corpo da função arrow podemos retirar o return e passa-lo na mesma linha do parâmetro.
</p>