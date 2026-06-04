# 📦 Armazenamento Local no Navegador

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Status](https://img.shields.io/badge/Status-Concluído-success?style=for-the-badge)

## 📖 Sobre o Projeto

Este repositório foi desenvolvido como parte da disciplina **Sistemas Web** (Aula 14 - Armazenamento Local). Aqui demonstro na prática os três principais mecanismos de armazenamento local disponíveis nos navegadores modernos:

- **LocalStorage** - Armazenamento permanente
- **SessionStorage** - Armazenamento por sessão/aba
- **Cookies** - Armazenamento com data de expiração

Cada mecanismo foi aplicado em um cenário prático diferente, mostrando suas características e casos de uso ideais.

---

## 🎯 O que aprendi com este projeto

### ✅ Conceitos teóricos

| Conceito | O que entendi |
|----------|---------------|
| **LocalStorage** | Armazena dados permanentemente no navegador, mesmo após fechar e reabrir. Capacidade ~5-10MB |
| **SessionStorage** | Armazena dados apenas durante a sessão da aba. Fechou a aba, perdeu os dados! |
| **Cookies** | Armazenamento com data de validade. Enviados automaticamente ao servidor em cada requisição |
| **JSON.stringify/parse** | Para salvar arrays e objetos, precisamos converter para string e depois voltar ao original |

### ✅ Habilidades práticas

1. **Manipular LocalStorage** - `setItem()`, `getItem()`, `removeItem()`
2. **Manipular SessionStorage** - Mesma API do LocalStorage, mas com escopo diferente
3. **Manipular Cookies** - Criar, ler e apagar usando `document.cookie` e `max-age`
4. **Persistir arrays** - Salvar listas inteiras usando JSON
5. **Feedback visual** - Mostrar mensagens de sucesso/erro para o usuário

---

## 🛠️ Tecnologias utilizadas

| Tecnologia | Finalidade |
|------------|------------|
| **HTML5** | Estrutura das páginas |
| **CSS3** | Estilização e layout responsivo |
| **JavaScript (Vanilla)** | Lógica de armazenamento e manipulação do DOM |
| **LocalStorage API** | Armazenamento permanente |
| **SessionStorage API** | Armazenamento por sessão |
| **Cookies API** | Armazenamento com expiração |

---

## 📋 Estrutura do Repositório
aula14-armazenamento-local/
│
├── exercicio1-localstorage.html # Bloco de anotações (LocalStorage)
├── exercicio2-sessionstorage.html # Carrinho de compras (SessionStorage)
├── exercicio3-cookies.html # Preferência de idioma (Cookies)
└── README.md # Documentação do projeto

---

## 🎨 Exercícios Detalhados

### 📝 Exercício 1 - Bloco de Anotações Pessoal (LocalStorage)

**Arquivo:** `exercicio1-localstorage.html`

Um bloco de anotações que salva seu texto permanentemente no navegador.

#### 🎯 Funcionalidades:
- ✅ Campo `<textarea>` para escrever suas anotações
- ✅ Botão **"Salvar anotação"** - grava no LocalStorage
- ✅ Botão **"Limpar anotação"** - remove do armazenamento
- ✅ Feedback visual das ações (mensagem de sucesso)
- ✅ Carregamento automático da última anotação salva

#### 🧪 Como testar:
```bash
1. Escreva um texto qualquer no campo
2. Clique em "Salvar anotação"
3. Feche o navegador completamente
4. Abra a página novamente
5. ✅ O texto continua lá!