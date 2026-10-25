# BDNoSQL 26/27 - Projeto Stack Exchange

Guia rápido para configuração do ambiente de desenvolvimento local.

## Setup do Ambiente (Python)

Vamos usar um virtual environment para isolar as dependências do projeto.

**Criar o ambiente:**

```
python -m venv venv

```

**Ativar o ambiente:**

* Windows: `venv\Scripts\activate`

* Mac/Linux: `source venv/bin/activate`

**Instalar dependências:**

```
pip install -r requirements.txt

```

**Segurança e Variáveis:**
Cria um ficheiro `.env` na raiz do projeto para as credenciais locais das bases de dados. Garante que o `.gitignore` inclui o seguinte antes de fazer o primeiro commit:

```
venv/
.env
__pycache__/
dataset/

```

##  Infraestrutura (Docker)

A stack completa (MongoDB, Neo4j, Qdrant e Redis) está configurada via Docker Compose.

**Levantar os containers (background):**

```
docker-compose up -d

```

**Parar os containers:**

```
docker-compose down

```

**Interfaces de Gestão Locais:**

* Neo4j Browser: http://localhost:7474

* Qdrant Dashboard: http://localhost:6333/dashboard
