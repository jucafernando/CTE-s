# CTE
Common table expression (expressão de tabela comum), é utilizado para faciliar a organização e lógica em 
querys mais complexas no SQL. A criação de uma CTE ocorre através de criação de tabelas temportárias e 
depois de criada, estruturada e utilizada, a CTE é apagada. A query abaixo foi criada para verificar qual
a idade média dos clientes, por status profissional:


![image](https://github.com/jucafernando/CTE-s/assets/21082881/b1d5217b-3964-4c11-9e3c-b06c597f888a)


Criei uma CTE com o id dos clientes e uma coluna apelidada e chamada de idade, contendo a subtração entre a função que retorna a data corrente(data atual do sistema) com o campo de data de nascimento dos clientes, dividido por 365(equivalente a um ano). Essa coluna, retorna a idade de cada cliente. Após criada a 
tabela temporária, selecionei os campos de status profissional dos clientes e criei uma coluna agregada chamada idade_media, onde eu utilizo a função de 
agragação AVG para retornar a média da coluna idade. Após isso, eu crio a junção através do left join para juntar a tabela temporária com a tabela de clientes
e retornar a média de idade dos clientes agrupado pelo status profissional, e ordenado pela média de idade dos clientes, selecionando da idade média mais baixa para a mais alta. 
Podemos observar que os clientes com a menor média de idade são os que trabalham como CLT, seguido dos clientes com status self employment(autonomos), enquanto a maior média de idade são os clientes aposentados.

CTE's podem ajudar e muito na organização de uma query, melhorando os resultados das análises dos dados e ajudando no pensamento lógico na busca de querys mais organizadas e mais fáceis de compreendê-las.

