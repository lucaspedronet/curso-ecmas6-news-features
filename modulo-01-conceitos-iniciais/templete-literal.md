<h1> Templete Literal </h1>

<p>É uma forma de incluir variáveis/constantes/objetos dentro de string no javascript ES6+ tornando-a menos verbosa.</p>

<div>
 <pre>
  // SEM TEMPLETE LITEREL
  const empresa = 'Pulso Criativo'
  const ano = 2017
  const msg = 'Minha empresa '+ empresa + ' foi criada no ano de '+ ano+'.'
  console.log(msg)
 </pre>
</div>

<p>No exemplo acima utilizamos o operador “+” para concatenar as string e variáveis, no exemplo abaixo vejamos como utilizamos o templete Literal.</p>

<div>
 <pre>
  const mensagem = `Minha empresa <span >${</span>empresa} foi criada no ano de ${ano}.`
  console.log(mensagem)
 </pre>
</div>

<p>Agora substituímos as aspas pela sinal de crase e quando queremos utilizar alguma variável chamamos ${} passando a variável entre chaves.</p>