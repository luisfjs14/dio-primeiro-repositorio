# 🐙 Introdução Rápida a Git e GitHub

Este guia resume os comandos essenciais do terminal (Shell) e do Git, ideais para iniciar o versionamento de projetos e o uso do GitHub.

---

## 🖥️ Comandos Úteis do Terminal (Shell)

Estes comandos são usados para navegar e gerenciar arquivos e diretórios no seu sistema operacional antes de interagir com o Git.

| Comando | Descrição | Exemplo de Uso |
| :--- | :--- | :--- |
| `mkdir` | **Cria um novo diretório (pasta).** | `mkdir meu-projeto-git` |
| `ls` | **Lista os arquivos e pastas** no diretório atual. | `ls -l` (lista detalhada) |
| `cd` | **Muda o diretório** (entra em uma pasta específica). | `cd meu-projeto-git` |
| `cd ..` | **Retorna ao diretório pai** (retrocede um nível de pasta). | `cd ..` |
| `pwd` | **Imprime o Caminho do Diretório Local** (Mostra onde você está). | `pwd` |
| `cat` | **Exibe o conteúdo de um arquivo** ou é usado para **criar arquivos de texto** rapidamente. | `cat arquivo.txt` |
| `eval` | **Executa argumentos como um comando shell** (raramente usado diretamente no fluxo Git básico). | |

---

## 🔑 Configuração de Acesso (SSH)

O SSH (Secure Shell) é o método mais seguro e prático para se comunicar com o GitHub sem ter que digitar a senha repetidamente.

| Comando | Descrição |
| :--- | :--- |
| `ssh-add id_ed25519` | **Adiciona sua chave SSH privada** (`id_ed25519` é o nome comum da chave mais moderna) ao agente SSH. Isso permite que você se autentique no GitHub de forma segura. |

---

## ⚙️ Comandos Essenciais do Git

O Git é o sistema de controle de versão. Estes comandos gerenciam o projeto *localmente* em sua máquina.

| Comando | Descrição |
| :--- | :--- |
| `git init` | **Inicializa um novo repositório Git** na pasta atual. Isso cria a pasta oculta `.git` onde todo o histórico de versões será armazenado. |
| `git clone [URL]` | **Copia um repositório remoto** (do GitHub, por exemplo) para sua máquina local. |
| `git status` | **Mostra o estado de trabalho** do seu repositório, indicando quais arquivos foram modificados, quais estão prontos para serem comitados (Staged) e quais são novos (Untracked). |
| `git add [arquivo]` | **Adiciona arquivos** modificados ou novos **à Staging Area** (área de preparação), indicando que eles devem ser incluídos no próximo *commit*. |
| `git add .` | **Adiciona todos os arquivos** do diretório atual e subdiretórios à Staging Area. |
| `git add -A` | **Adiciona todas as modificações** (incluindo exclusões) à Staging Area. Funciona de forma semelhante a `git add .` para fins práticos em projetos pequenos. |
| `git commit -m "mensagem"` | **Registra as mudanças** (arquivos na Staging Area) no histórico do repositório local. A mensagem é obrigatória e deve descrever as alterações. |

---

## ☁️ Comandos para o GitHub (Remoto)

Estes comandos sincronizam seu repositório local com o repositório remoto (na nuvem, como o GitHub).

| Comando | Descrição |
| :--- | :--- |
| `git push origin main` ou `git push origin master` | **Envia/Sobe os commits locais** para o repositório remoto (GitHub). <br> • `origin` é o nome padrão do repositório remoto. <br> • `main` ou `master` é o nome da branch principal. |
| `git pull origin main` | **Baixa as alterações** do repositório remoto para o seu repositório local e as mescla. É o oposto do `git push`. |
| `git remote add origin [URL]` | **Adiciona um novo repositório remoto** (como o que você criou no GitHub) ao seu repositório local. |

---

## 💡 Fluxo de Trabalho Básico

Para começar um projeto e enviá-lo ao GitHub:

1.  **Crie a Pasta e Inicialize o Git:**
    ```bash
    mkdir meu-projeto
    cd meu-projeto
    git init
    ```

2.  **Adicione e Comite as Mudanças (Localmente):**
    ```bash
    # Crie seus arquivos aqui
    git add . 
    git commit -m "feat: Estrutura inicial do projeto" 
    ```

3.  **Conecte e Envie para o GitHub (Remoto):**
    ```bash
    # 1. Adiciona o link do seu repositório no GitHub
    git remote add origin [URL_DO_SEU_REPOSITORIO] 
    
    # 2. Envia os commits para a branch principal
    git push -u origin main 
    ```
