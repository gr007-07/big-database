🛍️ Banco de Dados de Comércio - comercioEste repositório contém o script SQL para criar e popular um banco de dados simples para um sistema de comércio.

🌟 Visão Geral do ProjetoO banco de dados comercio foi projetado para gerenciar informações básicas de clientes, seus endereços e telefones, e um catálogo de produtos. Ele é estruturado em quatro tabelas principais com relações definidas para garantir a integridade dos dados.

📁 Estrutura do Banco de DadosO banco de dados comercio é composto pelas seguintes tabelas:TabelaDescriçãoChave PrimáriaChaves EstrangeirasclienteInformações pessoais dos clientes (Nome, Sexo, Email, CPF).IDCLIENTEN/AenderecoDetalhes de endereço do cliente (Rua, Bairro, Cidade, Estado).IDENDERECOID_CLIENTE (Referencia cliente)telefoneNúmeros de telefone do cliente (Tipo e Número).IDTELEFONEID_CLIENTE (Referencia cliente)produtoInformações sobre os produtos (Nome, Peso, Valor, Frete).IDPRODUTON/ARelações entre as TabelasA tabela endereco e a tabela telefone estão relacionadas com a tabela cliente por meio da chave estrangeira ID_CLIENTE.A relação entre cliente e endereco é de um para um (1:1), onde um cliente tem um único endereço associado (UNIQUE KEY ID_CLIENTE em endereco).A relação entre cliente e telefone é de um para muitos (1:N), onde um cliente pode ter vários telefones.

Tabela,Descrição,Chave Primária,Chaves Estrangeiras
cliente,"Informações pessoais dos clientes (Nome, Sexo, Email, CPF).",IDCLIENTE,N/A
endereco,"Detalhes de endereço do cliente (Rua, Bairro, Cidade, Estado).",IDENDERECO,ID_CLIENTE (Referencia cliente)
telefone,Números de telefone do cliente (Tipo e Número).,IDTELEFONE,ID_CLIENTE (Referencia cliente)
produto,"Informações sobre os produtos (Nome, Peso, Valor, Frete).",IDPRODUTO,N/A
