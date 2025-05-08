# 🔐 **Auditoria de Segurança Terminal Pura**

Este script em shell é uma ferramenta simples e eficaz para auditoria de segurança em alvos (IPs ou domínios), totalmente via terminal, sem dependência de interfaces gráficas. É ideal para pentesters, sysadmins e entusiastas de segurança que desejam realizar varreduras rápidas e leves em ambientes com recursos limitados ou onde GUIs não são viáveis.

## 🚀 **Objetivo**

O objetivo deste script é realizar varreduras e coletas iniciais de dados de segurança em alvos, como servidores, sites e redes, de maneira eficiente e rápida, utilizando ferramentas robustas e já consagradas do mundo da segurança, tudo via terminal.

## 📦 **Ferramentas Utilizadas**

* `nmap`: Realiza varreduras de portas e identificação de serviços.
* `whois`: Consulta de informações do domínio (registrante, dados de DNS, etc.).
* `dig`: Realiza consultas DNS detalhadas.
* `tcpdump`: Captura e analisa pacotes de rede.
* `curl`: Coleta conteúdo HTTP(S) de páginas web.
* `strings` e `xxd`: Ferramentas para análise de arquivos binários.
* `nikto`: Scanner de vulnerabilidades web.
* `dirb`: Força bruta de diretórios web.
* `arp-scan`: Detecta dispositivos na rede local.
* `netcat`: Ferramenta para testes de conectividade de rede.
* `lynis`: Auditoria de segurança do sistema local.
* `chkrootkit` / `rkhunter`: Ferramentas para detectar rootkits.
* `hydra` / `wfuzz`: Força bruta e fuzzing (comentados por padrão).

## ⚡ **Instalação e Uso**

### Requisitos

* Sistema operacional baseado em Debian/Ubuntu (Kali, Parrot, Ubuntu, etc.)
* Conexão com internet e permissões de `sudo` ou `root`
* Ferramentas de auditoria já configuradas (instalação automática incluída no script)

### Passos para executar

1. **Clone o repositório:**

   ```bash
   git clone https://github.com/seuusuario/auditoria-terminal-pura.git
   cd auditoria-terminal-pura
   ```

2. **Torne o script executável:**

   ```bash
   chmod +x auditoria.sh
   ```

3. **Execute o script:**

   Passe o IP ou domínio do alvo como argumento.

   ```bash
   ./auditoria.sh <IP-ou-domínio>
   ```

   Exemplo:

   ```bash
   ./auditoria.sh 192.168.0.1
   ```

   Os resultados serão salvos automaticamente em arquivos `.txt`, com um arquivo principal de resumo chamado `resultadosX.txt`.

### Detalhes dos Resultados

* **`nmap_results.txt`**: Saída da varredura de portas.
* **`capture.pcap`**: Pacotes capturados durante o uso do `tcpdump`.
* **`dig_results.txt`**: Resultado da consulta DNS.
* **`strings_output.txt` e `xxd_output.txt`**: Análise de conteúdo binário.
* **`nikto_results.txt`**: Relatório de vulnerabilidades web.
* **`lynis_audit.txt`**: Relatório da auditoria de segurança do sistema.
* **`chkrootkit.log`** / **`rkhunter.log`**: Logs da detecção de rootkits.

---

## ⚠️ **Aviso de Uso Responsável**

Este script é **apenas para fins educacionais e em ambientes autorizados**. A realização de auditorias de segurança sem permissão em sistemas que não são de sua propriedade ou para os quais você não tem autorização pode ser **ilegal** e sujeitá-lo a penalidades. **Use com responsabilidade** e sempre obtenha permissão expressa antes de testar qualquer sistema que não seja seu.

---

## 🧰 **Requisitos**

O script automaticamente instala todas as dependências necessárias. Caso precise instalar manualmente, use:

```bash
sudo apt update
sudo apt install -y nmap whois tcpdump curl nikto dirb arp-scan lynis chkrootkit rkhunter
```

Para ferramentas como `hydra` ou `wfuzz`, descomente no script conforme necessário.

---

## 🛠️ **Ferramentas Alternativas ou Comentadas**

O script vem com alguns testes de força bruta e fuzzing (como o `hydra` e `wfuzz`) **comentados**. Esses testes devem ser usados **com cautela**, apenas em sistemas onde você tem permissão explícita para realizar testes de segurança.

---

## 🧑‍💻 **Autor**

Feito por [Tolv Carmine Herlitz](https://github.com/seuusuario).

Este script é de uso livre. Sinta-se à vontade para modificar e compartilhar, mas lembre-se de sempre **agir com ética e responsabilidade**.

---
---

## 🔒 **Licença**

Este projeto é licenciado sob a Licença MIT - veja o arquivo [LICENSE](LICENSE) para mais detalhes.

