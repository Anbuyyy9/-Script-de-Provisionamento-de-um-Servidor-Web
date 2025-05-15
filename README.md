
# 🛠️ Script de Provisionamento de Servidor Web Apache2

Este repositório contém um **script em Shell (bash)** que automatiza a instalação e configuração de um servidor web Apache2 em sistemas Debian-based (como Ubuntu).  
O script realiza atualização do sistema, instalação do Apache2 e unzip, além de baixar e disponibilizar uma aplicação web no diretório padrão do servidor.

---

## 📋 Pré-requisitos

Antes de executar o script, verifique que:

- Você possui permissões de **root** ou usa `sudo`.
- Está rodando em um sistema baseado em Debian (Ubuntu, etc).
- A máquina possui acesso à internet para baixar pacotes e arquivos.

---

## ⚙️ Funcionalidades do Script

1. **Atualização do sistema:**

   ```bash
   apt-get update
   apt-get upgrade -y
   ```

2. **Instalação do Apache2 e unzip:**

   ```bash
   apt-get install apache2 -y
   apt-get install unzip -y
   ```

3. **Download e implantação da aplicação web:**

   ```bash
   cd /tmp
   wget https://github.com/denilsonbonatti/linux-site-dio/archive/refs/heads/main.zip
   unzip main.zip
   cd linux-site-dio-main
   cp -R * /var/www/html/
   ```

---

## 🚀 Como executar

Siga os passos abaixo para executar o script:

1. Clone este repositório:

   ```bash
   git clone https://github.com/Anbuyyy9/Script-de-Provisionamento-de-um-Servidor-Web.git
   cd Script-de-Provisionamento-de-um-Servidor-Web
   ```

2. Dê permissão de execução para o script:

   ```bash
   chmod +x provisionar.sh
   ```

3. Execute o script com privilégios administrativos:

   ```bash
   sudo ./provisionar.sh
   ```

---

## 🌐 Acesso

Após o provisionamento, acesse a aplicação web no navegador usando o IP do seu servidor:

```
http://<IP_DO_SERVIDOR>
```

---

## 🗂️ Estrutura do Projeto

```
/Script-de-Provisionamento-de-um-Servidor-Web
│
├── provisionar.sh    # Script de automação para provisionar o servidor
└── README.md         # Documentação do projeto
```

---

## 👨‍💻 Autor

Criado como parte de estudos e prática em automação e deploy de servidores web.

---

## 📄 Licença

Este projeto está sob a licença MIT — veja o arquivo LICENSE para mais detalhes.
