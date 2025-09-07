# Pré-processadores CSS - Resumo

## 🔹 O que são

Pré-processadores CSS são ferramentas que adicionam recursos extras ao
CSS tradicional, como **variáveis, funções, mixins, aninhamento de
seletores** e mais. Eles precisam ser compilados para CSS puro antes de
serem interpretados pelo navegador.

Os mais conhecidos são: - **Sass/SCSS** - **Less** - **Stylus**

------------------------------------------------------------------------

## 🔹 Vantagens

-   **Variáveis**: permitem armazenar valores reutilizáveis (ex: cores,
    espaçamentos).
-   **Aninhamento**: facilita a leitura de seletores relacionados.
-   **Mixins e funções**: reutilização de blocos de código.
-   **Importação modular**: divide estilos em múltiplos arquivos
    organizados.
-   **Compatibilidade**: ajudam a escrever CSS moderno em épocas de
    menor suporte do navegador.

------------------------------------------------------------------------

## 🔹 Desvantagens

-   **Configuração extra**: é preciso compilar para CSS puro.
-   **Curva de aprendizado**: sintaxe e recursos adicionais exigem
    prática.

------------------------------------------------------------------------

## 🔹 Comparação com CSS padrão

### CSS padrão

``` css
:root {
  --primary-color: blue;
}

button {
  background: var(--primary-color);
  color: white;
}
```

### Usando Sass

``` scss
$primary-color: blue;

button {
  background: $primary-color;
  color: white;

  &:hover {
    background: darken($primary-color, 10%);
  }
}
```

------------------------------------------------------------------------
