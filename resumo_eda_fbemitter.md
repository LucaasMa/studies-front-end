# Event-Driven Architecture (EDA) e FBEmitter - Resumo

## 🔹 O que é Event-Driven Architecture (EDA)?

A **Arquitetura Orientada a Eventos (EDA)** é um padrão de arquitetura
de software baseado na **produção, detecção e reação a eventos**.\
Em vez de depender de chamadas diretas e sequenciais, os componentes do
sistema se comunicam através de eventos.

------------------------------------------------------------------------

## 🔹 Conceitos Principais

-   **Evento**: algo que acontece no sistema (ex.: "usuário logado",
    "pedido confirmado").\
-   **Produtor (Emitter)**: gera eventos quando algo ocorre.\
-   **Consumidor (Listener)**: reage a eventos, executando ações
    específicas.\
-   **Event Bus / Dispatcher**: canal de comunicação entre emissores e
    ouvintes.

------------------------------------------------------------------------

## 🔹 Vantagens do EDA

-   **Baixo acoplamento** entre os componentes.\
-   **Escalabilidade**: novos consumidores podem ser adicionados sem
    modificar emissores.\
-   **Reatividade**: sistemas respondem a mudanças em tempo real.\
-   **Flexibilidade**: fácil de integrar novos fluxos de negócio.

------------------------------------------------------------------------

## 🔹 Desvantagens do EDA

-   Pode ser **mais difícil de depurar** (eventos assíncronos).\
-   **Ordem de execução** pode não ser previsível.\
-   Requer **monitoramento** para evitar eventos não tratados.

------------------------------------------------------------------------

## 🔹 Exemplo Genérico de EDA

``` js
const EventEmitter = require('events');
const emitter = new EventEmitter();

// Listener
emitter.on('pedidoConfirmado', (dados) => {
  console.log('Pedido confirmado para:', dados.cliente);
});

// Emitindo evento
emitter.emit('pedidoConfirmado', { cliente: 'Lucas' });
```

------------------------------------------------------------------------

## 🔹 O que é FBEmitter?

O EventEmitter do Facebook é uma implementação simples de emissor que prioriza velocidade e simplicidade. Conceitualmente, ele é semelhante a outros emissores, como o EventEmitter do Node, mas suas APIs específicas diferem.

Uso básico:

``` js
import { EventEmitter } from 'fbemitter';

const emitter = new EventEmitter();

// Criar listener
const subscription = emitter.addListener('mensagem', (data) => {
  console.log('Mensagem recebida:', data);
});

// Emitir evento
emitter.emit('mensagem', 'Olá mundo!');

// Remover listener quando não for mais necessário
subscription.remove();
```

------------------------------------------------------------------------

## 🔹 Vantagens do FBEmitter

-   API simples e leve.\
-   Bom para **fluxos locais** de eventos em aplicações front-end.\
-   Facilita o **desacoplamento de componentes** em React.

------------------------------------------------------------------------

## 🔹 Desvantagens do FBEmitter

-   Não é ideal para **sistemas distribuídos** (melhor usar Kafka,
    RabbitMQ, etc).\
-   É voltado mais para **escopo local** de eventos.\
-   Menos popular que outras soluções de Pub/Sub modernas.

------------------------------------------------------------------------
