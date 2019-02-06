<h1> Rest & Spread </h1>

<p>Esse operado é conhecido por utilizar três pontos seguidos <code><em>“...”<code><em> veremos como isso funciona, mas antes teremos que instalar uma dependência ao babel porque como essas novas <em><i>feactures</i></em>ainda não foram acopladas a versão principal do babel temos que adicionar um plugin.
</p>
<br><code><em>yarn add @babel/plugin-proposal-object-rest-spread</em></code><br>

<p>Após instalar o plugin vamos voltar em nosso arquivo .babelrc e criar  um sricpt para nosso plugin, ficando da seguinte maneira:
</p>
<br><div><pre>
{
   <span style="">"presets"</span>: ["@babel/preset-env"], //
    "plugins": ["@babel/plugin-proposal-object-rest-spread"]
}
</pre><div><br>
<p>
Salve as alterações e volte ao seu terminal e digite o comando yarn dev.
</p>