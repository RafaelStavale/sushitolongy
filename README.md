# sushitolongy

Ontologia de Sushi para aula de Engenharia de Ontologias.
Questões de Competência fechadas pela turma (total de 32):

- Quais são as partes dos pratos de sushi?
~~~~
partOfRecipe some Recipe
~~~~

- Quais são os tipos de sushi que não são do Japão?
~~~~
Recipe and not(hasProvenance value JapanCousine) (é necessário dizer que JapanCousine e AmericanCousine são diferentes)
~~~~

- Quais são os tipos de sushi que são do Japão?
~~~~
Recipe and hasProvenance value JapanCousine
~~~~

- Qual o país de origem de um determinado sushi X? (X = temaki de frango)
~~~~
Cousine and  inverse(hasProvenance) value X (ex.: RecipeSalmonPhiladelphiaRoll)
~~~~

- Quais são os modos de preparo do sushi?
~~~~
Procedure
~~~~

- Quais são os sushis que são feitos à mão?
~~~~
requires value Hand (não temos nenhum, mas classificamos as mãos como utensílios)
~~~~

- Quais sushis são feitos apenas com as mãos?
~~~~
Não é posível responder em razão do mundo aberto, pois o sushi pode ter apenas um utensílio hoje (mãos), mas assume que pode ter outros ainda não descritos.
~~~~

- Todo sushi é cru? (não tem um modo de preparo cozimento, fritura etc)
~~~~
Devido ao mundo aberto, não é possível responder essa pergunta, pois requer saber os sushis que não têm/são algo.
~~~~

- Existe modo de preparo que todo sushi tem?
~~~~
hasProcedure min 5 Recipe (5 é a quantidade de instâncias que temos em Recipe. Não temos nenhum modo de preparo comum a todas)
~~~~

- Quais utensílios são usadas no preparo de sushi?
~~~~
Utensils
~~~~

- Existe utensílio usado em todo tipo de sushi?
~~~~
requires min 5 Recipe (5 é a quantidade de instâncias que temos em Recipe. Não temos nenhum utensílio comum a todas)
~~~~

- Para determinado tipo de sushi X, quais receitas existem?
~~~~
Recipe and produces value X (CulinaryDish)
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
Não é possível responder em razão do mundo aberto. Ver resposta à questão "Existe sushi sem ingrediente X?".
~~~~

- Quais são os ingredientes que todo sushi tem ("obrigatórios")?
~~~~
partOfRecipe min 5 Recipe (5 é a quantidade de instâncias que temos em Recipe. Não temos nenhum ingrediente obrigatório a todas)
~~~~

- Quais os ingredientes de um determinado sushi X? (X = hot philadelphia)
~~~~
inverse(hasIngredient) some (produces value X) 
~~~~

- Quais frutas são usadas no preparo do sushi?
~~~~
Ingredient and classifiedAsIngredientClassification value Fruit (não temos nenhuma)
~~~~

- Quais vegetais são usados no preparo do sushi?
~~~~
classifiedAsIngredientClassification value Herb or 
classifiedAsIngredientClassification value Fruit or 
classifiedAsIngredientClassification value CerealGrain (como vegetal é um termo geral, se incluiu os que tínhamos, mas futuramente podem haver outros)
~~~~

- Quais peixes são usados no preparo do sushi?
~~~~
Ingredient and classifiedAsIngredientClassification value Seafood (Não separamos peixes de frutos do mar nesse momento)
~~~~

- Quais frutos do mar são usados no preparo do sushi?
~~~~
Ingredient and classifiedAsIngredientClassification value Seafood
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
hasFlavour value X
~~~~

- Quais sushis têm um determinado sabor X? (X = azedo)
~~~~
hasFlavour value X
~~~~

- Quais são os tipos possíveis de sushi?
~~~~
DishClassification
~~~~

- Quais os subtipos do Makizushi?
~~~~
Optamos por não criar essa classe, criando diretamente os subtipos como classes: Futomaki, Temaki, Uramaki.
~~~~

- Quais são os acompanhamentos (molhos ou outros) possíveis?
~~~~
Accompaniment
~~~~

- Existe sushi com mais de um tipo de peixe?
~~~~
Recipe and hasIngredient min 2 (Ingredient and classifiedAsIngredientClassification value Seafood)
~~~~

