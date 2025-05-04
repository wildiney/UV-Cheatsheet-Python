# 🧪 uv Cheatsheet

`uv` é um gerenciador de pacotes e ambientes para Python, escrito em Rust, que oferece uma solução unificada para gerenciamento de dependências, ambientes virtuais e ferramentas de desenvolvimento. Ele substitui ferramentas como `pip`, `virtualenv`, `pipx`, `poetry` e `pyenv`, proporcionando uma experiência moderna e eficiente.

---

## 📦 Gerenciamento de Pacotes

| Comando                      | Descrição                                           |
|------------------------------|-----------------------------------------------------|
| `uv pip install <pacote>`    | Instala pacotes no ambiente atual (semelhante ao pip) |
| `uv pip uninstall <pacote>`  | Remove um pacote                                    |
| `uv pip list`                | Lista todos os pacotes instalados                   |
| `uv pip freeze`              | Lista pacotes e versões instalados (como `pip freeze`) |

---

## 🛠️ Gerenciamento de Ferramentas Globais com `uv tool`

`uv tool` permite instalar e gerenciar ferramentas de linha de comando baseadas em Python em ambientes isolados, semelhantes ao `pipx`.

### Instalar uma ferramenta globalmente

`uv tool install <ferramenta>`

**Exemplo:**

`uv tool install ruff`

### Instalar múltiplas ferramentas

Atualmente, o comando `uv tool install` aceita apenas **um pacote por vez**. Portanto, para instalar várias ferramentas, execute o comando separadamente para cada uma delas:

`uv tool install ruff`

`uv tool install black`

`uv tool install mypy`

`uv tool install isort`

### Executar uma ferramenta instalada

`uv tool run <ferramenta> [args]`

**Exemplo:**

`uv tool run black --check .`

### Listar ferramentas instaladas

`uv tool list`

### Atualizar uma ferramenta

`uv tool upgrade <ferramenta>`

**Exemplo:**

`uv tool upgrade ruff`

### Remover uma ferramenta

`uv tool uninstall <ferramenta>`

**Exemplo:**

`uv tool uninstall mypy`

---

## ⚡ Execução Temporária de Ferramentas com `uvx`

`uvx` é um atalho para `uv tool run`, permitindo executar ferramentas sem instalá-las permanentemente.

**Exemplo:**

`uvx ruff check .`

Você também pode especificar versões específicas:

`uvx ruff@0.4.0 check .`

---

## 🧪 Ambientes Virtuais

| Comando                    | Descrição                                                  |
|----------------------------|------------------------------------------------------------|
| `uv venv <caminho>`        | Cria um ambiente virtual no caminho especificado           |
| `uv venv --python <versão>`| Cria o ambiente com uma versão específica do Python        |
| `uv venv .venv`            | Convenção para criar um ambiente virtual local na pasta do projeto |

---

## 🐍 Execução de Scripts

| Comando                             | Descrição                                 |
|-------------------------------------|-------------------------------------------|
| `uv run <script.py>`                | Executa um script Python com isolamento   |
| `uv run --python <versão> <script>` | Executa o script com uma versão específica do Python |

---

## 📁 Dica: Instalar Ferramentas Globais Comuns

Como o comando `uv tool install` aceita apenas um pacote por vez, instale cada ferramenta separadamente:

`uv tool install ruff`

`uv tool install black`

`uv tool install mypy`

`uv tool install isort`

---

## 📌 Comparativo de Comandos

| Tarefa                            | pip/virtualenv                  | uv                                |
|-----------------------------------|----------------------------------|------------------------------------|
| Criar ambiente virtual            | `python -m venv venv`           | `uv venv venv`                    |
| Instalar pacotes                  | `pip install`                   | `uv pip install`                  |
| Ferramentas globais               | `pipx install`                  | `uv tool install`                 |
| Executar ferramenta sem instalar  | `n/a`                           | `uvx <ferramenta>`                |

---

## 📚 Referências

- Documentação oficial do uv: [docs.astral.sh/uv](https://docs.astral.sh/uv/)
- Repositório no GitHub: [github.com/astral-sh/uv](https://github.com/astral-sh/uv)
- Documentação do Ruff: [docs.astral.sh/ruff](https://docs.astral.sh/ruff/)

---
