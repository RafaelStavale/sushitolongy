# sushitolongy

Ontologia de Sushi para aula de Engenharia de Ontologias.
Questões de Competência fechadas pela turma (total de 32):
- Quais são as partes dos pratos de sushi?
~~~~
R
~~~~

- Quais são os tipos de sushi que não são do Japão?
~~~~
R
~~~~

- Quais são os tipos de sushi que são do Japão?
~~~~
R
~~~~

- Qual o país de origem de um determinado sushi X? (X = temaki de frango)
~~~~
R
~~~~

- Quais são os modos de preparo do sushi?
~~~~
R
~~~~

- Quais são os sushis que são feitos à mão?
~~~~
R
~~~~

- Quais sushis são feitos apenas com as mãos?
~~~~
R
~~~~

- Todo sushi é cru? (não tem um modo de preparo cozimento, fritura etc)
~~~~
R
~~~~

- Existe modo de preparo que todo sushi tem?
~~~~
R
~~~~

- Quais utensílios são usadas no preparo de sushi?
~~~~
R
~~~~

- Existe utensílio usado em todo tipo de sushi?
~~~~
R
~~~~

- Para determinado tipo de sushi, quais receitas existem?
~~~~
R
~~~~

- Quais sushis levam um ingrediente X? (X = camarão, ovos, salmão, tempero)
~~~~
Recipe and hasIngredient value X (mostra os sushis que têm)
~~~~

- Existe sushi sem ingrediente X? (X = alga, carne, arroz, peixe, frutos do mar)
~~~~
  Não é possível responder essa questão devido ao mundo aberto.
	Explicando: o fato de uma receita não ter o ingrediente arroz agora não quer dizer que não terá no futuro, então não podemos dizer que ela não tem.
	Ou seja, a query Recipe and not(hasIngredient value SushiRice) retorna 0 instâncias.
	Essa pergunta é diferente da “Quais são os tipos de sushi que não são do Japão?”, pois nesta última uma receita tem apenas UM local de origem, e se esse está preenchido pode-se dizer que ela não tem mais nenhum outro. O número de ingredientes, no entanto, não é limitado.
~~~~

- Todos os sushis levam um ingrediente X no seu preparo? (X = arroz, sal, peixe, vinagre)
~~~~
Recipe and hasIngredient value X (mostra os sushis que têm, é necessário comparar com o total)
~~~~

- Quais os sushis que não contêm um determinado ingrediente X? (X = peixe, alga)
~~~~
R
~~~~

- Quais são os ingredientes que todo sushi tem?
~~~~
R
~~~~

- Quais os ingredientes de um determinado sushi X? (X = hot philadelphia)
~~~~
R
~~~~

- Quais frutas são usadas no preparo do sushi?
~~~~
R
~~~~

- Quais vegetais são usados no preparo do sushi?
~~~~
R
~~~~

- Quais peixes são usados no preparo do sushi?
~~~~
R
~~~~

- Quais frutos do mar são usados no preparo do sushi?
~~~~
R
~~~~

- Quais são os formas de apresentação/formatos de sushi? 
~~~~
PresentationClassification
~~~~

- Quais sushis são servidos com um determinado formato X? (X = enrolado)
~~~~
presentedAs value X
~~~~

- Todo sushi tem um determinado formato X? (X = enrolado)
~~~~
presentedAs value X (mostra os sushis que têm, é necessário comparar com o total)
~~~~

- Quais são os sabores possíveis dos sushis?
~~~~
Flavour
~~~~

- Existe sushi com um sabor X? (X = doce, amargo)
~~~~
R
~~~~

- Quais sushis têm um determinado sabor X? (X = azedo)
~~~~
R
~~~~

- Quais são os tipos possíveis de sushi?
~~~~
R
~~~~

- Quais os subtipos do Makizushi?
~~~~
R
~~~~

- Quais são os acompanhamentos (molhos ou outros) possíveis?
~~~~
R
~~~~

- Existe sushi com mais de um tipo de peixe?
~~~~
R
~~~~

