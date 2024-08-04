# Documentação 

Antes do inicio dos testes é muito importante esclarecer todas as duvidas com o time responsável sobre o produto:
* Requisitos funcionais e não-funcionais;
* Fluxos de usuário e cenários criticos;
* Integrações e dependências.
   
É importante ressaltar que a qualidade é uma cultura que deve ser adotada por toda a equipe. Mesmo com as melhores ferramentas disponíveis, a qualidade só será alcançada se todos os membros do time seguirem rigorosamente os processos e padrões estabelecidos.


## Sumário
1. USER STORY
2. CENÁRIOS E CASOS DE TESTE
3. RELATÓRIO COM TODOS OS BUGS ENCONTRADOS
4. EVIDÊNCIAS


## 1. User Story
As User Stories foram decididas baseadas nos pontos de função presentes no módulo de curso do Beedoo Chalenge.

### Users story: Listar Curso

#### DESCRIÇÃO:
**Como** um usuário do módulo de curso no Beedoo,  
**Eu quero** que seja criada uma seção chamada "Listar Curso" no módulo de curso,  
**Para que** eu possa visualizar a tela inicial do módulo, onde será exibida toda a grade de cursos disponíveis.

#### CRITÉRIOS DE ACEITE:
***Tela - Listar Curso***
* Elementos da Tela: 
  * A tela deve conter um menu fixo no cabeçalho: 
    * Com o texto "Beedoo QA Chalenge" no canto esquerdo e dois links de navegação "Listar Curso" e "Cadastrar Curso" no canto direito do menu.
	* Pagina de listagem dos cursos:
	  * Deve conter um titulo "Lista de cursos" e os cards, em duas colunas, com as informações dos cursos cadastrados:
		* Imagem da capa: Mostrar a imagem relacionada ao curso;
		* Tipo do Curso: Um campo para informar o tipo de curso, ex. "Presencial" ou "Online";
		* Nome do Curso: Um campo para informar o nome de curso;
		* Descrição do Curso: Um campo para informar detalhes sobre o curso;
		* Data de início: Um campo para informar a data de início do curso;
		* Data de fim: Um campo para informar a data de conclusão do curso;
		* Número de vagas: Um campo para informar o número de vagas disponível no curso;
		* Botão Excluir: Um botão para excluir as informações do curso.

#### REGRAS DE NEGÓCIO:
* Imagem da capa:
  	* A imagem deve ser exibida na parte superior do card;		
* Tipo de Curso:
  	* Deve ser exibido abaixo da imagem;
	* Font: Padrão do projeto, 12px;
	* Color: #EF6C00.
* Nome do Curso:
  	* Deve ser exibido abaixo do tipo do Curso;
	* Font: Padrão do projeto, 24px;
	* Color: #000000.
* Descrição do Curso:
  	* Deve ser exibido abaixo do Nome do Curso;
	* Font: Padrão do projeto, 12px;
	* Color: #9E9E9E.
* Data de Início:
	* Deve ser exibido abaixo da Descrição do Curso;
	* Font: Padrão do projeto, 14px;
	* Color: #1976D2;
	* Exemplo: "Inicio: AAAA-MM-DD".
* Data de Fim:  
  	* Deve ser exibido a frente da Data de Início;
	* Font: Padrão do projeto, 14px;
	* Color: #1976D2;
	* Exemplo: "Inicio: AAAA-MM-DD".
* Número de Vagas:
	* Deve ser exibido a frente da Data de Fim;
	* Font: Padrão do projeto, 14px;
	* Color: #26A69A.
* Botão Excluir Curso:
  * Ao clicar no botão botão "Excluir Curso", o sistema deve:
	* Apagar o curso na base de dados;
	* Exibir uma mensagem de sucesso "Curso excluído com sucesso!";

#### OBSERVAÇÃO:
* Fonte padrão do projeto:
  * ROBOTO.

### Users story: Cadastrar Curso

#### DESCRIÇÃO:
**Como** um usuário do módulo de curso no Beedoo,  
**Eu quero** ter uma seção chamada "Cadastrar Curso" no módulo de curso,  
**Para que** eu possa cadastrar novos cursos que serão disponibilizados para o público.


#### CRITÉRIOS DE ACEITE:
***Tela - Cadastrar Curso***
* Elementos da Tela: 
  * A tela deve conter um titulo "Cadastro de curso" e formulário com os campos:
    * Nome do Curso: Um campo para inserir o nome do curso;
		*	Descrição do curso: Um campo para inserir a detalhes descritivos sobre o curso;
		*	Instrutor: Um campo para inserir o nome do instrutor do curso;
		*	URL da Imagem da capa: Um campo para inserir a url da imagem do curso;
		*	Data de início: Um campo para inserir a data de início do curso;
		*	Data de fim: Um campo para inserir a data de conclusão do curso;
		*	Número de vagas: Um campo para inserir o número de vagas disponível no curso;
		*	Tipo de curso: Um campo para escolher o tipo de curso, ex. "Presencial" ou "Online"
		*	Endereço: Um campo para inserir um endereço, caso o tipo de curso seja presencial;
		*	Link de Inscrição: Um campo para inserir um link de inscrição, caso o tipo de curso seja online;
		*	Botão Cadastrar: Um botão para salvar as informações inseridas.

#### REGRAS DE NEGÓCIO:
* Nome do Curso:
  * Deve ser de preenchimento obrigatório;
	*	Deve permitir texto alfabético, números, espaços e caracteres especiais;
	*	Não deve permitir caracteres inválidos, como emojis ou símbolos.
* Descrição do Curso:
	*	Deve ser de preenchimento obrigatório;
	*	Deve permitir texto alfabético, números, espaços e caracteres especiais;
	*	Não deve permitir caracteres inválidos, como emojis,  símbolos e link;
	*	O campo deve ter um comprimento mínimo de 50 caracteres, para garantir que informações suficientes sejam fornecidas;
	*	O campo deve ter um limite máximo de 2000 caracteres para evitar descrições excessivamente longas;
	*	O campo deve aceitar texto simples, mas pode também permitir formatação básica (negrito, itálico, sublinhado) e listas (numeradas ou com marcadores);
* Instrutor:
	*	Deve ser de preenchimento obrigatório;
	*	Deve aceitar somente texto alfabético.
*	URL da Imagem da capa:
	*	Campo de imagem, não obrigatório;
	*	A URL deve começar com "http://" ou "https://".
	*	Deve permitir o upload de arquivos de imagem nos formatos JPG, WEBP ou PNG;
	*	O tamanho máximo do arquivo deve ser de 5MB.
*	Data de Início:
	*	Campo de data obrigatório;
	*	Deve permitir a seleção de datas futuras;
	*	Caso haja uma Data de Fim definida, a Data de Início deve obrigatoriamente ocorrer antes dessa Data de Fim.
*	Data de Fim:  
	*	Campo de data, não obrigatório;
	*	Deve permitir a seleção de datas futuras;
	*	Deve ser posterior à Data de Início.
* Número de Vagas:
	*	Campo de número de vagas, não obrigatório;
	*	Deve permitir somente números;
*	Tipo de Curso:
	*	Campo obrigatório;
	*	Seleção entre "Presencial" e "Online".
*	Endereço: 
	*	Campo só deve ser visível e obrigatório, caso o tipo de curso seja presencial;
	*	Deve permitir texto alfabético, números, espaços e caracteres especiais;
	*	Não deve permitir caracteres inválidos, como emojis,  símbolos e link;
	*	O campo deve ter um comprimento mínimo de 10 caracteres, para garantir que informações suficientes sejam fornecidas;
	*	O campo deve ter um limite máximo de 150 caracteres para evitar informações excessivamente longas;
*	Link de Inscrição: 
	*	Campo só deve ser visível e obrigatório, caso o tipo de curso seja online;
	*	A URL deve começar com "http://" ou "https://".
	
*	Botão cadastrar:
	*	Ao clicar no botão "Botão Cadastrar", o sistema deve:
		*	Validar os dados preenchidos nos campos obrigatórios.
			*	Se todos os dados estiverem válidos, o sistema deve:
				*	Cadastrar o novo curso na base de dados;
				*	Exibir uma mensagem de sucesso "Curso cadastrado com sucesso!";
				*	Redirecionar o usuário para a lista de cursos.
			*	Se algum campo obrigatório estiver vazio ou inválido, o sistema deve exibir uma mensagem de erro ao lado do campo em questão.


## 2. Cenários e Casos de teste
[Planilha](https://docs.google.com/spreadsheets/d/16mnkVMhV-VGeiGPn1Gvc-ow9MynUlqoaULRfZsUoK74/edit?usp=sharing)


## 3. Relatório com todos os bugs encontrados
* Vulnerabilidades Identificadas
	* Validação de Entrada Insuficiente
		* Descrição: O sistema permite o cadastro de cursos com campos obrigatórios em branco ou preenchidos de forma inadequada.
		* Risco: Dados incompletos ou inválidos são armazenados, o que pode comprometer a integridade dos dados e a funcionalidade do sistema.
	* Falta de Mensagens de Erro Específicas
		* Descrição: Não há feedback claro para o usuário sobre quais campos estão incorretos ou faltando.
		* Risco: Dificulta a correção de erros pelo usuário e pode levar a dados incorretos sendo salvos.

[Relatório](https://docs.google.com/spreadsheets/d/1z3YyZnf3VF9Y0zHVv9qv5CH5-1REu77xScnpZD1KmAk/edit?usp=sharing)

## 4. Evidências
[Evidências](https://drive.google.com/drive/folders/1o41EJ1vqw3x6O5tSbkQ4FTbl3GnH9Ca9?usp=sharing)


