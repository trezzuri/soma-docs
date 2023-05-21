# Personalize o formato de impressão


**Formatos de impressão são os layouts gerados quando você deseja imprimir ou enviar uma transação por e-mail.**


Esse recurso é útil para todas as transações no ERPNext, como todas as transações de compra e venda, documentos de RH e muito mais.


No ERPNext, existem três tipos de Formatos de Impressão, a saber, Formato de Impressão Padrão, Formato de Impressão Personalizado e Formato de Impressão HTML.


## Formato de impressão padrão


Cada Tipo de Documento Imprimível no ERPNext terá seu próprio Formato de Impressão Padrão que é gerado pelo Frappe Framework. A colocação dos campos nos Formatos de Impressão Padrão dependerá da posição dos respectivos campos no documento.


![Formato de impressão padrão](/files/customize-standard-print-format.png)


Quaisquer alterações feitas no Formato de Impressão Padrão deverão ser feitas usando um Formulário Personalizado. Você também pode verificar [adicionar campos em formatos de impressão](/docs/v13/user/manual/en/customize-erpnext/articles/making-fields-visible-in-print-format).


## Formato de impressão personalizado


Você também pode criar seus próprios formatos de impressão personalizados usando uma ferramenta chamada [Criador de formato de impressão](/docs/v13/user/manual/en/setting-up/print/print-format-builder). Esta ferramenta irá ajudá-lo a criar um formato de impressão personalizado simples, arrastando e soltando campos em um formato conforme sua preferência.


![Personalizar formato de impressão](/files/customize-print-format.gif)


Para a criação de Formatos de Impressão Personalizados, o ERPNext vem com vários modelos pré-definidos em três estilos, a saber: Moderno, Monocromático e Clássico.


Para criar suas versões, abra um modelo existente em:



>
> Construir > Visualizações > Formato de Impressão
>
>
>


## Configurações de impressão


Para editar/atualizar suas configurações de impressão e PDF, acesse:



>
> Configurações > Configurações de impressão
>
>
>


![Configurações de impressão](/files/print-settings.png)


## Formato de impressão HTML


Para criar um formato de impressão HTML, você precisaria de algum conhecimento de HTML, CSS e Python. Aqui está um exemplo de como um formato de impressão pode ser projetado com um formato muito específico.


![Formato de impressão HTML](/files/customize-custom-print-format-1.png)


Os formatos de impressão são fornecidos no lado do servidor usando a [linguagem de modelagem Jinja](https://jinja.palletsprojects.com/en/3.0.x/templates/). Todos os formulários têm acesso ao objeto doc que contém informações sobre o documento que está sendo formatado. Você também pode acessar utilitários comuns por meio do módulo frappe. Para obter suporte ao criar um formato de impressão baseado em HTML, você pode consultar o [Fórum da Comunidade ERPNext](https://discuss.erpnext.com/) ou iniciar uma nova postagem para sua consulta.


Para estilizar, o [Bootstrap CSS Framework](http://getbootstrap.com/) é fornecido e você pode aproveitar toda a gama de classes.


#### Referências


1. [Linguagem de modelagem Jinja: referência](https://jinja.palletsprojects.com/en/3.0.x/templates/)
2. [Bootstrap CSS Framework](http://getbootstrap.com/)


#### Exemplo



```
    {% raw %}<h3>{{ doc.select_print_heading or "Invoice" }}</h3>
    <div class="linha">
        <div class="col-md-3 text-right">Nome do cliente</div>
        <div class="col-md-9">{{ doc.customer_name }}</div>
    </div>
    <div class="linha">
        <div class="col-md-3 text-right">Data</div>
        <div class="col-md-9">{{ doc.get_formatted("invoice_date") }}</div>
    </div>

            {%- para linha em doc.items -%}

            {%- endfor -%}
        <table class="table table-bordered">
        <corpo>
            <tr>
                <th>Sr</th>
                <th>Nome do item</th>
                <th>Descrição</th>
                <th class="text-right">Quantidade</th>
                <th class="text-right">Taxa</th>
                <th class="text-right">Valor</th>
            </tr><tr>
                <td style="width: 3%;">{{ row.idx }}</td>
                <td style="largura: 20%;">
                    {{ row.item_name }}
                    {% if row.item_code != row.item_name -%}
                    <br>Código do item: {{ row.item_code}}
                    {%- fim se %}
                </td>
                <td style="largura: 37%;">
                    <div style="border: 0px;">{{ row.description }}</div></td>
                <td style="width: 10%; text-align: right;">{{ row.qty }} {{ row.uom or row.stock_uom }}</td>
                <td style="width: 15%; text-align: right;">{{
                    row.get_formatted("rate", doc) }}</td>
                <td style="width: 15%; text-align: right;">{{
                    row.get_formatted("amount", doc) }}</td>
            </tr></tbody>
    </table>{% enddraw %}

```

## Notas


1. Para obter valores formatados de data e moeda, use `doc.get_formatted("fieldname")`
2. Para strings traduzíveis, use `{{ '{{ _("Esta string está traduzida") }}' }}`