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

📝 **Resumo Final:** Aprender os comandos e diretórios do Linux é o primeiro passo para se tornar um profissional versátil na área de tecnologia. Dominar o terminal é essencial para devs, sysadmins, e qualquer usuário avançado do sistema.+