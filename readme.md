# 🐦 TICO (Módulo GAIO)

**TICO** é um módulo de inovação social e conexão acadêmica do ecossistema **GAIO** (Universidade Estadual de Goiás - UEG). Funciona como uma rede profissional interna (inspirada no modelo de redes modernas como o LinkedIn) focada em conectar talentos, agrupar equipes multidisciplinares e alocar estudantes e pesquisadores de acordo com as demandas de projetos de extensão, pesquisa (PIBIC/PIBITI) e inovação tecnológica.

---

## 🎯 Objetivo do Projeto
O principal objetivo do **TICO** é facilitar a formação de equipes colaborativas entre os diversos câmpus da UEG:
- **Estudantes:** cadastram seus perfis, histórico acadêmico e competências técnicas comprovadas (ex: Java, IoT, Manejo de Solo, Soldagem MIG, Design UI/UX).
- **Líderes e Orientadores:** publicam iniciativas, definem o escopo de atuação e abrem vagas vinculadas a editais de fomento ou voluntariado.
- **Matching Inteligente:** o sistema cruza as competências exigidas pelo projeto com as habilidades dos alunos cadastrados, sugerindo conexões com cálculo de afinidade técnica percentual.

---

## 🖥️ Módulos e Telas do Sistema (Frontend Thymeleaf)

A interface do TICO é construída em **HTML5**, **CSS3 puro** (sem frameworks utilitários pesados) e notações dinâmicas **Thymeleaf**, prontas para o consumo do Model no backend Spring Boot:

| Tela | Arquivo | Descrição |
| :--- | :--- | :--- |
| **Feed Social Acadêmico** | [`feed.html`](feed.html) | Tela central inspirada no LinkedIn (layout em 3 colunas): resumo do perfil e métricas, caixa de publicação de demandas/vagas, stream de postagens com reações e comentários, além de widgets laterais de editais urgentes e conexões recomendadas. |
| **Banco de Talentos** | [`talentos.html`](talentos.html) | Tela dedicada para busca de alunos e pesquisadores da UEG: painel de estatísticas, filtros avançados por câmpus, disponibilidade (imediata, parcial ou bolsista) e cards com porcentagem de afinidade (*Match %*). |
| **Editais & Eventos** | [`editais-eventos.html`](editais-eventos.html) | Vitrine de chamadas públicas (PIBIC/PIBITI, PROEC, FAPEG), eventos acadêmicos e hackathons com badges de contagem regressiva de prazos, valor de bolsas e acesso aos PDFs oficiais. |
| **Configurações da Conta** | [`configuracoes.html`](configuracoes.html) | Painel de controle do usuário dividido em abas: dados acadêmicos sincronizados, preferências de visibilidade no banco de talentos, alertas de novas vagas por e-mail e segurança/SSO UEG. |
| **Meu Perfil** | [`perfil.html`](perfil.html) | Visão em *Bento Grid* do acadêmico: identificação e redes (Lattes/GitHub), nuvem de tags de habilidades, linha do tempo de projetos concluídos/ativos e avisos da comunidade. |
| **Explorar Oportunidades** | [`explorar.html`](explorar.html) | Catálogo de projetos com vagas abertas, filtros por grandes áreas do conhecimento e pílulas de busca rápida por tecnologia. |
| **Criar Novo Projeto** | [`criar-projeto.html`](criar-projeto.html) | Formulário estruturado para submissão de projetos: escopo, alocação de vagas (remuneradas ou voluntárias) e seleção interativa de competências necessárias para o pareamento. |
| **Detalhes do Projeto** | [`projeto-detalhes.html`](projeto-detalhes.html) | Visão completa do projeto: justificativa, objetivos, competências aplicadas, perfil do orientador, requisitos de cada vaga e fluxo de candidatura. |
| **Autenticação & Onboarding** | [`login.html`](login.html) e [`cadastro.html`](cadastro.html) | Fluxo de início de sessão (com suporte a login institucional UEG) e onboarding em duas etapas com cadastro de competências iniciais. |

---

## 🎨 Identidade Visual ("Argila & Tinta")

A identidade visual do TICO foi desenhada exclusivamente para refletir a fauna e as cores regionais de Goiás, inspirando-se no pássaro mascote **Tico-tico** (com destaque para o tom ferrugem/terracota de sua gola):

* **Conceito:** Argila & Tinta (Editorial, Orgânico, Moderno e Acolhedor)
* **Cor Primária:** Tijolo Queimado (`#D46A4F`) — botões de ação, badges de destaque e acentos visuais.
* **Cor de Destaque:** Azul-Petróleo Noturno (`#182229`) — sidebar, títulos principais e cards contrastantes.
* **Cor de Fundo:** Algodão (`#F6F5F2`) — fundo neutro que minimiza o cansaço visual.
* **Superfícies:** Branco Puro (`#FFFFFF`) com bordas suaves (`#E2DFD8`) e sombras sutis de elevação.
* **Tipografia:** Google Fonts ([Inter](https://fonts.google.com/specimen/Inter) para leitura e [Nunito Sans](https://fonts.google.com/specimen/Nunito+Sans) em peso ExtraBold/Black para a marca).

---

## 🛠️ Tecnologias e Padrões de Código

* **Arquitetura Geral:** MVC (Model-View-Controller) com renderização Server-Side.
* **Backend:** Java 17+, Spring Boot, Spring Data JPA, Spring Security, Bean Validation.
* **Frontend:** HTML5 semântico, Thymeleaf 3, CSS3 modular puro ([`style.css`](style.css)).
* **Thymeleaf Integration:**
  * Uso consistente do namespace `xmlns:th="http://www.thymeleaf.org"`.
  * Associação de formulários via `th:action`, `th:object` e `th:field`.
  * Renderização condicional e iterações com `th:each`, `th:if` e `th:text`.
  * Notação com fallback Elvis (`?:`), garantindo que todos os arquivos `.html` possam ser abertos e testados diretamente no navegador estático durante o design, mantendo total compatibilidade com o servidor Spring em tempo de execução.

---

## 👥 Equipe e Atribuições

* **Desenvolvedor Backend / Líder Técnico:** Estruturação da arquitetura Spring, modelagem de entidades (JPA/Hibernate), serviços de cálculo de match, repositórios e endpoints de integração.
* **Desenvolvedor Frontend / Requisitos (Kawic):** Levantamento de requisitos e fluxos acadêmicos, desenvolvimento do design system responsivo em CSS3 puro, elaboração das telas em HTML5/Thymeleaf e massa de dados para prototipagem.

---

## ⚙️ Como Executar o Projeto Localmente

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/tico-gaio.git
   cd tico-gaio
   ```
2. Abra o projeto na sua IDE de preferência (IntelliJ IDEA, VS Code ou Eclipse).
3. Verifique as dependências do Maven no `pom.xml`.
4. Configure as credenciais do banco de dados no arquivo `application.properties`:
   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/tico_db
   spring.datasource.username=seu_usuario
   spring.datasource.password=sua_senha
   spring.jpa.hibernate.ddl-auto=update
   ```
5. Execute a classe principal da aplicação (`TicoApplication.java`).
6. Acesse a aplicação no navegador em: `http://localhost:8080/feed` (ou abra diretamente os arquivos `.html` para testes visuais rápidos).

---
*Projeto acadêmico em desenvolvimento integrado ao ecossistema GAIO — Universidade Estadual de Goiás (UEG).*