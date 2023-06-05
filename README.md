# engenharia_reversa
CREATE TABLE coberturas 
( 
 id (10) INT,  
 inicio_de_periodo DATE,  
 fim_de_periodo INT,  
 previsao_de_parto INT,  
 tipo (191) VARCHAR(n),  
 reprodutor_id (10) INT,  
); 

CREATE TABLE entradas 
( 
 id` (10) INT,  
 entrada_id` (10) INT,  
 entrable_type` (191) VARCHAR(n),  
 `fazenda_id`  (10) INT,  
); 

CREATE TABLE fazenda 
( 
 id (10) INT AUTO_INCREMENT,  
 nome (200) VARCHAR(n),  
 atividades (5000) VARCHAR(n),  
 atividade_principal (5000) INT,  
 hectares` double(8,2) FLOAT,  
 cep` (15) INT,  
 logradouro`(200) VARCHAR(n),  
 numero`(15) CHAR(n),  
 complemento`(100) VARCHAR(n),  
 cidade`  (200) INT,  
 estado (2) INT,  
 user_id` (10) INT,  
 ativo@boolean INT,  
); 

CREATE TABLE Fornecedores 
( 
 `id` (10) INT,  
 nome (200) VARCHAR(n),  
 telefone (15) CHAR(n),  
 email (60) VARCHAR(n),  
 cep (15) CHAR(n),  
 logradouro(200) VARCHAR(n),  
 numero(15) CHAR(n),  
 complemento(100) VARCHAR(n),  
 cidade(100) INT,  
 estado(2) VARCHAR(n) AUTO_INCREMENT,  
 idfazenda INT,  
); 

CREATE TABLE funcões 
( 
 id (10) INT,  
 nome (200) VARCHAR(n),  
 descrição (200) INT,  
 idFornecedores INT,  
); 

CREATE TABLE insumos 
( 
 idTabela1 INT,  
 nome(200) INT,  
 descrição(200) INT,  
 quantidade (15) INT,  
 unidade(50) VARCHAR(n),  
 nota_fiscal(200) INT,  
 valor_unitario double(8,2) FLOAT,  
 valor_total` double(8,2) INT,  
 fazenda_id INT,  
 fornecedor(10) INT,  
 idfuncões INT,  
); 

CREATE TABLE Lembretes 
( 
 id(10) INT,  
 titulo(50) VARCHAR(n),  
 data_fim DATE,  
 ativo@boolean INT,  
 user_id(10) INT,  
 idinsumos INT,  
); 

CREATE TABLE lotes 
( 
 id(10) INT,  
 nome(50) VARCHAR(n),  
 custo double(8,2) FLOAT,  
 inicio_manejo DATE,  
 fim_manejo INT,  
 quantidade_pesagens(15) CHAR(n),  
 meta_dia double (8,2) INT,  
 meta_final double(8,2) INT,  
 ativo@double FLOAT,  
 fazenda_id(10) INT,  
 idLembretes INT,  
); 

CREATE TABLE manejos 
( 
 id (10) INT,  
 detalhes(200) VARCHAR(n),  
 tipo(100) INT,  
 responsavel(100) INT,  
 via(100) INT,  
); 

CREATE TABLE matriz_cobertura 
( 
 id(10) INT,  
 matriz_id(10) INT,  
 cobertura_id INT,  
); 

CREATE TABLE `migrations 
( 
 id (10) INT,  
 migration (200) VARCHAR(n),  
 batch!(15) INT,  
); 

CREATE TABLE produtos 
( 
 id(10) INT,  
 nome(200) INT,  
 sexo(2) CHAR(n),  
 afixo(100) INT,  
 brinco(20) VARCHAR(n),  
 registro(200) INT,  
 foto(20) INT,  
 tod(40) CHAR(n),  
 toe(40) INT,  
 tat(400 INT,  
 fbb(40) INT,  
 peso` double(8,2) FLOAT,  
 valor` double(8,2) INT,  
 pelagem(40) VARCHAR(n),  
 data_de-nascimento DATE,  
 interno`@double INT,  
 te(1) FLOAT,  
 nome_pai(100) VARCHAR(n),  
 nome_mae(100) INT,  
 registro_pai(200) INT,  
 registro_mae(100) INT,  
 gf_pai(200) INT,  
 gm_pai(200) INT,  
 registro_gf_pai(200) INT,  
 registro_gm_pai(200) INT,  
 gf_mae(200) INT,  
 `gm_mae(200) INT,  
 registro_gf_mae(200) INT,  
 registro_gm_mae(200) INT,  
 ggf_pai_gf(200) INT,  
 ggm_pai_gf(200) INT,  
 registro_ggf_pai_gf(200) INT,  
 registro_ggm_pai_gf`(2000 INT,  
 ggf_pai_gm(200) INT,  
 ggm_pai_gm(200) INT,  
 registro_ggf_pai_gm(200) INT,  
 registro_ggm_pai_gm(200) INT,  
 ggf_mae_gf` char(200) INT,  
 ggm_mae_gf(200) INT,  
 registro_ggf_mae_gf(200) INT,  
 registro_ggm_mae_gf(200) INT,  
 ggf_mae_gm(200) INT,  
 ggm_mae_gm(200) INT,  
 registro_ggf_mae_gm(200) INT,  
 registro_ggm_mae_gm(200) INT,  
 fazenda_id` int(10) INT NOT NULL,  
 funcao_id` (10) INT NOT NULL,  
 raca_id`(10) INT NOT NULL,  
 lote_id` (10) INT,  
); 

CREATE TABLE password_resets 
( 
 email` (100) VARCHAR(n),  
 token(30) INT,  
); 

CREATE TABLE produtos_manejos 
( 
 `id` int(10) INT,  
 produto_id` int(10) INT,  
 manejo_id` int(10) INT,  
 quantidade` int(11) INT,  
 peso` double(6,3) FLOAT,  
); 

CREATE TABLE `produto_tipos 
( 
 idprodutos INT,  
 id` int(10) INT,  
 nome` varchar(200) INT,  
 descricao` (200) VARCHAR(n),  
); 

CREATE TABLE racças 
( 
 `id` int(10) INT,  
 nome` (200) VARCHAR(n),  
 descricao(200) INT,  
); 

CREATE TABLE receptoras 
( 
 id(10) INT,  
 brinco (40) CHAR(n),  
 tod` (40) INT,  
 toe`(40) INT,  
 tat` (40) INT,  
 saida_id` int(10) INT,  
 receptora_id` int(10) INT,  
); 

CREATE TABLE saidas 
( 
 id` (10) INT,  
 saidable_id` (10) INT,  
 saidable_type` varchar(200) INT,  
 fazenda_id` (10) INT,  
); 

CREATE TABLE saidas_semens_e_embrioes 
( 
 id` (10) INT,  
 quantidade (11) VARCHAR(n),  
 valor` double(8,2) FLOAT,  
 data_inicial date DATE,  
 data_final date INT,  
 data_do_implante` date INT,  
 data_de_congelamento` date INT,  
 novo_proprietario(200) VARCHAR(n),  
 codigo_do_novo_proprietario` (10) INT,  
 num_comunicacao_te` (200) VARCHAR(n),  
 veterinario(200) INT,  
 crmv_de_veterinario` (200) INT,  
 tipo_de_semen` (10) INT,  
 tipo_de_inseminacao (10) INT,  
 semens_e_embrioes_id`(10) INT,  
 tipo_de_saida_id` int(10) INT,  
 novo_proprietario_id` (10) INT,  
); 

CREATE TABLE saida_produtos 
( 
 id` (10) INT,  
 contrato_inicio` DATE,  
 contrato_fim INT,  
 data INT,  
 valor` double(7,2) FLOAT,  
 destino_estabelecimento  (200) INT,  
 pode_emprestar( 1) VARCHAR(n),  
 meio` enum(10) INT,  
 motivo` enum(100) INT,  
 motivo_descarte` (200) INT,  
 transferencia_definitiva` (20) INT,  
 destino_id` (10) INT,  
); 

CREATE TABLE semens_e_embrioes 
( 
 `id` (10) INT,  
 semen` char(10) CHAR(n),  
 interno` (10) INT,  
 valor` double(8,2) FLOAT,  
 quantidade (11) INT,  
 unidade` (200) VARCHAR(n),  
 data_da_colheita` date DATE,  
 nome_pai` (200) INT,  
 nome_mae` (200) INT,  
 registro_pai` (200) INT,  
 registro_mae` (200) INT,  
 gf_pai` char(200) INT,  
 gm_pai` char(200 INT,  
 registro_gf_pai` (200) INT,  
 registro_gm_pai` (200 INT,  
 gf_mae` (200) INT,  
 gm_mae` (200) INT,  
 registro_gf_mae` (200) INT,  
 registro_gm_mae(200) INT,  
 ggf_pai_gf` (200) INT,  
 ggm_pai_gf` (200) INT,  
 registro_ggf_pai_gf` (200) INT,  
 registro_ggm_pai_gf` (200) INT,  
 ggf_pai_gm` (200) INT,  
 ggm_pai_gm` (200) INT,  
 registro_ggf_pai_gm` (200) INT,  
 registro_ggm_pai_gm` (200) INT,  
 ggf_mae_gf` (200) INT,  
 ggm_mae_gf` (200) INT,  
 registro_ggm_mae_gf` (200) INT,  
 ggf_mae_gm` (200) INT,  
 ggm_mae_gm` (200) INT,  
 registro_ggm_mae_gm` (200) INT,  
 fazenda_id` (10) INT,  
 funcao_id` int(10) INT,  
 raca_id` (10) INT,  
 `lote_id` (10) INT,  
 idsaidas_semens_e_embrioes INT,  
); 

CREATE TABLE tipos_de_saida_semens_e_embrioes 
( 
 id` (10) INT,  
 nome` (200) VARCHAR(n),  
 descricao` (200) INT,  
); 

CREATE TABLE users 
( 
 id` (10) INT,  
 nome` (200) VARCHAR(n),  
 atividade_principal`  (200) INT,  
 imagem_de_perfil` (200) INT,  
 ativo@boolean(1) INT,  
 email` (200) INT,  
 user_tipo_id` (10) INT,  
 password` (200) INT,  
 remember_token` (100) INT,  
); 

CREATE TABLE users_fazendas 
( 
 idusers INT,  
 id` (10) INT,  
 user_id` (10) INT,  
 fazenda_id` int(10) INT,  
); 

CREATE TABLE `user_dados 
( 
 id` (10) INT,  
 nome` (200) VARCHAR(n),  
 email` (200) INT,  
 cpf` (11) INT,  
 rg` (14) INT,  
 cep` 14) INT,  
 `estado` (2) INT,  
 cidade` 255 INT,  
 municipio` 255) INT,  
 bairro` (255) INT,  
 logradouro` (255) INT,  
 numero` (10) INT,  
 telefone` (18) INT,  
 complemento` (255) INT,  
 codigo_abcc` (200) INT,  
 codigo_arco` (200) INT,  
 afixo` (200) INT,  
 user_id` (10) INT,  
); 

CREATE TABLE user_tipos 
( 
 id` (10) INT,  
 nome` (200) INT,  
 permissoes` (2000) INT,  
 perfil` (50) INT,  
); 

ALTER TABLE Fornecedores ADD FOREIGN KEY(idfazenda) REFERENCES fazenda (idfazenda)
ALTER TABLE funcões ADD FOREIGN KEY(idFornecedores) REFERENCES Fornecedores (idFornecedores)
ALTER TABLE insumos ADD FOREIGN KEY(idTabela1) REFERENCES Lembretes (idTabela1)
ALTER TABLE insumos ADD FOREIGN KEY(idfuncões) REFERENCES funcões (idfuncões)
ALTER TABLE Lembretes ADD FOREIGN KEY(idinsumos) REFERENCES insumos (idinsumos)
ALTER TABLE lotes ADD FOREIGN KEY(idLembretes) REFERENCES Lembretes (idLembretes)
ALTER TABLE matriz_cobertura ADD FOREIGN KEY(cobertura_id) REFERENCES coberturas (cobertura_id)
ALTER TABLE produtos ADD FOREIGN KEY(fazenda_id` int(10)) REFERENCES fazenda (fazenda_id` int(10))
ALTER TABLE `produto_tipos ADD FOREIGN KEY(idprodutos) REFERENCES produtos (idprodutos)
ALTER TABLE semens_e_embrioes ADD FOREIGN KEY(idsaidas_semens_e_embrioes) REFERENCES saidas_semens_e_embrioes (idsaidas_semens_e_embrioes)
ALTER TABLE users_fazendas ADD FOREIGN KEY(idusers) REFERENCES users (idusers)
