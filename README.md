# 🌀 Corte Smart
### Sistema Automatizado de Corte de Plástico Bolha 

O **Corte Smart** é uma solução de automação industrial desenvolvida para otimizar o processo de corte de plástico em rolos. Integrando hardware robusto, controle via aplicativo e princípios da Indústria 4.0, o sistema elimina a imprecisão do corte manual, reduz o desperdício e aumenta a segurança do operador.

---

## 📌 Índice
- [Sobre o Projeto](#-sobre-o-projeto)
- [Problema vs Solução](#-problema-vs-solução)
- [Funcionalidades](#-funcionalidades)
- [Arquitetura Técnica](#-arquitetura-técnica)
- [Metodologia e Testes](#-metodologia-e-testes)
- [Equipe](#-equipe)

---

## 📖 Sobre o Projeto
Desenvolvido na unidade **SENAI Cataguases**, o projeto une as áreas de Desenvolvimento de Sistemas e Gestão Industrial para criar uma máquina capaz de realizar cortes precisos com tolerância inferior a 1mm, totalmente controlada via interface digital.

## 🚀 Problema vs Solução

### O Problema
*   **Imprecisão:** Cortes manuais geram dimensões irregulares e desperdício.
*   **Baixa Produtividade:** Processo lento e dependente de esforço humano repetitivo.
*   **Insegurança:** Exposição dos operadores a lâminas e ferramentas cortantes.
*   **Falta de Dados:** Impossibilidade de rastreamento em tempo real.

### A Solução (Corte Smart)
*   **Automação:** Ciclo completo de avanço, medição e corte sem intervenção manual.
*   **Precisão:** Uso de motor de passo e encoder para garantir medidas exatas.
*   **Conectividade:** Controle total por aplicativo via Bluetooth ou Wi-Fi (IoT).
*   **Segurança:** Sensores de presença e botões de emergência integrados.

---

## ✨ Funcionalidades
- [x] **Configuração Remota:** Definição de comprimento (metros) e quantidade via App.
- [x] **Precisão Milimétrica:** Controle de tração via Motor NEMA 17.
- [x] **Segurança NR-12:** Parada imediata ao abrir a tampa ou acionar emergência.
- [x] **Sistema de Receitas:** Salve e carregue configurações de corte pré-definidas.
- [x] **Comunicação JSON:** Troca de dados ágil entre o ESP32 e a interface.

---

## 🛠 Arquitetura Técnica

### Hardware
*   **Microcontrolador:** ESP32 (Wi-Fi + Bluetooth).
*   **Atuadores:** Motor de passo NEMA 17 + Driver A4988 e Servo Motor (Guilhotina).
*   **Sensores:** Encoder rotativo incremental, sensor de presença infravermelho e fim de curso.
*   **Estrutura:** MDF, perfil de alumínio e rolos de tração emborrachados.

### Software
*   **Firmware:** Linguagem C++ (Arduino/ESP-IDF).
*   **Aplicativo:** Desenvolvido para Mobile/Desktop (Interface de controle e logs).
*   **Protocolo:** Comunicação sem fio via JSON.

---

## 📊 Metodologia e Testes
O projeto seguiu uma abordagem iterativa de prototipagem, resultando nos seguintes indicadores:
*   **Precisão de Corte:** Desvio máximo de apenas ±0,8 mm.
*   **Latência de Comando:** < 50ms via Bluetooth.
*   **Tempo de Resposta (Emergência):** Parada total em menos de 200ms.

---

## 👥 Equipe
**SENAI Unidade Cataguases** | Instrutora: *Juliana Sertore de Souza*


| Aluno | Curso | Função |
| :--- | :--- | :--- |
| **Nicoly Rodrigues** | Técnico em Dev. de Sistemas | Construção do site e protótipo |
| **Vitor José** | Técnico em Dev. de Sistemas | Construção do site e protótipo |
| **Samuel Meigre** | Gestão Industrial | Construção do protótipo |
| **Rebeka Fernandes** | Gestão Industrial | Construção do protótipo |

---
*Este projeto é um protótipo funcional para fins educacionais e de demonstração de viabilidade técnica em automação industrial.*
