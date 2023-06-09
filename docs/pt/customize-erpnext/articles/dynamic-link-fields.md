# Campos de link dinâmico


O campo Dynamic Link é um campo que pode pesquisar e manter o valor de qualquer DocType. Vamos considerar um exemplo para aprender como o campo Dynamic Link funciona.


Ao criar uma Oportunidade ou Cotação, temos que definir explicitamente se é para um Lead ou um Cliente. Com base em nossa seleção (Lead/Cliente), outro campo de link aparece onde podemos selecionar o Lead ou Cliente real.


Se você definir o campo anterior como Dynamic Link, onde selecionamos Lead ou Cliente real, o campo posterior será automaticamente vinculado ao mestre selecionado no primeiro campo, ou seja, Leads ou Clientes. Portanto, não precisamos inserir campos de link separados para Cliente e Lead.


Abaixo estão as etapas para inserir o campo dinâmico personalizado. Por exemplo, vamos inserir o campo de link dinâmico na entrada do diário.


#### Etapa 1: Inserir campo de link para DocType


Primeiro, criaremos um campo de link que será vinculado ao DocType.


![Campo de link personalizado](/files/customize-dynamic-link-1.gif)


Por **DocType** mencionado no campo Opção, queremos dizer DocType pai. Então, assim como Quotation é um DocType, que tem várias Quotation abaixo dele. Da mesma forma, DocType também é um DocType que possui Pedido de Venda, Pedido de Compra e outros doctypes criados como registros DocType.


**DocType**  

---- Pedido de Venda  

---- Fatura de compra  

---- Cotação  

---- Nota Fiscal  

---- Empregado  

---- Ordem de Serviço  

.. e assim por diante.


Portanto, vincular este campo ao DocType principal listará todos os registros DocType.


![campo de link de comprovante de diário](/files/customize-dynamic-link.png)


#### Etapa 2: Inserir campo de link dinâmico


O tipo deste campo personalizado será "Link Dinâmico". No campo Opção, será mencionado o nome do campo do link Doctype.


![Campo dinâmico personalizado](/files/customize-dynamic-link-2.gif)


Este campo permitirá selecionar o id do documento, com base no valor selecionado no campo do link Doctype. Por exemplo, se selecionarmos Pedido de venda no campo anterior, o campo Link dinâmico listará todos os IDs de pedidos de venda.


![Campo dinâmico personalizado](/files/customize-dynamic-link-3.gif)


**Opções de personalização no campo Doctype Link**


Por padrão, o campo de link DocType fornecerá todos os formulários/docTypes para seleção. Se você deseja que este campo mostre certos docTypes específicos no resultado da pesquisa, você precisará escrever um script personalizado para ele.


