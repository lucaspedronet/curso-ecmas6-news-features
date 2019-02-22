<h1> Const & Let </h1>

<p>
Se você utiliza o javaScript básico há algum tempo sabe que utilizamos a palavra reservada var nomeDaVariavel = “valor” para declarar/iniciar variáveis e com as novas feature de ECS6+ ganhamos mais duas novas maneiras de declaramos uma é a const e a outra é let.<br>
Uma constante não pode ter seu valor reatribuido, neste caso podemos multar seu valor e qual seria a diferencia entre multar e reatribuir valor de uma constante. Quando utilizamos a sintaxe de objetos conseguimos reatribuir os valores dos seus atributos vejamos:<br>
</p>
<div><pre>
function somar(a1){
    let y = 10
    if (a1 > y){
        let y = 5 //essa variável y é diferente da que foi criada anteriomente.
        return a1 + y
    }
}
console.log(somar(30))
