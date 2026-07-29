# MER

Este documento descreve o que é MER e como e porque utilizá-lo.

# O que é o MER?

O MER é a sigla para Modelo Entidade Realcionamento. Ele é, basicamente, um **desenho** 
representando nosso banco de dados e como nossas **entidades** (que serão nossas
tabelas depois) se ligam e se **relacionam**.

## Porque preciso fazer esse desenho? Não é mais fácil só fazer o banco?

É sim possível criar o banco sem fazer o MER. Porém, o MER faz parte do *planejamento* do
nosso banco de dados. É como fazer um prédio sem desenhar a planta antes. É possívelk, mas
 garanto que voce não ia querer morar nele.

 Ao fazer o MER, nós estamos cuidando para que nosso banco saia exatamente como
 necessário, sem mais nem menos. Assim, evitamos retrabalho lá na frente.

## Onde e como eu posso fazer este desenho?

O MER pode ser feito em qualquer plataforma ou progama que permita desenhar. Existem
progamas específicos para trabalhar com ele, mas voce pode usar até mesmo o Canva, o
Photoshop, o Paint ou até mesmo numa folha de papel. No entanto, eu recomendo utilizar os
progamas específicos como o BrModelo:

- https://www.brmodeloweb.com/

## Qual o passo a passo para desenharmos? 

Antes de fazermos o MER precisamos primeiro ter definido quais as **entidades** (tabelas) e
ter feito o **dicionáro de dados** (aquela lista que define os campos e os tipos de 
dados destes campos). Então, podemos começar desenhando as entidades no MER. Elas são
respresentadas por **retangulos** com o nome dentro.

Os atributos que nós planejamos anteriormente para estas **entidades** também devem
aparecer no desenho (assim sabemos como construir as tabelas depois só olhar o desenho). 
Eles são representados por bolinhas sem fundo, ou "brancas".

**ATENÇÃO** se um atributo for uma **chave primária** ele será representado por uma bolinha 
preenchida, ou "preta".

Ambas devem estar ligadas ás entidades (retangulos) por **linhas**.

## Relacionamentos

Para podermos criar as **chaves estrangeiras**, que são os campos que ligam uma tabela 
em outra, normalmente pegando emprestado a **chave primária** de outra tabela. Não 
usamos bolinhas para representá-las, e sim **losangos** com linhas ligando as entidades 
em questão. Dentro deste losango, damos um título para a relação. Por exemplo, um
**aluno** *pertence* á uma **turma**, ou então um **cliente** *compra* uma **bicicleta**.

Um passo importante para entender vos relacionamentos é a **cardinalidade**. Ela nos ajuda a
entender quantos registros de uma tabelka conseguem se relacionar com quantos de outra tabela. 
Confuso?

Pense só: em quantas vendas uma bicicleta pode estar? Uma só. Note que eu usei a palavra *pode*,
pois uma bicileta pode não ter sido vendida ainda.


Agora, uma venda pode ter quantas bicicletas? Várias, correto?

Um cliente pode fazer várias compras, quantas ele quiser. Pode também não fazer nenhuma.

### Tipos de cardinalidade

* **(0,1)** - Pode não partricipar de nenyum relacionamento ou participar de apenas um.
 *Exemplo: Um funcionário pode ou não ter um carro. *

* **(1,1)** - Deve participar de exatamente um relacionamento.
 *Exemplo: Todo empréstimo estar associado a um único cliente. *

* **(0,N)** - Pode não participar de nenhum relacionamento ou participar de vários.
 *Exemplo: Um cliente pode nunca fazer um empréstimo ou fazer vários ao longo do tempo. *

 * **(1,N)** - Deve participar de pelo menos um relacionamento, mas pode participar de vários.
  *Exemplo: Um empréstimo deve conter pelo menos uma bicicleta, mas pode conter várias. *

* **(N,N)** - Ambos os lados podem participar de vários relacionamentos. Também é chamado de 
relacionamento muitos-para-muitos.
 *Exemplo: Um aluno pode cursar várias disciplinas, e uma disciplina pode ter vários alunos. *

 ### Resumindo

 * **0** = opcional (pode não existir)
 * **1** = obrigatório (deve existir)
 * **N** = muitos (vários)

 Então:

 * **(0,1)** -> opcional e no máximo um.
 * **(1,1)** -> obrigatório e exatamente um.
 * **(0,N)** -> opcional e vários.
 * **(1,N)** -> obrigatório e vários.