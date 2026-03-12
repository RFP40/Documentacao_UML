# Documentação do Projeto: Nex_TI
## Plataforma Educacional Gamificada

O **Nex_TI** é um sistema web educacional focado na metodologia de **Estudo Ativo (Flashcards)** e **Gamificação**. Desenvolvido para tornar o aprendizado de tecnologia mais engajador, o sistema recompensa os alunos com Pontos de Experiência (XP) e Moedas Virtuais (Coins) conforme eles progridem nas disciplinas.

---

## 1. Requisitos Funcionais (RF)

- **RF01 - Autenticação e Gestão de Perfis:** O sistema deve permitir o cadastro autônomo de novos usuários na tela de login, além de gerenciar três níveis de acesso: Administrador (gestão de infraestrutura e permissões), Tutor (gestão de conteúdo e pedagógica) e Aluno (consumo de conteúdo e gamificação).
- **RF02 - Gestão de Estudos e Flashcards:** O sistema deve apresentar os conteúdos das disciplinas em formato de flashcards (frente e verso), permitindo que o aluno registre seus acertos e erros. Além disso, o sistema deve fornecer uma ferramenta para que o aluno crie e armazene seus próprios flashcards personalizados de forma local.
- **RF03 - Gamificação, Economia e Progressão:** O motor do sistema deve gerenciar a jornada do aluno de ponta a ponta: realizando um teste de nivelamento no primeiro acesso, atribuindo Pontos de Experiência (XP) e Moedas (Coins) a cada acerto, atualizando seu Rank automaticamente e permitindo o uso do saldo de moedas para o desbloqueio de Módulos e Fases Bônus na loja virtual.
- **RF04 - Painéis e Relatórios de Desempenho:** O sistema deve gerar painéis de acompanhamento (Dashboards) mostrando o progresso e estatísticas individuais para o aluno, além de relatórios gerenciais consolidados do desempenho geral da turma para os Tutores.
- **RF05 - Suporte em Níveis (IA e Tutor):** O sistema deve fornecer uma interface de suporte inicial via Agente Especialista (Inteligência Artificial) para dúvidas rápidas, permitindo ao aluno escalar a dúvida para um chamado (ticket) com o Tutor humano caso o problema não seja resolvido pela IA.

---

## 2. Requisitos Não Funcionais (RNF)

- **RNF01 - Arquitetura e Disponibilidade:** O sistema deve operar inicialmente como um MVP *serverless* hospedado em nuvem de alta disponibilidade (ex: GitHub Pages). A arquitetura escalar futura prevê a integração do front-end com uma API RESTful desenvolvida em C# (.NET) e persistência de dados em Microsoft SQL Server.
- **RNF02 - Usabilidade e Responsividade (UX/UI):** A interface deve adotar a abordagem *Mobile First*, adaptando-se fluidamente a smartphones, tablets e desktops. O design deve manter uma estética *Dark Mode* de terminal de código, fornecendo feedback visual e imediato (animações e cores) para cada ação de acerto ou erro do usuário.
- **RNF03 - Desempenho e Fluidez:** O sistema deve garantir a imersão do aluno durante os estudos, limitando a no máximo 1 segundo o tempo de resposta para virar uma carta (flashcard) e para computar/renderizar as recompensas (XP e Moedas) na tela.
- **RNF04 - Segurança de Dados:** Para a fase de integração com o banco de dados, o sistema deve garantir a proteção das informações sensíveis, armazenando as senhas dos usuários de forma criptografada (algoritmo de Hash) e protegendo as rotas da API através de tokens de autenticação (ex: JWT).

---

## 3. Histórias de Usuário (User Stories)

- **US01 - Acesso e Cadastro:** Como Visitante, eu quero poder criar uma conta nova diretamente pela tela de login, para ingressar rapidamente na plataforma como Aluno.
- **US02 - Estudo Ativo e Criação de Cartas:** Como Aluno, eu quero interagir com flashcards para fixar o conteúdo e ter a opção de criar meus próprios decks, para focar nos assuntos que tenho mais dificuldade.
- **US03 - Jornada Gamificada e Economia:** Como Aluno, eu quero realizar um teste de nivelamento inicial, ganhar XP/Moedas ao acertar as questões e usar meu saldo para desbloquear módulos, para manter meu engajamento e progressão no jogo.
- **US04 - Acompanhamento Pessoal:** Como Aluno, eu quero visualizar um dashboard com meu desempenho e histórico, para acompanhar minha evolução acadêmica de forma autônoma.
- **US05 - Suporte Integrado (Nível 1 e 2):** Como Aluno, eu quero consultar o Agente Especialista (IA) para dúvidas rápidas e poder escalar o problema para um Tutor humano, garantindo que meu aprendizado não fique travado.
- **US06 - Gestão de Conteúdo Global:** Como Tutor, eu quero criar e atualizar os flashcards das disciplinas, para que o material da plataforma se mantenha preciso e atualizado.
- **US07 - Acompanhamento Pedagógico:** Como Tutor, eu quero visualizar estatísticas de uso e desempenho da turma, para atuar de forma proativa com alunos inativos ou que precisem de intervenção.

---

## 4. Arquitetura e Tecnologias

O projeto adota uma arquitetura em camadas. Atualmente, o sistema opera como um Produto Mínimo Viável (MVP) totalmente funcional no Front-end. A modelagem de software já contempla a arquitetura final robusta a ser implementada na próxima fase.

- **Front-end:** HTML5, CSS3 (Flexbox/Grid), JavaScript Vanilla.
- **Back-end (Fase Atual):** JavaScript (Responsável pela simulação da lógica de gamificação, controle de estados e persistência de dados local).
- **Back-end (Implementação Futura):** API RESTful desenvolvida em C# (.NET Core).
- **Banco de Dados (Implementação Futura):** Microsoft SQL Server.
- **ORM (Implementação Futura):** Entity Framework Core.
- **Engenharia de Software:** Modelagem UML (Casos de Uso, Diagramas de Classes e Sequência) projetada e documentada para a integração final em C#.

---

## 5. Equipe de Desenvolvimento

- 💻 **[Maycon Douglas](https://github.com/MayconDIS)** (RA: H719CD3)
  *Scrum Master | Desenvolvedor Full-Stack | Documentação UML*

- 💾 **[Rafael Mesquita](https://github.com/RFP40)** (RA: H6722I0)
  *Product Owner (PO) | Desenvolvedor Back-end | Banco de Dados | Documentação UML*

- 🎨 **[Maciel Silva](https://github.com/maciellcs)** (RA: R280985)
  *Desenvolvedor Front-end Mobile | UI Design | Documentação UML*

- 🎨 **[Gabriel Alves](https://github.com/GabrielAlvesMoreira)** (RA: H67HJ4)
  *Desenvolvedor Front-end Mobile | UI Design | Documentação UML*

---
*(Projeto acadêmico desenvolvido para a disciplina de Projeto Integrado Multidisciplinar - PIM_III).*
