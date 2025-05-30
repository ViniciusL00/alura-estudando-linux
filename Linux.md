# 📘 Revisão de Aula: Fundamentos de Administração de Sistemas Linux e Computação em Nuvem

## 📂 1. Navegação no Terminal Linux

O terminal é uma interface poderosa que permite interagir diretamente com o sistema operacional. Conhecer seus comandos básicos é essencial para qualquer profissional de tecnologia.

### Comandos essenciais:

- `pwd` – Exibe o diretório atual.
- `ls` – Lista os arquivos e diretórios.
- `cd nome-do-diretório` – Acessa um diretório específico.
- `cd ..` – Retorna ao diretório anterior.
- `clear` – Limpa a tela do terminal.

#### Exemplo prático:

```bash
cd Documentos/projeto
ls
```

---

## 📁 2. Organização de Projetos

Manter uma estrutura de diretórios bem definida melhora a produtividade e facilita a colaboração em equipe.

### Boas práticas:

- Criar diretórios específicos para cada tipo de arquivo.
- Nomear arquivos de maneira clara e padronizada.
- Utilizar arquivos como `README.md` para documentar o projeto.

### Estrutura recomendada:

```
meu-projeto/
├── src/
│   ├── index.html
│   ├── style.css
│   └── script.js
├── assets/
│   └── imagens/
└── README.md
```

#### Exemplo prático:

```bash
mkdir meu-projeto
cd meu-projeto
mkdir src assets
touch src/index.html
```

---

## 🛠️ 3. Tarefas Administrativas no Linux

Para administrar um sistema Linux, é necessário compreender e executar tarefas com privilégios de superusuário.

### Comandos comuns:

- `sudo` – Executa comandos como administrador.
- `apt update` – Atualiza a lista de pacotes (distribuições baseadas em Debian).
- `apt upgrade` – Atualiza os pacotes instalados.
- `adduser nome` – Cria um novo usuário no sistema.
- `chmod` e `chown` – Gerenciam permissões e propriedade de arquivos.

#### Exemplo prático:

```bash
sudo apt update && sudo apt upgrade -y
sudo adduser novo-usuario
```

---

## ☁️ 4. Criação e Acesso a Máquinas Virtuais (VMs) na Nuvem via SSH

Com a expansão da computação em nuvem, é fundamental saber como criar e acessar máquinas virtuais de forma remota.

### Etapas principais:

1. Criar uma VM em uma plataforma de nuvem (como AWS, Google Cloud, Azure ou Oracle Cloud).
2. Configurar o IP público e liberar a porta 22 (SSH) no firewall.
3. Acessar a VM via terminal usando o protocolo SSH.

### Comando para acesso remoto via SSH:

```bash
ssh usuario@ip-da-vm
```

### Com chave privada (.pem):

```bash
ssh -i "minha-chave.pem" usuario@ip-da-vm
```

---

## 🧠 Dica complementar:

Para manter um processo rodando mesmo após o encerramento da sessão SSH:

```bash
nohup comando &
```

Alternativamente, utilize ferramentas como `tmux` ou `screen` para sessões persistentes.

---

## ✅ Conclusão

- Navegar e utilizar o terminal Linux com eficiência.
- Estruturar e organizar projetos de forma lógica e funcional.
- Realizar tarefas administrativas utilizando permissões de superusuário.
- Criar, configurar e acessar máquinas virtuais na nuvem com segurança.

---

# 🐧 Revisão de Aula: Terminal Linux e Estrutura de Diretórios

## 💻 Comandos Básicos do Terminal

- `git clone <url>`: Clona um repositório do GitHub para seu diretório atual.
- `ls`: Lista arquivos e pastas no diretório atual.
- `cd ./diretorio`: Entra no diretório especificado.
- `clear`: Limpa a tela do terminal.
- `pwd`: Mostra o caminho completo (absoluto) do diretório atual.
- `cd`: Volta para o diretório pessoal do usuário (home).
- `cd /`: Vai para o diretório raiz (root do sistema).
- `cd ./root`: Acessa o diretório `root`, mas só funciona se estiver dentro do caminho correto. ⚠️ Obs: o verdadeiro diretório do superusuário é `/root`.
- `cd ./usr`: Acessa o diretório `usr` relativo ao local atual. Se você estiver na raiz (`/`), vai para `/usr`.

## 🗂️ Estrutura de Diretórios do Linux

- `/bin` → Binários essenciais para uso do sistema e comandos básicos.
- `/boot` → Arquivos de inicialização do sistema, incluindo o kernel.
- `/dev` → Representações de dispositivos de hardware (como HDs, terminais, etc).
- `/etc` → Arquivos de configuração do sistema.
- `/home` → Diretórios pessoais dos usuários.
- `/lib` → Bibliotecas essenciais para binários em `/bin` e `/sbin`.
- `/media` → Ponto de montagem para mídias removíveis (pen drives, HDs externos).
- `/mnt` → Ponto de montagem temporário para sistemas de arquivos.
- `/opt` → Softwares adicionais não incluídos no sistema padrão.
- `/proc` → Sistema de arquivos virtual com info sobre processos e kernel.
- `/root` → Diretório pessoal do superusuário (root).
- `/run` → Informações temporárias do sistema desde a última inicialização.
- `/sbin` → Binários para administração e recuperação do sistema.
- `/srv` → Dados de serviços oferecidos pelo sistema (como servidores web).
- `/sys` → Informações e interface com o kernel do sistema.
- `/tmp` → Arquivos temporários criados por programas (limpos no reboot).
- `/usr` → Aplicativos de usuários, bibliotecas e arquivos adicionais.
- `/var` → Dados variáveis, como logs, emails e spools de impressão.

## 🧠 O que é o Kernel?

O **Kernel** é o núcleo do sistema operacional. Ele atua como uma ponte entre o hardware e o software. Suas funções principais incluem:

- Gerenciar recursos (CPU, memória, dispositivos).
- Controlar processos e multitarefa.
- Interagir com drivers e periféricos.

👉 Sem o kernel, o sistema não funciona. É ele quem conversa com a "máquina real".

---

📝 **Resumo Final:** Aprender os comandos e diretórios do Linux é o primeiro passo para se tornar um profissional versátil na área de tecnologia. Dominar o terminal é essencial para devs, sysadmins, e qualquer usuário avançado do sistema.


# 🐧 Revisão de Comandos Essenciais no Terminal Linux

## 📁 Diretórios e Navegação

- `pwd` (📍 *Print Working Directory*): Mostra o caminho completo do diretório atual.
  ```bash
  pwd
  ```

- `ls` (📂 *List*): Lista os arquivos e pastas do diretório atual.
  - Use `ls -a` para mostrar arquivos ocultos (que começam com `.`).
  ```bash
  ls -a
  ```

- `cd` (📂 *Change Directory*): Muda para o diretório especificado.
  ```bash
  cd /projeto
  ```

## 🔐 Permissões de Superusuário

- `sudo` (*SuperUser Do*): Executa comandos com permissões elevadas (root).
  ```bash
  sudo ls /root
  ```

- `sudo -i`: Inicia uma sessão interativa como root. Ideal para executar vários comandos administrativos seguidos.
  ```bash
  sudo -i
  ```

- `sudo su`: Inicia uma sessão como root, mas mantém o ambiente do usuário atual.
  ```bash
  sudo su
  ```

## 📄 Manipulação de Arquivos

- `cat` (*Concatenate*): Exibe o conteúdo de arquivos ou concatena arquivos.
  ```bash
  cat arquivo.txt
  ```

## 🚪 Sessões

- `exit`: Encerra a sessão atual do terminal (inclusive sessões com root).
  ```bash
  exit
  ```

## 🔗 Git

- `git clone`: Faz uma cópia local de um repositório remoto do Git.
  ```bash
  git clone https://github.com/usuario/repositorio.git
  ```

---

📝 **Resumo Final**: Estes comandos são a base para navegar, manipular arquivos, acessar permissões elevadas e usar Git no terminal Linux. Praticar cada um deles é essencial para dominar o ambiente de linha de comando!

# 🗂️ Revisão: Criando Estrutura de Diretórios no Terminal Linux

Nesta aula, aprendemos como criar pastas e arquivos diretamente do terminal. Aqui vai um resumo com exemplos e explicações simples. 🚀

## 📁 Criando Diretórios

- `mkdir <nome>`: Cria um novo diretório (pasta).
  ```bash
  mkdir projeto_python
  ```
  ✅ Cria uma pasta chamada `projeto_python` no diretório atual.

## 📄 Criando Arquivos

- `touch <nome_arquivo>`: Cria um novo arquivo vazio.
  ```bash
  touch projeto_python/projeto_ideias.txt
  ```
  ✅ Cria um arquivo `.txt` chamado `projeto_ideias.txt` dentro da pasta `projeto_python`.

## 👀 Visualizando o Conteúdo de um Arquivo

- `cat <arquivo>`: Exibe o conteúdo de um arquivo no terminal.
  ```bash
  cat projeto_python/projeto_ideias.txt
  ```
  ✅ Mostra o que está escrito dentro do arquivo `.txt` (se houver conteúdo).

## ✍️ Editando Arquivos no Terminal

- `nano <arquivo>`: Abre o editor de texto `nano` para editar arquivos no terminal.
  ```bash
  nano projeto_python/projeto_ideias.txt
  ```
  ✅ Permite escrever ou editar o conteúdo do arquivo diretamente pela linha de comando.

> 💡 Dica: Para salvar e sair do `nano`, use `Ctrl + O` para salvar e `Ctrl + X` para sair.

---

# 📂 Revisão: Movendo Arquivos e Diretórios no Terminal Linux

Nesta aula você aprendeu a mover arquivos e pastas usando o terminal Linux. Aqui vai um resumo prático pra revisar com estilo! 🚀

## 🗂️ Criando Pastas

- `mkdir <nome>`: Cria um diretório novo.
  ```bash
  mkdir ideias

## 📁 Movendo Arquivos

`mv <origem> <destino>`: Move arquivos ou diretórios de um local para outro.

`mv /home/vinic/projeto_phyton/projeto_ideias.txt /home/vinic/projeto_phyton/ideias` 

✅ Move o arquivo projeto_ideias.txt para dentro da pasta ideias.

## 🔍 Listando com Detalhes

`ls -la`: Lista todos os arquivos (inclusive ocultos) com detalhes como permissões, dono, grupo e data de modificação.

`ls -la`

## 📦 Movendo Diretórios

Também é possível mover pastas com `mv`, da mesma forma que arquivos.

`mkdir rascunho`
`mv rascunho /home/vinic/projeto_phyton/ideias`


# 📄 Revisão: Copiando e Renomeando Arquivos e Diretórios no Terminal Linux

Vamos revisar como duplicar arquivos e dar nomes novos para pastas e arquivos direto pelo terminal. 🎯

## 📑 Copiando Arquivos

- `cp <arquivo_origem> <arquivo_destino>`: Cria uma cópia do arquivo.
  ```bash
  cp projeto_ideias.txt projeto_ideias_v1.txt
  ```
  ✅ Cria uma cópia chamada `projeto_ideias_v1.txt` a partir do arquivo `projeto_ideias.txt`.

## ✏️ Renomeando Arquivos ou Diretórios

- `mv <nome_antigo> <nome_novo>`: Também é usado para renomear.
  ```bash
  mv rascunho modelo
  ```
  ✅ Agora o diretório ou arquivo chamado `rascunho` passa a se chamar `modelo`.

---

📝 **Resumo Final**: Com `cp` você faz backups e versões dos seus arquivos. Com `mv`, você reorganiza e renomeia como quiser. Tudo isso direto do terminal! 🧠💻

## 🐧 Comando Essenciais

* `mkdir (Make Directory): Cria novos diretórios. (tilizar o comando mkdir para criar e organizar projetos e diretórios de maneira hierárquica)`

* `touch: Cria um arquivo vazio ou atualiza a data de modificação de um arquivo existente. (Criar e editar arquivos de texto com touch)`

* `nano: Editor de texto no terminal, usado para criar e editar arquivos. (Usar o comando nano para inserir e modificar conteúdos diretamente no terminal de um computador)`

* `mv (Move): Move ou renomeia arquivos e diretórios. (Aplicar o comando mv para movimentar e renomear arquivos e diretórios)`

* `cp (Copy): Copia arquivos e diretórios. (Utilizar o comando cp para criar cópias de arquivos.)`

* `clear: Limpa a tela do terminal, removendo o histórico visível.`

* `ls -l (List Long): Lista arquivos e diretórios com detalhes, incluindo permissões e proprietários. (Usar o comando ls com a opção -l para verificar permissões e obter mais detalhes de itens contidos em um diretório)`

* `ls -al (List All Long): Combina as opções -a e -l, listando todos os arquivos com detalhes.`

---

# 🗑️ Revisão: Removendo Arquivos e Obtendo Informações no Terminal Linux

Nesta aula, você aprendeu como apagar arquivos e diretórios, consultar ajuda no terminal e redirecionar saídas. Bora revisar com estilo! 🚀

## 📘 Acessando Ajuda

- `ls --help`: Mostra todas as opções e flags disponíveis para o comando `ls`.
- `man -k <palavra-chave>`: Mostra uma lista de comandos relacionados à palavra, com descrição resumida.
  ```bash
  man -k copy
  ```

## 🗑️ Removendo Arquivos e Diretórios

- `rm <arquivo>`: Remove arquivos.
- `rmdir <diretório>`: Remove diretórios vazios.
- `rm -r <diretório>`: Remove diretórios e seu conteúdo recursivamente (⚠️ cuidado!).
- `rm -ri <diretório>`: Mesma função do `-r`, mas pede confirmação antes de deletar cada item (🛡️ segurança extra).

## 📤 Redirecionando Saída para Arquivos

- `>`: Sobrescreve um arquivo com a nova saída.
  ```bash
  ls > lista_projeto.txt
  ```
- `>>`: Adiciona conteúdo ao final do arquivo, sem apagar o que já está lá.
  ```bash
  ls >> lista_projeto.txt
  ```

## 💬 Comando echo

- `echo <mensagem>`: Mostra mensagens no terminal.
- Pode ser usado para adicionar textos em arquivos:
  ```bash
  echo projeto_funcional >> lista_projeto.txt
  ```
  ✅ Isso adiciona a linha "projeto_funcional" ao final do arquivo `lista_projeto.txt`.

---

📝 **Resumo Final**: Saber remover arquivos com segurança e redirecionar saídas te ajuda a organizar melhor seus projetos e evitar acidentais desastres! Use `rm -ri` com sabedoria, e `echo` para interações rápidas ou anotações nos seus arquivos! 💣📄💾

# 📚 Revisão Rápida de Gerenciador de Pacotes 🐧

## Gerenciador de Pacotes (APT)
- `sudo apt update` 🔄  
  Atualiza a lista de pacotes disponíveis e suas versões no sistema. Pergunta ao terminal: "Tem atualização aí?"  
  **Precisa de superusuário.**

- `sudo apt upgrade` ⬆️  
  Instala todas as atualizações disponíveis para os pacotes do sistema. Manda: "Agora atualiza tudo, por favor!"  
  **Precisa de superusuário.**

- `sudo apt install pacote` ➕  
  Instala um pacote específico que você quiser. Tipo pedir pro Linux: "Me traz esse programa aí."  
  **Precisa de superusuário.**

- `sudo apt remove pacote` ➖  
  Remove um pacote instalado do sistema. É o “tira esse troço daqui!”  
  **Precisa de superusuário.**

---

# 🔍 Revisão: Analisando Processos e Recursos no Linux com `top` 🖥️🐧

O comando `top` é uma das ferramentas mais úteis do terminal Linux para **monitorar processos em tempo real**. Ele exibe quais programas estão rodando e **quanto de CPU, memória e outros recursos** cada um está usando.

---

## 🚀 Comando Principal

```bash
top
```

Esse comando abre uma interface em tempo real no terminal mostrando os processos em execução.

---

## 🧠 Colunas do `top` – O que significa cada uma?

| Campo        | Significado                                                                 |
|--------------|------------------------------------------------------------------------------|
| **PID**      | Process ID — Identificador único do processo.                               |
| **USER**     | Nome do usuário que iniciou o processo.                                     |
| **PR**       | Prioridade do processo (quanto menor, maior prioridade).                    |
| **NI**       | Valor de "Nice" — influência na prioridade. Valores negativos = mais prioridade. |
| **VIRT**     | Memória virtual usada pelo processo (em KB).                                |
| **RES**      | Memória residente (RAM efetivamente usada).                                 |
| **SHR**      | Memória compartilhada com outros processos.                                 |
| **S**        | Estado do processo: S = sleeping, R = running, Z = zombie, T = stopped.     |
| **%CPU**     | Porcentagem de CPU que o processo está usando.                              |
| **%MEM**     | Porcentagem de RAM que o processo está usando.                              |
| **TIME+**    | Tempo total de CPU usado pelo processo desde o início.                      |
| **COMMAND**  | Comando que iniciou o processo.                                              |

---

## 📊 Atalhos dentro do `top`

- 🔼 **P**: Ordena os processos pelo uso de CPU (de maior para menor).
- 🧠 **M**: Ordena os processos pelo uso de memória RAM.

---

## 🧠 Dica Ninja

Se quiser sair do `top`, basta apertar `q`.

---

## 📌 Resumo

- Use `top` para ver tudo rodando no seu sistema.
- Ordene por CPU com **P** e por memória com **M**.
- Entenda as colunas para saber exatamente o que está consumindo recursos.
- Saber usar o `top` te dá poder de diagnóstico e te transforma num verdadeiro **sysadmin** de respeito. 💪🐧

---

# 🧠 Revisão: Filtrando e Inspecionando Processos no Linux 🖥️🐧

Aprender a filtrar e inspecionar processos é fundamental para manter o controle do sistema Linux. Nesta revisão, vamos entender como usar o comando `ps` e suas variantes para ver o que está acontecendo por trás dos panos.

---

## 🔍 Comando `ps`: Status dos Processos

### 📌 Básico

```bash
ps
```

Exibe os processos ativos no terminal atual (sessão atual).

---

## 🔎 `ps aux`: Visão Geral dos Processos

```bash
ps aux
```

Mostra **todos os processos** do sistema com informações detalhadas.

| Campo     | Descrição                                                |
|-----------|----------------------------------------------------------|
| **VSZ**   | Quantidade de memória virtual usada pelo processo (em KB). |
| **RSS**   | Memória física usada atualmente (Resident Set Size).     |
| **TTY**   | Terminal associado ao processo (se houver).              |
| **STAT**  | Estado atual do processo (ex: S = sleeping, R = running, Z = zombie, T = stopped). |
| **START** | Hora de início do processo.                              |

---

## 🎯 Filtrando processos específicos

- `ps -u root`: Mostra **apenas processos do usuário root**.
- `ps -u vinic`: Mostra **os processos do seu usuário**.
- `ps -C bash`: Filtra os processos **relacionados ao Bash**, o interpretador de comandos.

---

## 🌳 Visualização em Árvore

```bash
pstree
```

Mostra os processos como **uma árvore**, revelando quem iniciou quem. Ideal para ver hierarquias e relações entre os processos.

---

## 🧠 Comandos avançados

### 🔥 Ordenar por uso de memória

```bash
ps aux --sort=-%mem
```

- Mostra todos os processos **ordenados do que mais consome memória para o que menos consome**.
- O `--sort=-%mem` significa "ordenar decrescentemente por uso de memória".

### 🎯 Mostrar só os 10 maiores consumidores de RAM

```bash
ps aux --sort=-%mem | head -n 11
```

- Esse comando combina dois comandos:
  - `ps aux --sort=-%mem`: Ordena processos por memória.
  - `head -n 11`: Mostra apenas as 11 primeiras linhas (a primeira é o cabeçalho, as 10 seguintes são os processos com maior consumo de memória).

---

## ✅ Resumo Rápido

| Comando                            | O que faz 📌                                    |
|-----------------------------------|-------------------------------------------------|
| `ps aux`                          | Mostra todos os processos com detalhes          |
| `ps -u nome_usuario`              | Filtra processos por usuário                    |
| `ps -C nome_do_programa`          | Filtra processos por nome de programa           |
| `pstree`                          | Mostra os processos em formato de árvore        |
| `ps aux --sort=-%mem`             | Ordena processos do que mais consome memória    |
| `ps aux --sort=-%mem | head -n 11`| Mostra só os top 10 consumidores de RAM         |

---

# 🧠 Revisão: Filtrando e Ordenando Saída de Comandos no Terminal Linux 🖥️🐧

Ao utilizar o terminal, muitas vezes a **saída dos comandos pode ser extensa**, dificultando a análise direta. Felizmente, podemos **filtrar, ordenar e exibir** apenas as partes relevantes usando alguns comandos.
---

## 🔗 Pipe (`|`): Encadeamento de Comandos

```bash
comando1 | comando2
```

- O **pipe (`|`)** envia a **saída do primeiro comando** como **entrada para o segundo**.
- Permite **encadear comandos** para refinar o resultado final.

---

## 🔍 `grep`: Filtro por Padrão

```bash
ps aux | grep firefox
```

- O comando `grep` **busca padrões de texto**.
- No exemplo acima, ele filtra a lista de processos para mostrar **apenas os que contêm "firefox"**.

---

## 📋 `head` e `tail`: Visualizar Linhas Específicas

### 👀 `head`

```bash
head -n 5 arquivo.txt
```

- Exibe as **primeiras 5 linhas** do arquivo ou da saída de um comando.
- Padrão: 10 linhas se não usar `-n`.

### 👇 `tail`

```bash
tail -n 5 arquivo.txt
```

- Exibe as **últimas 5 linhas**.
- Também exibe 10 por padrão sem `-n`.

---

## 🧮 `sort`: Ordenar a Saída

### 🔥 Ordenar por Uso de CPU

```bash
ps aux --sort=-%CPU
```

- Ordena os processos com **base no uso da CPU**.
- O sinal **`-`** indica **ordem decrescente** (do maior para o menor).

---

- 🔢 **Ordenar por uso de CPU em ordem crescente**:
  ```bash
  ps aux --sort=%CPU

---

## ✅ Resumo Rápido

| Comando                             | O que faz 📌                                        |
|-------------------------------------|-----------------------------------------------------|
| `comando1 | comando2`               | Usa a saída de um como entrada de outro             |
| `grep padrão`                       | Filtra linhas que contêm o padrão                   |
| `head -n X`                         | Mostra as X primeiras linhas                        |
| `tail -n X`                         | Mostra as X últimas linhas                          |
| `sort`                              | Ordena linhas de texto                              |
| `ps aux --sort=-%CPU`               | Ordena processos do maior para o menor uso de CPU   |
| `ps aux --sort=%CPU`                | Ordena processos do menor para o maior uso de CPU   |

---

# 🧠 Revisão: Controle de Processos no Linux 🖥️

Aprender a controlar processos é essencial para gerenciar corretamente o que está rodando no seu sistema. Aqui vão os principais comandos e suas funções 👇

---

## 🧨 `kill`: Encerra processos manualmente

### ✅ Encerramento suave
```bash
kill [PID]
```
- Envia o sinal **SIGTERM**, pedindo para o processo encerrar de forma segura.

### ❌ Encerramento forçado
```bash
kill -9 [PID]
```
- Envia o sinal **SIGKILL**, forçando o processo a encerrar **imediatamente**, sem chance de salvar dados.

### ⏸️ Pausar processo
```bash
kill -STOP [PID]
```
- Envia o sinal **SIGSTOP**, pausando o processo sem encerrar.

### ▶️ Retomar processo pausado
```bash
kill -CONT [PID]
```
- Envia o sinal **SIGCONT**, retomando o processo pausado.

---

## 🔎 `pkill`: Encerra processo pelo nome
```bash
pkill nome_do_processo
```
- Encerra todos os processos que tenham o nome indicado. Ex: `pkill firefox`

---

## 🚫 `killall`: Encerra todos processos com mesmo nome
```bash
killall nome_do_processo
```
- Mata todos os processos com o nome exato informado. Útil para encerrar tudo de uma vez.

---

## 🧬 `pstree`: Visualiza processos como uma árvore 🌳
```bash
pstree
```
- Mostra processos em forma de árvore, destacando quem criou quem (pai e filhos).

---

## 📌 Extras úteis (não explicados antes):

### 🔍 `ps -p [PID]`
- Mostra informações detalhadas de **um processo específico**.

### 🔍 `ps -C [comando]`
- Filtra os processos que rodam um **comando específico**, ex: `ps -C bash`

---

💡 **Dica de ouro**: Use `kill` para agir com precisão e `pkill` ou `killall` para resolver rapidamente processos travados ou em massa.

---
