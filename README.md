

# 📚Projeto React(TSX) com Docker, MySQL e Vite

Este projeto foi criado com **Create React App** e configurado para rodar tanto em **ambiente de desenvolvimento** quanto em **produção** usando Docker.

---

## 🚀 Criar um projeto

1. **Criação do projeto**
   ```bash
   npx create-react-app my-app
---

# 🛠 Configuração do Docker


 *Observações sobre como cheguei ao resultado*:

- Criei o Dockerfile, subi o container e funcionou ✔

- Pesquisei sobre usar Nginx junto com Node, entendendo a diferença entre Vite no dev e produção.

---

# ⚙ Configuração do docker-compose

Criei o docker-compose.yml

Subi o MySQL e configurei o phpMyAdmin (consultando documentação do Docker Hub) ✔

Linkei a aplicação React no YAML usando o Dockerfile correspondente ✔

**💻 Volumes e redes**

- Adicionei volume para persistência do banco de dados

- Criei a network usando **docker network create**

- Adicionei as redes aos containers

**🔥 Hot reload**

- Percebi que em ambiente de desenvolvimento não estava funcionando o hot reload

- Pesquisei soluções e encontrei profiles no Docker Compose

- Inicialmente tentei com overriding, mas não funcionou

-  Mas não estava subindo o contâiner do vite, então fui perguntar a algum prompt o que poderia ser e descobri que o problema era o polling do Vite
---

⚡ Como rodar

1. **Para ambiente de desenvolvimento**
   ```bash
   docker compose up --profile dev --build
---

1. **Para ambiente de produção**
   ```bash
   docker compose up --profile prod --build
---



