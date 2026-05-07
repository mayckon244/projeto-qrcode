# 🎬 Mídia Indoor

Sistema simples de gerenciamento e exibição de mídia indoor desenvolvido com Node.js, Express e upload de arquivos.

O projeto permite:

* Exibir vídeos automaticamente em tela cheia
* Fazer upload de novos vídeos
* Fazer upload de imagens
* Substituir automaticamente o vídeo atual
* Servir conteúdo estático para painéis de mídia indoor
* Criar uma estrutura simples para totens, TVs ou painéis digitais

---

# 📌 Tecnologias Utilizadas

## Backend

* Node.js
* Express.js
* Multer
* CORS
* SQLite

## Frontend

* HTML5
* CSS3
* JavaScript Vanilla

---

# 📁 Estrutura do Projeto

```bash
midia-indor/
│
├── data/
│   └── database.sqlite
│
├── public/
│   ├── assets/
│   │   ├── imagens/
│   │   └── videos/
│   │
│   ├── admin.html
│   ├── admin.css
│   ├── index.html
│   ├── script.js
│   └── style.css
│
├── server/
│   ├── db.js
│   └── server.js
│
├── package.json
└── package-lock.json
```

---

# ⚙️ Funcionalidades

## 📺 Reprodução automática de vídeo

O sistema carrega automaticamente o vídeo principal armazenado em:

```bash
/public/assets/videos/video.mp4
```

Caso nenhum vídeo exista, o sistema tenta utilizar um vídeo padrão.

---

## ⬆️ Upload de Vídeos

Através da rota:

```http
POST /upload/video
```

O sistema:

1. Recebe o vídeo enviado
2. Remove o vídeo anterior
3. Renomeia automaticamente para:

```bash
video.mp4
```

Isso garante que o player sempre utilize o vídeo mais recente.

---

## 🖼️ Upload de Imagens

Rota:

```http
POST /upload/imagem
```

As imagens são armazenadas em:

```bash
/public/assets/imagens
```

---

## 🔍 Consulta do Último Vídeo

Rota:

```http
GET /last-video
```

Retorna:

```json
{
  "filename": "video.mp4"
}
```

---

# 🚀 Como Executar o Projeto

## 1. Clone o repositório

```bash
git clone https://github.com/seu-usuario/midia-indor.git
```

---

## 2. Entre na pasta

```bash
cd midia-indor
```

---

## 3. Instale as dependências

```bash
npm install
```

---

## 4. Execute o servidor

```bash
node server/server.js
```

Servidor iniciado em:

```bash
http://localhost:3001
```

---

# 🌐 Acessos do Sistema

## Página principal

```bash
http://localhost:3001
```

---

## Painel administrativo

```bash
http://localhost:3001/admin.html
```

---

# 📦 Dependências

## Express

Responsável pelo servidor HTTP.

---

## Multer

Responsável pelo upload de arquivos.

---

## CORS

Permite comunicação entre aplicações.

---

## SQLite / better-sqlite3

Banco de dados leve utilizado no projeto.

---

# 🔐 Limitações Atuais

O projeto ainda possui limitações importantes:

* Não existe autenticação no painel admin
* Não existe controle de usuários
* Não existe proteção contra upload malicioso
* Não existe validação de tamanho de arquivo
* Não existe suporte para múltiplos vídeos simultâneos
* Não existe sistema de playlists
* Não existe logs de atividade

Isso significa que o sistema ainda está em nível inicial/protótipo.

---

# 🛠️ Melhorias Futuras

Algumas melhorias realmente importantes:

* Sistema de login JWT
* Painel administrativo moderno
* Dashboard em React
* Agendamento de mídia
* Suporte para playlists
* Suporte para múltiplas telas
* Upload drag-and-drop
* Compressão automática de vídeo
* Monitoramento remoto
* Deploy em VPS
* Dockerização
* Integração com banco PostgreSQL
* API REST completa

---

# 📡 Rotas da API

| Método | Rota           | Descrição                    |
| ------ | -------------- | ---------------------------- |
| POST   | /upload/video  | Upload do vídeo principal    |
| POST   | /upload/imagem | Upload de imagem             |
| GET    | /last-video    | Retorna último vídeo enviado |

---

# 🧠 Como o Sistema Funciona

O fluxo principal é simples:

1. O frontend carrega automaticamente o vídeo principal
2. O backend serve os arquivos estáticos
3. O administrador envia um novo vídeo
4. O servidor substitui o arquivo antigo
5. O player passa a exibir automaticamente o novo conteúdo

---

# 💻 Exemplo de Inicialização

```bash
node server/server.js
```

Saída esperada:

```bash
Servidor rodando em http://localhost:3001
```

---

# 📷 Possíveis Aplicações

Esse sistema pode ser usado para:

* TVs corporativas
* Painéis comerciais
* Cardápios digitais
* Propaganda indoor
* Totens digitais
* Exibição de anúncios
* Comunicação interna empresarial

---

# 📄 Licença

Projeto desenvolvido para fins educacionais.

Você pode modificar e utilizar livremente.

---

# 👨‍💻 Autor

Desenvolvido por Mayckon.

---

# ⭐ Observação Importante

O projeto funciona como MVP/protótipo.

Ele resolve o básico da exibição de mídia indoor, mas ainda não possui arquitetura robusta para produção real.

Se quiser transformar isso em um sistema profissional, os próximos passos deveriam ser:

* Separar frontend e backend
* Criar autenticação
* Implementar streaming otimizado
* Adicionar controle remoto das telas
* Criar API estruturada
* Implementar segurança de upload
* Criar sistema multiusuário
* Fazer deploy em nuvem
