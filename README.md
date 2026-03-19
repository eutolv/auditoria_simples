# 🔐 Auditoria de Segurança — Terminal Puro

Script em shell para **auditoria rápida de segurança em alvos (IP ou domínio)**, totalmente via terminal e sem dependência de interface gráfica.

Projetado para cenários onde você precisa de **velocidade, leveza e automação básica**.

---

## ⚡ O que ele faz

* Varredura de portas e serviços
* Coleta de informações de domínio (WHOIS, DNS)
* Análise de superfície web
* Captura de tráfego de rede
* Auditoria básica do sistema local
* Geração automática de relatórios

Tudo em um único fluxo via terminal.

---

## 🧰 Ferramentas utilizadas

* `nmap` → portas e serviços
* `whois` / `dig` → informações de domínio
* `tcpdump` → captura de pacotes
* `curl` → coleta HTTP
* `nikto` → vulnerabilidades web
* `dirb` → descoberta de diretórios
* `arp-scan` → dispositivos na rede
* `lynis` → auditoria local
* `chkrootkit` / `rkhunter` → rootkits

Extras (desativados por padrão):

* `hydra`, `wfuzz`

---

## ▶️ Como usar

```bash
git clone https://github.com/seuusuario/auditoria-terminal-pura.git
cd auditoria-terminal-pura
chmod +x auditoria.sh
./auditoria.sh <IP-ou-dominio>
```

Exemplo:

```bash
./auditoria.sh 192.168.0.1
```

---

## 📄 Saída

Os resultados são salvos automaticamente em arquivos `.txt`.

Principais arquivos:

* `nmap_results.txt`
* `nikto_results.txt`
* `dig_results.txt`
* `lynis_audit.txt`
* `chkrootkit.log`
* `rkhunter.log`
* `capture.pcap`

Arquivo principal:

* `resultadosX.txt` (resumo geral)

---

## 💡 Quando usar

* Reconhecimento inicial de alvo
* Auditorias rápidas sem setup complexo
* Ambientes sem interface gráfica
* Testes em máquinas com poucos recursos

---

## ⚠️ Uso responsável

Este script deve ser utilizado **apenas em ambientes autorizados**.

Executar auditorias sem permissão pode ser ilegal.

---

## 🔧 Dependências

O script tenta instalar automaticamente as ferramentas necessárias.

Caso precise manualmente:

```bash
sudo apt update
sudo apt install -y nmap whois tcpdump curl nikto dirb arp-scan lynis chkrootkit rkhunter
```

---

## 🧠 Limitações

* Não substitui ferramentas profissionais completas
* Pode gerar grande volume de dados não filtrados
* Depende de ferramentas externas

---

## 👤 Autor

Tolv Carmine Herlitz

---

## 📜 Licença

Este projeto está licenciado sob a Licença MIT. 

---

## 🏛️ Sobre a Legacy Release License (LRL)

Este projeto utiliza MIT para facilitar uso e adoção.

Mas também sou o criador da **Legacy Release License (LRL)** — um modelo de licença baseado em tempo, pensado para dar uma “segunda vida” a softwares após o fim do suporte.

A ideia é simples:
- enquanto o projeto está ativo → controle total  
- quando é abandonado → a comunidade pode manter  
- com o tempo → vira legado aberto  

Se quiser conhecer:

👉 https://github.com/eutolv/legacy-release-license
