1. Visão Geral
O CorteControl é uma interface de controle de última geração (HMI - Human Machine Interface) projetada para sistemas automatizados de corte de materiais flexíveis (plásticos, fitas, cabos). O sistema permite configurar parâmetros de precisão, monitorar a saúde da máquina em tempo real e gerenciar receitas de produção através de uma conexão sem fio (Bluetooth ou Wi-Fi).

2. Tecnologias Utilizadas
Front-end: HTML5, CSS3 (Variáveis CSS, Flexbox, Grid) e JavaScript Vanilla (ES6+).

Design: Estética Dark Industrial inspirada em interfaces de aviação e centros de comando.

Comunicação (Protocolo): Estrutura de dados baseada em JSON para troca de informações com microcontroladores (ESP32/Arduino).

Visualização: Gráficos em tempo real via CSS dinâmico e animações SVG.

3. Funcionalidades Principais
Controle de Lote: Definição de comprimento (metros) e quantidade de peças.

Monitoramento em Tempo Real: Visualização animada do estado da guilhotina, motor e avanço do material.

Gerenciador de Receitas: Salva configurações frequentes para troca rápida de setup (Ex: Bobina Padrão vs. Tiras Curtas).

Dashboard de Produção: Histórico de operações concluídas e métricas de eficiência (uptime, metros totais).

Protocolo de Segurança: Botão de interrupção de emergência e sensores de estado (tampa, travamento, presença).

4. Arquitetura de Implementação (Hardware)
Para que este site controle uma máquina real, a arquitetura recomendada é:

Componentes Sugeridos:
Cérebro: ESP32 (devido ao suporte nativo a Bluetooth Low Energy e Wi-Fi).

Tração: Motor de Passo NEMA 17 + Driver A4988 (garante precisão milimétrica).

Corte: Servo Motor MG996R (alto torque para acionar a lâmina).

Medição: Encoder rotativo acoplado ao rolo de tração (feedback de erro).

5. Protocolo de Comunicação JSON
O aplicativo envia e espera receber dados no seguinte formato:

Comando de Envio (App -> Máquina):

JSON
{
  "cmd": "start",
  "length": 1.50,
  "qty": 10,
  "speed": 60
}
Status de Retorno (Máquina -> App):

JSON
{
  "status": "running",
  "done": 4,
  "voltage": 12.1,
  "sensors": { "cover": "closed", "material": "ok" }
}
6. Como Executar
Desktop: Basta abrir o arquivo cortadora.html em qualquer navegador moderno.

Mobile: O layout é totalmente responsivo. Você pode hospedar o arquivo no GitHub Pages ou em um servidor local e acessar pelo IP no celular.

App Nativo: Este código pode ser encapsulado usando Apache Cordova ou Capacitor para se tornar um aplicativo .apk ou .ipa instalável.

7. Próximos Passos (Roadmap)
[ ] Implementar a biblioteca Web Serial API para conexão via USB direta do navegador.

[ ] Integrar Web Bluetooth API para pareamento direto sem necessidade de app intermediário.

[ ] Adicionar exportação de relatórios de produção em CSV.
