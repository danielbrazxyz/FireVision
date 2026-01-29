
<p align="center">
  <img width="200" style="text-align: center"  height="200" alt="image" src="https://github.com/user-attachments/assets/3045c2e9-b55c-47fa-851f-15289f1beac3" />
</p>

 # FireVision


Repositório do trabalho da disciplina de PIC 1 do curso de Engenharia de Computação da Universidade Federal do Espírito Santo.

#### Trabalho desenvolvido por:

<p>
Daniel Silva Braz<br>
 João Vitor Coimbra Silva<br>
Thiago Messias Martinelli
</p>





## Sumário
- [Resumo](#resumo)
- [Introdução](#Introdução)
- [Embasamento Teórico](#Embasamento-teórico)
- [Materiais e Metodologia](#Materiais-e-metodologia)
- [Estratégia de Codificação](#Estratégia-de-codificação-do-alfabeto)
- [Resultados e Discussão](#Resultados-e-discussão)
- [Referências Bibliográficas](#Referências-bibliográficas)

---

## Resumo
  <p>Os incêndios representam uma das principais ameaças à segurança humana e ambiental, especialmente em áreas urbanas e florestais. Nesse contexto, este projeto apresenta o desenvolvimento do FIREVISION, um robô móvel inteligente voltado ao combate inicial a incêndios. O sistema é capaz de se locomover em ambientes internos, detectar focos de fogo por meio de sensores específicos, extinguir automaticamente o incêndio e identificar a presença de pessoas utilizando visão computacional. O controle do robô é realizado remotamente por meio de um aplicativo para dispositivos móveis. O projeto busca reduzir riscos à vida humana, otimizar o tempo de resposta em emergências e promover o uso da robótica e automação como ferramentas de apoio à segurança pública e ambiental.

Palavras-chave: Robótica móvel; Combate a incêndios; Visão computacional; Automação; Sistemas embarcados.</p>


## Introdução
<p>Incêndios são responsáveis por grandes prejuízos sociais, econômicos e ambientais, além de representarem um risco direto à vida humana. No Brasil, episódios recorrentes de queimadas e incêndios estruturais demonstram a necessidade de soluções tecnológicas que auxiliem no combate rápido e seguro dessas ocorrências.

Tradicionalmente, o combate a incêndios depende fortemente da atuação humana, expondo bombeiros e equipes de resgate a ambientes extremamente perigosos. Diante disso, o uso de robôs móveis surge como uma alternativa viável para atuar em cenários de risco, especialmente em estágios iniciais do incêndio.

O projeto FIREVISION tem como objetivo desenvolver um robô inteligente capaz de detectar focos de incêndio, extingui-los automaticamente e identificar a presença de pessoas no local, reduzindo a exposição humana ao perigo e contribuindo para ações preventivas e corretivas.</p>


## Embasamento Teórico
<p>Trabalho desenvolvido por:

### 2.1 Robótica Móvel

A robótica móvel estuda sistemas robóticos capazes de se locomover de forma autônoma ou semiautônoma em diferentes ambientes. Esses sistemas utilizam motores, sensores e unidades de processamento para realizar navegação, controle e tomada de decisão.

### 2.2 Sensores de Incêndio

Sensores de chama e sensores de temperatura são amplamente utilizados para a detecção de incêndios. Sensores de chama operam a partir da detecção de radiação infravermelha emitida pelo fogo, enquanto sensores térmicos monitoram variações anormais de temperatura no ambiente.

### 2.3 Visão Computacional

A visão computacional permite que sistemas computacionais interpretem imagens e vídeos. No FIREVISION, essa tecnologia é utilizada para identificar a presença de pessoas no ambiente, aumentando a segurança durante operações de combate a incêndios.

### 2.4 Internet das Coisas (IoT)

A IoT possibilita a comunicação entre dispositivos físicos por meio da internet ou redes sem fio. No projeto, essa tecnologia é empregada para permitir o controle remoto do robô e o envio de alertas ao usuário.</p>


## Materiais e Metodologia
<p> 
  
### 3.1 Materiais Utilizados

Placa microcontroladora (ESP32);

Sensores de chama;

Câmera para captura de imagens;

Motores DC e driver de controle;

Bomba d’água e reservatório;

Estrutura mecânica com rodas;

Fonte de alimentação.

### 3.2 Metodologia

O desenvolvimento do projeto seguiu as seguintes etapas metodológicas:

Definição dos requisitos do sistema;

Aquisição e testes dos componentes eletrônicos;

Montagem da estrutura física do robô;

Programação do firmware do microcontrolador;

Implementação do sistema de comunicação com o aplicativo móvel;

Desenvolvimento e treinamento do modelo de visão computacional;

Integração dos módulos;

Testes em ambiente controlado.</p>

## Resultados e Discussão

<p>Os testes iniciais demonstraram que o robô é capaz de se locomover adequadamente pelo ambiente, detectar focos de incêndio e acionar o sistema de extinção de forma automática. A detecção de pessoas por meio da câmera mostrou-se eficiente em ambientes bem iluminados.

Entretanto, foram observadas limitações relacionadas à autonomia energética e à precisão da detecção em ambientes com fumaça densa, indicando a necessidade de melhorias futuras.</p>


## Conclusão
<p>O projeto FIREVISION demonstrou ser uma solução viável e inovadora para o combate inicial a incêndios, integrando robótica móvel, sensores e visão computacional. A proposta contribui para a redução de riscos humanos, promove o uso da tecnologia em prol da segurança pública e está alinhada aos Objetivos de Desenvolvimento Sustentável da ONU, especialmente os ODS 9, 11 e 13.

Como trabalhos futuros, propõe-se a melhoria da autonomia do sistema, a ampliação dos algoritmos de detecção e a realização de testes em ambientes mais complexos.</p>

