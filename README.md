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
    3- Regiões com mais leitos disponiveis,
    4- Fluxo de pacientes nos hospitais,
    5- Regiões mais afetadas por Nivel de Urgencia.
 

#### 4.3 TABELA DE DADOS DO SISTEMA:
    a) Esta tabela deve conter todos os atributos do sistema e um mínimo de 10 linhas/registros de dados.
    b) Esta tabela tem a intenção de simular um relatório com todos os dados que serão armazenados 
    
![Exemplo de Tabela de dados do Hospitais contra o covid](https://github.com/GuilhermeFiorot/Hospital/blob/master/arquivos/TabelaHospitalcontraCovid.xlsx?raw=true "Tabela - Hospitais Contra Covid")
    
    
### 5.MODELO CONCEITUAL<br>
        
![Alt text](https://github.com/GuilhermeFiorot/Hospital/blob/master/images/modelo_conceitual_hospcontracovid.png?raw=true "Modelo Conceitual")
        
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
     Leitos disponiveis: Campo que armazena o número de telefone para cada hospital.<br>
     Medico ID: Campo que armazena o número do ID do medico para cada hospital.<br>

    Prontuario: Tabela que armazena as informações relativas ao prontuario<br>
     Id: campo que armazena o Id para cada prontuario.<br>
     Paciente CPF: campo que armazena o número de Cadastro de Pessoa Física para cada prontuario do paciente.<br>
     Hospital ID: campo que armazena o número do ID do hospital para cada prontuario.<br>
     Nivel de urgencia: campo que armazena o nivel de urgência para cada prontuario.<br>
     Data prontuario: campo que armazena a data de atendimento do paciente no hospital.<br>
    
    Medico:
     Id: campo que armazena o id do medico.<br>
     Nome medico: campo que armazena o nome para cada medico do Hospital.<br>
     Cpf Medico: campo que armazena a Cadastro de Pessoa Fisica para cada medico do Hospital.<br>
     Crm Medico: campo que armazena o Conselho Regional de Medicina para cada medico do Hospital.<br>
    
### 6	MODELO LÓGICO<br>
        a) inclusão do esquema lógico do banco de dados
        b) verificação de correspondencia com o modelo conceitual 
        (não serão aceitos modelos que não estejam em conformidade)
 ![Alt text](https://raw.githubusercontent.com/GuilhermeFiorot/Hospital/master/images/modelo_logico.png?raw=true "Modelo Logico")
    
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
        nivel_de_urgencia varchar(50),
        data_prontuario date);

        CREATE TABLE Hospital (
        id integer primary key,
        nome_do_hospital varchar(80),
        cep integer,
        estado varchar(50),
        cidade varchar(50),
        leitos_disponíveis integer,
        fk_medico_id integer,
        foreign KEY (fk_medico_id) REFERENCES medico(id));

        CREATE TABLE Medico(
        id integer primary key,
        nome_medico varchar(50),
        cpf_medico varchar(50),
        crm_medico varchar(50));


        
       
### 8	INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>
       
    --DROP--
 
    DROP TABLE Paciente CASCADE;

    DROP TABLE Hospital CASCADE;

    DROP TABLE Prontuario CASCADE;

    DROP TABLE Endereco CASCADE;
       
    DROP TABLE Medico CASCADE;
    
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
    nivel_de_urgencia varchar(50),
    data_prontuario date);

    CREATE TABLE Hospital (
    id integer primary key,
    nome_do_hospital varchar(80),
    cep integer,
    estado varchar(50),
    cidade varchar(50),
    leitos_disponíveis integer,
    fk_medico_id integer,
    foreign KEY (fk_medico_id) REFERENCES medico(id));

    CREATE TABLE Medico(
    id integer primary key,
    nome_medico varchar(50),
    cpf_medico varchar(50),
    crm_medico varchar(50));


    --INSERT Dados--
 
    insert into endereco (id, cep, numero, estado, cidade)
         values(1, 60713000, 12, 'CE','Fortaleza'),
         (2, 64089204, 24,'PI','Teresina'),
         (3, 85045520, 52,'PR','Guarapuava'),
         (4, 77423402, 42,'TO','Gurupi'),
         (5, 69047147, 69,'AM','Manaus'),
         (6, 60743000, 12, 'CE','Fortaleza'),
         (7, 64049204, 24,'PI','Teresina'),
         (8, 85055520, 52,'PR','Guarapuava'),
         (9, 77443402, 42,'TO','Gurupi'),
         (10, 69047147, 69,'AM','Manaus');

    insert into hospital (id, nome_do_hospital, cep, estado, cidade, leitos_disponíveis, fk_medico_id)
        values(1, 'Hospital São Camilo Fortaleza', 60160280, 'CE','Fortaleza', 40, 1),
        (2, 'Hospital São Marcos', 64001280, 'PI','Teresina', 32, 2),
        (3, 'Hospital Regional de Guarapuava', 85053525, 'PR','Guarapuava', 52, 3),
        (4, 'Hospital Unimed Gurupi', 77103010, 'TO','Gurupi', 12, 4),
        (5, 'Hospital Adventista de Manaus', 69075351, 'AM','Manaus', 79, 5),
        (6, 'Hospital São Camilo Fortaleza', 60160280, 'CE','Fortaleza', 40, 6),
        (7, 'Hospital São Marcos', 64001280, 'PI','Teresina', 32, 7),
        (8, 'Hospital Regional de Guarapuava', 85053525, 'PR','Guarapuava', 52, 8),
        (9, 'Hospital Unimed Gurupi', 77103010, 'TO','Gurupi', 12, 9),
        (10, 'Hospital Adventista de Manaus', 69075351, 'AM','Manaus', 79, 10);

    insert into paciente (nome, cpf, rg, fk_endereco_id, data_nascimento, telefone)
        values('Julia Silva', '34696258084', '232123238', 1, '2000-01-01', '99972-2019'),
        ('Willian Wirosse', '18799489074', '506051869', 2, '2000-02-01', '99973-2020'),
        ('Matheus Melotti', '14354280051', '102667251', 3, '2001-02-09', '99862-1197'),
        ('Guilherme Firme', '28370507093', '155258114', 4, '2000-05-10', '99132-2119'),
        ('Adenildo Alves', '17112496020', '329334372', 5, '2000-10-01', '99872-2021'),
        ('Anastacia Klein', '34693258084', '155781091', 6, '2000-01-11', '99972-2030'),
        ('Waldir Xavier', '18799589074', '370079097', 7, '2000-12-31', '99973-2040'),
        ('Thalita Melotti', '14354980051', '223256195', 8, '2001-02-19', '99862-1157'),
        ('Ricardo Alves', '28370506093', '192179275', 9, '2000-08-20', '99132-2419'),
        ('Ademar Maranguni', '17112436020', '284065638', 10, '2000-11-21', '99872-2921');

    insert into prontuario (prontuario_id, fk_paciente_cpf, fk_hospital_id ,nivel_de_urgencia, data_prontuario)
        values(1, '34696258084', 1, 'Urgente', '2021-01-09'),
        (2, '18799489074', 2,'Nao urgente', '2021-03-19'),
        (3, '14354280051', 3,'Emergencia', '2020-09-09'),
        (4, '28370507093', 4,'Pouco Urgente', '2021-01-01'),
        (5, '17112496020', 5,'Muito Urgente', '2021-08-27'),
        (6, '34693258084', 6,'Urgente', '2020-11-09'),
        (7, '18799589074', 7, 'Nao urgente', '2021-03-21'),
        (8, '14354980051', 8,'Emergencia', '2021-01-19'),
        (9, '28370506093', 9,'Pouco Urgente', '2021-02-09'),
        (10, '17112436020', 10,'Muito Urgente', '2020-04-19');
    
    insert into medico(id, nome_medico, cpf_medico, crm_medico)
        values(1, 'Dr. Alceu Valença', '42675216038', 1234),
        (2, 'Dr. Davi Damiano', '92120563004', 4321 ),
        (3, 'Dra. Catherine Zardo', '29688119083', 4728),
        (4, 'Dr. Tarcisio Acordon', '38280205004', 1714),
        (5, 'Dra. Ariana Grande', '30143905007', 9877),
        (6, 'Dr. Breno Vargas', '41672216038', 1334),
        (7, 'Dr. Davi Santiago', '92120583004', 4311),
        (8, 'Dra. Milene Souza', '29687119083', 3728),
        (9, 'Dr. Delacruz Batista', '38280206004', 1716),
        (10, 'Dr. Emanuel Xavier', '30144905007', 8877);

### 9	TABELAS E PRINCIPAIS CONSULTAS<br>
    OBS: Incluir para cada tópico as instruções SQL + imagens (print da tela) mostrando os resultados.<br>
#### 9.1	CONSULTAS DAS TABELAS COM TODOS OS DADOS INSERIDOS (Todas) <br>
 Select * 
    From endereco
![Alt text](https://github.com/GuilhermeFiorot/Hospital/blob/master/images/tabela_endereco.png?raw=true "Tabela Endereco") 
 
 Select * 
    From hospital
 ![Alt text](https://github.com/GuilhermeFiorot/Hospital/blob/master/images/tabela_hospital1.png?raw=true "Tabela Hospital")
 
 Select * 
    From paciente
 ![Alt text](https://github.com/GuilhermeFiorot/Hospital/blob/master/images/tabela_paciente.png?raw=true "Tabela Paciente")
 
 Select * 
    From prontuario
 ![Alt text](https://github.com/GuilhermeFiorot/Hospital/blob/master/images/tabela_prontuario1.png?raw=true "Tabela Prontuario")
 
  Select * 
    From medico
 ![Alt text](https://raw.githubusercontent.com/GuilhermeFiorot/Hospital/master/images/tabela_medico.png?raw=true "Tabela Medico")
 
># Marco de Entrega 01: Do item 1 até o item 9.1<br>

#### 9.2	CONSULTAS DAS TABELAS COM FILTROS WHERE (Mínimo 4)<br>

        Codigo + Print em : [Collab](https://colab.research.google.com/drive/1HrHPFqiefvlehPXBQPVJBg-KE9hxvD3i#scrollTo=kCGKpGono59M/)
    
#### 9.3	CONSULTAS QUE USAM OPERADORES LÓGICOS, ARITMÉTICOS E TABELAS OU CAMPOS RENOMEADOS (Mínimo 11)
        a) Criar 5 consultas que envolvam os operadores lógicos AND, OR e Not

        https://colab.research.google.com/drive/1HrHPFqiefvlehPXBQPVJBg-KE9hxvD3i#scrollTo=-L_bAVLZqei3

        b) Criar no mínimo 3 consultas com operadores aritméticos 

        https://colab.research.google.com/drive/1HrHPFqiefvlehPXBQPVJBg-KE9hxvD3i#scrollTo=wDGL4nYcqlf6

        c) Criar no mínimo 3 consultas com operação de renomear nomes de campos ou tabelas

        https://colab.research.google.com/drive/1HrHPFqiefvlehPXBQPVJBg-KE9hxvD3i#scrollTo=O2OB9ys-qn6Y

#### 9.4	CONSULTAS QUE USAM OPERADORES LIKE E DATAS (Mínimo 12) <br>
        a) Criar outras 5 consultas que envolvam like ou ilike

        https://colab.research.google.com/drive/1HrHPFqiefvlehPXBQPVJBg-KE9hxvD3i#scrollTo=D-6yLmUmsdMn&line=1&uniqifier=1

        b) Criar uma consulta para cada tipo de função data apresentada.

        https://colab.research.google.com/drive/1HrHPFqiefvlehPXBQPVJBg-KE9hxvD3i#scrollTo=1famV6oTsev6&line=1&uniqifier=1

#### 9.5	INSTRUÇÕES APLICANDO ATUALIZAÇÃO E EXCLUSÃO DE DADOS (Mínimo 6)<br>
        a) Criar minimo 3 de exclusão

        https://colab.research.google.com/drive/1HrHPFqiefvlehPXBQPVJBg-KE9hxvD3i#scrollTo=iiCs1Aadu-0U

        b) Criar minimo 3 de atualização

       https://colab.research.google.com/drive/1HrHPFqiefvlehPXBQPVJBg-KE9hxvD3i#scrollTo=B874hooXvgjw

#### 9.6	CONSULTAS COM INNER JOIN E ORDER BY (Mínimo 6)<br>
        a) Uma junção que envolva todas as tabelas possuindo no mínimo 2 registros no resultado

        https://colab.research.google.com/drive/1HrHPFqiefvlehPXBQPVJBg-KE9hxvD3i#scrollTo=BKK-uMRR8CWl

        b) Outras junções que o grupo considere como sendo as de principal importância para o trabalho

        https://colab.research.google.com/drive/1HrHPFqiefvlehPXBQPVJBg-KE9hxvD3i#scrollTo=RVxOgRoz8Diq

#### 9.7	CONSULTAS COM GROUP BY E FUNÇÕES DE AGRUPAMENTO (Mínimo 6)<br>
        a) Criar minimo 2 envolvendo algum tipo de junção

        https://colab.research.google.com/drive/1HrHPFqiefvlehPXBQPVJBg-KE9hxvD3i#scrollTo=10S7M2ntpIJU

#### 9.8	CONSULTAS COM LEFT, RIGHT E FULL JOIN (Mínimo 4)<br>
        a) Criar minimo 1 de cada tipo

        https://colab.research.google.com/drive/1HrHPFqiefvlehPXBQPVJBg-KE9hxvD3i#scrollTo=bHiZulNipLfx
    
#### 9.9	CONSULTAS COM SELF JOIN E VIEW (Mínimo 6)<br>
        a) Uma junção que envolva Self Join (caso não ocorra na base justificar e substituir por uma view)

        https://colab.research.google.com/drive/1HrHPFqiefvlehPXBQPVJBg-KE9hxvD3i#scrollTo=NyctY7KWfN-4
    
        b) Outras junções com views que o grupo considere como sendo de relevante importância para o trabalho
    
        https://colab.research.google.com/drive/1HrHPFqiefvlehPXBQPVJBg-KE9hxvD3i#scrollTo=5qWU4vGyfQP0

#### 9.10	SUBCONSULTAS (Mínimo 4)<br>
        a) Criar minimo 1 envolvendo GROUP BY
    
        https://colab.research.google.com/drive/1HrHPFqiefvlehPXBQPVJBg-KE9hxvD3i#scrollTo=CswaQNv1fWSb
   
        b) Criar minimo 1 envolvendo algum tipo de junção
   
        https://colab.research.google.com/drive/1HrHPFqiefvlehPXBQPVJBg-KE9hxvD3i#scrollTo=JgtWQiadfZs7
    
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


