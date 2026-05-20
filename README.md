# Atividade Prática - Armazenamento Local

**Disciplina:** Sistemas Web  
**Aula:** 14 - Armazenamento Local  

## Sobre o Projeto

Este repositório contém três páginas HTML que demonstram os diferentes mecanismos de armazenamento local no navegador: LocalStorage, SessionStorage e Cookies.

## Estrutura do Repositório

## Exercícios

### Exercício 1 - Bloco de Anotações Pessoal (LocalStorage)

**Arquivo:** `exercicio1-localstorage.html`

Bloco de anotações que utiliza LocalStorage para salvar o texto permanentemente.

**Funcionalidades:**
- Campo `<textarea>` para digitar anotações
- Botão "Salvar anotação" - grava no LocalStorage
- Botão "Limpar anotação" - remove do armazenamento
- Feedback visual das ações
- Ao abrir a página, carrega automaticamente a anotação salva

**Como testar:** Escreva um texto, salve, feche o navegador e abra novamente. O texto deve continuar no campo.

---

### Exercício 2 - Carrinho de Compras da Sessão (SessionStorage)

**Arquivo:** `exercicio2-sessionstorage.html`

Simulação de carrinho de compras usando SessionStorage.

**Funcionalidades:**
- Campo para nome do produto
- Botão "Adicionar ao carrinho"
- Lista (`<ul>`) com produtos adicionados
- Botão para remover cada produto individualmente
- Contador de itens no carrinho
- Botão "Esvaziar carrinho"

**Como testar:** Adicione produtos, recarregue a página (F5) - a lista continua. Feche a aba e abra novamente - o carrinho estará vazio.

---

### Exercício 3 - Preferência de Idioma (Cookies)

**Arquivo:** `exercicio3-cookies.html`

Sistema de preferência de idioma utilizando Cookies com validade de 14 dias.

**Funcionalidades:**
- Pelo menos 3 textos que mudam conforme o idioma
- `<select>` com opções Português e English
- Botão "Salvar preferência"
- Botão "Remover preferência"
- Funções auxiliares: `setCookie`, `getCookie` e `deleteCookie`

**Como testar:** Selecione English, salve e recarregue - os textos devem continuar em inglês. Use F12 → Application → Cookies para ver o cookie "idioma". Clique em "Remover preferência" e recarregue - volta ao português.

## Requisitos Atendidos

### Gerais
- [x] Estrutura HTML5 completa (DOCTYPE, lang="pt-BR", charset, viewport)
- [x] Título da página identificando o exercício
- [x] `<h1>` visível indicando o nome da aplicação
- [x] Estilo CSS básico para legibilidade
- [x] JavaScript dentro de `<script>` antes do fechamento do `</body>`
- [x] Mensagem de feedback para o usuário
- [x] Arquivos versionados e publicados no GitHub

### Exercício 1 (LocalStorage)
- [x] `localStorage.setItem()` para gravar o texto
- [x] `localStorage.getItem()` ao carregar a página
- [x] `localStorage.removeItem()` ao limpar
- [x] Chave fixa: "minhaAnotacao"
- [x] Persiste após fechar e reabrir o navegador

### Exercício 2 (SessionStorage)
- [x] `sessionStorage.setItem()` quando o carrinho muda
- [x] `sessionStorage.getItem()` ao carregar a página
- [x] Array salvo como JSON (`JSON.stringify` / `JSON.parse`)
- [x] `sessionStorage.removeItem()` ao esvaziar
- [x] Ao recarregar (F5) os produtos continuam
- [x] Ao fechar a aba o carrinho começa vazio

### Exercício 3 (Cookies)
- [x] `document.cookie` para salvar o idioma
- [x] Expiração com `max-age` (14 dias = 1209600 segundos)
- [x] Inclui `path=/` ao criar e apagar o cookie
- [x] Lê o cookie e aplica o idioma ao carregar
- [x] Botão "Remover preferência" apaga com `max-age=0`
- [x] Textos mudam com JavaScript (`textContent`)

## Diferenças entre os Armazenamentos

| Característica | LocalStorage (Ex. 1) | SessionStorage (Ex. 2) | Cookies (Ex. 3) |
|----------------|----------------------|------------------------|-----------------|
| Projeto | Bloco de anotações | Carrinho de compras | Preferência de idioma |
| Duração | Permanente (até apagar) | Enquanto a aba estiver aberta | 14 dias (configurado) |
| API principal | `localStorage.setItem` | `sessionStorage.setItem` | `document.cookie` |
| Teste principal | Fecha e reabre → anotação continua | Fecha aba → carrinho esvazia | Recarrega → idioma continua salvo |

## Como Executar

1. Clone o repositório:
```bash
git clone https://github.com/seu-usuario/aula14-armazenamento-local.git