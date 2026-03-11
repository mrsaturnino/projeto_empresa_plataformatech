# Projeto de Infraestrutura de Rede Lógica: PlataformaTech

Este projeto detalha a implementação de uma rede local (LAN) para a empresa **PlataformaTech**, desenvolvida no simulador **Cisco Packet Tracer**. O objetivo foi estruturar uma rede segmentada em topologia estrela de Classe C para atender a quatro departamentos distintos com requisitos específicos de endereçamento e segurança.

## 1. Escopo do Projeto

A rede foi projetada para suportar os seguintes departamentos:
* **Engenharia**: 24 hosts (20 estações, 2 servidores, 2 impressoras);
* **Compras**: 24 hosts (20 estações, 2 servidores, 2 impressoras);
* **TI Interno**: 24 hosts (20 estações, 2 servidores, 2 impressoras);
* **Infraestrutura**: 24 hosts (20 estações, 2 servidores, 2 impressoras).

### Hardware Utilizado
* **Switches**: 04 x Cisco 2950-24 (um por departamento);
* **Hosts**: Estações de trabalho, Servidores e Impressoras de rede.

> **Nota Técnica**: Para realizar a interconexão (Uplink) entre os departamentos, foi configurada uma porta de tronco em cada switch, otimizando a comunicação entre as sub-redes.

## 2. Planejamento de Endereçamento IP

Para otimizar o uso dos endereços e suportar os 24 hosts por segmento, foi utilizada a máscara de sub-rede **CIDR /27** (255.255.255.224), que permite até 30 endereços válidos por sub-rede.

| Departamento | Rede | 1º IP Válido | Último IP Válido | Broadcast | Atribuição |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Engenharia** | 192.168.0.0 | 192.168.0.1 | 192.168.0.30 | 192.168.0.31 | Estático |
| **Compras** | 192.168.0.32 | 192.168.0.33 | 192.168.0.62 | 192.168.0.63 | Dinâmico |
| **TI Interno** | 192.168.0.64 | 192.168.0.65 | 192.168.0.94 | 192.168.0.95 | Estático |
| **Infraestrutura** | 192.168.0.96 | 192.168.0.97 | 192.168.0.126 | 192.168.0.127 | Dinâmico |



## 3. Segmentação com VLANs

Cada departamento possui segmentação interna via VLANs para reduzir o domínio de broadcast e aumentar a segurança da rede:

* **VLAN 1 (Portas 1-12)**: 10 estações, 1 servidor e 1 impressora;
* **VLAN 2 (Portas 13-24)**: 10 estações, 1 servidor e 1 impressora.



## 4. Tecnologias e Habilidades Aplicadas

* **Simulação de Redes**: Cisco Packet Tracer;
* **Protocolos**: TCP/IP, Ethernet, VLAN (802.1Q), Trunking;
* **Serviços de Rede**: Configuração de DHCP e DNS;
* **Troubleshooting**: Diagnóstico de conectividade e segmentação lógica.

---
*Projeto desenvolvido como parte do aprimoramento contínuo em Infraestrutura e Redes.*
