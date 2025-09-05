# BEM e ITCSS - Resumo

## 🔹 BEM (Block Element Modifier)

### O que é

BEM é uma metodologia de nomenclatura para CSS. A ideia é dividir a interface em **blocos**, **elementos** e **modificadores** que representam variações.

**Exemplo de estrutura:**

``` css
/* Bloco */
.button {}

/* Elemento */
.button__icon {}

/* Modificador */
.button--disabled {}
```

### Vantagens

-   Facilita a **leitura e manutenção** do código.\
-   Evita **conflito de nomes** entre componentes.\
-   Traz **previsibilidade** e consistência.\
-   Escalável para equipes grandes.

### Desvantagens

-   Sintaxe pode ficar **verbosa** (`.menu__item--active`).\
-   Requer disciplina para seguir corretamente.\
-   Pode ser considerado "rigoroso" demais para projetos pequenos.

------------------------------------------------------------------------

## 🔹 ITCSS (Inverted Triangle CSS)

### O que é

ITCSS é uma arquitetura para organizar o CSS em camadas, formando um
"triângulo invertido": começa do mais **genérico** até o mais
**específico**.

**Estrutura típica de pastas:**

    1. Settings (variáveis)
    2. Tools (mixins, funções)
    3. Generic (reset/normalize)
    4. Elements (tags HTML básicas)
    5. Objects (estruturas sem estilo visual forte)
    6. Components (botões, cards, etc.)
    7. Utilities (classes utilitárias, helpers)

### Vantagens

-   Deixa o CSS **modular e previsível**.\
-   Facilita a **escalabilidade** em projetos grandes.\
-   Ajuda a **evitar repetição** e cascata descontrolada.

### Desvantagens

-   Requer **curva de aprendizado** maior.\
-   Pode parecer **complexo demais** para projetos pequenos.\
-   Necessita disciplina para seguir a hierarquia corretamente.

------------------------------------------------------------------------

