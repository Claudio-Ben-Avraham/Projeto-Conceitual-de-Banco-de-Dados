
# Descrição do Desafio Banco de Dados

Objetivo:

O objetivo deste projeto é criar um modelo conceitual de banco de dados que gerencie o processo de pedidos e ordens de serviço de clientes, garantindo a rastreabilidade e organização das informações ao longo do ciclo de vida do pedido.
Contexto:

O sistema abrange o processo completo de um cliente realizando um pedido, que posteriormente é convertido em uma ordem de serviço, caso o pedido seja viável. Um técnico executa a ordem de serviço e, após a finalização, a ordem é arquivada. O modelo deve permitir o gerenciamento eficaz de informações sobre os clientes, os pedidos e o status das ordens de serviço.

Explicação:

    CLIENTE: Tem um identificador único id_cliente, nome, tipo de conta (PF ou PJ) e CPF/CNPJ.
    RESPONSAVEL: Possui id_responsavel, nome e cargo.
    PEDIDO: Tem um identificador único id_pedido, com referência ao cliente que realizou o pedido (id_cliente), descrição e status do pedido.
    ORDEM_SERVICO: Conectada a um pedido e a um responsável, com status e data de execução.
    PAGAMENTO: Cada pedido pode ter múltiplas formas de pagamento, com id_pagamento, id_pedido, forma de pagamento e valor.
    ENTREGA: Relacionada a um pedido, com status de entrega e código de rastreio.

Entidades:

    Cliente: Representa a pessoa ou empresa que realiza o pedido. Pode ser uma pessoa física (PF) ou jurídica (PJ), mas uma conta não pode ser registrada como ambas simultaneamente.
    Responsável: Indivíduo ou entidade responsável pela execução do pedido ou pela ordem de serviço.
    Pedido: Representa a solicitação feita pelo cliente, que será analisada e, se possível, convertida em uma ordem de serviço.
    Ordem de Serviço: Refere-se à execução do pedido, sendo analisada, executada pelo técnico e arquivada após sua conclusão.

Relacionamentos:

    Solicita: Um cliente faz um pedido.
    Analisa: Um responsável analisa o pedido.
    Executa/Arquiva: O responsável executa e arquiva a ordem de serviço.
    Possui: Um pedido pode ter múltiplos pagamentos.
    Tem: Um pedido pode ter uma ou mais entregas, com status e código de rastreio.

Imagem:

![Banco de Dados Desafio](https://github.com/user-attachments/assets/6a3ae21e-3088-4a0f-a1c7-6db4d7b0ebc4)
