# MUSA - Mural UnB de Socialização Artística 
[![Version](https://img.shields.io/badge/version-2.0.0-blue.svg)](https://github.com/FGA0138-MDS-Ajax/2025.2-Inti)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26.svg?logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6.svg?logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E.svg?logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Capacitor](https://img.shields.io/badge/Capacitor-119EFF.svg?logo=capacitor&logoColor=white)](https://capacitorjs.com/)
[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F.svg?logo=springboot&logoColor=white)](https://spring.io/projects/spring-boot)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1.svg?logo=postgresql&logoColor=white)](https://www.postgresql.org/)

## Sobre o Projeto

O **MUSA** é uma aplicação web moderna desenvolvida pelo grupo **Inti** da turma 2025.2 da disciplina de Métodos de Desenvolvimento de Software (MDS) da Faculdade de Ciências e Tecnologia em Engenharias da Universidade de Brasília (FCTE - UnB).

A plataforma foi projetada para otimizar o monitoramento e gestão de usuários em sistemas de saúde e assistência social, proporcionando uma solução integrada que facilita o acompanhamento de pacientes, análise de dados e tomada de decisões baseadas em evidências.

### Arquitetura Web-Centric

O MUSA segue o padrão **SPA (Single Page Application)**, desenvolvido com HTML5, CSS3 e JavaScript puro. A arquitetura foi projetada para ser **web-centric**, garantindo um _single-source-of-truth_ (fonte única de verdade) para o código.

### Distribuição Mobile

A aplicação pode ser distribuída para plataformas móveis (iOS e Android) através do **Capacitor**, que atua como um _wrapper_ nativo instanciando uma **WebView** que carrega o site web principal a partir de sua URL hospedada.

---

## Objetivos do Projeto

- **Centralização de Dados**: Unificar informações de usuários em uma plataforma única e acessível
- **Monitoramento Eficiente**: Facilitar o acompanhamento contínuo de pacientes e beneficiários
- **Análise de Dados**: Fornecer ferramentas analíticas para identificação de padrões e tendências
- **Tomada de Decisão**: Apoiar gestores com informações precisas e atualizadas
- **Acessibilidade**: Garantir interface intuitiva e acessível para todos os usuários

---

## Principais Funcionalidades

### Gestão de Usuários
Sistema completo para cadastro, atualização e acompanhamento de usuários do sistema de saúde e assistência social.

### Dashboard Analítico
Visualização de dados em tempo real com gráficos e indicadores de desempenho para facilitar a análise e monitoramento.

### Autenticação e Segurança
Sistema robusto de autenticação com JWT, garantindo segurança no acesso e proteção de dados sensíveis.

### Busca e Filtros
Ferramentas avançadas de busca e filtragem para localização rápida de informações específicas.

### Gestão de Eventos
Criação, listagem e gerenciamento de eventos relacionados ao sistema de saúde e assistência.

---

## Navegação da Documentação

<div class="grid cards" markdown>

-   :material-rocket-launch:{ .lg .middle } **[Começando](comecando.md)**

    ---

    Guia completo de instalação e configuração do ambiente de desenvolvimento

-   :material-code-braces:{ .lg .middle } **[Arquitetura](arquitetura.md)**

    ---

    Entenda a estrutura técnica e componentes do sistema

-   :material-account-group:{ .lg .middle } **[Equipe](equipe.md)**

    ---

    Conheça os profissionais por trás do projeto MUSA

-   :material-lightbulb:{ .lg .middle } **[Lean Inception](lean.md)**

    ---

    Processo de concepção e definição do produto

</div>

---

## Tecnologias Utilizadas

### Frontend
- **HTML5** - Estrutura semântica
- **CSS3** - Estilização e responsividade
- **JavaScript (ES6+)** - Lógica da aplicação

### Mobile
- **Capacitor** - Wrapper nativo para iOS/Android

### Backend
- **Java 17+**
- **Spring Boot** - Framework backend
- **PostgreSQL** - Banco de dados relacional
- **JWT** - Autenticação e autorização

### Ferramentas de Desenvolvimento
- **Node.js** - Runtime JavaScript
- **npm** - Gerenciamento de pacotes
- **Prettier** - Formatação de código
- **Live Server** - Servidor de desenvolvimento

---

## Metodologia de Desenvolvimento

O desenvolvimento do MUSA segue práticas ágeis e metodologias consolidadas:

- **Lean Inception**: Utilizada para alinhamento inicial e definição do MVP
- **Desenvolvimento Iterativo**: Entregas incrementais com feedback contínuo
- **Qualidade de Código**: Práticas de code review e formatação automatizada
- **Documentação Contínua**: Manutenção de documentação técnica e de usuário

---

## Início Rápido

```bash
# Clone o repositório
git clone https://github.com/fga-eps-mds/2025.2-Inti.git
cd 2025.2-Inti

# Instale as dependências
npm install

# Execute com Live Server no VS Code
# Clique com botão direito em index.html > "Open with Live Server"
```

Para instruções detalhadas, consulte o [Guia de Início](comecando.md).

---

## Contato e Contribuição

O MUSA é um projeto em constante evolução. Para mais informações, sugestões ou contribuições, consulte nossa [página da equipe](equipe.md) ou acesse o [repositório oficial no GitHub](https://github.com/fga-eps-mds/2025.2-Inti).

---

**Última atualização**: Dezembro 2025  
**Versão da Documentação**: 2.0  
**Grupo**: Inti - MDS 2025.2 - UnB
