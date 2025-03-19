
# Problemas comuns relacionados com Jupyter Notebooks

Este guia explica como configurar o MkDocs com suporte a Jupyter Notebooks, além de resolver problemas comuns relacionados a plugins e dependências.

---

## Comandos e Explicações

### 1. **Atualizar o `jupyter_core`**
```bash
poetry run pip install --upgrade jupyter_core
```
**O que faz?** Atualiza a biblioteca jupyter_core para a versão mais recente.

**Por que é importante?** O jupyter_core é uma dependência do Jupyter, e atualizá-lo pode corrigir avisos de depreciação ou bugs.

### 2. Verificar o Plugin mkdocs-jupyter no mkdocs.yml
```yaml
plugins:
  - mkdocs-jupyter
```
**O que faz?** Habilita o plugin `mkdocs-jupyter` no arquivo de configuração do MkDocs.

**Por que é importante?** Esse plugin permite que Jupyter Notebooks (.ipynb) sejam convertidos em páginas estáticas no site gerado pelo MkDocs.

### 3. Remover e Reinstalar Dependências
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

### 4. Verificar se o Plugin mkdocs-jupyter Está Funcionando
```bash
poetry run python -c "import mkdocs_jupyter"
```
**O que faz?** Tenta importar o módulo mkdocs_jupyter no ambiente virtual do Poetry.

**Por que é importante?** Se o comando não gerar erros, significa que o plugin está instalado corretamente.

### 5. Iniciar o Servidor MkDocs
``` bash
poetry run mkdocs serve
```

**O que faz?** Inicia o servidor de desenvolvimento do MkDocs.

**Por que é importante?** Permite visualizar a documentação localmente em http://127.0.0.1:8000/.


### Resumo dos Passos

1. Atualize o jupyter_core para evitar avisos de depreciação.

2. Verifique o mkdocs.yml para garantir que o plugin mkdocs-jupyter está habilitado.

3. Remova e reinstale as dependências (mkdocs e mkdocs-jupyter) para resolver problemas de instalação.

4. Verifique se o plugin está funcionando tentando importar o módulo mkdocs_jupyter.

5. Inicie o servidor MkDocs para visualizar a documentação.



plugins:
  - mkdocs-jupyter


poetry remove mkdocs-jupyter mkdocs
poetry cache clear mkdocs-jupyter --all
poetry add mkdocs mkdocs-jupyter

poetry run python -c "import mkdocs_jupyter"
poetry run mkdocs serve

