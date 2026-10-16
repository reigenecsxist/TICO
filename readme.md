# 🐦 TICO (Módulo GAIO)

**TICO** é um módulo de inovação social do ecossistema **GAIO** (Universidade Estadual de Goiás - UEG). Funciona como uma rede de conexão acadêmica (semelhante a um LinkedIn interno) focada em agrupar equipes e alocar talentos de acordo com as necessidades de projetos de extensão, pesquisa e desenvolvimento.

---

## 🎯 Objetivo do Projeto
O principal objetivo do TICO é facilitar a formação de equipes multidisciplinares dentro da universidade. Alunos podem cadastrar seus perfis e habilidades, enquanto líderes e orientadores podem registrar projetos e abrir vagas específicas (ex: "Preciso de alguém que saiba Java" ou "Preciso de alguém para Soldagem"). O sistema realiza o *match* entre a demanda do projeto e o talento disponível.

## 🚀 Fases de Desenvolvimento

Este projeto está sendo desenvolvido inicialmente de forma **Standalone** (independente), focando na validação das regras de negócio e usabilidade. 

- **Fase 1 (Atual):** MVP Monolítico com renderização Server-Side.
- **Fase 2 (Futura):** Integração com o GAIO principal via API (exposição de endpoints REST).

## 🛠️ Tecnologias Utilizadas

O projeto segue a arquitetura **MVC** (Model-View-Controller) no backend, renderizando telas dinâmicas no frontend.

* **Backend:** Java, Spring Boot, Spring Data JPA, Bean Validation.
* **Frontend:** Thymeleaf, HTML5, CSS3 puro (Design System customizado).
* **Banco de Dados:** [PostgreSQL / MySQL] (Em definição).

## 🎨 Identidade Visual
Para se diferenciar das demais aplicações do ecossistema GAIO, o TICO adota uma paleta exclusiva e orgânica inspirada no pássaro mascote, o **Tico-tico**, focando no tom de sua gola (ferrugem/terracota):

* **Conceito:** Argila & Tinta (Design Editorial, Orgânico e Elegante)
* **Cor Primária:** Tijolo Queimado (`#D46A4F`)
* **Cor de Destaque:** Azul-Petróleo Noturno (`#182229`)
* **Background:** Algodão (`#F6F5F2`)

## 👥 Equipe e Divisão de Tarefas

* **Desenvolvedor Backend / Líder Técnico:** Estruturação do projeto Spring, modelagem de dados (JPA/Entities), regras de negócio (Services) de alocação/match, integração com Thymeleaf e futura arquitetura de API.
* **Desenvolvedor Frontend / Requisitos (Kawic):** Levantamento de requisitos, prototipagem (wireframes), design de interface (HTML/CSS), estruturação do Thymeleaf e geração de massa de dados para testes.

## ⚙️ Como executar o projeto localmente

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/tico-gaio.git
   ```
2. Abra o projeto na sua IDE favorita (IntelliJ IDEA, VS Code ou Eclipse).
3. Atualize as dependências do Maven.
4. Configure as credenciais do banco de dados no arquivo `application.properties` ou `application.yml`:
   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/tico_db
   spring.datasource.username=seu_usuario
   spring.datasource.password=sua_senha
   spring.jpa.hibernate.ddl-auto=update
   ```
5. Execute a classe principal `TicoApplication.java`.
6. Acesse no navegador: `http://localhost:8080`

---
*Projeto acadêmico em desenvolvimento para a Universidade Estadual de Goiás (UEG).*