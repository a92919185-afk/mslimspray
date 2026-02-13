# Documentação Padrão de Landing Page (Flag Page)

Esta documentação define a estrutura "Gold Standard" para Landing Pages de alta conversão (modelo "Flag Page"), baseada no projeto **MS Spray (Alemanha)**.

**IMPORTANTE:** Todas as futuras páginas solicitadas devem seguir rigorosamente esta estrutura, hierarquia visual e lógica de conversão, salvo instrução específica em contrário.

---

## 1. Conceito & Estrutura Visual
O design deve transmitir **confiança, autoridade médica/científica e simplicidade**.
*   **Estilo:** Clean, Light Mode, "Medical Premium".
*   **Fundo:** Branco (`#FFFFFF`) ou Cinza muito claro (`#FAFAFA`).
*   **Tipografia:** `DM Sans` (ou similar moderna sem serifa). Pesos **Bold (700-900)** para títulos.
*   **Imagens:** Produtos com alta qualidade, `filter: drop-shadow` para profundidade, formato WebP.

## 2. Estrutura de Seções (Ordem Obrigatória)

### A. Header (Fixo)
*   **Layout:** Centralizado.
*   **Elementos:**
    *   **Logo:** Imagem (`images/logo.webp`) centralizada. Altura ~40px.
    *   **Badge (Opcional):** "Distribuidor Autorizado" à direita (desktop) ou oculto (mobile).
*   **Comportamento:** Fundo `backdrop-filter: blur`, fixo no topo.

### B. Hero Section (A Dobra)
*   **Fundo:** Gradiente sutil (Branco -> Cinza Claro).
*   **Ordem dos Elementos:**
    1.  **Pills/Badges:** Ex: "100% Natural", "Frete Grátis", Bandeira do País.
    2.  **Imagem do Produto:** (`images/product.webp`) centralizada, destaque grande.
    3.  **Headline:** Grande, Bold (900), com Span colorido na palavra chave.
    4.  **Subheadline:** Descritiva, focada em benefícios (não características).
    5.  **CTA Principal:** Botão largo, cor de destaque, ícone de seta.
    6.  **Prova Social Rápida:** "Garantia de X dias" + "X Clientes Satisfeitos".

### C. Trust Bar
*   **Design:** Faixa cor sólida (Dark/Contrastante com o resto da página).
*   **Conteúdo:** 4 Colunas (Ícone + Título + Subtítulo).
*   **Exemplos:** Entrega Rápida, Suporte 24/7, Compra Segura, Ingredientes Naturais.

### D. Flag / Geo Section (O "Coração" da Flag Page)
*   **Objetivo:** Segmentar e validar o usuário pelo país.
*   **Layout:** Grid de Cards (3 colunas em Desktop, 1 em Mobile).
*   **Cards:**
    *   Bandeira do País (topo).
    *   Badge "Em Estoque".
    *   Nome do País.
    *   Detalhe de Envio (ex: "Entrega em 2-3 dias").
    *   Botão/Link "Verificar Disponibilidade" -> Direto para Checkout.

### E. Benefits Grid
*   **Layout:** Grid 3x2.
*   **Estilo:** Bordas finas, ícones em destaque com fundo colorido suave (`bg-glow`).
*   **Conteúdo:** 6 Benefícios chave. Título curto + Descrição de 2 linhas.

### F. Reviews (Prova Social)
*   **Layout:** Grid de Cards.
*   **Elementos:**
    *   Estrelas (5/5).
    *   Badge "Verificado" (Verde).
    *   Texto do depoimento (Itálico).
    *   Autor (Avatar com iniciais + Nome + Cidade/País).

### G. FAQ (Dúvidas Frequentes)
*   **Formato:** Acordeão (Accordion) interativo.
*   **Perguntas Chave:** Tempo de resultado, Envio, Garantia, Como usar.

### H. Final CTA
*   **Objetivo:** Última chamada para ação antes do rodapé.
*   **Elementos:** Título de urgência/transformação + Subtítulo + Botão CTA igual ao Hero.

### I. Footer (Legal & Compliance)
*   **Links:** **Termos, Privacidade, Impressum, Contato**.
*   **Comportamento:** **MODAL NA MESMA PÁGINA** (Sem recarregar).
*   **Disclaimers:** Texto legal obrigatório (Anvisa/FDA/etc) em fonte pequena (`0.6rem`) e cor discreta (`#999`).
*   **Nota de Afiliado:** "Site operado por distribuidor independente".

---

## 3. Design System (Variáveis CSS Padrão)

```css
:root {
    /* Cores Base */
    --bg: #FAFAFA;
    --bg-white: #FFFFFF;
    
    /* Cor da Marca (Exemplo M-Slim: Roxo) */
    --primary: #7B2D8E;      /* Ajustar conforme produto */
    --primary-dark: #5C1D6E;
    --primary-light: #9B4DB8;
    --primary-glow: rgba(123, 45, 142, 0.08);
    
    /* Cores Funcionais */
    --green: #2EAD6B;       /* Sucesso / Estoque */
    --text-dark: #1A1A1A;   /* Títulos */
    --text-body: #444444;   /* Corpo */
    --text-muted: #999999;  /* Disclaimers */
    --border: #E8E8E8;
}
```

## 4. Checklist de Implementação
- [ ] Criar pasta `images/` e adicionar `logo.webp` e `product.webp`.
- [ ] Configurar Links de Checkout (FastTrack ou similar) em **todos** os CTAs e Cards de Bandeira.
- [ ] Verificar se Modais do rodapé estão abrindo sem erro de JS.
- [ ] Validar Responsividade (Header, Grid de Bandeiras e Grid de Benefícios devem empilhar no mobile).
- [ ] Garantir que Disclaimers estejam visíveis mas discretos.

---
**Este documento serve como a verdade absoluta para a criação de novas Landing Pages neste projeto.**
