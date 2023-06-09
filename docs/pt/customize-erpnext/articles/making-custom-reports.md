# Fazendo relatórios personalizados


Existem três tipos de relatórios no SOMA.


### 1. Criador de relatórios


O Report Builder é uma ferramenta de personalização de relatórios integrada no SOMA. Isso permite definir campos específicos do formulário que serão adicionados no relatório. Além disso, você pode definir os filtros necessários, classificar e dar um nome preferido ao relatório.






### 2. Relatório de consulta


O relatório de consulta é escrito em SQL, que extrai valores do banco de dados da conta e exibe o mesmo no relatório. Embora as consultas SQL possam ser escritas no front-end, como HTML, elas foram restritas aos usuários da nuvem SOMA. Isso porque permite que usuários sem acesso a um relatório específico busquem dados diretamente do banco de dados.


Verifique o relatório Item do pedido de compra a ser recebido no módulo Estoque, por exemplo, de um relatório de consulta. [Clique aqui](https://frappeframework.com/docs/user/en/desk/reports/query-report) para saber como criar um relatório de consulta.


### 3. Relatório de script


Os relatórios de script são escritos em Python e armazenados no lado do servidor. São relatórios complexos que envolvem lógica e cálculo. Como esses relatórios são escritos no lado do servidor, não é possível personalizá-los a partir da conta hospedada.


Verifique o relatório de análise financeira no módulo de contas para obter um exemplo de relatório de script. [Clique aqui](https://frappeframework.com/docs/user/en/desk/reports/script-report) para saber como criar Relatório de Script.



> 
> Observação: **Filtro Dinâmico** está disponível em Relatórios de Script e Relatórios de Consulta; no entanto, não no Report Builder.
> 
> 
> 


