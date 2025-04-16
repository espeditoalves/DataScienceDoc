- [1. DataScienceDoc 📊](#1-datasciencedoc-)
  - [1.1. ✨ Recursos](#11--recursos)
  - [1.2. 🛠️ Tecnologias Utilizadas](#12-️-tecnologias-utilizadas)
- [2. Problemas comuns relacionados com Jupyter Notebooks](#2-problemas-comuns-relacionados-com-jupyter-notebooks)
  - [2.1. Comandos e Explicações](#21-comandos-e-explicações)
    - [2.1.1. **Atualizar o `jupyter_core`**](#211-atualizar-o-jupyter_core)
    - [2.1.2. Verificar o Plugin mkdocs-jupyter no mkdocs.yml](#212-verificar-o-plugin-mkdocs-jupyter-no-mkdocsyml)
    - [2.1.3. Remover e Reinstalar Dependências](#213-remover-e-reinstalar-dependências)
    - [2.1.4. Verificar se o Plugin mkdocs-jupyter Está Funcionando](#214-verificar-se-o-plugin-mkdocs-jupyter-está-funcionando)
    - [2.1.5. Iniciar o Servidor MkDocs](#215-iniciar-o-servidor-mkdocs)
    - [2.1.6. Resumo dos Passos](#216-resumo-dos-passos)

# 1. DataScienceDoc 📊

**DataScienceDoc** é um repositório de conhecimento em **`Ciência de Dados`**, criado para documentar estudos, projetos e tutoriais em um formato organizado e acessível.

- ✨ Destaques:

- 📂 Organizado – Estrutura clara e fácil de navegar.

- 📚 Tutoriais & Projetos – Conteúdo prático e didático.

- 🚀 Gerado com MkDocs – Site estático rápido e responsivo.

🔗 Acesse agora: https://espeditoalves.github.io/DataScienceDoc/

## 1.1. ✨ Recursos

- 📚 Documentação estruturada de conceitos e técnicas de Data Science
- 🛠️ Exemplos práticos e snippets de código
- 📊 Anotações sobre ferramentas, frameworks e melhores práticas
- 🔍 Facilidade de navegação e busca

## 1.2. 🛠️ Tecnologias Utilizadas

- **MkDocs** - Gerador de documentação estática
- **Material for MkDocs** - Tema moderno e responsivo
- **Git/GitHub** - Versionamento e hospedagem
- **Python** - Linguagem principal para exemplos


# 2. Problemas comuns relacionados com Jupyter Notebooks

Este guia explica como configurar o MkDocs com suporte a Jupyter Notebooks, além de resolver problemas comuns relacionados a plugins e dependências.

---

## 2.1. Comandos e Explicações

### 2.1.1. **Atualizar o `jupyter_core`**
```bash
poetry run pip install --upgrade jupyter_core
```
**O que faz?** Atualiza a biblioteca jupyter_core para a versão mais recente.

**Por que é importante?** O jupyter_core é uma dependência do Jupyter, e atualizá-lo pode corrigir avisos de depreciação ou bugs.

### 2.1.2. Verificar o Plugin mkdocs-jupyter no mkdocs.yml
```yaml
plugins:
  - mkdocs-jupyter
```
**O que faz?** Habilita o plugin `mkdocs-jupyter` no arquivo de configuração do MkDocs.

**Por que é importante?** Esse plugin permite que Jupyter Notebooks (.ipynb) sejam convertidos em páginas estáticas no site gerado pelo MkDocs.

### 2.1.3. Remover e Reinstalar Dependências
``` bash
poetry remove mkdocs-jupyter mkdocs
poetry cache clear mkdocs-jupyter --all
poetry add mkdocs mkdocs-jupyter
```
**O que faz?** 
1. Remove as dependências `mkdocs` e `mkdocs-jupyter`.
2. Limpa o cache do Poetry relacionado ao mkdocs-jupyter.
3. Reinstala as dependências mkdocs e mkdocs-jupyter.

Por que é importante? Isso resolve problemas de instalação corrompida ou conflitos de versões.

### 2.1.4. Verificar se o Plugin mkdocs-jupyter Está Funcionando
```bash
poetry run python -c "import mkdocs_jupyter"
```
**O que faz?** Tenta importar o módulo mkdocs_jupyter no ambiente virtual do Poetry.

**Por que é importante?** Se o comando não gerar erros, significa que o plugin está instalado corretamente.

### 2.1.5. Iniciar o Servidor MkDocs
``` bash
poetry run mkdocs serve
```

**O que faz?** Inicia o servidor de desenvolvimento do MkDocs.

**Por que é importante?** Permite visualizar a documentação localmente em http://127.0.0.1:8000/.


### 2.1.6. Resumo dos Passos

1. Atualize o jupyter_core para evitar avisos de depreciação.

2. Verifique o mkdocs.yml para garantir que o plugin mkdocs-jupyter está habilitado.

3. Remova e reinstale as dependências (mkdocs e mkdocs-jupyter) para resolver problemas de instalação.

4. Verifique se o plugin está funcionando tentando importar o módulo mkdocs_jupyter.

5. Inicie o servidor MkDocs para visualizar a documentação.

Como funciona o gh-deploy?
Ele gera a versão estática do site.
Cria um novo branch chamado gh-pages no repositório.
Publica os arquivos no GitHub Pages automaticamente.
poetry run mkdocs gh-deploy

--- 

Adicionar e commit das mudanças
No terminal, dentro do seu projeto, rode:

1️⃣ Adicionar e commit das mudanças
```sh
git add .
git commit -m "Atualizando documentação"
git push origin main  # Envie as mudanças para o GitHub
```
2️⃣ Rodar o comando de deploy
Agora, gere e publique a nova versão do site com:

```sh
mkdocs gh-deploy
```
Ou, se estiver usando Poetry:

```sh
poetry run mkdocs gh-deploy
```
3️⃣ Conferir se atualizou


------------
plugins:
  - mkdocs-jupyter


poetry remove mkdocs-jupyter mkdocs
poetry cache clear mkdocs-jupyter --all
poetry add mkdocs mkdocs-jupyter

poetry run python -c "import mkdocs_jupyter"
poetry run mkdocs serve

