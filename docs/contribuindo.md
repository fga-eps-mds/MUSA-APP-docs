# Contribuindo para o MUSA

Obrigado por considerar contribuir para o projeto MUSA! Este documento fornece diretrizes e melhores práticas para contribuições.

---

## Código de Conduta

Ao participar deste projeto, você concorda em manter um ambiente respeitoso e colaborativo. Esperamos que todos os contribuidores:

- Sejam respeitosos e inclusivos
- Aceitem críticas construtivas
- Foquem no que é melhor para a comunidade
- Demonstrem empatia com outros membros

---

## Como Contribuir

### 1. Reportando Bugs

Encontrou um bug? Ajude-nos a melhorar!

**Antes de reportar:**
- Verifique se o bug já foi reportado nas [Issues](https://github.com/fga-eps-mds/2025.2-Inti/issues)
- Certifique-se de estar usando a versão mais recente

**Ao reportar:**
- Use um título claro e descritivo
- Descreva os passos para reproduzir o problema
- Explique o comportamento esperado vs. observado
- Inclua screenshots se aplicável
- Mencione seu sistema operacional e versão do navegador

**Template de Issue:**

```markdown
**Descrição do Bug**
Uma descrição clara do que é o bug.

**Passos para Reproduzir**
1. Vá para '...'
2. Clique em '...'
3. Role até '...'
4. Veja o erro

**Comportamento Esperado**
O que deveria acontecer.

**Screenshots**
Se aplicável, adicione screenshots.

**Ambiente:**
- OS: [ex: Windows 11]
- Navegador: [ex: Chrome 120]
- Versão: [ex: 2.0.0]
```

---

### 2. Sugerindo Melhorias

Tem uma ideia para melhorar o MUSA?

**Antes de sugerir:**
- Verifique se a sugestão já foi feita
- Certifique-se de que está alinhada com os objetivos do projeto

**Ao sugerir:**
- Use um título claro e descritivo
- Forneça uma descrição detalhada da melhoria
- Explique por que seria útil para a maioria dos usuários
- Liste exemplos de como funcionaria

---

### 3. Contribuindo com Código

#### Preparando o Ambiente

1. **Fork o repositório**
   ```bash
   # Clique em "Fork" no GitHub
   ```

2. **Clone seu fork**
   ```bash
   git clone https://github.com/SEU-USUARIO/2025.2-Inti.git
   cd 2025.2-Inti
   ```

3. **Adicione o repositório original como upstream**
   ```bash
   git remote add upstream https://github.com/fga-eps-mds/2025.2-Inti.git
   ```

4. **Instale as dependências**
   ```bash
   npm install
   ```

#### Fluxo de Trabalho

1. **Crie uma branch para sua feature**
   ```bash
   git checkout -b feature/nome-da-feature
   ```

2. **Faça suas alterações**
   - Escreva código limpo e legível
   - Siga os padrões do projeto
   - Comente código complexo

3. **Formate o código**
   ```bash
   npx prettier --write .
   ```

4. **Teste suas alterações**
   - Teste em diferentes navegadores
   - Teste responsividade mobile
   - Verifique se não quebrou funcionalidades existentes

5. **Commit suas alterações**
   ```bash
   git add .
   git commit -m "[FEAT]: adiciona nova funcionalidade"
   ```

6. **Mantenha sua branch atualizada**
   ```bash
   git fetch upstream
   git rebase upstream/main
   ```

7. **Push para seu fork**
   ```bash
   git push origin feature/nome-da-feature
   ```

8. **Abra um Pull Request**
   - Vá para o repositório original no GitHub
   - Clique em "New Pull Request"
   - Selecione sua branch
   - Preencha o template de PR

---

## Padrões de Código

### JavaScript

#### Nomenclatura

```javascript
// Variáveis e funções: camelCase
const userName = 'João';
function getUserData() { }

// Constantes: UPPER_CASE
const API_URL = 'https://api.musa.com';
const MAX_RETRIES = 3;

// Classes: PascalCase
class UserManager { }
```

#### Estrutura de Funções

```javascript
/**
 * Busca dados do usuário pelo ID
 * @param {number} userId - ID do usuário
 * @returns {Promise<Object>} Dados do usuário
 */
async function getUserById(userId) {
  try {
    const response = await fetch(`${API_URL}/users/${userId}`);
    return await response.json();
  } catch (error) {
    console.error('Erro ao buscar usuário:', error);
    throw error;
  }
}
```

#### Boas Práticas

- Use `const` por padrão, `let` quando necessário, evite `var`
- Prefira arrow functions para callbacks
- Use template literals para strings
- Evite código duplicado (DRY - Don't Repeat Yourself)
- Mantenha funções pequenas e focadas (Single Responsibility)

### HTML

```html
<!-- Use estrutura semântica -->
<header>
  <nav>
    <ul>
      <li><a href="#home">Home</a></li>
    </ul>
  </nav>
</header>

<main>
  <section>
    <h1>Título da Seção</h1>
    <p>Conteúdo...</p>
  </section>
</main>

<footer>
  <p>&copy; 2025 MUSA</p>
</footer>
```

### CSS

```css
/* Use nomenclatura BEM quando apropriado */
.card { }
.card__title { }
.card__content { }
.card--featured { }

/* Organize propriedades logicamente */
.element {
  /* Posicionamento */
  position: relative;
  top: 0;
  left: 0;
  
  /* Box Model */
  display: flex;
  width: 100%;
  padding: 1rem;
  margin: 0;
  
  /* Tipografia */
  font-size: 1rem;
  color: #333;
  
  /* Visual */
  background: #fff;
  border: 1px solid #ddd;
  
  /* Outros */
  cursor: pointer;
}
```

---

## Padrão de Commits

### Formato

```
[TIPO]: descrição curta

Descrição detalhada (opcional)
```

### Tipos de Commit

| Tipo | Descrição | Exemplo |
|------|-----------|---------|
| `[FEAT]` | Nova funcionalidade | `[FEAT]: adiciona sistema de busca` |
| `[FIX]` | Correção de bug | `[FIX]: corrige erro no login` |
| `[DOCS]` | Documentação | `[DOCS]: atualiza README` |
| `[STYLE]` | Formatação | `[STYLE]: formata código com Prettier` |
| `[REFACTOR]` | Refatoração | `[REFACTOR]: simplifica função de validação` |
| `[TEST]` | Testes | `[TEST]: adiciona testes unitários` |
| `[CHORE]` | Manutenção | `[CHORE]: atualiza dependências` |

### Boas Práticas de Commit

- Use o imperativo ("adiciona" não "adicionado")
- Primeira linha com no máximo 72 caracteres
- Seja específico e descritivo
- Um commit por mudança lógica
- Não commite código comentado ou console.logs

**Bom:**
```bash
git commit -m "[FEAT]: adiciona validação de email no formulário de cadastro"
```

**Ruim:**
```bash
git commit -m "mudanças"
git commit -m "fix"
git commit -m "atualizações várias"
```

---

## Template de Pull Request

Ao abrir um PR, use o seguinte template:

```markdown
## Descrição
Breve descrição das mudanças realizadas.

## Tipo de Mudança
- [ ] Bug fix
- [ ] Nova funcionalidade
- [ ] Breaking change
- [ ] Documentação

## Como Testar
1. Passo 1
2. Passo 2
3. Passo 3

## Checklist
- [ ] Código formatado com Prettier
- [ ] Testado em Chrome
- [ ] Testado em Firefox
- [ ] Testado em mobile
- [ ] Documentação atualizada
- [ ] Sem console.logs ou código comentado

## Screenshots (se aplicável)
Adicione screenshots das mudanças visuais.

## Issues Relacionadas
Closes #123
```

---

## Processo de Review

### Para Revisores

- Seja construtivo e respeitoso
- Teste as mudanças localmente
- Verifique se segue os padrões do projeto
- Aprove apenas se estiver confiante

### Para Contribuidores

- Responda aos comentários prontamente
- Faça as alterações solicitadas
- Agradeça o feedback
- Seja paciente durante o processo

---

## Estrutura de Branches

```
main
  ├── develop
  │   ├── feature/nome-da-feature
  │   ├── feature/outra-feature
  │   └── bugfix/nome-do-bug
  └── hotfix/bug-critico
```

### Convenções

- `main`: Código em produção
- `develop`: Código em desenvolvimento
- `feature/*`: Novas funcionalidades
- `bugfix/*`: Correções de bugs
- `hotfix/*`: Correções urgentes em produção

---

## Ferramentas de Desenvolvimento

### Extensões VS Code Recomendadas

```json
{
  "recommendations": [
    "esbenp.prettier-vscode",
    "dbaeumer.vscode-eslint",
    "ritwickdey.liveserver",
    "formulahendry.auto-rename-tag",
    "christian-kohler.path-intellisense",
    "eamodio.gitlens"
  ]
}
```

### Scripts NPM Úteis

```json
{
  "scripts": {
    "format": "prettier --write .",
    "format:check": "prettier --check .",
    "serve": "live-server"
  }
}
```

---

## Recursos para Contribuidores

### Documentação

- [Guia de Início](comecando.md)
- [Arquitetura do Sistema](arquitetura.md)
- [Equipe](equipe.md)

### Links Úteis

- [Git Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf)
- [Markdown Guide](https://www.markdownguide.org/)
- [JavaScript Style Guide](https://github.com/airbnb/javascript)
- [Conventional Commits](https://www.conventionalcommits.org/)

---

## Dúvidas?

Se você tiver dúvidas sobre como contribuir:

1. Consulte a documentação existente
2. Verifique as [Issues](https://github.com/fga-eps-mds/2025.2-Inti/issues)
3. Entre em contato com a [equipe](equipe.md)
4. Abra uma issue com a tag `question`

---

## Agradecimentos

Obrigado por contribuir para o MUSA! Cada contribuição, por menor que seja, ajuda a tornar o projeto melhor para todos.

**Juntos, construímos algo incrível! 🚀**
