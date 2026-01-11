# 🎮 Jogos Be Eventos

> **Nota:** Este é um repositório **Showcase (Estudo de Caso)**. O código-fonte completo é proprietário e confidencial, pertencendo à **Be Eventos**. Este documento serve para demonstrar a arquitetura, as tecnologias utilizadas e as competências técnicas aplicadas no desenvolvimento.



![Status do Projeto](https://img.shields.io/badge/Status-Finalizado-green) 

![Tech](https://img.shields.io/badge/Tech-React_|_Supabase_|_PWA-blue)

## 🎯 Visão Geral do Projeto

Este projeto consiste em uma plataforma de **Jogos Interativos (Gamificação)** desenvolvida para modernizar treinamentos de **Segurança do Trabalho (SIPAT)** e eventos corporativos. 

O objetivo principal foi transformar conteúdos técnicos e obrigatórios em experiências engajadoras, aumentando a retenção de informação pelos colaboradores através de mecânicas de jogos.

### 🖼️ Demonstração Visual

| Central de Jogos (Game Hub) | Jogo da Memória |
|:---:|:---:|
| ![Game Hub](./caminho-para-print-hub.png) <br> *Interface central onde o usuário escolhe a atividade* | ![Jogo Memória](./caminho-para-print-memoria.png) <br> *Dinâmica de pares focada em EPIs e Sinalização* |



---

## 🛠️ Tecnologias e Arquitetura

O sistema foi construído com foco em performance, escalabilidade e facilidade de manutenção.

### Front-end & Lógica
* **React.js (v18):** Biblioteca principal para construção da interface reativa e baseada em componentes.
* **React Router Dom (v6):** Gerenciamento de rotas e navegação SPA (Single Page Application).
* **CSS3 & Design Responsivo:** Estilização modular para garantir funcionamento em Desktops, Tablets e Mobile.
* **PWA (Progressive Web App):** Configurado para funcionar como aplicativo nativo, permitindo instalação em dispositivos móveis e funcionamento offline (via Service Workers).

### Back-end & Dados
* **Supabase:** Utilizado como BaaS (Backend as a Service) para:
    * Autenticação e Login de usuários.
    * Banco de dados PostgreSQL em tempo real para ranking e pontuações.
* **Integração via API:** Comunicação assíncrona para persistência de dados dos jogos.

### Estrutura de Pastas (Visão Simplificada)
A arquitetura foi pensada para permitir a adição modular de novos jogos sem quebrar o ecossistema existente.

```text
src/
├── components/
│   ├── GameHub/           # Central de seleção de jogos
│   ├── JogoDaMemoria/     # Lógica e UI do Jogo da Memória
│   ├── JogoDoAcerte/      # Lógica do Jogo "Acerte ou Saia"
│   ├── Login/             # Autenticação e proteção de rotas
│   └── Shared/            # Componentes reutilizáveis (Modais, Botões)
├── services/
│   └── supabaseClient.js  # Configuração do cliente Supabase
└── App.js                 # Roteamento e Controle de Sessão
