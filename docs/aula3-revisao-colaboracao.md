# Processo de Trabalho, Colaboração e Boas Práticas no GitHub

## Visão Geral do Fluxo de Trabalho GitHub Flow

O GitHub Flow é um fluxo de trabalho leve e baseado em branches que permite experimentar novas ideias com segurança, sem comprometer o projeto principal . Os passos fundamentais são:

- Criar um branch a partir do `main`
- Fazer commits das alterações
- Abrir um pull request
- Colaborar e discutir as mudanças
- Fazer mais commits se necessário
- Fazer o deploy para teste final
- Fazer o merge do branch no `main` 

## Processo Detalhado de Trabalho

### 1. Branches: Isolamento de Alterações

Branching é um conceito central no Git. Por padrão, a versão de produção do projeto vive no branch `main`. Para experimentar uma nova funcionalidade ou corrigir um problema, cria-se um novo branch do projeto, que inicialmente é idêntico ao `main`, mas qualquer alteração feita só afetará este novo branch .

### 2. Commits: Registro de Alterações

Conforme as alterações são feitas nos arquivos, elas devem ser commitadas (salvas como snapshots) no branch de trabalho. O processo de commit envolve duas etapas principais:

- **Working Tree**: área onde os arquivos são modificados
- **Staging Area (Index)**: local onde as alterações são preparadas para o commit
- **Commit**: snapshot de tudo que está na staging area 

Comandos essenciais:
```bash
git status                    # verifica o status
git add <arquivo>             # move para staging area
git commit -m "mensagem"      # cria o snapshot
```

### 3. Ambientes Local e Remoto

- **Repositório remoto**: cópia do repositório no GitHub, fonte da verdade para o time
- **Repositório local**: cópia completa armazenada no computador do desenvolvedor 

A interação entre eles ocorre através de quatro comandos principais: `git clone`, `git fetch`, `git pull` e `git push` .

## Formas de Colaboração

### Pull Requests: O Centro da Colaboração

Pull requests são a principal forma de colaboração no GitHub. Eles permitem que membros do time revisem código, forneçam feedback e discutam alterações antes de mesclar ao branch principal .

Recomenda-se abrir um pull request o mais cedo possível no processo, mesmo que o trabalho não esteja perfeito, para dar visibilidade aos colegas e evitar retrabalho .

### Revisões de Código (Code Review)

Qualquer pessoa com acesso de leitura pode revisar e comentar as alterações propostas. Ao submeter uma revisão, é possível escolher entre três status :

- **Comentário**: compartilhar feedback sem aprovar ou solicitar alterações
- **Aprovar**: aprovar as mudanças para merge
- **Solicitar alterações**: identificar problemas que precisam ser corrigidos antes do merge

Os revisores podem comentar em linhas específicas, sugerir alterações que os autores podem aplicar diretamente e discutir abordagens de implementação .

### CODEOWNERS e Revisões Automáticas

É possível definir proprietários de código em um arquivo `CODEOWNERS`. Quando um pull request modifica código de sua responsabilidade, essas pessoas ou equipes são automaticamente solicitadas como revisoras .

## Boas Práticas

### 1. Commits com Mensagens Claras

Mensagens de commit descritivas são essenciais para rastrear mudanças no projeto :

- Comece com um verbo de ação: "Fix", "Add" ou "Update"
- Mantenha a mensagem curta e precisa, descrevendo **o que** e **por que** foi alterado

Exemplo: `git commit -m "Corrige problema de login ajustando tempo de sessão"` 

### 2. Estratégia de Branching

Escolha uma estratégia que se adapte ao time :

- **Git Flow**: branches específicos para features, desenvolvimento e releases (ideal para projetos com releases planejadas)
- **Feature Branching**: cada nova funcionalidade tem seu próprio branch
- **Trunk-Based Development**: desenvolvedores trabalham com pequenas mudanças diretamente no branch principal

### 3. Manutenção do Repositório

Um repositório limpo e organizado facilita a manutenção e aumenta a produtividade :

- Exclua branches antigos que não são mais necessários
- Evite enviar arquivos grandes usando `.gitignore`
- Utilize `git rebase` para manter o histórico limpo e evitar commits de merge desnecessários

### 4. Versionamento e Referências

Em produção, evite usar `@main` nas referências. Em vez disso :

- Fixe em um SHA de commit específico ou em uma tag
- Use versionamento semântico (v1, v1.1, v2) para ações e workflows reutilizáveis
- Tags permitem deprecação de versões antigas sem quebrar pipelines

### 5. Qualidade e Automação no Pull Request

Pull requests devem focar em um único problema ou funcionalidade, descrevendo claramente o que está sendo alterado e fornecendo contexto para os revisores . Utilize:

- **Conversa geral**: comentários amplos sobre o pull request
- **Comentários em linha**: discussões específicas sobre trechos de código
- **Resolução de conversas**: marcar como resolvidas após o feedback ser tratado 

### 6. Configuração Inicial

Antes de começar a trabalhar, configure corretamente o ambiente :

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seu@email.com"
git config --global core.autocrlf true  # Windows
git config --global core.autocrlf input # Mac/Linux
```

---

## Referências

SALESFORCE. **Work with the GitHub Workflow**. Trailhead. Disponível em: <https://trailhead.salesforce.com/pt-BR/content/learn/modules/git-and-git-hub-basics/work-with-the-git-hub-workflow>. Acesso em: 25 fev. 2026. 

GITHUB DOCS. **Collaborating with pull requests**. Disponível em: <https://docs.github.com/en/pull-requests/collaborating-with-pull-requests>. Acesso em: 25 fev. 2026. 

GITHUB DOCS. **Best practices for Projects**. Disponível em: <https://docs.github.com/en/issues/planning-and-tracking-with-projects/learning-about-projects/best-practices-for-projects>. Acesso em: 25 fev. 2026. 

CODENOVA. **Best Practices for Git and GitHub Collaboration**. Medium. Disponível em: <https://medium.com/@codenova/best-practices-for-git-and-github-collaboration-348cc3b774d1>. Acesso em: 25 fev. 2026. 

GITHUB DOCS. **About pull request reviews**. Disponível em: <https://docs.github.com/articles/about-pull-request-reviews>. Acesso em: 25 fev. 2026. 

GITHUB DOCS. **Sobre revisões de pull request**. Disponível em: <https://docs.github.com/pt/pull-requests/collaborating-with-pull-requests/reviewing-changes-in-pull-requests/about-pull-request-reviews>. Acesso em: 25 fev. 2026. 

GITHUB COMMUNITY. **Organization best practices for reusable workflows and actions for an enterprise**. Disponível em: <https://github.com/orgs/community/discussions/171037>. Acesso em: 25 fev. 2026. 