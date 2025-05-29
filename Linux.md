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