\[Younes Engenharia Elétrica]



# APC — Algoritmos e Programação de Computadores

> Primeiro contato com programação na graduação de Engenharia. Ofertada pelo Departamento de Ciências da Computação.

\---

## Sobre a Disciplina

A APC é a porta de entrada dos estudantes de Engenharia no mundo da programação. Saber programar é uma habilidade **essencial** para o profissional de Engenharia, e muitas disciplinas futuras exigirão que o aluno escreva código para resolver problemas.

\---

## Estrutura Curricular

|Aspecto|Detalhe|
|-|-|
|**Créditos totais**|6|
|**Teoria**|4 créditos|
|**Prática (laboratório)**|2 créditos|

### Conteúdo da Teoria

* Variáveis e tipos de dados
* Estruturas condicionais (if/else)
* Laços de repetição (loops)
* Funções e modularização
* Algoritmos fundamentais

### Conteúdo da Prática

* Resolução de desafios de programação
* Aplicação dos conceitos teóricos em código
* Desenvolvimento de habilidades de resolução de problemas

> \*\*Dica:\*\* É na prática que os conceitos realmente se fixam. Resolver os problemas é desafiador, mas extremamente recompensador!

\---

## Dificuldades Comuns

É normal encontrar **muitos erros** enquanto se programa — desde os mais simples até os mais complexos. Na verdade, os programadores passam grande parte do tempo **depurando código**.

### Como lidar:

* Não se desestimule — erros fazem parte do processo
* Acontece com todo mundo, desde iniciantes até experientes
* Cada erro resolvido é uma oportunidade de aprendizado
* Persistência é a chave para dominar a programação

\---

## Por que investir em APC?

|Motivo|Impacto|
|-|-|
|Base para disciplinas futuras|Várias matérias exigem programação|
|Ferramenta para Engenharia|Resolve problemas reais de forma automatizada|
|Pensamento lógico|Desenvolve capacidade de análise e resolução de problemas|
|Mercado de trabalho|Habilidade altamente valorizada|

\---

## Resumo

> A APC é \*\*fundamental\*\* para a formação do engenheiro. Dedique-se à teoria, pratique bastante nos laboratórios e não desanime com os erros — eles são parte natural do caminho. A recompensa de ver o código funcionando vale todo o esforço!

\---

*Disciplina ofertada pelo Departamento de Ciências da Computação.*



# Semana 01 — introdução à programação com OctoStudio e arquitetura de computadores com Little Man Computer.



\---

## Aula 1 — OctoStudio: Programação com Blocos no Celular

### O que é o OctoStudio?

O **OctoStudio** é um aplicativo gratuito de programação por blocos, criado pelos mesmos desenvolvedores do **Scratch** no **MIT Media Lab** (Lifelong Kindergarten research group).

Diferente do Scratch, que é voltado para computadores, o OctoStudio foi projetado especialmente para **dispositivos móveis** (smartphones e tablets), permitindo que os alunos programem **a qualquer hora e em qualquer lugar**. 

Características principais

|Recurso|Descrição|
|-|-|
|**Plataforma**|Android, iOS e Chromebooks|
|**Idade recomendada**|7 a 12+ anos|
|**Custo**|Totalmente gratuito, sem anúncios ou compras internas|
|**Linguagem**|Programação visual por blocos (baseada no Scratch)|
|**Interatividade**|Usa sensores do celular: acelerômetro, câmera e microfone|
|**Multimídia**|Permite adicionar fotos e sons do próprio dispositivo|

### Como funciona?

Os alunos montam programas arrastando e encaixando **blocos de código coloridos**, exatamente como no Scratch. A diferença está na interação: é possível **sacudir, inclinar e tocar** no celular para controlar os personagens e objetos criados. 

### Projeto da aula: Apresentação Pessoal

Na primeira aula, os alunos criaram um **programa de apresentação deles mesmos** usando o OctoStudio. O projeto envolveu:

* Criar personagens ou usar fotos próprias
* Adicionar animações e movimentos
* Incluir sons e falas
* Programar interações (toque na tela, movimento do celular)
* Compartilhar o projeto com colegas

> Esse exercício introduziu os conceitos básicos de programação — sequência de comandos, eventos e multimídia — de forma lúdica e criativa.

\---

## Aula 2 — Little Man Computer (LMC): Simulador de CPU

### O que é o Little Man Computer?

O **Little Man Computer (LMC)** é um modelo simplificado de computador criado pelo Dr. Stuart Madnick em 1965, usado para fins educacionais. Ele representa uma arquitetura **Von Neumann** básica, com todos os elementos essenciais de um computador moderno, mas em uma escala muito simples. Os alunos utilizaram o simulador online disponível no site **101computing.net**, que permite visualizar passo a passo como a CPU executa um programa. 

### Arquitetura do LMC

O simulador demonstra o ciclo **Busca-Decodifica-Executa (FDE Cycle)** e os principais registradores da CPU:

|Componente|Sigla|Função|
|-|-|-|
|**Contador de Programa**|PC|Indica a próxima instrução a ser executada|
|**Registrador de Instrução Atual**|CIR|Armazena a instrução sendo executada|
|**Registrador de Endereço de Memória**|MAR|Guarda o endereço da memória a ser acessado|
|**Registrador de Dados de Memória**|MDR|Guarda o dado lido/escrito na memória|
|**Acumulador**|ACC|Registrador principal para operações aritméticas|

### Memória (RAM)

* **100 células de memória** (chamadas de *mailboxes*), numeradas de 00 a 99
* Cada célula armazena um número decimal de 3 dígitos
* Tanto **instruções** quanto **dados** ficam na mesma memória (arquitetura Von Neumann)

### Conjunto de Instruções

O LMC é programado em **assembly** usando mnemônicos simples: 

|Mnemônico|Nome|Descrição|Opcode|
|-|-|-|-|
|`INP`|INPUT|Lê um valor do usuário para o acumulador|901|
|`OUT`|OUTPUT|Mostra o valor do acumulador|902|
|`LDA`|LOAD|Carrega o acumulador com o conteúdo de um endereço|5xx|
|`STA`|STORE|Guarda o valor do acumulador em um endereço|3xx|
|`ADD`|ADD|Soma o conteúdo de um endereço ao acumulador|1xx|
|`SUB`|SUBTRACT|Subtrai o conteúdo de um endereço do acumulador|2xx|
|`BRP`|BRANCH IF POSITIVE|Desvia se o acumulador for zero ou positivo|8xx|
|`BRZ`|BRANCH IF ZERO|Desvia se o acumulador for zero|7xx|
|`BRA`|BRANCH ALWAYS|Desvio incondicional|6xx|
|`HLT`|HALT|Para a execução|000|
|`DAT`|DATA|Reserva um endereço para armazenar dados|—|

> \*\*Nota:\*\* `xx` representa um endereço de memória (00 a 99).

### O que os alunos aprenderam?

* Como a CPU executa instruções passo a passo (ciclo FDE)
* A diferença entre **dados** e **instruções** na memória
* O funcionamento dos **registradores** da CPU
* Como escrever programas simples em **assembly**
* O conceito de **desvios condicionais** (`BRP`, `BRZ`) e **incondicionais** (`BRA`)

### Exemplo de programa LMC

Um programa simples que lê dois números e calcula a diferença:

```asm
INP         // Lê primeiro número
STA FIRST   // Armazena em FIRST
INP         // Lê segundo número
STA SECOND  // Armazena em SECOND
LDA FIRST   // Carrega primeiro número
SUB SECOND  // Subtrai segundo número
OUT         // Mostra resultado
HLT         // Para
FIRST DAT   // Reserva espaço para dado
SECOND DAT  // Reserva espaço para dado
```

\---

## Comparação: OctoStudio vs. Little Man Computer

|Aspecto|OctoStudio|Little Man Computer|
|-|-|-|
|**Nível de abstração**|Alto (blocos visuais)|Baixo (assembly)|
|**Plataforma**|Mobile (celular/tablet)|Navegador web|
|**Foco**|Criatividade e interatividade|Arquitetura de computadores|
|**Conceitos**|Eventos, animação, multimídia|CPU, memória, registradores, assembly|
|**Público-alvo**|Iniciantes em programação|Estudantes de ciência da computação|

\---

# Semana 02 — desenvolvimento de programa no LMC.  



