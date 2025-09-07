# Acessibilidade Web - Resumo

## 🔹 O que é Acessibilidade Web?

Acessibilidade Web é a prática de garantir que pessoas com diferentes
tipos de deficiência (visual, auditiva, motora, cognitiva) possam
**perceber, entender, navegar e interagir** com a web de forma
igualitária.

Isso envolve desde o uso correto de **HTML semântico** até o suporte a
**tecnologias assistivas**, como leitores de tela e navegação por
teclado.

------------------------------------------------------------------------

## 🔹 WCAG (Web Content Accessibility Guidelines)

As **WCAG** são diretrizes internacionais criadas pelo W3C para
padronizar boas práticas de acessibilidade.\
É organizada em 4 princípios fundamentais:

1.  **Perceptível** -- a informação deve ser apresentada de forma que
    todos possam perceber (ex: texto alternativo para imagens).\
2.  **Operável** -- todos devem conseguir interagir (ex: navegação via
    teclado).\
3.  **Compreensível** -- o conteúdo deve ser claro e previsível (ex:
    formulários bem estruturados).\
4.  **Robusto** -- compatível com diferentes navegadores e tecnologias
    assistivas.

Cada critério é classificado em **níveis de conformidade**:\
- **A** (básico)\
- **AA** (recomendado, mais comum em regulamentações)\
- **AAA** (avançado, nem sempre obrigatório)

------------------------------------------------------------------------

## 🔹 Boas práticas de Acessibilidade

-   Usar **HTML semântico** corretamente (`<header>`, `<nav>`, `<main>`,
    `<footer>`).\
-   Garantir **contraste de cores** adequado (mínimo 4.5:1 para texto
    normal).\
-   Fornecer **texto alternativo** (`alt`) para imagens.\
-   Estruturar formulários com **labels associados**.\
-   Permitir **navegação por teclado** (foco visível, `tabindex`).\
-   Usar **ARIA apenas quando necessário**, sem substituir semântica
    nativa.\
-   Testar com **ferramentas automáticas** (WAVE, Lighthouse, axe) e
    **usuários reais**.

------------------------------------------------------------------------

## 🔹 Vantagens de aplicar Acessibilidade

-   **Inclusão**: garante acesso para todos.\
-   **SEO**: melhora ranqueamento em buscadores.\
-   **Usabilidade**: beneficia também usuários sem deficiência.\
-   **Conformidade legal**: muitas leis exigem WCAG (como a **Lei
    Brasileira de Inclusão** e normas internacionais como a **ADA** nos
    EUA).

------------------------------------------------------------------------

## 🔹 Desafios e desvantagens

-   **Custo inicial maior** em projetos que não consideram
    acessibilidade desde o começo.\
-   **Curva de aprendizado** para entender WCAG e tecnologias
    assistivas.\
-   **Complexidade em sistemas legados**, que podem precisar de grande
    refatoração.

------------------------------------------------------------------------

## 🔹 Exemplos de código

### Imagem acessível

``` html
<img src="grafico.png" alt="Gráfico mostrando aumento de 20% nas vendas em 2024" />
```

### Formulário acessível

``` html
<label for="email">E-mail</label>
<input type="email" id="email" name="email" required />
```

### Botão acessível

``` html
<button aria-label="Fechar menu">✖</button>
```

------------------------------------------------------------------------