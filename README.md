
<p align="center">
  <img width="200" style="text-align: center"  height="200" alt="image" src="https://github.com/user-attachments/assets/3045c2e9-b55c-47fa-851f-15289f1beac3" />
</p>

 # FireVision


🔥 FireVision

Repositório do trabalho da disciplina de Projeto Integrado de Computação I (PIC I)
Curso de Engenharia de Computação – Universidade Federal do Espírito Santo (UFES)

👨‍💻 Trabalho desenvolvido por

Daniel Silva Braz

João Vitor Coimbra Silva

Thiago Messias Martinelli

📑 Sumário

Resumo

Introdução

Embasamento Teórico

Materiais e Metodologia

Estratégia de Codificação

Resultados e Discussão

Fluxogramas e Diagramas Técnicos

Conclusão

Referências Bibliográficas

1. Resumo

Os incêndios representam uma das principais ameaças à segurança humana e ambiental, especialmente em áreas urbanas e florestais. Nesse contexto, este projeto apresenta o desenvolvimento do FireVision, um robô móvel inteligente voltado ao combate inicial a incêndios em pequena escala.

O sistema é capaz de se locomover em ambientes internos, detectar focos de fogo por meio de sensores de chama, extinguir automaticamente o incêndio utilizando um sistema de bombeamento de água e operar de forma remota por meio de um aplicativo móvel via comunicação sem fio. O projeto busca reduzir riscos à vida humana, otimizar o tempo de resposta em emergências e promover o uso da robótica e automação como ferramentas de apoio à segurança pública e ambiental.

Palavras-chave: Robótica móvel; Combate a incêndios; Automação; Sistemas embarcados; IoT.

2. Introdução

Incêndios são responsáveis por grandes prejuízos sociais, econômicos e ambientais, além de representarem um risco direto à vida humana. No Brasil, episódios recorrentes de queimadas e incêndios estruturais evidenciam a necessidade de soluções tecnológicas capazes de auxiliar no combate rápido e seguro dessas ocorrências.

Tradicionalmente, o combate a incêndios depende fortemente da atuação humana, expondo bombeiros e equipes de resgate a ambientes extremamente perigosos. Diante desse cenário, o uso de robôs móveis surge como uma alternativa viável para atuar em situações de risco, especialmente em estágios iniciais do incêndio.

O projeto FireVision tem como objetivo desenvolver um robô inteligente capaz de detectar focos de incêndio, extingui-los automaticamente e permitir controle remoto, reduzindo a exposição humana ao perigo e contribuindo para ações preventivas e corretivas.

3. Embasamento Teórico
3.1 Robótica Móvel

A robótica móvel estuda sistemas robóticos capazes de se locomover de forma autônoma ou semiautônoma em diferentes ambientes. Esses sistemas utilizam motores, sensores e unidades de processamento para realizar navegação, controle e tomada de decisão.

3.2 Sensores de Incêndio

Sensores de chama operam a partir da detecção de radiação infravermelha emitida pelo fogo. Esses sensores são amplamente utilizados em sistemas de detecção precoce de incêndios devido à sua rápida resposta e baixo custo.

3.3 Internet das Coisas (IoT)

A Internet das Coisas possibilita a comunicação entre dispositivos físicos por meio de redes sem fio. No projeto FireVision, essa tecnologia é empregada para permitir o controle remoto do robô por meio de um aplicativo móvel.

4. Materiais e Metodologia
4.1 Materiais Utilizados

ESP32 (microcontrolador com Wi-Fi e Bluetooth);

Sensores de chama (3 unidades);

Motores DC (4 unidades);

Ponte H L298N;

Bomba d’água com relé;

Servomotor;

Rodas e estrutura mecânica;

Bateria Li-ion 7,4 V – 3200 mAh;

Cabos e resistores.

4.2 Metodologia

O desenvolvimento do projeto seguiu as seguintes etapas:

Definição dos requisitos do sistema;

Seleção e testes dos componentes eletrônicos;

Montagem da estrutura mecânica;

Integração do sistema eletrônico;

Desenvolvimento do firmware do microcontrolador;

Implementação da comunicação com o aplicativo móvel;

Testes em ambiente controlado.

5. Estratégia de Codificação

A estratégia de codificação adotada priorizou:

Uso de PWM para controle de velocidade dos motores;

Utilização da função millis() ao invés de delay(), garantindo execução não bloqueante;

Prioridade do modo automático, com acionamento do modo manual apenas quando não houver detecção de chamas;

Organização modular do código, facilitando manutenção e expansão futura.

6. Resultados e Discussão

Os testes realizados demonstraram que o robô é capaz de se locomover adequadamente pelo ambiente, detectar focos de incêndio e acionar o sistema de extinção de forma automática. O controle manual mostrou-se eficiente em situações onde não havia detecção de chamas.

Entretanto, foram observadas limitações relacionadas à autonomia energética e à precisão dos sensores em ambientes com muita iluminação externa, indicando a necessidade de ajustes futuros.

7. Fluxogramas e Diagramas Técnicos
7.1 Fluxograma Geral de Funcionamento
flowchart TD
    A[Início] --> B[Inicialização do ESP32]
    B --> C[Leitura dos sensores]
    C --> D{Chama detectada?}

    D -- Sim --> E[Modo automático]
    E --> F[Mover até a chama]
    F --> G[Acionar bomba]
    G --> H{Chama extinta?}
    H -- Não --> G
    H -- Sim --> C

    D -- Não --> I{Controle manual ativo?}
    I -- Sim --> J[Executar comandos]
    I -- Não --> C


Figura 1 – Fluxograma geral de funcionamento do sistema FireVision.

7.2 Fluxograma de Detecção e Combate
flowchart TD
    A[Sensor de chama] --> B{Fogo detectado?}
    B -- Sim --> C[Ajustar direção]
    C --> D[Ativar bomba]
    D --> E{Ainda há fogo?}
    E -- Sim --> D
    E -- Não --> A
    B -- Não --> A


Figura 2 – Fluxograma do sistema de combate a incêndio.

7.3 Diagrama de Blocos do Sistema
Sensores de chama ──▶ ESP32 ──▶ Ponte H ──▶ Motores
                         │
                         ├──▶ Relé ──▶ Bomba d'água
                         └──▶ Wi-Fi ──▶ Aplicativo móvel


Figura 3 – Diagrama de blocos do sistema eletrônico.

7.4 Diagrama de Estados
stateDiagram-v2
    [*] --> Inicializacao
    Inicializacao --> Monitoramento
    Monitoramento --> Combate : Fogo detectado
    Monitoramento --> Manual : Sem fogo
    Combate --> Monitoramento : Fogo extinto
    Manual --> Monitoramento : Sem comandos


Figura 4 – Diagrama de estados do robô FireVision.

8. Conclusão

O projeto FireVision demonstrou ser uma solução viável e inovadora para o combate inicial a incêndios em pequena escala. A integração entre robótica móvel, sensores e sistemas embarcados permitiu o desenvolvimento de um robô funcional, capaz de operar de forma autônoma ou manual.

Como trabalhos futuros, sugere-se a melhoria da autonomia energética, a inclusão de novos sensores e a realização de testes em ambientes mais complexos.

9. Referências Bibliográficas

CRAIG, J. J. Introduction to Robotics: Mechanics and Control. Pearson.

SIEGWART, R.; NOURBAKHSH, I. Introduction to Autonomous Mobile Robots. MIT Press.

ESPRESSIF SYSTEMS. ESP32 Technical Reference Manual.

IEEE. Standards for Robotics and Automation.
