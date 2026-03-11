# Projeto de Infraestrutura de Rede Lógica: PlataformaTech

Este projeto detalha a implementação de uma rede local (LAN) desenvolvida como parte da trilha de aprendizado na plataforma **Hardware Redes Brasil**, sob a orientação do **Professor Alfredo Júnior**. A estrutura foi desenhada para a empresa **PlataformaTech**, utilizando uma topologia estrela de Classe C segmentada para atender a requisitos corporativos de endereçamento e segurança.

## 1. Escopo do Projeto

A rede foi projetada para suportar os seguintes departamentos da **PlataformaTech**:
* **Engenharia**: 24 hosts (20 estações, 2 servidores, 2 impressoras);
* **Compras**: 24 hosts (20 estações, 2 servidores, 2 impressoras);
* **TI Interno**: 24 hosts (20 estações, 2 servidores, 2 impressoras);
* **Infraestrutura**: 24 hosts (20 estações, 2 servidores, 2 impressoras).

### Hardware Utilizado
* **Switches**: 04 x Cisco 2950-24 (um por departamento);
* **Hosts**: Estações de trabalho, Servidores e Impressoras de rede.

> **Nota Técnica**: Para viabilizar o Uplink entre os departamentos utilizando o switch Cisco 2950-24, foi configurada uma porta de tronco (Trunk) em cada switch. Essa configuração permite que o tráfego de múltiplas VLANs transite de forma eficiente e segura entre os ativos de rede.

## 2. Planejamento de Endereçamento IP

Para otimizar o uso do endereçamento Classe C, adotou-se a máscara de sub-rede **CIDR /27** (255.255.255.224), garantindo até 30 endereços válidos por segmento.

| Departamento | Rede | 1º IP Válido | Último IP Válido | Broadcast | Atribuição |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Engenharia** | 192.168.0.0 | 192.168.0.1 | 192.168.0.30 | 192.168.0.31 | Estático |
| **Compras** | 192.168.0.32 | 192.168.0.33 | 192.168.0.62 | 192.168.0.63 | Dinâmico |
| **TI Interno** | 192.168.0.64 | 192.168.0.65 | 192.168.0.94 | 192.168.0.95 | Estático |
| **Infraestrutura** | 192.168.0.96 | 192.168.0.97 | 192.168.0.126 | 192.168.0.127 | Dinâmico |



## 3. Segmentação com VLANs

A rede utiliza segmentação lógica para reduzir domínios de broadcast e aumentar a segurança departamental:

* **VLAN 1 (Portas 1-12)**: Atende 10 estações, 1 servidor e 1 impressora;
* **VLAN 2 (Portas 13-24)**: Atende 10 estações, 1 servidor e 1 impressora.

## 4. Tecnologias Aplicadas
* **Simulação**: Cisco Packet Tracer;
* **Protocolos**: TCP/IP, Ethernet, VLAN (802.1Q), Trunking;
* **Serviços**: DHCP e DNS;
* [cite_start]**Documentação**: Padrão KCS para gestão de conhecimento técnico[cite: 48].

---
*Este projeto foi realizado sob a mentoria do Professor Alfredo Júnior (Hardware Redes Brasil) e serve como portfólio técnico de André Saturnino.*
