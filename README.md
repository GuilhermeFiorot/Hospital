# TRABALHO 01:  Título do Trabalho
Trabalho desenvolvido durante a disciplina de BD1

# Sumário

### 1. COMPONENTES<br>
Integrantes do grupo<br>
Guilherme Firme Fiorot: guilhermefirme3@gmail.com<br>
Matheus Melotti: matheusmelotti@gmail.com<br>
...<br>

### 2.INTRODUÇÃO E MOTIVAÇÃO<br>
Este documento contém a especificação do projeto do banco de dados <Hospital> 
<br>e motivação da escolha realizada. <br>

> A empresa "Hospitais contra o covid" visa o desenvolvimento de um sistema capaz de criar e administrar prontuários médicos para o atendimento mais prático de pacientes contaminados pelo Covid-19, hospitais podem alocar os novos pacientes em seus leitos a partir de suas disponibilidades e pacientes serão atendidos mais rapidamente e terão maiores informações sobre os hospitais de sua região e suas metodologias de tratamento.Facilidade e rapidez no processo da eliminação do vírus e tratamento do paciente. Maior integração do paciente para com os hospitais. Acompanhamento médico atualizado constantemente. Acompanhamento familiar sobre o estado do paciente. Impacto social gerado pela possibilidade de compreender e realizar estudos das regiões com melhores capacidades de tratamento e das mais afetadas pelo vírus.

### 3.MINI-MUNDO<br>

Descrever o mini-mundo! (Não deve ser maior do que 30 linhas, se necessário resumir para justar) <br>
Entrevista com o usuário e identificação dos requisitos.(quando for o caso de sistemas com cliente real)<br>
Descrição textual das regras de negócio definidas como um  subconjunto do mundo real 
cujos elementos são propriedades que desejamos incluir, processar, armazenar, 
gerenciar, atualizar, e que descrevem a proposta/solução a ser desenvolvida.

> O sistema proposto por "Hospitais contra covid" ajudara tanto os pacientes como os hospitais a administrar os prontuários médicos para o atendimento mais prático dos pacientes contaminados pela Covid-19. O paciente chegara e fara um cadastro com nome, cpf, rg, data de nascimento, telefone e endereço. Esse endereço será armazenado em uma tabela separada. No hospital ele terá que guardar o nome do hospital, cep, estado, cidade, leitos disponiveis, nome medico, crm do medico e cpf do medico. Após o cadastro do Paciente e Hospital, o paciente será direcionado para o hospital mais perto de sua residencia e assim quando chegar no hospital será gerado seu prontuario com cpf do paciente, id do hospital e nivel da urgencia. 

### 4.PROTOTIPAÇÃO, PERGUNTAS A SEREM RESPONDIDAS E TABELA DE DADOS<br>
#### 4.1 RASCUNHOS BÁSICOS DA INTERFACE (MOCKUPS)<br>
Neste ponto a codificação não e necessária, somente as ideias de telas devem ser criadas, o princípio aqui é pensar na criação da interface para identificar possíveis informações a serem armazenadas ou descartadas <br>

Sugestão: https://balsamiq.com/products/mockups/<br>

![Alt text](https://github.com/GuilhermeFiorot/Hospital/blob/master/balsamiqhospitaiscontracovid.png?raw=true "Title")
![Arquivo PDF do Protótipo Balsamiq feito para Hospitais contra o covid](https://github.com/GuilhermeFiorot/Hospital/blob/master/arquivos/hospitaiscontracovid.pdf?raw=true "Hospitais contra o covid")
#### 4.2 QUAIS PERGUNTAS PODEM SER RESPONDIDAS COM O SISTEMA PROPOSTO?
    a) O sistema proposto poderá fornecer quais tipos de relatórios e informaçes? 
    b) Crie uma lista com os 5 principais relatórios que poderão ser obtidos por meio do sistema proposto!
 
> A Hospitais contra Covid podera fornecer os principais relatórios:

    1- Quantidade de Pacientes por Nivel de Urgencia, 
    2- Quantidade de hospitais por região,
    3- Regiões mais providas de investimentos na saúde,
    4- Fluxo de pacientes nos hospitais,
    5- Regiões mais afetadas pela covid.
 

#### 4.3 TABELA DE DADOS DO SISTEMA:
    a) Esta tabela deve conter todos os atributos do sistema e um mínimo de 10 linhas/registros de dados.
    b) Esta tabela tem a intenção de simular um relatório com todos os dados que serão armazenados 
    
![Exemplo de Tabela de dados do Hospitais contra o covid](https://github.com/GuilhermeFiorot/Hospital/blob/master/arquivos/TabelaHospitalcontraCovid.xlsx?raw=true "Tabela - Hospitais Contra Covid")
    
    
### 5.MODELO CONCEITUAL<br>
        
![Alt text](https://github.com/GuilhermeFiorot/Hospital/blob/master/images/ModeloConceitual_HospiralContraCovid.png?raw=true "Modelo Conceitual")
        
#### 5.1 Validação do Modelo Conceitual
    [Grupo01]: [Guilherme e Matheus, sem alterações]
    [Grupo02]: [Guilherme e Matheus, algumas alterações pós reunião com o professor.]

#### 5.2 Descrição dos dados 
    
    Paciente: Tabela que armazena as informações relativas ao paciente<br>
     Nome: campo que armazena o Nome para cada paciente.<br>
     Cpf: campo que armazena o número de Cadastro de Pessoa Física para cada cliente da empresa.<br>
     Rg: campo que armazena o número do Registro Geral para cada paciente.<br>
     Endereco id: campo que armazena o número id do endereço para cada paciente.<br>
     Data nascimento: campo que armazena a data de nascimento para cada paciente.<br>
     Telefone: campo que armazena o número de telefone para cada paciente.<br>
    
    Endereco: Tabela que armazena as informações relativas ao endereço do paciente<br>
     Id: campo que armazena o ID para cada endereço.<br>
     Cep: campo que armazena o número do cep para cada endereço.<br>
     Numero: campo que armazena o número para cada endereço.<br>
     Estado: campo que armazena o Estado para cada endereço.<br>
     Cidade: campo que armazena a Cidade para cada endereço.<br>
 
    Hospital: Tabela que armazena as informações relativas ao Hospital<br>
     Id: campo que armazena o id do hospital.<br>
     Nome do Hospital: campo que armazena o nome para cada hospital.<br>
     Cep: campo que armazena o número do Registro Geral para cada hospital.<br>
     Estado: campo que armazena o número id do endereço para cada hospital.<br>
     Cidade: campo que armazena a data de nascimento para cada hospital.<br>
     Leitos disponiveis: campo que armazena o número de telefone para cada hospital.<br>
     Nome medico: campo que armazena o nome para cada medico do Hospital.<br>
     Cpf Medico: campo que armazena a Cadastro de Pessoa Fisica para cada medico do Hospital.<br>
     Crm Medico: campo que armazena o Conselho Regional de Medicina para cada medico do Hospital.<br>
    
    Prontuario: Tabela que armazena as informações relativas ao prontuario<br>
     Id: campo que armazena o Id para cada prontuario.<br>
     Paciente CPF: campo que armazena o número de Cadastro de Pessoa Física para cada prontuario do paciente.<br>
     Hospital ID: campo que armazena o número do ID do hospital para cada prontuario.<br>
     Nivel de urgencia: campo que armazena o nivel de urgência para cada prontuario.<br>
     
### 6	MODELO LÓGICO<br>
        a) inclusão do esquema lógico do banco de dados
        b) verificação de correspondencia com o modelo conceitual 
        (não serão aceitos modelos que não estejam em conformidade)
 ![Alt text](https://github.com/GuilhermeFiorot/Hospital/blob/master/images/ModeloLogico_HospitalContraCovid.png?raw=true "Modelo Logico")
 
### 7	MODELO FÍSICO<br>
 
        CREATE TABLE Paciente (
        nome varchar(50),
        cpf varchar(50) primary KEY,
        rg varchar(50),
        fk_Endereco_id integer,
        foreign key (fk_Endereco_id) references Endereco(id),
        data_nascimento date,
        telefone varchar(50));

        CREATE TABLE Endereco (
        id integer primary KEY,
        cep varchar(50),
        numero integer,
        estado varchar(50),
        cidade varchar(50));

        CREATE TABLE Prontuario (
        prontuario_id integer primary KEY,
        fk_Paciente_cpf varchar(50),
        foreign key (fk_Paciente_cpf) references Paciente(cpf),
        fk_hospital_id integer,
        foreign key (fk_hospital_id) references Hospital(id),
        nivel_de_urgencia varchar(50));

        CREATE TABLE Hospital (
        id integer primary key,
        nome_do_hospital varchar(80),
        cep varchar(50),
        estado varchar(50),
        cidade varchar(50),
        leitos_disponíveis integer,
        nome_medico varchar(50),
        cpf_medico varchar(50),
        crm_medico integer);

        
       
### 8	INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>
       
    --DROP--
 
    DROP TABLE Paciente CASCADE;

    DROP TABLE Hospital CASCADE;

    DROP TABLE Prontuario CASCADE;

    DROP TABLE Endereco CASCADE;
    
    --Create Table--
 
    CREATE TABLE Paciente (
    nome varchar(50),
    cpf varchar(50) primary KEY,
    rg varchar(50),
    fk_Endereco_id integer,
    foreign key (fk_Endereco_id) references Endereco(id),
    data_nascimento date,
    telefone varchar(50));

    CREATE TABLE Endereco (
    id integer primary KEY,
    cep varchar(50),
    numero integer,
    estado varchar(50),
    cidade varchar(50));

    CREATE TABLE Prontuario (
    prontuario_id integer primary KEY,
    fk_Paciente_cpf varchar(50),
    foreign key (fk_Paciente_cpf) references Paciente(cpf),
    fk_hospital_id integer,
    foreign key (fk_hospital_id) references Hospital(id),
    nivel_de_urgencia varchar(50));

    CREATE TABLE Hospital (
    id integer primary key,
    nome_do_hospital varchar(80),
    cep varchar(50),
    estado varchar(50),
    cidade varchar(50),
    leitos_disponíveis integer,
    nome_medico varchar(50),
    cpf_medico varchar(50),
    crm_medico integer);


    --INSERT Dados--
 
    insert into endereco (id, cep, numero, estado, cidade)
         values(1, 60713000, 12, 'CE','Fortaleza'),
         (2, 64089204, 24,'PI','Teresina'),
         (3, 85045520, 52,'PR','Guarapuava'),(4, 77423402, 42,'TO','Gurupi'),
         (5, 69047147, 69,'AM','Manaus'),
         (6, 60743000, 12, 'CE','Fortaleza'),
         (7, 64049204, 24,'PI','Teresina'),
         (8, 85055520, 52,'PR','Guarapuava'),
         (9, 77443402, 42,'TO','Gurupi'),
         (10, 69047147, 69,'AM','Manaus');

    insert into hospital (id, nome_do_hospital, cep, estado, cidade, leitos_disponíveis,
         nome_medico, cpf_medico, crm_medico)
         values(1, 'Hospital São Camilo Fortaleza', 60160280, 'CE', 'Fortaleza', 40, 'Dr. Alceu Valença',
         '42675216038', 1234),
         (2, 'Hospital São Marcos', 64001280, 'PI', 'Teresina', 32, 'Dr. Davi Damiano', '92120563004',
         4321),
         (3, 'Hospital Regional de Guarapuava', 85053525, 'PR', 'Guarapuava', 52, 'Dra. Catherine Zardo',
         '29688119083', 4728),
         (4, 'Hospital Unimed Gurupi', 77103010, 'TO', 'Gurupi', 12, 'Dr. Tarcisio Acordon',
         '38280205004', 1714),
         (5, 'Hospital Adventista de Manaus', 69075351, 'AM', 'Manaus', 79, 'Dra. Ariana Grande',
         '30143905007', 9877),
         (6, 'Hospital São Camilo Fortaleza', 60160280, 'CE', 'Fortaleza', 40, 'Dr. Breno Vargas',
         '41672216038', 1334),
         (7, 'Hospital São Marcos', 64001280, 'PI', 'Teresina', 32, 'Dr. Davi Santiago', '92120583004',
         4311),
         (8, 'Hospital Regional de Guarapuava', 85053525, 'PR', 'Guarapuava', 52, 'Dra. Milene Souza',
         '29687119083', 3728),
         (9, 'Hospital Unimed Gurupi', 77103010, 'TO', 'Gurupi', 12, 'Dr. Delacruz Batista',
         '38280206004', 1716),
         (10, 'Hospital Adventista de Manaus', 69075351, 'AM', 'Manaus', 79, 'Dr. Emanuel Xavier',
         '30144905007', 8877);

    insert into paciente (nome, cpf, rg, fk_endereco_id, data_nascimento, telefone)
        values('Julia Silva', '34696258084', 232123238, 1, '2000-01-01', 99972-2019),
        ('Willian Wirosse', '18799489074', 506051869, 2, '2000-02-01', 99973-2020),
        ('Matheus Melotti', '14354280051', 102667251, 3, '2001-02-09', 99862-1197),
        ('Guilherme Firme', '28370507093', 155258114, 4, '2000-05-10', 99132-2119),
        ('Adenildo Alves', '17112496020', 329334372, 5, '2000-10-01', 99872-2021),
        ('Anastacia Klein', '34693258084', 155781091, 6, '2000-01-11', 99972-2030),
        ('Waldir Xavier', '18799589074', 370079097, 7, '2000-12-31', 99973-2040),
        ('Thalita Melotti', '14354980051', 223256195, 8, '2001-02-19', 99862-1157),
        ('Ricardo Alves', '28370506093', 192179275, 9, '2000-08-20', 99132-2419),
        ('Ademar Maranguni', '17112436020', 284065638, 10, '2000-11-21', 99872-2921);

    insert into prontuario (prontuario_id, nivel_de_urgencia)
         values(1, 'Urgente'),
         (2, 'Nao urgente'),
         (3, 'Emergencia'),
         (4, 'Pouco Urgente'),
         (5, 'Muito Urgente'),
         (6, 'Urgente'),
         (7, 'Nao urgente'),
         (8, 'Emergencia'),
         (9, 'Pouco Urgente'),
         (10, 'Muito Urgente');

### 9	TABELAS E PRINCIPAIS CONSULTAS<br>
    OBS: Incluir para cada tópico as instruções SQL + imagens (print da tela) mostrando os resultados.<br>
#### 9.1	CONSULTAS DAS TABELAS COM TODOS OS DADOS INSERIDOS (Todas) <br>
 Select * 
    From endereco
![Alt text](https://github.com/GuilhermeFiorot/Hospital/blob/master/images/tabela_endereco.png?raw=true "Tabela Endereco") 
 
 Select * 
    From hospital
 ![Alt text](https://github.com/GuilhermeFiorot/Hospital/blob/master/images/tabela_hospital.png?raw=true "Tabela Hospital")
 
 Select * 
    From paciente
 ![Alt text](https://github.com/GuilhermeFiorot/Hospital/blob/master/images/tabela_paciente.png?raw=true "Tabela Paciente")
 
 Select * 
    From prontuario
 ![Alt text](https://github.com/GuilhermeFiorot/Hospital/blob/master/images/tabela_prontuario.png?raw=true "Tabela Prontuario")
 
># Marco de Entrega 01: Do item 1 até o item 9.1<br>

#### 9.2	CONSULTAS DAS TABELAS COM FILTROS WHERE (Mínimo 4)<br>
    
    Select * From estado Where cidade = 'Gurupi';
    Select * From hospital Where nome_do_hospital = 'Hospital São Marcos';
    Select * From prontuario Where nivel_de_urgencia = 'Urgente';
    Select * From endereco Where estado = 'CE';
    
#### 9.3	CONSULTAS QUE USAM OPERADORES LÓGICOS, ARITMÉTICOS E TABELAS OU CAMPOS RENOMEADOS (Mínimo 11)
    a) Criar 5 consultas que envolvam os operadores lógicos AND, OR e Not
    
    select * from hospital where (leitos_disponíveis > 0 and leitos_disponíveis < 70);
    select * from hospital where (estado = 'CE' or estado = 'PR');
    select * from endereco where estado not in ('AM');                                                                          
    select * from prontuario where (nivel_de_urgencia = 'Urgente' or nivel_de_urgencia = 'Nao urgente');
    select * from endereco where estado not in ('PR');
                                                                                      
    b) Criar no mínimo 3 consultas com operadores aritméticos 
                                                                                      
    select * from hospital where (leitos_disponíveis/2 > 20);
    select * from hospital where (leitos_disponíveis-1 != 0);
    select * from hospital where (leitos_disponíveis/5 > 10);
    
    c) Criar no mínimo 3 consultas com operação de renomear nomes de campos ou tabelas

    select nome_do_hospital, cep, estado, cidade as regiao, leitos_disponíveis as vagas from hospital;
    select nome as paciente, cpf, rg, fk_endereco_id as id_endereco from paciente;
    select fk_paciente_cpf as cpf_do_paciente, fk_hospital_id as hospital, nivel_de_urgencia from prontuario;

#### 9.4	CONSULTAS QUE USAM OPERADORES LIKE E DATAS (Mínimo 12) <br>
    a) Criar outras 5 consultas que envolvam like ou ilike
    
    Select * From paciente p Where nome like '%a'
    Select * From paciente p Where nome like 'T%a'
    Select * From endereco e Where e.cidade ilike 'G%'
    Select * From endereco e Where e.estado like 'C_'
    Select * From hospital h Where h.nome_do_hospital ilike '___'
    
    b) Criar uma consulta para cada tipo de função data apresentada.
    
    Select * From paciente p Where p.data_nascimento = current_date;
    Select p.data_nascimento, current_date as dia_atual, age(current_date,p.data_nascimento) From paciente p;
    Select p.data_nascimento, date_part('days', p.data_nascimento) From paciente p;
    Select isfinite(data_nascimento) From paciente p;
    Select p.data_nascimento, extract('year' From p.data_nascimento) as datanascimento From paciente p;
    Select concat(date_part('year', p.data_nascimento), ', ', p.nome) From paciente p;
    Select * From paciente p Where data_nascimento > '2000-12-30';

#### 9.5	INSTRUÇÕES APLICANDO ATUALIZAÇÃO E EXCLUSÃO DE DADOS (Mínimo 6)<br>
    a) Criar minimo 3 de exclusão
   
    Delete From paciente Where rg = 155781091
    Delete From hospital Where id = 10
    Delete From endereco Where id = 10
    
    b) Criar minimo 3 de atualização
    
    Update endereco Set cep = 62010820, estado = 'CE', cidade = 'Sobral' Where id = 8
    Update paciente Set nome = 'Julia Silva Costa' Where rg = 155781091
    Update prontuario Set nivel_de_urgencia = 'Muito urgente' Where prontuario_id = 1

#### 9.6	CONSULTAS COM INNER JOIN E ORDER BY (Mínimo 6)<br>
    a) Uma junção que envolva todas as tabelas possuindo no mínimo 2 registros no resultado
    
    select p.nome, e.estado, h.nome_do_hospital , p2.nivel_de_urgencia, h.nome_medico
    from hospital h
    inner join prontuario p2 on (h.id = p2.fk_hospital_id)
    inner join paciente p on (p2.fk_paciente_cpf = p.cpf)
    inner join endereco e on  (p.fk_endereco_id = e.id)
    where p2.nivel_de_urgencia = 'Urgente'
    order by p.nome;
    
    b) Outras junções que o grupo considere como sendo as de principal importância para o trabalho
    
    select p.nome, p.cpf, p.rg, e.estado, e.cidade, e.cep, e.numero
    from paciente p
    inner join endereco e on (p.fk_endereco_id = e.id)
    where e.id between 2 and 5
    order by p.nome;

    select p.nome, p2.nivel_de_urgencia, h.nome_do_hospital, h.nome_medico
    from hospital h
    inner join prontuario p2 on (h.id = p2.fk_hospital_id)
    inner join paciente p on (p.cpf = p2.fk_paciente_cpf)
    where p2.nivel_de_urgencia = 'Emergencia'
    order by p2.nivel_de_urgencia;

    select h.leitos_disponíveis, h.cidade, h.estado, h.nome_do_hospital, h.nome_do_hospital, p2.nivel_de_urgencia 
    from hospital h
    inner join prontuario p2 on (h.id = p2.fk_hospital_id)
    where h.leitos_disponíveis > 20
    order by h.leitos_disponíveis asc;

    select e.estado, e.cidade, p2.nivel_de_urgencia,
    from paciente p
    inner join prontuario p2 on (p.cpf = p2.fk_paciente_cpf)
    inner join endereco e on (p.fk_endereco_id = e.id)
    where p2.nivel_de_urgencia = 'Nao urgente' and 'Pouco Urgente'
    order by e.estado;

    select e.estado, e.cidade, p2.nivel_de_urgencia,
    from paciente p
    inner join prontuario p2 on (p.cpf = p2.fk_paciente_cpf)
    inner join endereco e on (p.fk_endereco_id = e.id)
    where p2.nivel_de_urgencia = 'Urgente' and 'Muito Urgente'
    order by e.estado;

#### 9.7	CONSULTAS COM GROUP BY E FUNÇÕES DE AGRUPAMENTO (Mínimo 6)<br>
    a) Criar minimo 2 envolvendo algum tipo de junção
    
    select p2.nivel_de_urgencia , count(p2.*)
    from prontuario p2
    inner join hospital h on (p2.fk_hospital_id = h.id)
    group by p2.nivel_de_urgencia;

    select h.nome_do_hospital , sum(h.leitos_disponíveis)
    from hospital h
    inner join prontuario p2 on (h.id = p2.fk_hospital_id)
    group by h.nome_do_hospital
    order by sum(h.leitos_disponíveis) desc;

    select h.nome_do_hospital, p2.nivel_de_urgencia , count(p2.*)
    from prontuario p2
    inner join hospital h on (p2.fk_hospital_id = h.id)
    where p2.nivel_de_urgencia = 'Urgente'
    group by h.nome_do_hospital
    order by count(p2.*) desc;

    select h.nome_do_hospital, count(h.nome_medico) as numero_de_medicos
    from prontuario p2
    inner join hospital h on (p2.fk_hospital_id = h.id)
    group by h.nome_do_hospital
    order by numero_de_medicos DESC;

    select e.estado, count(e.cidade) as quant_de_cidades
    from paciente p
    inner join endereco e ON (p.fk_endereco_id = e.id)
    group by e.estado
    order by quant_de_cidades DESC;

    select e.estado ,count(h.id) as quant_hospital
    from paciente p
    inner join endereco e ON (p.fk_endereco_id = e.id)
    inner join prontuario p2 on (p.cpf = p2.fk_paciente_cpf)
    inner join hospital h on (p2.fk_hospital_id = h.id)
    where e.estado = h.estado
    group by e.estado
    order by quant_hospital DESC;

#### 9.8	CONSULTAS COM LEFT, RIGHT E FULL JOIN (Mínimo 4)<br>
    a) Criar minimo 1 de cada tipo
        
    select * from prontuario p2 left join hospital h on h.id = p2.prontuario_id group by p2.prontuario_id, h.id ;
    
    select * from paciente p left join hospital h ON (p.fk_endereco_id = h.id);
    
    select * from prontuario p2 right join paciente p on p2.fk_paciente_cpf = p.cpf right join hospital h on h.id = p2.prontuario_id group by p2.fk_paciente_cpf, p.cpf, p2.prontuario_id , h.id;
    
    select * from prontuario p2 full join hospital h on h.id = p2.prontuario_id group by p2.prontuario_id, h.id ;

#### 9.9	CONSULTAS COM SELF JOIN E VIEW (Mínimo 6)<br>
        a) Uma junção que envolva Self Join (caso não ocorra na base justificar e substituir por uma view)

        create view hospita_mais_leitos_disponiveis as
        select h.nome_do_hospital , sum(h.leitos_disponíveis)
        from hospital h
        group by h.nome_do_hospital
        order by sum(h.leitos_disponíveis) desc
        limit 1;

        create view hospita_menos_leitos_disponiveis as;
        select h.nome_do_hospital , sum(h.leitos_disponíveis)
        from hospital h
        group by h.nome_do_hospital
        order by sum(h.leitos_disponíveis) asc
        limit 1;

        create view quantidade_hospital_por_estado_dos_pacientes as
        select e.estado ,count(h.id) as quant_hospital
        from paciente p
        inner join endereco e ON (p.fk_endereco_id = e.id)
        inner join prontuario p2 on (p.cpf = p2.fk_paciente_cpf)
        inner join hospital h on (p2.fk_hospital_id = h.id)
        where e.estado = h.estado

        create view pacientes_por_nivel_de_urgencia as;
        select p2.nivel_de_urgencia, p.nome, count(p2.*)
        from paciente p
        inner join prontuario p2 on (p.cpf = p2.fk_paciente_cpf)
        group by p2.nivel_de_urgencia
        order by count(p2.*) desc;
        group by e.estado
        order by quant_hospital DESC;
    
        b) Outras junções com views que o grupo considere como sendo de relevante importância para o trabalho

#### 9.10	SUBCONSULTAS (Mínimo 4)<br>
     a) Criar minimo 1 envolvendo GROUP BY
    
    select * from prontuario p2 join hospital h on h.id = p2.prontuario_id group by p2.prontuario_id, h.id ;
    select * from prontuario p2 join paciente p on p2.fk_paciente_cpf = p.cpf join hospital h on h.id = p2.prontuario_id group by p2.fk_paciente_cpf, p.cpf, p2.prontuario_id, h.id;
   
     b) Criar minimo 1 envolvendo algum tipo de junção
   
    select * from paciente p inner join endereco e on p.fk_endereco_id = e.id;
    SELECT * FROM paciente p INNER JOIN hospital h ON (p.fk_endereco_id = h.id);

># Marco de Entrega 02: Do item 9.2 até o ítem 9.10<br>

### 10 RELATÓRIOS E GRÁFICOS

#### a) análises e resultados provenientes do banco de dados desenvolvido (usar modelo disponível)
#### b) link com exemplo de relatórios será disponiblizado pelo professor no AVA
#### OBS: Esta é uma atividade de grande relevância no contexto do trabalho. Mantenha o foco nos 5 principais relatórios/resultados visando obter o melhor resultado possível.

    

### 11	AJUSTES DA DOCUMENTAÇÃO, CRIAÇÃO DOS SLIDES E VÍDEO PARA APRESENTAÇAO FINAL <br>

#### a) Modelo (pecha kucha)<br>
#### b) Tempo de apresentação 6:40 

># Marco de Entrega 03: Itens 10 e 11<br>
<br>
<br>
<br> 



### 12 FORMATACAO NO GIT:<br> 
https://help.github.com/articles/basic-writing-and-formatting-syntax/
<comentario no git>
    
##### About Formatting
    https://help.github.com/articles/about-writing-and-formatting-on-github/
    
##### Basic Formatting in Git
    
    https://help.github.com/articles/basic-writing-and-formatting-syntax/#referencing-issues-and-pull-requests
    
    
##### Working with advanced formatting
    https://help.github.com/articles/working-with-advanced-formatting/
#### Mastering Markdown
    https://guides.github.com/features/mastering-markdown/

    
### OBSERVAÇÕES IMPORTANTES

#### Todos os arquivos que fazem parte do projeto (Imagens, pdfs, arquivos fonte, etc..), devem estar presentes no GIT. Os arquivos do projeto vigente não devem ser armazenados em quaisquer outras plataformas.
1. <strong>Caso existam arquivos com conteúdos sigilosos<strong>, comunicar o professor que definirá em conjunto com o grupo a melhor forma de armazenamento do arquivo.

#### Todos os grupos deverão fazer Fork deste repositório e dar permissões administrativas ao usuário do git "profmoisesomena", para acompanhamento do trabalho.

#### Os usuários criados no GIT devem possuir o nome de identificação do aluno (não serão aceitos nomes como Eu123, meuprojeto, pro456, etc). Em caso de dúvida comunicar o professor.


Link para BrModelo:<br>
http://www.sis4.com/brModelo/download.html
<br>


Link para curso de GIT<br>
![https://www.youtube.com/curso_git](https://www.youtube.com/playlist?list=PLo7sFyCeiGUdIyEmHdfbuD2eR4XPDqnN2?raw=true "Title")


