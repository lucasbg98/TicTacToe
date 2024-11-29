Aqui está o README atualizado com a inclusão do **ngrok** para permitir o acesso remoto:

---

# Tic Tac Toe (Jogo da Velha)

Este é um projeto de **Jogo da Velha (Tic Tac Toe)**, desenvolvido com **Java (Spring Boot)** no backend e **React.js** no frontend. Ele também utiliza o **ngrok** para permitir que outros usuários acessem seu servidor local, possibilitando partidas multiplayer entre dispositivos.

---

## 🛠️ Tecnologias Utilizadas

### Backend
- **Java** com **Spring Boot**
  - Gerenciamento de partidas
  - API REST para comunicação com o frontend
  - Armazenamento dos dados (partidas, resultados, etc.)

### Frontend
- **React.js**
  - Interface de usuário interativa
  - Componentes reutilizáveis para a lógica do jogo
  - Comunicação com a API REST do backend

### Conexão Remota
- **ngrok**
  - Túnel seguro para expor o backend local à internet.
  - Permite que outros jogadores se conectem ao seu servidor local para partidas multiplayer.

---

## 🎮 Funcionalidades

1. **Jogo Multiplayer:**
   - Jogue localmente ou permita que outro usuário se conecte remotamente via ngrok.

2. **Histórico de Partidas:**
   - Registro de partidas jogadas e resultados.

3. **Resolução Automática:**
   - O jogo detecta automaticamente vitórias, empates ou jogadas inválidas.

4. **Interface Responsiva:**
   - Suporte para diferentes tamanhos de tela (desktop e mobile).

5. **API RESTful:**
   - Endpoints para criar partidas, consultar o histórico e armazenar dados.

---

## 🚀 Como Executar o Projeto

### Pré-requisitos

- **Java 17** ou superior instalado.
- **Node.js** e **npm** instalados.
- **ngrok** instalado.

### Passos para Rodar Localmente

#### Backend
1. Clone o repositório:  
   ```bash
   git clone https://github.com/seu-usuario/tictactoe.git
   cd tictactoe/backend
   ```
2. Compile e execute o backend:
   ```bash
   ./mvnw spring-boot:run
   ```
3. O servidor estará disponível em: `http://localhost:8080`.

4. Inicie o **ngrok** para expor o servidor backend:
   ```bash
   ngrok http 8080
   ```
5. Copie o endereço gerado pelo ngrok (algo como `https://<subdomínio>.ngrok.io`) e compartilhe com outros jogadores.

#### Frontend
1. Acesse a pasta do frontend:  
   ```bash
   cd ../frontend
   ```
2. Instale as dependências:  
   ```bash
   npm install
   ```
3. Configure o arquivo de ambiente do frontend (`.env` ou similar) para apontar para o endereço do ngrok, por exemplo:  
   ```
   REACT_APP_API_URL=https://<subdomínio>.ngrok.io
   ```
4. Inicie o servidor de desenvolvimento:
   ```bash
   npm start
   ```
5. Acesse o frontend em: `http://localhost:3000` e comece a jogar.

---

## 📚 Estrutura do Projeto

```
tictactoe/
├── backend/          # Código fonte do backend em Java Spring Boot
├── frontend/         # Código fonte do frontend em React.js
├── README.md         # Este arquivo
└── .gitignore        # Arquivos a serem ignorados pelo Git
```

---

## 📋 API Endpoints Principais

### Partidas
- **`GET /api/games`**: Lista todas as partidas.
- **`POST /api/games`**: Cria uma nova partida.
- **`PUT /api/games/{id}/move`**: Registra uma jogada.

### Resultados
- **`GET /api/games/{id}/result`**: Obtém o resultado de uma partida.

---

## 🔧 Melhorias Futuras

- Adicionar um modo **Player vs CPU** com inteligência artificial.
- Implementar autenticação para usuários.
- Criar um modo de jogo online em tempo real.
- Melhorar a interface visual com animações e sons.

---

## 👥 Contribuidores

- **[Lucas Bragança Gonçalves](https://github.com/lucasbg98)**  
  Desenvolvedor Fullstack.

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou enviar pull requests.

---

Se tiver dúvidas ou sugestões, entre em contato ou abra uma issue neste repositório. 😊

---
