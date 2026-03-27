# Convenção `cc-` (componentes customizados)

Documentação interna do projeto sobre ficheiros com prefixo **`cc-`** neste fork do tema Dawn.

## Objetivo da padronização

Os componentes **`cc-`** estendem os componentes **originais do tema Dawn**: mantêm o mesmo papel e comportamento base e acrescentam apenas as **customizações** pedidas pelo projeto.

### Vantagens

- **Rastreabilidade:** fica explícito o que é “core Dawn” versus “customização do cliente/projeto”.
- **Rollback e manutenção:** em relayout, correção de bug ou atualização do tema, é mais simples **comparar** com o componente original ou **repor** a versão base sem perder a referência.
- **Backup lógico:** a feature original do tema continua representada pela secção/snippet/asset **sem** o prefixo `cc-`; o `cc-` funciona como camada de evolução controlada.

A mesma lógica aplica-se a **snippets**, **estilos** e **JavaScript**: equivalentes `cc-` devem seguir o mesmo critério (estender o original, documentar o desvio).

## Estratégia de branches

Foram criadas **duas branches**, **uma por feature**, para isolar a evolução do código conforme as **demandas** do projeto. Cada linha de trabalho pode evoluir e integrar de forma independente, reduzindo conflitos e mistura de escopos num único branch.

## Inventário atual

| Área    | Ficheiro | Descrição |
|---------|----------|-----------|
| Secção  | [`sections/cc-slideshow.liquid`](../sections/cc-slideshow.liquid) | Slideshow custom; suporte a **vídeo** no slide e refinamentos em relação ao slideshow base. |
| Estilos | [`assets/cc-component-slideshow.css`](../assets/cc-component-slideshow.css) | Estilos específicos do slideshow `cc-` (inclui dots e detalhes visuais). |
| Assets  | [`assets/cc-slideshow-arrow-prev.svg`](../assets/cc-slideshow-arrow-prev.svg), [`assets/cc-slideshow-arrow-next.svg`](../assets/cc-slideshow-arrow-next.svg) | Setas do carrossel alinhadas ao visual custom. |
| Secção  | [`sections/cc-image-banner.liquid`](../sections/cc-image-banner.liquid) | Banner custom (vídeo, overlays, etc.) em extensão ao padrão do tema. |

Atualizar esta tabela quando forem adicionados novos ficheiros `cc-`.

## Slideshow com vídeo e dots customizadas

No slide com **vídeo**, foram criadas **dots (indicadores) customizadas** para reforçar a hierarquia visual: o bloco já chama atenção por ser **animado**; os indicadores personalizados ajudam a percecionar o número de slides e o slide ativo, reforçando o componente em vez de competir de forma confusa com a animação.
