# TRABALHO 01:  Empresa de energia solar
Trabalho desenvolvido durante a disciplina de BD1

# Sumário

### 1. COMPONENTES<br>
Integrantes do grupo<br>
Daniel da Silva Lippaus: lippaus18@gmail.com<br>
Daniel Oliveira Lemos: danielolemos10@gmail.com<br>
Lorenzzo Gabriel Ramos Doelinger Oliveira: lorenzzooliveira7@gmail.com<br>
Rodolfo Müller do Amaral: amaralrodolfo38@gmail.com<br>
<br>


### 2.MINI-MUNDO<br>
Descrição textual das regras de negócio definidas como um subconjunto do mundo real cujos elementos são propriedades que desejamos incluir, processar, armazenar, gerenciar, atualizar, e que descrevem a proposta/solução a ser desenvolvida.

> O sistema proposto para a SERVTEC Energia Solar conterá as informacões aqui detalhadas. Dos clientes serão armazenados o nome, o endereço, o email, o telefone e o CPF. Dos orçamentos serão armazenados o número, o nome do cliente, o seu representante comercial, a pessoa que o indicou (caso haja), o gasto médio mensal, a quantidade de kWh sugerida para o cliente, o número de parcelas do financiamento, o valor das parcelas propostas, o valor do projeto caso seja pago à vista, o seu status, a data de atualização do status, a data de confecção do orçamento, o tipo de padrão de energia, a quantidade de painéis que o inversor proposto suporta, a potência média mensal com o total de placas, a área média dos módulos e a economia total gerada com o sistema em 25 anos. Dos representantes comerciais serão armazenados o nome e o número de telefone. Cada representante comercial pode ter vários orçamentos relacionados ao seu nome, mas um orámento pode estar relacionado a um só representante comercial. Um orçamento pode ser aprovado, reprovado ou arquivado. Um cliente pode ter um ou mais orçamentos relacionados ao seu nome. Os padrões de energia podem ser monofásicos, bifásicos ou trifásicos. 

### 3.PERGUNTAS A SEREM RESPONDIDAS<br>
#### 3.1 QUAIS PERGUNTAS PODEM SER RESPONDIDAS COM O SISTEMA PROPOSTO?
    a) O sistema proposto poderá fornecer quais tipos de relatórios e informações? 
    b) Crie uma lista com os 5 principais relatórios que poderão ser obtidos por meio do sistema proposto!
    
> A Empresa SERVTEC Energia Solar precisa inicialmente dos seguintes relatórios sobre orçamentos, projetos e representantes:
* Relatório que mostre a quantidade de orçamentos aprovados em determinada época do ano.
* Relatório que mostre qual a região com mais pedidos de orçamento.
* Relatório que mostre quantos projetos são feitos por semestre.
* Relatório que mostre a quantidade de projetos aprovados, reprovados e arquivados por semestre.
* Relatório que mostre qual representante mais fez orçamentos por semestre.

    
### 5.MODELO CONCEITUAL<br>
    A) Utilizar a Notação adequada (Preferencialmente utilizar o BR Modelo 3)
    B) O mínimo de entidades do modelo conceitual pare este trabalho será igual a 3 e o Máximo 5.
        * informe quais são as 3 principais entidades do sistema em densenvolvimento<br>(se houverem mais de 3 entidades, pense na importância da entidade para o sistema)       
    C) Principais fluxos de informação/entidades do sistema (mínimo 3). <br>Dica: normalmente estes fluxos estão associados as tabelas que conterão maior quantidade de dados 
    D) Qualidade e Clareza
        Garantir que a semântica dos atributos seja clara no esquema (nomes coerentes com os dados).
        Criar o esquema de forma a garantir a redução de informação redundante, possibilidade de valores null, 
        e tuplas falsas (Aplicar os conceitos de normalização abordados).   
        
![image](https://github.com/user-attachments/assets/b2de9043-8f4e-45e6-a4f4-fb6a06521c2b)



    
#### 5.1 Validação do Modelo Conceitual
    [Grupo 01]: Marlon Silva
    [Grupo 02]: [Nomes dos que participaram na avaliação]

#### 5.2 Descrição dos dados 
    CLIENTE: Tabela que armazena as informações relativas aos clientes.
    ClienteID (chave primária): Identificador único de cliente;
    Nome: Nome completo do cliente;
    Endereco: Endereço do cliente;
    Email: E-mail do cliente;
    Telefone: Telefone de contato do cliente;
    CPF: Número de Cadastro de Pessoa Física do cliente.

    ORÇAMENTOS: Tabela que armazena as informações relativas aos orçamentos realizados.
    OrcamentoID (chave primária): Identificador único do orçamento;
    ValorParcelasPropostas: Valor das parcelas propostas a partir da negociação;
    ValorProjetoVista: Valor do projeto caso o pagamento seja feito à vista;
    Numero: Número do projeto;
    Status: Qual a situação atual do projeto (Em Análise, Aprovado, Rejeitado, Cancelado);
    NomeCliente: Nome do cliente ao qual o orçamento está atrelado;
    DataAtualizacaoStatus: Data da última atualização de status do projeto;
    RepresentanteComercial: Nome do representante comercial que é responsável pelo orçamento;
    DatadeConfeccao: Data em que o orçamento foi feito;
    PessoaqueIndicou: Nome da pessoa que indicou a empresa para fazer o projeto;
    TipodePadraodeEnergia: Tipo de padrão de energia do cliente;
    GastoMedioMensal: Gasto médio mensal do cliente para poder dimensionar o aparelho de energia solar;
    QuantidadedePaineisqueoInversorSuporta: Quantidade de painéis que o inversor suporta nessa instalação;
    QuantidadekWhSugerida: Qual a quantidade de kWh sugerida para a instalação de acordo com os dados fornecidos pelo cliente;
    PotenciaMediaMensal: Qual a potência média mensal fornecida pelo aparelho;
    NumerodeParcelas: Número de parcelas estabelecidas para o orçamento;
    EconomiaTotalem25Anos: Qual a economia total que o cliente terá em 25 anos se colocar as placas solares;
    AreaMediadosModulos: Qual a área média de ocupação dos módulos da instalação.

    REPRESENTANTE COMERCIAL:
    RepresentanteID (chave primária): Identificador único do representante comercial;
    Nome: Nome completo do representante comercial;
    Telefone: Telefone de contato do representante comercial.
    

># Marco de Entrega 01: Do item 1 até o item 5.2 (5 PTS) <br> 

### 6	MODELO LÓGICO<br>
    a) inclusão do esquema lógico do banco de dados
    b) verificação de correspondencia com o modelo conceitual 
    (não serão aceitos modelos que não estejam em conformidade)
	
![image](https://github.com/user-attachments/assets/64b52ff7-04c9-4d93-9943-9d2b666003c4)




### 7	MODELO FÍSICO<br>
	DROP TABLE IF EXISTS CLIENTE
	CREATE TABLE CLIENTE (
	    ClienteID INT PRIMARY KEY,
	    Nome VARCHAR(255) NOT NULL,
	    Endereco VARCHAR(255) NOT NULL,
	    Email VARCHAR(255) NOT NULL,
	    Telefone VARCHAR(20) NOT NULL,
	    CPF VARCHAR(20) NOT NULL
	);
	
	DROP TABLE IF EXISTS REPRESENTANTE_COMERCIAL
	CREATE TABLE REPRESENTANTE_COMERCIAL (
	    RepresentanteID INT PRIMARY KEY,
	    Nome VARCHAR(255) NOT NULL,
	    Telefone VARCHAR(20) NOT NULL
	);
	
	DROP TABLE IF EXISTS ORCAMENTOS
	CREATE TABLE ORCAMENTOS (
	    OrcamentoID INT PRIMARY KEY,
	    ValorParcelasPropostas DECIMAL(10, 2) NOT NULL,
	    ValorProjetoAVista DECIMAL(10, 2) NOT NULL,
	    Numero INT NOT NULL,
	    Status VARCHAR(50) NOT NULL,
	    NomeCliente VARCHAR(255) NOT NULL,
	    DataAtualizacaoStatus DATE NOT NULL,
	    RepresentanteComercial INT,
	    DataDeConfecao DATE NOT NULL,
	    PessoaQueIndicou VARCHAR(255),
	    TipoDePadraoDeEnergia VARCHAR(255),
	    GastoMedioMensal DECIMAL(10, 2),
	    QuantidadePaineisQueOInversorSuporta INT,
	    QuantidadeWhSugerida DECIMAL(10, 2),
	    PotenciaMediaMensal DECIMAL(10, 2),
	    NumeroDeParcelas INT,
	    EconomiaTotalEm25Anos DECIMAL(10, 2),
	    AreaMediaDosModulos DECIMAL(10, 2),
	    CONSTRAINT FK_RepresentanteComercial FOREIGN KEY (RepresentanteComercial) REFERENCES REPRESENTANTE_COMERCIAL(RepresentanteID)
	);
	
	DROP TABLE IF EXISTS Possui
	CREATE TABLE Possui (
	    ClienteID INT,
	    OrcamentoID INT,
	    PRIMARY KEY (ClienteID, OrcamentoID),
	    CONSTRAINT FK_Cliente FOREIGN KEY (ClienteID) REFERENCES CLIENTE(ClienteID),
	    CONSTRAINT FK_Orcamento FOREIGN KEY (OrcamentoID) REFERENCES ORCAMENTOS(OrcamentoID)
	);
	
	DROP TABLE IF EXISTS Associado
	CREATE TABLE Associado (
	    OrcamentoID INT,
	    RepresentanteID INT,
	    PRIMARY KEY (OrcamentoID, RepresentanteID),
	    CONSTRAINT FK_Orcamento_Associado FOREIGN KEY (OrcamentoID) REFERENCES ORCAMENTOS(OrcamentoID),
	    CONSTRAINT FK_Representante_Associado FOREIGN KEY (RepresentanteID) REFERENCES REPRESENTANTE_COMERCIAL(RepresentanteID)
	);


      
### 8	INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>
	INSERT INTO CLIENTE (ClienteID, Nome, Endereco, Email, Telefone, CPF) VALUES 
	(1, 'João Silva', 'Rua dos Pássaros, 123, Bairro Centro, Município Passa Tempo, Estado MG', 'joao.silva@gmail.com', '99856-2525', '123.456.789-01'),
	(2, 'Maria Oliveira', 'Avenida Brasil, 456, Bairro Norte, Município Ampére, Estado PR', 'maria.oliveira@gmail.com', '99635-6954', '987.654.321-02'),
	(3, 'Carlos Pereira', 'Praça Carlos Alberto, 789, Bairro Sul, Município Alto Feliz, Estado Z', 'carlos.pereira@gmail.com', '98563-9898', '159.753.486-03'),
	(4, 'Luciana Lima', 'Rua Dois, 321, Bairro Leste, Município Alvorada, Estado RS', 'luciana.lima@gmail.com', '99784-5214', '258.456.789-04'),
	(5, 'Fernando Alves', 'Avenida José Sette, 654, Bairro Oeste, Município Cariacica, Estado ES', 'fernando.alves@gmail.com', '99245-6367', '369.258.147-05'),
	(6, 'Patrícia Silva', 'Praça das Flores, 987, Bairro Alto, Município Areado, Estado MG', 'patricia.silva@gmail.com', '99200-4118', '456.789.123-06'),
	(7, 'Roberto Costa', 'Rua Grande, 147, Bairro Baixo, Município Aricanduva, Estado MG', 'roberto.costa@gmail.com', '99745-3562', '654.321.987-07');
	
	INSERT INTO REPRESENTANTE_COMERCIAL (RepresentanteID, Nome, Telefone) VALUES 
	(1, 'Ana Costa', '9898-2532'),
	(2, 'Luiz Souza', '99978-4515'),
	(3, 'Juliana Santos', '99625-3247'),
	(4, 'Marcos Pereira', '99532-7481');
	
	INSERT INTO ORCAMENTOS (OrcamentoID, ValorParcelasPropostas, ValorProjetoAVista, Numero, Status, NomeCliente, DataAtualizacaoStatus, RepresentanteComercial, DataDeConfecao, PessoaQueIndicou, TipoDePadraoDeEnergia, GastoMedioMensal, QuantidadePaineisQueOInversorSuporta, QuantidadekWhSugerida, PotenciaMediaMensal, NumeroDeParcelas, EconomiaTotalEm25Anos, AreaMediaDosModulos) VALUES 
	(1, 12000.00, 10000.00, 123, 'Em Análise', 'João Silva', '2024-07-01', 1, '2024-06-15', 'Carlos Pereira', 'Monofásico', 200.00, 10, 3000.00, 250.00, 12, 5000.00, 50.00),
	(2, 15000.00, 13000.00, 456, 'Aprovado', 'Maria Oliveira', '2024-07-02', 2, '2024-06-20', 'João Silva', 'Bifásico', 300.00, 12, 4000.00, 350.00, 24, 6000.00, 60.00),
	(3, 18000.00, 16000.00, 789, 'Rejeitado', 'Carlos Pereira', '2024-07-03', 4, '2024-06-25', 'Maria Oliveira', 'Trifásico', 400.00, 15, 5000.00, 450.00, 36, 7000.00, 70.00),
	(4, 20000.00, 18000.00, 101, 'Cancelado', 'Luciana Lima', '2024-07-04', 3, '2024-07-01', 'Fernando Alves', 'Bifásico', 500.00, 20, 6000.00, 550.00, 24, 8000.00, 80.00),
	(5, 22000.00, 20000.00, 202, 'Em Análise', 'Fernando Alves', '2024-07-05', 4, '2024-07-02', 'Luciana Lima', 'Trifásico', 600.00, 25, 7000.00, 650.00, 36, 9000.00, 90.00),
	(6, 25000.00, 23000.00, 303, 'Aprovado', 'Patrícia Silva', '2024-07-06', 1, '2024-07-03', 'Roberto Costa', 'Monofásico', 700.00, 30, 8000.00, 750.00, 12, 10000.00, 100.00);
	
	INSERT INTO Possui (ClienteID, OrcamentoID) VALUES 
	(1, 1),
	(2, 2),
	(3, 3),
	(4, 4),
	(5, 5),
	(6, 6),
	(7, 6);
	
	INSERT INTO Associado (OrcamentoID, RepresentanteID) VALUES 
	(1, 1),
	(2, 2),
	(4, 3),
	(5, 4),
	(6, 1);

### 9	TABELAS E PRINCIPAIS CONSULTAS<br>
    OBS: Usa template da disciplina disponibilizado no Colab.<br>
#### 9.1	CONSULTAS DAS TABELAS COM TODOS OS DADOS INSERIDOS (Todas) <br>

#### 9.2	CONSULTAS DAS TABELAS COM FILTROS WHERE (Mínimo 4)<br>

#### 9.3	CONSULTAS QUE USAM OPERADORES LÓGICOS, ARITMÉTICOS E TABELAS OU CAMPOS RENOMEADOS (Mínimo 11)
    a) Criar 5 consultas que envolvam os operadores lógicos AND, OR e Not
    b) Criar no mínimo 3 consultas com operadores aritméticos 
    c) Criar no mínimo 3 consultas com operação de renomear nomes de campos ou tabelas

#### 9.4	CONSULTAS QUE USAM OPERADORES LIKE E DATAS (Mínimo 12) <br>
    a) Criar outras 5 consultas que envolvam like ou ilike
    b) Criar uma consulta para cada tipo de função data apresentada.

># Marco de Entrega 02: Do item 6. até o item 9.1 (5 PTS) <br>

#### 9.5	INSTRUÇÕES APLICANDO ATUALIZAÇÃO E EXCLUSÃO DE DADOS (Mínimo 6)<br>
    a) Criar minimo 3 de exclusão
    b) Criar minimo 3 de atualização

#### 9.6	CONSULTAS COM INNER JOIN E ORDER BY (Mínimo 6)<br>
    a) Uma junção que envolva todas as tabelas possuindo no mínimo 2 registros no resultado
    b) Outras junções que o grupo considere como sendo as de principal importância para o trabalho

#### 9.7	CONSULTAS COM GROUP BY E FUNÇÕES DE AGRUPAMENTO (Mínimo 6)<br>
    a) Criar minimo 2 envolvendo algum tipo de junção

#### 9.8	CONSULTAS COM LEFT, RIGHT E FULL JOIN (Mínimo 4)<br>
    a) Criar minimo 1 de cada tipo

#### 9.9	CONSULTAS COM SELF JOIN E VIEW (Mínimo 6)<br>
        a) Uma junção que envolva Self Join (caso não ocorra na base justificar e substituir por uma view)
        b) Outras junções com views que o grupo considere como sendo de relevante importância para o trabalho

#### 9.10	SUBCONSULTAS (Mínimo 4)<br>
     a) Criar minimo 1 envolvendo GROUP BY
     b) Criar minimo 1 envolvendo algum tipo de junção

># Marco de Entrega 03: Do item 9.2 até o ítem 9.10 (10 PTS)<br>

### 10 RELATÓRIOS E GRÁFICOS

#### a) análises e resultados provenientes do banco de dados desenvolvido (usar modelo disponível)
#### b) link com exemplo de relatórios será disponiblizado pelo professor no AVA
#### OBS: Esta é uma atividade de grande relevância no contexto do trabalho. Mantenha o foco nos 5 principais relatórios/resultados visando obter o melhor resultado possível.

    

### 11	AJUSTES DA DOCUMENTAÇÃO, CRIAÇÃO DOS SLIDES E VÍDEO PARA APRESENTAÇAO FINAL <br>

#### a) Modelo (pecha kucha)<br>
#### b) Tempo de apresentação 6:40 

># Marco de Entrega 04: Itens 10 e 11 (20 PTS) <br>
<br>
<br>
