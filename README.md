# 🚀 Gerador de QR Code e Senhas

Um projeto em Node.js desenvolvido para gerar QR Codes personalizados e senhas aleatórias diretamente pelo terminal.

O sistema utiliza interação via CLI (Command Line Interface), permitindo que o usuário escolha funcionalidades através do terminal.

---

# 📌 Funcionalidades

## ✅ Gerador de QR Code

Permite gerar QR Codes a partir de textos, links ou qualquer conteúdo informado pelo usuário.

### Exemplos:

* Links
* URLs de redes sociais
* Wi-Fi
* Texto simples
* PIX copia e cola
* Contatos

---

## ✅ Gerador de Senhas

Gera senhas aleatórias automaticamente.

### Características:

* Letras maiúsculas
* Letras minúsculas
* Números
* Caracteres especiais
* Comprimento configurável

---

# 🛠️ Tecnologias Utilizadas

| Tecnologia           | Função                          |
| -------------------- | ------------------------------- |
| Node.js              | Ambiente de execução JavaScript |
| Prompt               | Entrada de dados no terminal    |
| QRCode Terminal      | Geração de QR Codes no terminal |
| Chalk                | Estilização do terminal         |
| JavaScript ESModules | Estrutura moderna do projeto    |

---

# 📂 Estrutura do Projeto

```bash
projeto/
│
├── src/
│   ├── index.js
│   │
│   ├── prompts-schema/
│   │   └── prompt-schema-main.js
│   │
│   ├── services/
│   │   ├── password/
│   │   │   └── create.js
│   │   │
│   │   └── qr-code/
│   │       └── create.js
│
├── .env
├── package.json
├── package-lock.json
└── README.md
```

---

# ⚙️ Pré-requisitos

Antes de executar o projeto, você precisa ter instalado:

## ✅ Node.js

Versão recomendada:

```bash
v20+
```

Verifique a versão instalada:

```bash
node -v
```

Download oficial:

🔗 [https://nodejs.org](https://nodejs.org)

---

# 📥 Instalação

## 1️⃣ Clone o repositório

```bash
git clone https://github.com/SEU-USUARIO/SEU-REPOSITORIO.git
```

---

## 2️⃣ Entre na pasta do projeto

```bash
cd SEU-REPOSITORIO
```

---

## 3️⃣ Instale as dependências

```bash
npm install
```

---

# ▶️ Executando o Projeto

## Método padrão

```bash
npm start
```

---

## Método alternativo

```bash
node --env-file=.env src/index.js
```

---

# 🧠 Como o Sistema Funciona

O projeto inicia pelo arquivo:

```bash
src/index.js
```

Esse arquivo:

* Inicializa o terminal
* Carrega os prompts
* Exibe o menu principal
* Direciona para os serviços

Fluxo básico:

```text
Usuário → Prompt → Escolha → Serviço → Resultado
```

---

# 📋 Menu Principal

Ao iniciar o sistema, o terminal exibe:

```bash
1 - Gerar QRCode
2 - Gerar Senha
```

---

# 🔐 Gerador de Senhas

O sistema cria senhas aleatórias utilizando:

* Letras
* Números
* Símbolos
* Mistura aleatória

Exemplo:

```bash
A9@fL#2xQ!
```

---

# 📱 Gerador de QR Code

O usuário informa um conteúdo e o sistema gera automaticamente o QR Code diretamente no terminal.

Exemplo:

```bash
https://github.com
```

Resultado:

```text
█▀▀▀▀▀█ ▀▄▀▄ █▀▀▀▀▀█
█ ███ █ ▄▀██ █ ███ █
█ ▀▀▀ █ █▀▄█ █ ▀▀▀ █
▀▀▀▀▀▀▀ ▀ ▀▀ ▀▀▀▀▀▀▀
```

---

# 📦 Scripts Disponíveis

## Iniciar projeto

```bash
npm start
```

---

# 📄 package.json

Exemplo de configuração:

```json
{
  "name": "qrcode-project",
  "version": "1.0.0",
  "type": "module",
  "main": "src/index.js",
  "scripts": {
    "start": "node --env-file=.env src/index.js"
  }
}
```

---

# ⚠️ Problemas Comuns

## ❌ Cannot use import statement outside a module

### Motivo:

Falta:

```json
"type": "module"
```

no `package.json`.

---

## ❌ npm install falhando

### Possíveis causas:

* Node desatualizado
* Pasta com caracteres especiais
* Projeto dentro do OneDrive
* Dependências corrompidas

---

## ❌ Módulo não encontrado

### Verifique:

Imports ESModules precisam terminar com:

```js
.js
```

Exemplo correto:

```js
import createQRCode from './services/qr-code/create.js'
```

---

# 🧱 Arquitetura do Projeto

O projeto utiliza separação por responsabilidade.

## `index.js`

Responsável por:

* Inicialização
* Fluxo principal
* Navegação

---

## `services/`

Contém a lógica de negócio.

Exemplo:

```bash
services/password/
services/qr-code/
```

---

## `prompts-schema/`

Define validações e entradas do usuário.

---

# 📈 Melhorias Futuras

Ideias para evolução:

* Exportar QRCode como imagem PNG
* Interface gráfica
* Histórico de QR Codes
* Criptografia de senhas
* Salvar resultados em banco de dados
* API REST
* Deploy em nuvem
* Dockerização
* Testes automatizados

---

# 🧪 Exemplo de Execução

```bash
npm start
```

Saída:

```bash
? Escolha uma opção
1 - Gerar QRCode
2 - Gerar Senha
```

---

# 📚 Conceitos Aprendidos

Esse projeto ajuda a praticar:

* Node.js
* Terminal CLI
* Modularização
* ESModules
* Organização de código
* Fluxo assíncrono
* Entrada de dados
* Estrutura de projetos

---

# 🤝 Contribuição

Contribuições são bem-vindas.

## Passos:

```bash
git fork
git clone
git checkout -b minha-feature
```

Depois:

```bash
git commit -m "Nova feature"
git push origin minha-feature
```

---

# 📜 Licença

Este projeto está sob licença MIT.

---

# 👨‍💻 Autor

Desenvolvido por Mayckon.

---

# ⭐ Considerações Finais

Esse projeto é pequeno, mas possui conceitos importantes usados em aplicações reais:

* Organização
* Separação de responsabilidades
* Fluxo modular
* Automação via terminal
* Manipulação de entrada do usuário

O principal objetivo não é apenas gerar QR Codes ou senhas, mas entender como estruturar aplicações Node.js de forma limpa e escalável.
