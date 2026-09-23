Para testar o que acabamos de ver sobre variáveis e operadores, tente resolver o seguinte exercício proposto pelo autor:

**Escreva um programa que exiba o resultado de** $2a \times 3b$**, onde** $a$ **vale 3 e** $b$ **vale 5.** _Dica: Na matemática escrevemos_ $2a$_, mas no Python você precisa indicar explicitamente a multiplicação usando o asterisco (__*__)._

	R:  

**Faça um programa que peça dois números inteiros ao usuário (usando** **input****). Calcule e imprima a soma desses dois números na tela.** _Dica: Lembre-se de usar_ _int(input(...))_ _para que o Python faça a soma matemática e não a junção dos textos!_

	R: a = int(input("Digite um número: "))
	 b = int(input("Digite outro número: "))
	  print("O resultado da soma é:", a + b)
	  

**Escreva um programa que pergunte a velocidade do carro de um usuário. Caso ultrapasse 80 km/h, exiba uma mensagem dizendo que o usuário foi multado. Nesse caso, calcule e exiba o valor da multa, cobrando R$ 5,00 por cada km acima de 80 km/h.**

	R: a = int(input("Quantos km/h você está nesse exato momento?"))

if a <= 80: print("Continue assim! Você é um motorista exemplar.")
else:
	calc = (a - 80) * 5
		 print(f"Você foi multado em: {calc} reais por excesso de velocidade")



Vamos criar um programa que apenas pergunta a idade de uma pessoa e decide:

- **Se** a idade for **maior ou igual a 18**, ele diz: `"Você pode entrar!"`
- **Senão** (se for menor), ele diz: `"Entrada proibida para menores!"`

Esse programa não precisa de contas, apenas de uma comparação simples (`>= 18`).

	R: idade = int(input("Qual sua idade?"))

if idade < 18: 
	print("Entrada proibida para menores!") else: print("Você pode entrar!")




**Escreva um programa para exibir uma contagem regressiva para o lançamento de um foguete. O programa deve imprimir** **10, 9, 8, ..., 1, 0** **e, no final, a palavra** **"Fogo!"** **na tela.**

	R: foguete = 10 print("O foguete partirá em")

while foguete >= 0:
	print(foguete) 
	foguete = foguete - 1

print("Fogo!")


**Escreva um programa que peça para o usuário digitar o preço de 3 produtos (um de cada vez). No final, o programa deve exibir o valor total da compra.**

	R: contador = 1 
	total = 0
	 while contador <= 3: 
	 preço = float(input(f"Digite o número do produto {contador}: R$ "))
	  total = total + produto
	   contador = contador + 1

print("A soma de todos os produtos é: R$", total)




Imagine que você está guardando dinheiro em um cofrinho eletrônico. Você quer ir adicionando valores (depósitos) de forma contínua.

- O programa deve pedir para você digitar um valor de depósito.
- Se você digitar **0**, o programa entende que você terminou de guardar dinheiro, interrompe a repetição imediatamente usando o **break** e mostra o saldo total acumulado.

	R: Valor_depositado = 0 
	while True: 
	Valor_depositar = float(input("Digite um valor de depósito: R$ "))
	 if Valor_depositar == 0:
		  break
	   Valor_depositado = Valor_depositado + Valor_depositar

print(f"Total depositado é de: R$ {Valor_depositado}")



Para unir esses dois conceitos incríveis (adicionar itens e listá-los), tente escrever este programa:

**Escreva um programa que peça para o usuário digitar os nomes de 3 convidados para uma festa (adicionando cada um deles à lista usando** **.append()****). No final, utilize a estrutura** **for** **para exibir todos os nomes da lista de convidados, um por um.**

_Dica de estrutura:_

1. Crie uma lista vazia chamada `convidados = []`.
2. Use um loop `while` de 3 rodadas (ou pergunte 3 vezes seguidas com `input`) para ler os nomes e adicioná-los com `convidados.append(...)`.
3. Fora do loop, use o `for` para mostrar a lista final.

Como ficaria o seu código para esse desafio? Escreva aqui e vamos testar juntos!

	R: 
	```
convidados = [ ]
lista_convidados = 0

while lista_convidados < 3:
    nome = input("Digite o nome do convidado: ")
    convidados.append(nome)
    lista_convidados = lista_convidados + 1 

print("Lista de Convidados")
for convidado in convidados:
    print(convidado)
```




imagine que temos a seguinte string:

```
texto = "Programação"
```

Responda para mim:

1. **O que o comando** **print(texto[0:4])** **vai exibir na tela?** _(Dica: conte com calma os andares começando do 0, lembrando que o índice 4 fica de fora!)_
2. **O que acontece se tentarmos executar** **texto = "p"****?**
   
	   R: 
	   nome = input("Digite seu nome:")
	    print(f"nome entrou no sistema")