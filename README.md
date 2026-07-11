# Password-Guardian
Site criado para ambiente app scipt que consome a API de vazamento de senhas do "haveibeenpwned", com o objetivo de verificar a quantidade de vezes que a senha foi exposta em vazamentos.
## 🚀 Funcionalidades

- 🔍 Verificação de senhas contra bilhões de credenciais vazadas.
- 🔒 A senha nunca é enviada para servidores externos.
- ⚡ Resultado em poucos segundos.
- 🌐 Interface moderna inspirada em soluções enterprise de cibersegurança.
- ☁️ Deploy gratuito utilizando Google Apps Script.

---

## 🛡️ Como funciona

O Password Guardian utiliza a API **Pwned Passwords** do Have I Been Pwned e o modelo de privacidade **k-Anonymity**.

O fluxo é:

1. O navegador calcula o hash SHA-1 da senha.
2. Apenas os primeiros 5 caracteres do hash são enviados ao HIBP.
3. O HIBP retorna todos os hashes que possuem aquele prefixo.
4. A comparação do hash completo ocorre localmente no navegador.
5. A senha original nunca deixa o dispositivo do usuário.

Exemplo:

```text
Senha digitada:
MinhaSenha123!

SHA1:
4D186321C1A7F0F354B297E8914AB240...

Enviado ao HIBP:
4D186

Comparação realizada localmente:
321C1A7F0F354B297E8914AB240...
```

---

## 🏗️ Arquitetura

```text
Usuário
   ↓
Frontend (HTML + CSS + JS)
   ↓
Google Apps Script
   ↓
HIBP Pwned Password API
   ↓
Resultado
```

---

## 💻 Tecnologias utilizadas

- Google Apps Script
- HTML5
- CSS3
- JavaScript ES6
- Web Crypto API
- Have I Been Pwned API

---

## 📂 Estrutura do projeto

```text
PasswordGuardian/
│
├── Code.gs
└── index.html
```

---

## ⚙️ Instalação

### 1. Criar um projeto no Google Apps Script

Acesse:

https://script.google.com

---

### 2. Criar os arquivos

Crie os seguintes arquivos:

```text
Code.gs
index.html
```

---

### 3. Copiar os códigos

Cole o conteúdo fornecido nos respectivos arquivos.

---

### 4. Publicar

```text
Implantar
→ Nova implantação
→ Aplicativo da Web
→ Quem tem acesso: Qualquer pessoa
```
