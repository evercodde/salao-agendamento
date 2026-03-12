1️⃣ Modelo Completo do Banco de Dados (Supabase / PostgreSQL)

Este modelo já está preparado para:

portfólio

serviços

agenda

clientes

histórico de atendimento

produtos usados

expansão futura (IA e passaporte capilar)

Estrutura Geral do Banco

Principais tabelas:

usuarios
clientes
categorias_servico
servicos
agendamentos
produtos
consumo_produtos
portfolio_fotos
configuracoes_salao
bloqueios_agenda
Extensão necessária (Supabase)
create extension if not exists "uuid-ossp";
Tabela Usuários (Admin)
create table usuarios (
id uuid primary key default uuid_generate_v4(),
nome text not null,
email text unique not null,
telefone text,
tipo_usuario text default 'admin',
created_at timestamp default now()
);
Tabela Clientes
create table clientes (
id uuid primary key default uuid_generate_v4(),
nome text not null,
telefone text not null,
email text,
observacoes text,
created_at timestamp default now()
);
Categorias de Serviço
create table categorias_servico (
id uuid primary key default uuid_generate_v4(),
nome text not null,
descricao text
);
Serviços
create table servicos (
id uuid primary key default uuid_generate_v4(),
nome text not null,
categoria_id uuid references categorias_servico(id),
preco_base numeric,
preco_variavel boolean default false,
duracao_minutos integer not null,
intervalo_minutos integer default 10,
ativo boolean default true,
descricao text,
created_at timestamp default now()
);
Agendamentos
create table agendamentos (
id uuid primary key default uuid_generate_v4(),

cliente_id uuid references clientes(id),
servico_id uuid references servicos(id),

data date not null,
hora_inicio time not null,
hora_fim time not null,

descricao_cliente text,

status text default 'pendente',

lembrete_enviado boolean default false,

created_at timestamp default now()
);

Status possíveis:

pendente
confirmado
cancelado
finalizado
Bloqueios de Agenda (folga, almoço etc)
create table bloqueios_agenda (
id uuid primary key default uuid_generate_v4(),
data date not null,
hora_inicio time,
hora_fim time,
motivo text
);
Produtos
create table produtos (
id uuid primary key default uuid_generate_v4(),
nome text not null,
unidade_medida text,
descricao text
);

Exemplo:

Shampoo
Gramas

Ox
Ml
Consumo de Produtos por Atendimento
create table consumo_produtos (
id uuid primary key default uuid_generate_v4(),

agendamento_id uuid references agendamentos(id),

produto_id uuid references produtos(id),

quantidade numeric
);
Portfólio
create table portfolio_fotos (
id uuid primary key default uuid_generate_v4(),

categoria_id uuid references categorias_servico(id),

url_imagem text not null,

descricao text,

data_upload timestamp default now()
);
Configurações do salão

Define horário de funcionamento.

create table configuracoes_salao (

id uuid primary key default uuid_generate_v4(),

hora_abertura time,
hora_fechamento time,

intervalo_padrao integer default 10,

dias_funcionamento text
);

Exemplo:

segunda,terca,quarta,quinta,sexta,sabado
