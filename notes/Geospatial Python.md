
==Conda-forge== **builds and distributes software packages**, specializing in the hard-to-build or unique packages that often arise in a scientific computing context. Conda-forge is community-driven and community-curated.

# Ambientes (conda/mamba)

**Criar Ambiente**:
```bash
conda create -n nome python=3.12
```
**Ativar**:
```bash
conda activate nome
```
**Instalar pacote**:
```bash
# instala pacte direto do channel (-c) conda-forge
mamba install -c conda-forge numpy

# instala pacote em um ambiente específico (-n envname)
conda install -n myenv numpy
```
**Procurar informações de um pacote**: 
```bash
conda search -c conda-forge numpy --info
```

Utilizar o comando abaixo (Channel específico) quando instalar pacotes geoespaciais. A vantagem é que, normalmente pacotes voltados para SIG, utilizam outros pacotes como dependências. Mamba resolve isso ao instalar tudo que é necessário para um pacote GIS rodar sem conflitos.
`-c conda-forge numpy

**Listar ambientes**:
```bash
conda env list
```

**Listar pacotes**:
```bash
conda list
mamba list
```

**Avaliar a integridade do ambiente**
```bash
conda check
```

**Exportar ambiente (pacotes e versões)**
```bash
# exportando todos os pacotes e versões
conda env export > myenv.yml

# exportando com um nome específico
conda env export -n myenv > newname.yml
```

**Criar ambiente a partir de arquivo**:
```bash
# cria ambiente a partir de um arquivo
conda env create -f enviroment.yml

# criar ambiente com novo nome
conda env create -f environment.yml -n newname 
```

**Remover ambiente**: 
```bash
conda remove -n envname --all
```

# VS Code

### Development Enhancement Extensions

#### Code Quality and Formatting: 
- [Black Formatter](https://marketplace.visualstudio.com/items?itemName=ms-python.black-formatter): Automatic Python code formatting following PEP 8 standards 
- [Pylint](https://marketplace.visualstudio.com/items?itemName=ms-python.pylint): Advanced Python linting for catching errors and enforcing coding standards 
- [autoDocstring](https://marketplace.visualstudio.com/items?itemName=njpwerner.autodocstring): Automatically generates Python docstrings for your functions 
- [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode): Code formatter for JavaScript, JSON, CSS, and more

##### Development Tools: 
- [Docker](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-docker): Docker support for VS CodeDevelopment Tools: 
- [IntelliCode](https://marketplace.visualstudio.com/items?itemName=VisualStudioExptTeam.vscodeintellicode): AI-assisted code completion and suggestions 
- [CodeSnap](https://marketplace.visualstudio.com/items?itemName=adpyke.codesnap): Generate beautiful code screenshots for documentation

#### Git and Collaboration Extensions

##### Version Control: 
- [GitLens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens): Supercharge Git capabilities with blame annotations, history, and more 
- [GitHub Pull Requests](https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-pull-request-github): Manage GitHub pull requests directly in VS Code 
- [GitHub Actions](https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-github-actions): Edit and monitor GitHub Actions workflows

##### AI-Powered Development: 
- [GitHub Copilot](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot): AI pair programmer that suggests code as you type 
- [GitHub Copilot Chat](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot-chat): Conversational AI for coding questions and explanations

#### Documentation Extensions

##### Documentation: 
- [Markdown All in One](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one): Complete Markdown support with preview, shortcuts, and table of contents 
- [Markdown Shortcuts](https://marketplace.visualstudio.com/items?itemName=mdickin.markdown-shortcuts): Quick formatting shortcuts for Markdown documents


# Comandos Essenciais do CMD (Windows)

## 📂 Navegação e Diretórios

| Comando | Descrição |
|---|---|
| `cd [caminho]` | Muda o diretório atual |
| `cd ..` | Sobe um nível na hierarquia |
| `cd \` | Vai para a raiz do disco |
| `dir` | Lista arquivos e pastas do diretório atual |
| `dir /a` | Lista arquivos ocultos também |
| `mkdir [nome]` | Cria uma nova pasta |
| `rmdir [nome]` | Remove uma pasta vazia |
| `rmdir /s /q [nome]` | Remove pasta e todo o conteúdo |

---

## 📄 Gerenciamento de Arquivos

| Comando | Descrição |
|---|---|
| `del [arquivo]` | Deleta um arquivo |
| `del /f [arquivo]` | Força a exclusão |
| `copy [origem] [destino]` | Copia arquivo |
| `move [origem] [destino]` | Move ou renomeia arquivo |
| `ren [nome] [novo nome]` | Renomeia arquivo ou pasta |
| `type [arquivo]` | Exibe conteúdo de um arquivo de texto |
| `echo [texto] > [arquivo]` | Cria/sobrescreve arquivo com texto |
| `echo [texto] >> [arquivo]` | Acrescenta texto a um arquivo |

---

## 🌐 Rede e Diagnósticos

| Comando | Descrição |
|---|---|
| `ipconfig` | Exibe configurações de rede e IP |
| `ipconfig /all` | Detalhes completos de rede |
| `ipconfig /flushdns` | Limpa o cache DNS |
| `ping [endereço]` | Testa conectividade (ex: `ping google.com`) |
| `tracert [endereço]` | Rastreia a rota de rede |
| `netstat -an` | Lista conexões de rede ativas |
| `nslookup [domínio]` | Resolve DNS de um domínio |

---

## 🛠️ Sistema e Manutenção

| Comando | Descrição |
|---|---|
| `sfc /scannow` | Verifica e repara arquivos do sistema |
| `chkdsk C: /f /r` | Verifica erros no disco (requer reinício) |
| `tasklist` | Lista processos em execução |
| `taskkill /IM [processo] /F` | Encerra um processo pelo nome |
| `systeminfo` | Exibe informações detalhadas do sistema |
| `driverquery` | Lista todos os drivers instalados |

---

## ⚡ Desligar e Reiniciar

| Comando | Descrição |
|---|---|
| `shutdown -s -t 0` | Desliga imediatamente |
| `shutdown -r -t 0` | Reinicia imediatamente |
| `shutdown -a` | Cancela um desligamento agendado |

---

## 🔧 Comandos Gerais

| Comando | Descrição |
|---|---|
| `cls` | Limpa a tela do CMD |
| `help` | Lista todos os comandos disponíveis |
| `[comando] /?` | Exibe ajuda de um comando específico |
| `exit` | Fecha o CMD |
| `color [código]` | Muda a cor do CMD (ex: `color 0a` = verde) |

---

## 💡 Dicas Rápidas

- Use **Tab** para autocompletar caminhos e nomes de arquivos
- Use **seta ↑** para navegar pelo histórico de comandos
- Use **Ctrl + C** para cancelar um comando em execução
- Use `|` (pipe) para encadear comandos (ex: `dir | more`)
- Coloque caminhos com espaços entre aspas: `cd "C:\Minha Pasta"`
# Git

Essencialmente, Git é a ferramenta que roda no meu hardware e é responsável por criar um histórico de alterações dos meus códigos.

GitHub é a plataforma online onde fica armazenado esse histórico e, adicionalmente, possui ferramentas que facilitam a colaboração com outros colegas programadores.

Alguns conceitos básicos: 
- **Repository (Repo)**: local onde ficam salvos todos os meus arquivos
- **Commit**: um "save state" do meu projeto. Posso voltar nesse ponto sempre que necessário
- **Main**: versão principal do meu projeto/script. Normalmente é a versão estável.
- **Branch**: Literalmente uma ramificação do código (versão paralela), pode ser algo experimental, em desenvolvimento, instável e que ainda não faz part de "main"
- **Remote**: Uma versão do repositório hospedada em algum servidor (como GitHub, por exemplo)


Working Directory → Staging Area → Local Repository → GitHub 
      (edit)                    (git add)           (git commit)       (git push)

---

Todo o fluxo de trabalho abaixo (Git), ocorre localmente. O repositório criado não tem vínculo com o GitHub, isso é criado depois pelo usuário. 

O comando `git status` exibe o status de todos os arquivos. São exibidas mensagens para arquivos alterados localmente **not staged for commit** e arquivos que foram adicionadas ao **staging > changes to be commited**.

O arquivo que foi alterado localmente no VS code, ainda não está no ambiente intermediário "staging". Nesse ponto, não há nada para fazer commit. Primeiro é preciso utilizar `git add` e designar qual arquivo estará pronto para commit. Sempre que fizer uma alteração nesse mesmo arquivo após o primeiro `git add`, é preciso repetir o comando, se não, somente as alterações que foram feitas num primeiro momento é que serão salvas no momento do commit.

O comando `git diff` exibe o que há de diferente entre o arquivo que está em main (criado após o último commit) e o arquivo ==alterado localmente==. Caso o arquivo vá para staging `git add`, o comando não retorna nada, mas é acusado em git status que houve uma alteração.

![[Pasted image 20260328155008.png]]

| Situação                       | O que aparece                           |
| ------------------------------ | --------------------------------------- |
| Arquivo editado, sem `git add` | `Changes not staged for commit`         |
| Arquivo com `git add` feito    | `Changes to be committed`               |
| Nada editado e staging vazio   | `nothing to commit, working tree clean` |
### Comandos essenciais

**Verificar instalação**
```bash
Check git version
git --version

# Check installation location
where git
```

**Configurar**
```bash
# Replace with your actual name and GitHub email 
git config --global user.name "Your Full Name" 
git config --global user.email "your.github@email.com"

# View all global configuration 
git config --global --list 

# Check specific values 
git config --global user.name git config --global user.email
```

**Criar novo repositório**

```bash
# Navigate to your project folder 
cd ~/my-geo-project 

# Initialize Git repository 
git init 

# Check repository status 
git status
```

**Adicionar arquivos para 'staging area' e verificar mudanças**: 
```bash
# Add specific files 
git add analysis.py

# Add all files in current directory 
git add .

# See status of all files 
git status 

# See detailed changes 
git diff
```

**Commit de mudanças**: 
```bash
# Commit with inline message 
git commit -m "Add rainfall analysis function" 

# Commit all tracked files (skip staging) 
git commit -am "Update visualization parameters"
```

**==Conectando ao GitHub==**:
Usamos o comando abaixo quando temos um repositório local e queremos subir no git hub.
- O repositório na nuvem precisa ter o mesmo nome
- **Não marcar a opção "Add README"**, pois isso pode causar conflito.

```bash
# Add remote repository 
git remote add origin https://github.com/<user-name>/<repo-name>.git
```

|Comando|Função|
|---|---|
|`git init`|Transforma a pasta em repositório Git|
|`git remote add origin`|Liga sua pasta ao repositório no GitHub|
|`git add .`|Prepara todos os arquivos para commit|
|`git commit -m`|Salva um snapshot com mensagem|
|`git push -u origin main`|Envia para o GitHub|

==**Clonando repositório**==:
```bash
git clone https://github.com/b-siani/<repo-name>.git
```

Até aqui, os comandos serviram como save state local (git commit). Para que as alterações fiquem salvas na nuvem do GitHub, usamos os comandos abaixo:

```bash
# Push to GitHub (first time) 
git push -u origin main 

# Push subsequent changes 
git push

# Pull changes from GitHub 
git pull
```

**Basic Branching **

```bash
# Create new branch for experimental feature 
git checkout -b branch-name 

# List all branches 
git branch 

# Switch back to main branch 
git checkout main 

# Merge feature branch into main 
git merge branch-name

# Delete merged branch 
git branch -d satellite-analysis
```

**Visualizando histórico do projeto**

```bash
# Histórico de commits
git log

# Formato compacto
git log --oneline

# Histórico de um arquivo específico 
git log -- data_processing.py
```

**Desfazer commit**
```bash
# Undo last commit but keep changes
git reset --soft HEAD~1
```


# GitHub

Usualmente existem dois workflows

1. Start on GitHub, then clone: 
	1. Create repository on GitHub with README 
	2. Clone to your local machine: `git clone` 
2. Start locally, then push to GitHub: 
	1. Create repository locally: `git init` 
	2. Create matching repository on GitHub 
	3. Connect and push: `git remote add origin <url>` then `git push -u origin main`

```
my-geo-project/
├── README.md
├── .gitignore
├── requirements.txt
├── data/
│   ├── raw/
│   └── processed/
├── src/
│   ├── data_processing.py
│   └── analysis.py
├── notebooks/
│   └── exploratory_analysis.ipynb
└── outputs/
    ├── figures/
    └── results/
```



# Docker

## O que é Docker?

Docker é uma plataforma que permite empacotar e executar aplicações em **ambientes isolados e portáteis** chamados contêineres. Um contêiner inclui tudo que a aplicação precisa: código, dependências e configurações — garantindo que rode igual em qualquer máquina.

> No contexto GIS/Python: a imagem `giswqs/pygis:book` é um exemplo real de ambiente Docker pré-configurado com todas as libs geoespaciais.

---
## Conceitos Fundamentais

| Conceito           | O que é                                                                                         |
| ------------------ | ----------------------------------------------------------------------------------------------- |
| **Imagem**         | Template somente leitura. Define o ambiente (ex: `giswqs/pygis:book`). Criada via `Dockerfile`. |
| **Container**      | Instância em execução de uma imagem. É o processo ativo na memória.                             |
| **Volume**         | Diretório persistente montado no container. Dados sobrevivem ao container ser removido.         |
| **Dockerfile**     | Arquivo de instruções para construir uma imagem customizada.                                    |
| **Registry**       | Repositório de imagens (ex: Docker Hub).                                                        |
| **Docker Compose** | Ferramenta para orquestrar múltiplos containers com um único arquivo `.yml`.                    |

> **Analogia:** Imagem = receita de bolo | Container = bolo assado | Volume = pote para guardar o resultado

---

## Fluxo Básico

Dockerfile → docker build → Imagem → docker run → Container  
↑  
Docker Hub (docker pull)

---
## Comandos — Imagens

```bash
docker pull ubuntu:22.04          # Baixa imagem do Docker Hub
docker images                     # Lista imagens locais
docker build -t minha-imagem .    # Cria imagem a partir do Dockerfile (pasta atual)
docker rmi nome-imagem            # Remove imagem local
docker search pygis               # Busca imagens no Docker Hub
```

---
## Comandos — Containers

```bash
# Criar e iniciar
docker run nome-imagem                          # Cria e inicia container
docker run -it nome-imagem bash                 # Modo interativo com terminal
docker run -d nome-imagem                       # Modo background (detached)
docker run --name meu-container nome-imagem     # Nomeia o container
docker run -p 8888:8888 nome-imagem             # Mapeia porta host:container
docker run -v /pasta/local:/pasta/container nome-imagem  # Monta volume

# Gerenciar
docker start meu-container        # Inicia container parado
docker stop meu-container         # Para container com segurança
docker restart meu-container      # Reinicia container
docker rm meu-container           # Remove container parado
docker rm -f meu-container        # Força remoção de container ativo

# Inspecionar
docker ps                         # Lista containers em execução
docker ps -a                      # Lista todos os containers
docker logs meu-container         # Exibe logs do container
docker inspect meu-container      # Detalhes completos (JSON)
docker stats meu-container        # Uso de CPU/RAM em tempo real
docker top meu-container          # Processos rodando dentro do container

# Executar comandos dentro do container
docker exec -it meu-container bash           # Abre terminal interativo
docker exec meu-container ls /var/           # Executa comando pontual
```

---
## Comandos — Volumes

```bash
docker volume create meu-volume          # Cria volume nomeado
docker volume ls                         # Lista volumes
docker volume inspect meu-volume         # Detalhes do volume
docker volume rm meu-volume             # Remove volume
docker run -v meu-volume:/dados imagem  # Usa volume nomeado no container
```

---
## Comandos — Redes

```bash
docker network ls                                # Lista redes
docker network create minha-rede                # Cria rede
docker network connect minha-rede container     # Conecta container à rede
docker run --network minha-rede nome-imagem     # Inicia já conectado à rede
```

---
## Docker Compose (essencial para pipelines)

```yaml
# docker-compose.yml — exemplo GIS com PostGIS
version: '3.8'
services:
  postgis:
    image: postgis/postgis:15-3.3
    environment:
      POSTGRES_PASSWORD: senha123
    volumes:
      - pgdata:/var/lib/postgresql/data
    ports:
      - "5432:5432"

  jupyter:
    image: giswqs/pygis:book
    ports:
      - "8888:8888"
    volumes:
      - ./notebooks:/home/jovyan/work

volumes:
  pgdata:
```

```bash
docker compose up -d       # Sobe todos os serviços em background
docker compose down        # Para e remove os containers
docker compose logs -f     # Acompanha logs em tempo real
docker compose ps          # Status dos serviços
```

---
## Flags Úteis do `docker run`

| Flag                   | Descrição                                 |
| ---------------------- | ----------------------------------------- |
| `-d`                   | Roda em background (detached)             |
| `-it`                  | Modo interativo com terminal              |
| `-p 8888:8888`         | Mapeia porta local:container              |
| `-v /local:/container` | Monta diretório como volume               |
| `--name`               | Define nome do container                  |
| `--network`            | Conecta a uma rede específica             |
| `-e VAR=valor`         | Define variável de ambiente               |
| `--rm`                 | Remove container automaticamente ao parar |

---
## Limpeza

```bash
docker system prune              # Remove tudo não utilizado (containers, imagens, redes)
docker system prune -a           # Inclui imagens sem container associado
docker rm $(docker ps -a -q)     # Remove todos os containers parados
docker rmi $(docker images -q)   # Remove todas as imagens locais
```

---
## Caso de uso: ambiente PyGIS (do meu estudo)

```bash
# Subir o ambiente do livro do Qiusheng Wu
# Windows CMD
docker run -it --rm -p 8888:8888 -v %cd%:/home/jovyan/work giswqs/pygis:book

# Windows PowerShell
docker run -it --rm -p 8888:8888 -v ${PWD}:/home/jovyan/work giswqs/pygis:book

# Caminho direto 
docker run -it --rm -p 8888:8888 -v C:\Users\Bruno\seus-notebooks:/home/jovyan/work giswqs/pygis:book
```

> Acesse: `http://localhost:8888` para abrir o JupyterLab com todas as libs geoespaciais prontas.


