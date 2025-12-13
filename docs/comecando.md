# Começando com MUSA

Este guia completo irá ajudá-lo a configurar o ambiente de desenvolvimento e executar o projeto MUSA em sua máquina local.

---

## Pré-requisitos

Antes de começar, certifique-se de ter as seguintes ferramentas instaladas em seu sistema:

### Obrigatórios

- **[Git](https://git-scm.com/downloads)** - Sistema de controle de versão
- **[Node.js](https://nodejs.org/)** (v18 ou superior) - Runtime JavaScript
- **[npm](https://www.npmjs.com/)** - Gerenciador de pacotes (incluído com Node.js)

### Recomendados

- **[Visual Studio Code](https://code.visualstudio.com/)** - Editor de código recomendado
- **Extensão [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)** - Servidor de desenvolvimento com hot-reload
- **Extensão [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)** - Formatação automática de código

---

## Verificando Instalações

Antes de prosseguir, verifique se as ferramentas estão instaladas corretamente:

```bash
# Verificar versão do Git
git --version

# Verificar versão do Node.js
node --version

# Verificar versão do npm
npm --version
```

**Saídas esperadas:**
```
git version 2.x.x
v18.x.x (ou superior)
9.x.x (ou superior)
```

---

## Instalação do Projeto

### 1. Clone o Repositório

Abra o terminal e execute:

```bash
git clone https://github.com/fga-eps-mds/2025.2-Inti.git
cd 2025.2-Inti
```

### 2. Instale as Dependências

Dentro do diretório do projeto, execute:

```bash
npm install
```

Este comando irá:
- Ler o arquivo `package.json`
- Baixar todas as dependências necessárias
- Criar a pasta `node_modules`

---

## Executando o Projeto

### Método 1: Live Server (Recomendado)

O Live Server proporciona hot-reload automático, atualizando o navegador sempre que você salvar alterações.

#### Passos:

1. **Instale a extensão Live Server** no VS Code
   - Abra o VS Code
   - Vá em Extensions (Ctrl+Shift+X)
   - Busque por "Live Server"
   - Clique em "Install"

2. **Abra o projeto no VS Code**
   ```bash
   code .
   ```

3. **Inicie o Live Server**
   - Clique com botão direito em `index.html`
   - Selecione **"Open with Live Server"**

4. **Acesse no navegador**
   - O navegador abrirá automaticamente em `http://localhost:5500`

### Método 2: Servidor HTTP Simples

Caso prefira não usar o VS Code, você pode usar o servidor HTTP do Node.js:

```bash
# Instale o http-server globalmente
npm install -g http-server

# Execute o servidor
http-server -p 8080

# Acesse http://localhost:8080 no navegador
```

---

## Testando Responsividade Mobile

Para testar a aplicação em diferentes tamanhos de tela:

### DevTools do Navegador

1. Abra as **DevTools** (F12 ou Ctrl+Shift+I)
2. Ative o **modo de visualização mobile** (Ctrl+Shift+M)
3. Selecione diferentes dispositivos no dropdown
4. Teste em diferentes resoluções

### Extensão Mobile Simulator

Para testes mais avançados, instale a extensão:

- **[Mobile Simulator](https://chromewebstore.google.com/detail/mobile-simulator-responsi/ckejmhbmlajgoklhgbapkiccekfoccmk)** para Chrome

---

## Estrutura do Projeto

Após a instalação, você terá a seguinte estrutura:

```
2025.2-Inti/
│
├── css/                        # Estilos
│   └── style.css
│
├── js/                         # Scripts
│   ├── app.js                  # Orquestrador principal
│   ├── auth.js                 # Autenticação
│   └── router.js               # Roteamento SPA
│
├── pages/                      # Páginas HTML
│   ├── login.html
│   ├── cadastro.html
│   ├── home.html
│   ├── eventos.html
│   ├── create.html
│   ├── search.html
│   └── user.html
│
├── assets/                     # Recursos estáticos
│
├── node_modules/               # Dependências (gerado)
│
├── index.html                  # Ponto de entrada
├── package.json                # Configuração npm
└── README.md                   # Documentação
```

---

## Padrões de Desenvolvimento

### Formatação de Código

O projeto utiliza **Prettier** para garantir consistência no código.

**SEMPRE** execute antes de fazer commit:

```bash
npx prettier --write .
```

### Configuração do Prettier

O arquivo `.prettierrc` contém as configurações:

```json
{
  "semi": true,
  "singleQuote": true,
  "tabWidth": 2,
  "trailingComma": "es5"
}
```

### Arquivos Ignorados

O `.prettierignore` define quais arquivos não devem ser formatados:

```
node_modules/
dist/
build/
*.min.js
*.min.css
```

---

## Fluxo de Trabalho Git

### Fluxo Correto de Commit

```bash
# 1. Formate o código
npx prettier --write .

# 2. Adicione as alterações
git add .

# 3. Faça o commit com mensagem descritiva
git commit -m "[FEAT]: adiciona página de eventos"

# 4. Envie para o repositório
git push
```

### Padrão de Mensagens de Commit

Use prefixos para categorizar seus commits:

- `[FEAT]`: Nova funcionalidade
- `[FIX]`: Correção de bug
- `[DOCS]`: Alterações na documentação
- `[STYLE]`: Formatação, espaços em branco
- `[REFACTOR]`: Refatoração de código
- `[TEST]`: Adição ou correção de testes
- `[CHORE]`: Tarefas de manutenção

**Exemplos:**

```bash
git commit -m "[FEAT]: adiciona sistema de busca de eventos"
git commit -m "[FIX]: corrige bug no login de usuários"
git commit -m "[DOCS]: atualiza README com instruções de instalação"
git commit -m "[STYLE]: formata código com Prettier"
```

---

## Configuração do VS Code

### Settings Recomendados

Crie ou edite `.vscode/settings.json`:

```json
{
  "editor.formatOnSave": true,
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "files.autoSave": "onFocusChange",
  "liveServer.settings.port": 5500
}
```

### Extensões Recomendadas

Instale as seguintes extensões para melhor experiência:

1. **Live Server** - Servidor de desenvolvimento
2. **Prettier** - Formatação de código
3. **ESLint** - Linting JavaScript
4. **HTML CSS Support** - Autocomplete CSS em HTML
5. **Path Intellisense** - Autocomplete de caminhos
6. **GitLens** - Visualização avançada de Git

---

## Solução de Problemas

### Erro: "npm: command not found"

**Problema:** Node.js/npm não está instalado ou não está no PATH.

**Solução:**
1. Instale o Node.js do [site oficial](https://nodejs.org/)
2. Reinicie o terminal
3. Verifique com `npm --version`

### Erro: "Cannot find module"

**Problema:** Dependências não foram instaladas.

**Solução:**
```bash
rm -rf node_modules package-lock.json
npm install
```

### Erro: "Port already in use"

**Problema:** A porta já está sendo usada por outro processo.

**Solução:**

**Linux/macOS:**
```bash
# Encontre o processo usando a porta 5500
lsof -i :5500

# Mate o processo
kill -9 <PID>
```

**Windows:**
```powershell
# Encontre o processo
netstat -ano | findstr :5500

# Mate o processo
taskkill /PID <PID> /F
```

### Live Server não atualiza automaticamente

**Problema:** Mudanças no código não refletem no navegador.

**Solução:**
1. Verifique se o Live Server está ativo (ícone no canto inferior direito)
2. Recarregue a página manualmente (Ctrl+R)
3. Limpe o cache do navegador (Ctrl+Shift+Delete)
4. Reinicie o Live Server

---

## Próximos Passos

Agora que você tem o ambiente configurado:

1. **Explore a [Arquitetura](arquitetura.md)** para entender a estrutura do sistema
2. **Conheça a [Equipe](equipe.md)** por trás do projeto
3. **Consulte o [Lean Inception](lean.md)** para entender o processo de concepção

---

## Recursos Adicionais

### Documentação Oficial

- [HTML MDN](https://developer.mozilla.org/en-US/docs/Web/HTML)
- [CSS MDN](https://developer.mozilla.org/en-US/docs/Web/CSS)
- [JavaScript MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
- [Capacitor Docs](https://capacitorjs.com/docs)

### Tutoriais

- [Git Tutorial](https://git-scm.com/docs/gittutorial)
- [JavaScript ES6+](https://javascript.info/)
- [SPA Architecture](https://developer.mozilla.org/en-US/docs/Glossary/SPA)

### Comunidade

- [GitHub Repository](https://github.com/fga-eps-mds/2025.2-Inti)
- [Issues](https://github.com/fga-eps-mds/2025.2-Inti/issues)

---

## Suporte

Se você encontrar problemas não listados aqui:

1. Verifique as [Issues](https://github.com/fga-eps-mds/2025.2-Inti/issues) existentes
2. Crie uma nova issue com detalhes do problema
3. Entre em contato com a [equipe](equipe.md)

**Boa codificação! 🚀**
