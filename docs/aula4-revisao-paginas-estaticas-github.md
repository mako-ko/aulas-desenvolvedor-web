# Criação de Páginas Estáticas no GitHub (GitHub Pages)

## Definição e Conceito Fundamental

**GitHub Pages** é um serviço gratuito de hospedagem de sites estáticos oferecido pelo GitHub. Ele permite publicar diretamente no navegador arquivos HTML, CSS e JavaScript a partir de um repositório do GitHub . Por não suportar código executado no servidor (como PHP ou bancos de dados), é classificado como hospedagem de sites **estáticos** . O serviço integra-se perfeitamente ao fluxo de desenvolvimento Git: cada alteração enviada (*push*) ao repositório pode acionar uma reconstrução automática do site .

## Tipos de Sites no GitHub Pages

Existem três modalidades principais de publicação :

- **Site de Usuário**: vinculado a uma conta pessoal. O repositório deve ser nomeado exatamente como `<username>.github.io`. Fica disponível em `https://<username>.github.io/`. Apenas um por conta.
- **Site de Organização**: similar ao de usuário, mas vinculado a uma organização no GitHub. Repositório: `<organization>.github.io`.
- **Site de Projeto**: associado a um repositório específico. Pode haver múltiplos por conta/organização. Fica disponível em `https://<username>.github.io/<repository>/` ou em domínio personalizado.

## Processo de Criação Passo a Passo

### 1. Preparação do Repositório

- **Criação**: crie um novo repositório no GitHub. Para um site de usuário, nomeie como `username.github.io` (substitua "username" pelo seu nome de usuário) . Para sites de projeto, qualquer nome é válido.
- **Estrutura mínima**: o arquivo `index.html` na raiz do repositório é essencial, pois será a página inicial do site . Pastas comuns incluem `css/`, `js/` e `assets/` para organização .

### 2. Ativação do Serviço

- Acesse a aba **Settings** (Configurações) do repositório .
- No menu lateral, clique em **Pages** .
- Em "Source" (Origem), selecione o branch que contém os arquivos do site (geralmente `main` ou `gh-pages`) e a pasta (`/ (root)` ou `/docs`) .
- Clique em **Save**. O GitHub fornecerá a URL pública do site .

### 3. Publicação de Conteúdo

- **Método local**: clone o repositório, adicione/alterne arquivos localmente e faça push das alterações .
- **Método direto no GitHub**: utilize a interface web para criar, editar e fazer upload de arquivos .
- **Aguardar deploy**: o processo de build e publicação leva de alguns segundos a alguns minutos. A URL final será algo como `https://username.github.io/repository/` .

## Personalização e Funcionalidades Avançadas

### Jekyll e Geração de Sites Estáticos

O GitHub Pages possui suporte nativo ao **Jekyll**, um gerador de sites estáticos que converte Markdown e arquivos de template em HTML . Para utilizá-lo:

- Crie um arquivo `_config.yml` na raiz com as configurações do site .
- Utilize a pasta `_posts` para artigos de blog no formato `ANO-MÊS-DIA-titulo.md` .
- Escolha temas diretamente nas configurações do Pages ou em sites como `jekyllthemes.io` .
- Use **YAML Front Matter** no topo dos arquivos para definir metadados (layout, título, autor) .

### Domínio Personalizado e HTTPS

- **CNAME**: crie um arquivo chamado `CNAME` na raiz do repositório contendo seu domínio personalizado (ex: `www.meusite.com`) .
- **DNS**: no seu provedor de domínio, configure registros apontando para o GitHub:
    - **CNAME** de `www` para `username.github.io`.
    - **Registros A** para domínios apontando para os endereços IP do GitHub (185.199.108.153, etc.) .
- **HTTPS**: o GitHub fornece certificados SSL automaticamente. Habilite a opção "Enforce HTTPS" nas configurações do Pages .

### Automação com GitHub Actions

É possível criar fluxos de trabalho automatizados (*workflows*) com GitHub Actions para buildar e publicar o site sempre que houver alterações . Isso é especialmente útil para projetos que utilizam frameworks JavaScript (React, Vue) ou geradores que exigem etapa de build (Hugo, VuePress) .

## Limitações Importantes

- **Conteúdo estático apenas**: não há suporte a linguagens server-side (PHP, Python, Ruby) nem bancos de dados .
- **Tamanho**: limite de 1 GB por repositório .
- **Largura de banda**: limite suave de 100 GB por mês .
- **Builds**: limite de 10 builds por hora .
- **Público x Privado**: embora o repositório possa ser privado, o site publicado será público (exceto para contas empresariais com recurso específico) .

## Boas Práticas

- **Commits frequentes**: publique atualizações com mensagens claras para manter histórico rastreável .
- **Testes locais**: utilize ferramentas como o Jekyll localmente para pré-visualizar antes do push .
- **Otimização**: comprima imagens, minimize CSS/JS e utilize CDN para recursos pesados .
- **Segurança**: nunca armazene senhas ou chaves de API nos arquivos. Utilize variáveis de ambiente ou arquivos ignorados pelo Git .
- **Backup**: mantenha cópias locais do repositório .

---

## Referências

KARTIKNAIK18. **github-pages**: How to host a static website (HTML, CSS, JS) for free using GitHub Pages. Disponível em: <https://github.com/KARTIKNAIK18/github-pages>. Acesso em: 25 fev. 2026 .

TUFTS UNIVERSITY. **Creating websites with GitHub Pages**. Tufts Technology Services. Disponível em: <https://tuftswork.atlassian.net/wiki/spaces/ESPTS/pages/707756079/>. Acesso em: 25 fev. 2026 .

**Github Pages 体验全攻略：从零到一的部署指南**. 百度开发者中心, 11 set. 2025. Disponível em: <https://developer.baidu.com/article/detail.html?id=3562508>. Acesso em: 25 fev. 2026 .

**Github Pages 体验全攻略：从零开始的静态网站部署教程**. 百度智能云, 22 set. 2025. Disponível em: <https://cloud.baidu.com/article/3717193>. Acesso em: 25 fev. 2026 .

FENTON, Tom. **How to Create a Free Web Page Using GitHub Pages**. Virtualization Review, 15 jan. 2026. Disponível em: <https://virtualizationreview.com/articles/2026/01/15/how-to-create-a-free-web-page-using-github-pages.aspx>. Acesso em: 25 fev. 2026 .

TEAM IT SECURITY. **Building and Deploying a Custom Site Using GitHub Actions and GitHub Pages**. Disponível em: <https://tsecurity.de/de/2676321/IT+Programmierung/Building+and+Deploying+a+Custom+Site+Using+GitHub+Actions+and+GitHub+Pages./>. Acesso em: 25 fev. 2026 .

WEBSTUDIO. **GitHub Pages**. Webstudio Documentation. Disponível em: <https://docs.webstudio.is/university/self-hosting/github-pages>. Acesso em: 25 fev. 2026 .

FAHIM, Marium. **GitHub Hosting: An Easy Guide To Host Websites with GitHub**. CyberPanel, 21 jul. 2025. Disponível em: <https://cyberpanel.net/blog/github-hosting>. Acesso em: 25 fev. 2026 .

**利用GitHub搭建静态网站的完整步骤与实践指南**. trae.cn, 17 nov. 2025. Disponível em: <https://www.trae.cn/article/706648066>. Acesso em: 25 fev. 2026 .

MICROSOFT. **¿Qué es GitHub Pages?** Microsoft Learn. Disponível em: <https://learn.microsoft.com/es-es/training/modules/create-host-web-sites-github-pages/2-what-is-github-pages>. Acesso em: 25 fev. 2026 .