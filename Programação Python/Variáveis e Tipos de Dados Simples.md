Neste capítulo conheceremos os diferentes tipos de dados com os quais podemos trabalhar em nossos programas Python. Aprenderemos também a ==armazenar dados em variáveis e usar essas variáveis em nossos programas.==

##### Variáveis:
Vamos experimentar usar uma variável. Acrescente uma nova linha no início do arquivo e modifique a segunda linha:
`message = "Hello Python world!"`
`print(message)` 
Você deverá ver a mesma saída vista anteriormente: Hello Python world! ==Acrescentamos uma variável chamada message.== Toda variável armazena um valor, que é a informação associada a essa variável. Nesse caso, o valor é o texto “Hello Python world!”. Acrescentar uma variável implica um pouco mais de trabalho para o interpretador Python. Quando processa a primeira linha, ele associa o texto “Hello Python world!” à variável message. Quando chega à segunda linha, o interpretador exibe o valor associado à message na tela.
Podemos mudar o valor de uma variável em nosso programa a qualquer momento, e Python sempre manterá o controle do valor atual.

###### Nomeando e usando variáveis:
Ao usar variáveis em Python, é preciso seguir algumas regras e diretrizes. Quebrar algumas dessas regras provocará erros; outras diretrizes simplesmente ajudam a escrever um código mais fácil de ler e de entender. Lembre-se de ter as seguintes regras em mente: • ==Nomes de variáveis podem conter apenas letras, números e underscores.== Podem começar com uma letra ou um underscore, mas não com um número. Por exemplo, podemos chamar uma variável de message_1, mas não de 1_message. 
• Espaços não são permitidos em nomes de variáveis, mas underscores podem ser usados para separar palavras em nomes de variáveis. Por exemplo, greeting_message funciona, mas greeting message causará erros. 
• Evite usar palavras reservadas e nomes de funções em Python como nomes de variáveis, ou seja, não use palavras que Python reservou para um propósito particular de programação, por exemplo, a palavra print. (Veja a seção “Palavras reservadas e funções embutidas de Python”.) 
• Nomes de variáveis devem ser concisos, porém descritivos. Por exemplo, name é melhor que n, student_name é melhor que s_n e name_length é melhor que length_of_persons_name. 
• Tome cuidado ao usar a letra minúscula l e a letra maiúscula O, pois elas podem ser confundidas com os números 1 e 0.

Quando houver um erro em seu programa, o interpretador Python faz o melhor que puder para ajudar você a descobrir onde está o problema. O interpretador oferece um traceback quando um programa não é capaz de executar com sucesso. ==Um traceback é um registro do ponto em que o interpretador se deparou com problemas quando tentou executar seu código.== Eis um exemplo do traceback fornecido por Python após o nome da variável ter sido digitado incorretamente por engano: 
`Traceback (most recent call last): u File "hello_world.py", line 2, in v print(mesage) w NameError: name 'mesage' is not defined` 
A saída em u informa que um erro ocorreu na linha 2 do arquivo hello_world.py. O interpretador mostra essa linha para nos ajudar a identificar o erro rapidamente v e informa o tipo do erro encontrado w. Nesse caso, ele encontrou um erro de nome e informa que a variável exibida, mesage, não foi definida. Python não é capaz de identificar o nome da variável especificada. Um erro de nome geralmente quer dizer que esquecemos de definir o valor de uma variável antes de usá-la ou que cometemos um erro de ortografia quando fornecemos o nome da variável. É claro que, nesse exemplo, omitimos a letra s do nome da variável message na segunda linha. O interpretador Python não faz uma verificação de ortografia em seu código, mas garante que os nomes das variáveis estejam escritos de forma consistente.

#### Strings
Como a maior parte dos programas define e reúne algum tipo de dado e então faz algo útil com eles, classificar diferentes tipos de dados é conveniente. O primeiro tipo de dado que veremos é a string. As strings, à primeira vista, são bem simples, mas você pode usá-las de vários modos diferentes. ==Uma string é simplesmente uma série de caracteres. Tudo que estiver entre aspas é considerada uma string em Python, e você pode usar aspas simples ou duplas em torno de suas strings==, assim: 
`"This is a string."` 
`'This is also a string.'` 
Essa flexibilidade permite usar aspas e apóstrofos em suas strings: 
'I told my friend, "Python is my favorite language!"' 
"The language 'Python' is named after Monty Python, not the snake."
"One of Python's strengths is its diverse and supportive community."

##### Mudando para letras maiúsculas e minúsculas em uma string usando métodos 
Uma das tarefas mais simples que podemos fazer com strings é mudar o tipo de letra, isto é, minúscula ou maiúscula, das palavras de uma string. Observe o código a seguir e tente determinar o que está acontecendo: 
`name.py`
`name = "ada lovelace"` 
`print(name.title())` 
Salve esse arquivo como name.py e então execute-o. Você deverá ver esta saída: 
`Ada Lovelace` 
Nesse exemplo, a string com letras minúsculas "ada lovelace" é armazenada na variável name. O método title() aparece depois da variável na instrução print(). ==Um método é uma ação que Python pode executar em um dado.== O ponto (.) após name em name.title() informa a Python que o método title() deve atuar na variável name. Todo método é seguido de um conjunto de parênteses, pois os métodos, com frequência, precisam de informações adicionais para realizar sua tarefa. Essas informações são fornecidas entre os parênteses. A função title() não precisa de nenhuma informação adicional, portanto seus parênteses estão vazios.
==itle() exibe cada palavra com uma letra maiúscula no início. Isso é útil, pois, muitas vezes, você vai querer pensar em um nome como uma informação. Por exemplo, você pode querer que seu programa reconheça os valores de entrada Ada, ADA e ada como o mesmo nome e exiba todos eles como Ada.== Vários outros métodos úteis estão disponíveis para tratar letras maiúsculas e minúsculas também. Por exemplo, você pode mudar uma string para que tenha somente letras maiúsculas ou somente letras minúsculas, assim: 
`name = "Ada Lovelace"`
`print(name.upper())` 
`print(name.lower())` 
Essas instruções exibirão o seguinte: 
`ADA LOVELACE` 
`ada lovelace` 
O método lower() é particularmente útil para armazenar dados. ==Muitas vezes, você não vai querer confiar no fato de seus usuários fornecerem letras maiúsculas ou minúsculas, portanto fará a conversão das strings para letras minúsculas antes de armazená-las.== Então, quando quiser exibir a informação, usará o tipo de letra que fizer mais sentido para cada string.

#### Combinando ou concatenando strings
Muitas vezes, será conveniente combinar strings. Por exemplo, você pode
querer armazenar um primeiro nome e um sobrenome em variáveis
separadas e, então, combiná-las quando quiser exibir o nome completo de
alguém:
`first_name = "ada"`
`last_name = "lovelace"`
`u full_name = first_name + " " + last_name`
`print(full_name)`
Python usa o símbolo de adição (+) para combinar strings. Nesse
exemplo, usamos + para criar um nome completo combinando first_name,um espaço e last_name u, o que resultou em:
ada lovelace
Esse método de combinar strings se chama concatenação.
Podemos usar concatenação para compor uma mensagem e então
armazenar a mensagem completa em uma variável:
`first_name = "ada"`
`last_name = "lovelace"`
`full_name = first_name + " " + last_name`
`u message = "Hello, " + full_name.title() + "!"`
`v print(message)`
Esse código também exibe a mensagem “Hello, Ada Lovelace!”, mas
armazenar a mensagem em uma variável em u deixa a instrução print final
em v muito mais simples.

#### Acrescentando espaços em branco em strings com tabulações ou quebras
#### de linha
Em programação, espaços em branco se referem a ==qualquer caractere que
não é mostrado, como espaços, tabulações e símbolos de fim de linha.
Podemos usar espaços em branco para organizar a saída de modo que ela seja mais legível aos usuários.==
**Para acrescentar uma tabulação em seu texto, utilize a combinação de**
**caracteres \t como mostrado em u:**
```
>>> print("ola")
ola
>>> print("\tola")
	ola
```
**Para acrescentar uma quebra de linha em uma string, utilize a**
**combinação de caracteres \n:**
```
print("Languages:\nPython\nC\nJavaScript")
Languages:
Python
C
JavaScript
```
Também podemos combinar tabulações e quebras de linha em uma única
string. A string "\n\t" diz a Python para passar para uma nova linha e
iniciar a próxima com uma tabulação**. O exemplo a seguir mostra como**
**usar uma string de uma só linha para gerar quatro linhas na saída:**
```
>>> print("Languages:\n\tpython\n\tC\n\tJavaScript")
Languages:
	python
	C
	JavaScript
```

#### Removendo espaços em branco
Espaços em branco extras podem ser confusos em seus programas. Para os
programadores, 'python' e 'python ' parecem praticamente iguais.
Contudo, para um programa, são duas strings diferentes. Python identifica
o espaço extra em 'python ' e o considera significativo, a menos que você
informe o contrário.
É importante pensar em espaços em branco, pois, com frequência, você
vai querer comparar duas strings para determinar se são iguais. Por
exemplo, ==uma situação importante pode envolver a verificação dos nomes
de usuário das pessoas quando elas fizerem login em um site.== Espaços em
branco extras podem ser confusos em situações muito mais simples
também. Felizmente, Python facilita eliminar espaços em branco extras dos
dados fornecidos pelas pessoas.
==Python é capaz de encontrar espaços em branco dos lados direito e
esquerdo de uma string.== Para garantir que não haja espaços em branco do
lado direito de uma string, utilize o método rstrip().
```
u >>> favorite_language = 'python '
v >>> favorite_language
'python '
w >>> favorite_language.rstrip()
'python'
x >>> favorite_language
'python '
```
O valor armazenado em favorite_language em u contém um espaço em
branco extra no final da string. Quando solicitamos esse valor a Python em
uma sessão de terminal, podemos ver o espaço no final do valor v. Quando
o método rstrip() atua na variável favorite_language em w, esse espaço
extra é removido. ==Entretanto, a remoção é temporária. Se solicitar o valor
de favorite_language novamente, você poderá ver que a string é a mesma
que foi fornecida, incluindo o espaço em branco extra x.==
Para remover o espaço em branco da string de modo permanente, você
deve armazenar o valor com o caractere removido de volta na variável:
```
>>> favorite_language = 'python '
u >>> favorite_language = favorite_language.rstrip()
>>> favorite_language
'python'
```
Para remover o espaço em branco da string, você deve remover o espaço
em branco do lado direito da string e então armazenar esse valor de volta
na variável original, como mostrado em u. Alterar o valor de uma variável e
então armazenar o novo valor de volta na variável original é uma operação frequente em programação. É assim que o valor de uma variável pode
mudar à medida que um programa é executado ou em resposta à entrada
de usuário.
Também podemos remover espaços em branco do lado esquerdo de uma
string usando o método lstrip(), ou remover espaços em branco dos dois
lados ao mesmo tempo com strip():
```
u >>> favorite_language = ' python '
v >>> favorite_language.rstrip()
' python'
w >>> favorite_language.lstrip()
'python '
x >>> favorite_language.strip()
'python'
```
Nesse exemplo, começamos com um valor que tem espaços em branco
no início e no fim u. Então removemos os espaços extras do lado direito
em v, do lado esquerdo em w e de ambos os lados em x. Fazer
experimentos com essas funções de remoção pode ajudar você a ter
familiaridade com a manipulação de strings. No mundo real, essas funções
de remoção são usadas com mais frequência para limpar entradas de
usuário antes de armazená-las em um programa.

#### Evitando erros de sintaxe com strings pg67