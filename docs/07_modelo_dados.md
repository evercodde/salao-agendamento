# Modelo de Dados

## Cliente

id
nome
telefone
email

## CategoriaServico

id
nome
descricao

## Servico

id
nome
categoria_id
preco_base
preco_variavel
duracao_minutos
intervalo_minutos
ativo

## Agendamento

id
cliente_id
servico_id
data
hora_inicio
hora_fim
descricao_cliente
status

## Produto

id
nome
unidade_medida

## ConsumoProduto

id
agendamento_id
produto_id
quantidade

## Portfolio

id
categoria_id
url_imagem
descricao
data_upload
