# Primeiros passos em programação (com Python)

Olá, amor :). Bem-vinda a um guia que tenta pincelar sobre conceitos básicos de
programação e usa Python pra isso.

A ideia desse primeiro tutorial é configurar seu ambiente de trabalho (seu
laptop) para que você possa começar a escrever programas sem problemas e de
maneira organizada.

No final desse tutorial você:
- Vai ter um editor de texto instalado
- Vai ter o interpretador Python 2.7 instalado
- Vai executar um programa "Olá, mundo!" com sucesso

## Instalando um editor de texto

O primeiro passo pra poder começar a brincar de programar é ter um editor de
texto que preste, porque?

- Você precisa de algo que não seja agressivo aos olhos,
já que você vai passar um tempo na frente dele, codando
- Tem vários utilitários já prontos e integrados pra facilitar sua vida

Vamos instalar o Atom, ele foi feito pela galera do Github e é um editor de
texto bem moderno e popular, escrito em JavaScript. Para baixar ele, vá
[nesse site](www.atom.io) e clique no botão meio vermelho de Download. Espere
acabar de baixar e instale.

Abra o Atom. De primeira vai ter um monte de coisa à mostra, respire, tome seu
tempo e dê uma lida superficial em tudo, a maioria é inútil agora, mas pode ser
bom saber que existem :).

Acabou de ler e tem uma aba nova pra escrever coisas? Parabéns, primeira etapa
concluída com sucesso!!!

## Instalando o Python

Agora vamos instalar o interpretador Python, que nada mais é do que um programa
que lê seu código em Python e o *interpreta* para uma linguagem que o computador
entenda. É chamado de interpretação porque cada comando é interpretado em
seguida do outro, ao contrário da compilação normal, mas não vou entrar muito
nisso.

Entre [aqui](https://www.python.org/downloads/release/python-2714/) para baixar
o Python, você quer a opção *Windows x86-64 MSI installer*. Como normal, espere
o download acabar e abra o aplicativo baixado. Pode dar "Next" em tudo com as
opções padrão mesmo! Seu Python está instalado!

### Verifique sua instalação

Vamos verificar que o Python está instalado corretamente. Abra um *Terminal*
(ou *Prompt de Comando*, ou *Command Prompt*) e tente rodar o comando:

`python --version`

Caso tudo tenha dado certo, a resposta no terminal será algo como:

`Python 2.7.14`

Caso você receba uma outra mensagem, como por exemplo:

```
'python' is not recognized as an internal or external command,
operable program or batch file.
```

Não se desespere! Significa que o terminal não achou o programa do Python, isso
normalmente quer dizer que o terminal tá procurando nos lugares comuns de
programas e não achou o Python! Precisamos botar o Python na lista de
"programas comuns" do Windows. Como fazer isso:

1. Botão direito em "Meu computador", "Propriedades".
1. Clicar em "Configurações avançadas do sistema"
1. Na nova janela que abriu, clicar em "Variáveis de ambiente" (tá pro final
  da tela)
1. Procure pela variável "Path", marque ela e clique em "Editar". Veja a imagem
![Variável de ambiente](img/path-variable.png)
1. Clique em "Nova", ou "Adicionar" e escreva o diretório de
instalação do seu Python, o padrão é `C:\Python27`.
1. Clique OK em tudo para sair dessas janelas doidas e salvar.
1. Abra um **NOVO** terminal
1. Tente executar novamente o comando `python --version`, deve
exibir a mensagem certa dessa vez.
1. Caso não apareça a mensagem certa, verifique onde instalou o
Python, ou tente reinstalá-lo.

## Olá, mundo!

Agora vamos escrever nosso primeiro programa! Como tradição, escreveremos um
"Hello world", mas em versão tupiniquim.

Abra seu Atom e, em uma aba vazia, digite o seguinte código:

```
#!/usr/bin/python

print "Ola, mundo!"
```

Salve esse arquivo como `olamundo.py`. Como você deve ter imaginado, `py` é a
extensão dos arquivos em Python. Agora, no seu terminal, navegue até a pasta
onde você salvou seu programa.

Dicas: `dir` lista todos os arquivos da pasta
em que você está, e `cd <nome_da_pasta>` navega até a pasta <nome_da_pasta>.

Quando você conseguir chegar na pasta certa, no seu terminal, execute:

`python olamundo.py`

Você deve ver a mensagem "Ola, mundo" no seu terminal! Caso alguma coisa dê
errado, tente ver a mensagem de erro, você pode ter cometido algum erro de
digitação na hora de escrever o código!

Esse código que escrevemos usa 2 coisas, a primeira linha é um comentário,
e é apenas um aviso de que esse é um programa em Python, caso não tivesse a
extensão .py no arquivo, esse comentário seria usado para saber que é Python.

A segunda linha, `print "Ola, mundo!"` chama a função `print`, disponível no
Python, passando a *String* (cadeia de caracteres) *Ola, mundo!* como
parâmetro. A função `print` exibe o que você pedir no terminal!

### Bônus

Quer ver o "Olá, mundo!" com acento agudo no *a*? É possível! Basta avisar
ao Python que você está tentando exibir uma *String* (cadeia de caracteres)
que tem caracteres com acento. Para isso o código de `olamundo.py` vira:

```
#!/usr/bin/python
# -*- coding: utf-8 -*-

msg = "Olá, mundo!"
print msg.decode("utf-8")
```

As diferenças para o código anterior são um comentário mágico,
`# -*- coding: utf-8 -*-`, que avisa ao Python que você tá usando caracteres
especiais (fora do alfabeto americano).

E na segunda parte, definimos uma variável! A variável `msg` recebe o valor
"Olá, mundo!", e ao invés de passar a String direto pra função `print`, damos
um passo a mais, usamos o valor na variável `msg` para isso. O
`.decode("utf-8")` avisa à função `print` que é uma String com caracteres
especiais.

Tente rodar o programa de novo `python olamundo.py` e veja
o que acontece!

## Conclusão

É isso pro primeiro dia! É muita coisa de uma vez só, e por um tempo, o código
vai parecer mágica e totalmente não intuitivo, mas com os próximos passos, vai
ficar cada vez mais claro o que cada coisa faz!
