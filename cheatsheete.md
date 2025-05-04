# 🧪 uv Cheatsheet

`uv` é um gerenciador de pacotes ultra-rápido para Python, com foco em simplicidade e performance.  
Site oficial: <https://github.com/astral-sh/uv>

---

## 📦 Gerenciamento de Pacotes

| Comando                      | Descrição                                           |
|-----------------------------|-----------------------------------------------------|
| `uv pip install <pacote>`   | Instala pacotes no ambiente atual (como pip)       |
| `uv pip uninstall <pacote>` | Remove um pacote                                    |
| `uv pip freeze`             | Lista pacotes e versões instalados (como `pip freeze`) |
| `uv pip list`               | Lista todos os pacotes instalados                  |

---

## 🛠️ `uv tool` – Ferramentas Globais

| Comando                          | Descrição                                              |
|----------------------------------|--------------------------------------------------------|
| `uv tool add <tool>`             | Instala uma ferramenta global (ex: `uv tool add ruff`) |
| `uv tool list`                   | Lista ferramentas instaladas com `uv tool`            |
| `uv tool remove <tool>`          | Remove a ferramenta                                    |
| `uv tool update`                 | Atualiza todas as ferramentas                         |
| `uv tool run <tool>`             | Executa uma ferramenta instalada (sem ativar env)     |

---

## 🧪 Ambientes Virtuais

| Comando                    | Descrição                                                  |
|---------------------------|--------------------------------------------------------------|
| `uv venv <path>`          | Cria um ambiente virtual em `<path>`                        |
| `uv venv --python <bin>`  | Cria o ambiente com uma versão específica do Python         |
| `uv venv .venv`           | Convenção para criar um env local na pasta do projeto       |

---

## 🐍 Execução de Scripts

| Comando                     | Descrição                                 |
|----------------------------|---------------------------------------------|
| `uv pip install -r requirements.txt` | Instala pacotes de um arquivo de requisitos |
| `uv run <script.py>`       | Executa um script Python com isolamento     |

---

## 📌 Outras Utilidades

| Comando                  | Descrição                         |
|--------------------------|-----------------------------------|
| `uv sync`                | Instala dependências a partir de `pyproject.toml` |
| `uv --help`              | Mostra ajuda geral                |
| `uv pip --help`          | Ajuda específica para o subcomando `pip` |
| `uv tool --help`         | Ajuda para ferramentas globais    |

---

## 📁 Dica: Instalar Ferramentas Globais Comuns

```bash
uv tool add ruff black mypy isort
