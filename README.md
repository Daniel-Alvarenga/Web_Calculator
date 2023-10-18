# Web_Calculator
Web calculator inspired by the native calculator of w11

[Acesse o site aqui][link]

[link]: https://dra-calculadora.netlify.app/


https://github.com/Daniel-Alvarenga/Web_Calculator/assets/128755697/162afeaf-71f4-4c92-9da5-d53d39b67390


Esse repositório contém os arquivos de uma página web que simula uma calculadora nativa, semelhante à do Windows 11.
Ela pode ser minimizada, encerrada e maximizada, e além de fazer os cálculos simples que se propõe a fazer (soma, subtração, multiplicação e divisão), através de uma interface mais reclusa ao uso mobile (a entrada de valores é apenas pelos botões da tela), a calculadore possui uma memória temporária, que armazena suas últimas operações.
A principal função empregada no desenvolvimento do projeto foi a função eval de JavaScript, que dentre suas funcinalidades, permite com que uma string que representa uma série de números e simbolos que representam uma operação matemática, possa ser interpretada como tal.

Aqui está o seu uso:

```javascript
  var expression = new String(document.getElementById("input2").value);
  document.getElementById("input2").value = eval(expression.toString());
```

Para fins de exemplo, a expressão pode ser "1 + 1 + 5", e com o uso de eval teremos o resultado 5 calculado.

O uso dessa função permite com que o usuário realmente faça cálculos com expressões mais extensas, com mais de dois números sendo operados.
Outra coisa relacionada à aplicação de funções interessante que foi usada é a questão do acesso de uma mensa função para todos os botões numéricos, onde o que muda é apenas o parâmetro que identifica qual o número "pressionado" pelo usuário:

```html
<button class="btn" onclick="bnt (0)" id="bntev3">0</button>
<button class="btn" onclick="bnt (1)" id="bntev3">1</button>
  ...
<button class="btn" onclick="bnt (9)" id="bntev3">9</button>
```

A função responsável por icrementar o número à string que será usada para o cálculo posteriormente que chamam é a mesma:

```javascript
function bnt(q){
    var valor0 = new String(document.getElementById("input2").value);
    if((document.getElementById("input1").value).includes(" =") && !valor0[valor0.length-1].includes(".") && !document.getElementById("input2").value == "" ){
        document.getElementById("input1").value = "";
        document.getElementById("input2").value = "";
    }
    if(document.getElementById("input2").value .includes("Não é possível dividir por zero" ) || document.getElementById("input2").value == "Resultado indefinido "){
        document.getElementById("input2").value = "";
    }
    input2.style.fontSize = "45px";
    if(document.getElementById("input2").value == "0"){
        document.getElementById("input2").value = "";
    }
    var valor = new String(document.getElementById("input1").value);
    var carp = "+-*/×÷";
    if(carp.includes(valor[(valor.length)-2])  && !valor0[(valor0.length)-1].includes("(") && !valor0[(valor0.length)-1].includes("-") && y == 1){
        document.getElementById("input2").value = "";
    }
    document.getElementById("input2").value = document.getElementById("input2").value  + q;
    y = 0;
}
```

Apesar de ter um funcionamento considerável quanto à execuçaõ de scripts, essa calculadora deixa a desejar no quesito estilização, haja visto que é um projeto que fiz há quase 1 ano, quando estava iniciando os estudos sobre CSS.
Por fim agradeço quem leu até aqui!

Stop, think and code...
