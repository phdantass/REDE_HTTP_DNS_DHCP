# 🌐 Projeto Prático: Simulação e Configuração de Infraestrutura de Rede Local (LAN & WAN)

Este repositório contém a documentação e o arquivo de simulação de uma topologia de rede corporativa completa desenvolvida no **Cisco Packet Tracer**. O projeto foi estruturado para demonstrar a aplicação prática de roteamento, segmentação de endereçamento IP, gerenciamento de serviços fundamentais de rede e comunicação WAN.

---

## 🛠️ Tecnologias e Ferramentas Utilizadas

- **Simulador:** Cisco Packet Tracer
- **Ativos de Rede:** Roteador Cisco 1941, Switches, Servidores e PCs Clientes
- **Serviços:** DHCP, DNS, HTTP, ICMP
- **Roteamento & WAN:** CLI Cisco IOS, Endereçamento IPv4

---

## 📐 Esquema de Endereçamento IP

Para garantir organização, segurança e escalabilidade na sub-rede interna (**192.168.0.0/24**), adotou-se o seguinte planejamento:

| Dispositivo / Serviço | Endereço IP / Prefix | Descrição |
| :--- | :--- | :--- |
| **Gateway Padrão** | `192.168.0.1 /24` | Configurado no Roteador Cisco 1941 (Interface LAN) |
| **Servidores da Rede** | `192.168.0.10` - `192.168.0.12` | Endereços estáticos reservados para serviços centrais |
| **Pool DHCP (Clientes)** | `192.168.0.100` em diante | Range para alocação dinâmica nas estações de trabalho |
| **Interface WAN** | `100.10.2.190` | Conexão de simulação do Provedor/Internet via Cloud |

---

## ⚙️ Serviços e Configurações Implementadas

1. **Roteamento e Configuração via CLI:**
   - Definição de rotas, gateway da LAN e interface de comunicação WAN no Roteador Cisco 1941.

2. **Servidor DHCP (`192.168.0.10`):**
   - Automação da entrega de IP, Máscara de Sub-rede, Gateway Padrão e DNS para todas as estações de trabalho a partir do IP `.100`.

3. **Servidor HTTP (`192.168.0.11`):**
   - Hospedagem do portal web interno e documentação do ambiente corporativo.

4. **Servidor DNS (`192.168.0.12`):**
   - Configuração de **Registro A** apontando o domínio personalizado `www.pedroisaias.com.br` diretamente para o IP da aplicação web (`192.168.0.11`).

---

## 🧪 Validação e Testes Práticos

- **Conectividade Física e Lógica:** Testes de tráfego ICMP (`ping`) realizados entre os PCs clientes, gateway e servidores com 100% de êxito.
- **Resolução de Nomes e Acesso Web:** Validação do fluxo de navegação completo. As estações de trabalho obtiveram IP via DHCP, resolveram o domínio via DNS e acessaram a página web interna pelo navegador.

---

## 📌 Aprendizados e Conclusão

O desenvolvimento desta topologia reforçou a importância do planejamento estruturado de endereçamento IP e consolidou conceitos essenciais de arquitetura de redes corporativas, preparação para exames de certificação (como CCNA) e administração de infraestrutura de TI.

---
