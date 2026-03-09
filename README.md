# DESAFIO-QA-BEEDOO-2026
Manual QA test execution and bug reporting for Beedoo's technical challenge

# OBJETIVO DA APLICAÇÃO
Com base na análise do sistema, a aplicação parece ter como objetivo permitir o cadastro e gerenciamento de cursos, possibilitando que usuários registrem informações como nome do curso, descrição, instrutor, datas, número de vagas, imagem e link de inscrição.
Após o cadastro, os cursos são exibidos em uma listagem em formato de cards, permitindo que os usuários visualizem rapidamente as informações principais de cada curso. Esse tipo de aplicação poderia ser utilizado por plataformas de treinamento, empresas ou instituições educacionais para organizar e divulgar cursos disponíveis.

# PRINCIPAIS FLUXOS DA APLICAÇÃO

FLUXO DE CADASTRO
Permite que o usuário crie um novo curso preenchendo as informações no formulário de cadastro.

Fluxo:

1) Acessar a página de cadastro de cursos
2) Preencher os campos do formulário (nome, instrutor, datas, vagas, descrição, imagem, link de inscrição, etc.)
3) Definir se o curso é presencial e inserir endereço quando necessário
4) Clicar no botão Cadastrar
5) O curso é adicionado à listagem

Durante os testes foi observado que o sistema possui poucas validações, permitindo o cadastro com diversos dados inválidos.


FLUXO DE VISUALIZAÇÃO DE CURSO
Permite que os usuários visualizem os cursos cadastrados na aplicação.

Fluxo:

1) Acessar a página principal/listagem de cursos
2) Visualizar os cursos exibidos em formato de card
3) Consultar informações como nome do curso, instrutor, datas e descrição

Durante os testes foi observado que textos muito longos podem quebrar o layout dos cards


FLUXO DE EXCLUSÃO 
Permite remover cursos da listagem.

Fluxo esperado:

1) Localizar um curso na listagem
2) Clicar no botão Excluir
3) O curso deveria ser removido da lista

Durante os testes foi identificado que o botão de exclusão não executa nenhuma ação, impedindo a remoção de cursos cadastrados.

# OBJETIVOS DOS TESTES

Os testes foram realizados com o objetivo de validar:

  - funcionamento do cadastro de cursos;

  - validação de campos obrigatórios;

  - regras de datas;

  - validação de número de vagas;

  - validação de URLs;

  - comportamento da listagem de cursos;

  - integridade do layout dos cards;

  - persistência dos dados após recarregar a página;

  - funcionamento da exclusão de cursos;


# ESTRATÉGIA DOS TESTES

A estratégia utilizada foi baseada em testes manuais exploratórios, cobrindo:

  - fluxo feliz (happy path)

  - cenários de borda

  - entradas inválidas

  - validação de dados

  - comportamento da interface

Os cenários foram estruturados em casos de teste com passos definidos, resultado esperado e resultado obtido.


# CASOS DE TESTES E BUGS ENCONTRADOS

A execução dos testes e o registro dos bugs identificados estão documentados na planilha abaixo:

Relatório de Testes e Bugs (Google Sheets)
[https://docs.google.com/spreadsheets/d/1gFT3BWgmrlHU8aWkbq0iY2X7qK45mvwW2JWu7bh79RU/edit?usp=sharing]

Evidências de Testes (Google Drive)
[https://drive.google.com/drive/folders/1i0ZWBbeMXm6bPyKSLBx6TQwl_n3gSbJG?usp=sharing]

A planilha contém:

  - casos de teste executados, passos de reprodução, resultados esperados, resultados obtidos, status da execução, bugs identificados e severidade dos defeitos.


# PONTOS DO SISTEMA CONSIDERADOS MAIS CRÍTICOS PARA TESTE

O ponto mais crítico da aplicação é o formulário de cadastro de cursos, pois ele é responsável pela entrada de todas as informações utilizadas no sistema. Caso não existam validações adequadas, o sistema pode armazenar dados incompletos ou inconsistentes, comprometendo a integridade das informações.
Outro ponto crítico é a validação das regras de negócio da aplicação, especialmente em campos como datas do curso, número de vagas e obrigatoriedade de determinados dados. Falhas nessas validações podem permitir o registro de informações inválidas, o que pode gerar comportamentos inesperados na aplicação.
Também é importante testar a exibição dos cursos na listagem, garantindo que todas as informações cadastradas sejam apresentadas corretamente e que a interface permaneça organizada, mesmo quando são inseridos textos mais longos.
Por fim, as ações disponíveis nos cursos, como acessar o link de inscrição ou excluir um curso, também são consideradas críticas, pois fazem parte das principais interações do usuário com o sistema. Caso essas funcionalidades não funcionem corretamente, a experiência do usuário e o gerenciamento dos cursos ficam comprometidos.

# CONCLUSÃO

A aplicação apresenta funcionamento básico do fluxo de cadastro e persistência dos cursos após recarregar a página. No entanto, foram identificadas diversas falhas de validação de dados e inconsistências na interface que podem comprometer a experiência do usuário e a confiabilidade das informações cadastradas. Recomenda-se a implementação de validações adicionais nos campos do formulário e a correção das funcionalidades identificadas durante os testes.
