# DESAFIO-BEEDOO

# User Stories

## CRIAR CURSO
Como administradora do sistema,
Eu quero criar um novo curso,
Para que eu possa disponibilizar para os usuários.

## EXCLUIR CURSO
Como administradora do sistema,
Eu quero deletar cursos cadastrados,
Para que eu remova conteúdos desnecessários.

## LISTAR CURSOS
Como administradora do sistema,
Eu quero visualizar os cursos em listas,
Para que eu possa escolher qual curso ver em detalhes.


# CASOS DE TESTE EM GHERKIN

# Cenário: Criar curso Válido
Feature: Criação de curso

Scenario: criar curso válido
  Given estou na pagina de cadastro de curso com o formulário aberto
  When preencho os campos com dados validos
  And clico no botao "cadastrar curso"
  Then o curso deve ser criado com sucesso
  And uma mensagem de "curso cadastrado com sucesso" deve aparecer no topo da página

# Cenário: Criar curso Inválido
Feature: Criação de Curso

Scenario: criar curso inválido
  Given estou na página de cadastro de curso
  When deixo campos obrigatórios sem preenchimento
  And ao clicar no botão "cadastrar curso"
  Then o sistema deve exibir uma mensagem de erro
  And o curso não deve ser criado

# Cenário: Criar Curso Sem Preenchimento
Feature: Criação de Curso

Scenario: Criar curso em sem preenchimento 
  Given estou na página de cadastro de curso
  When deixo todos os campos sem preenchimento
  And ao clicar no botão "cadastrar curso"
  Then o sistema deve exibir uma mensagem de erro
  And o curso não deve ser criado

# Cenário: Excluir Curso
Feature: Exclusão de curso

Scenario: Excluir curso
  Given estou na página de listagem de cursos
  When eu localizo o curso que quer oexcluir
  And clico no botão "excluir curso"
  Then uma mensagem de "curso excluído com sucesso" deve ser exibida na tela
  And o curso deve ser excluído da lista


# PASSO-A-PASSO PARA EXECUÇÃO DE CASO DE TESTE

# Caso de Teste TC1: Criar curso com dados válidos
Pré-condições:
- O usuário deve estar logado na página de cadastro de curso.
- A página de cadastro de curso deve estar visível.

Passos:
1- Abra a página de cadastro de curso
2- Insira os dados válidos nos campos vazios:
  - Nome do curso
  - Descrição do curso
  - Intrutor
  - Url da imagem de capa
  - Data de início
  - Data de fim
  - Número de vagas
  - Tipo de curso
3- Clique no botão "Cadastrar curso"

Resultado Esperado:
  - O curso deve ser criado com sucesso
  - Uma mensagem de curso criado com sucesso deve ser exibida na tela

Resutado Obtido:
  - Curso criado com sucesso
  - Mensagem exibida na tela "curso criado com sucesso"

# Caso de Teste TC2: Criar curso com dados inválidos
Pré-condições:
- O usuário deve estar logado na página de cadastro de curso.
- A página de cadastro de curso deve estar visível.

Passos:
1- Abra a página de cadastro de curso
2- Insira deixe alguns campos vazios
3- Clique no botão "Cadastrar curso"

Resultado Esperado:
  - O curso não deve ser criado com sucesso
  - Uma mensagem de erro deve ser exibida na tela

Resutado Obtido:
  - Curso criado com sucesso
  - Mensagem exibida na tela "curso criado com sucesso"

Observações:
  - O curso foi criado mesmo faltando dados necessários

# Caso de Teste TC3: Criar curso sem preencher dados
Pré-condições:
- O usuário deve estar logado na página de cadastro de curso.
- A página de cadastro de curso deve estar visível.

Passos:
1- Abra a página de cadastro de curso
2- Insira deixe todos os campos vazios
3- Clique no botão "Cadastrar curso"

Resultado Esperado:
  - O curso não deve ser criado com sucesso
  - Uma mensagem de erro deve ser exibida na tela

Resutado Obtido:
  - Curso criado com sucesso
  - Mensagem exibida na tela "curso criado com sucesso"

Observações:
  - O curso foi criado mesmo faltando todos dados necessários

# Caso de Teste TC4: Excluir curso
Pré-condições:
- O usuário deve estar logado na página de listagem de cursos.
- A página de listagem de cursos deve estar visível.
- Precisa ter pelo menos um curso cadastrado visível.

Passos:
1- Abra a página de listagem de cursos
2- Localize o curso que deseja deletar
3- Clique no botão "Excluir Curso"

Resultado Esperado:
  - Curso deve ser excluído da lista com sucesso
  - Mensagem exibida na tela "curso excluído com sucesso"

Resutado Obtido:
  - O curso não foi excluído da listagem
  - Uma mensagem foi exibida na tela "curso excluído com sucesso" mesmo que o curso não tenha sido excluído

Observações:
  - O curso continua na listagem mesmo depois de clicar no botão "Excluir Curso"


# LINKS 
- Planilha de Casos de Teste: https://docs.google.com/spreadsheets/d/1EeS2nxbWJPS9Exv8EM0FWy13d6B4wvu8VJKJNcwDVOo/edit?usp=sharing
- Evidências de Teste - Vídeos MP4: https://drive.google.com/drive/folders/1obIATClbmHI7ysP4W-LQJS-SZqdHp1Vr?usp=sharing



  


