# Frontend Mentor - Solução: Componente de Pré-visualização de Artigo

Esta é a minha solução para o desafio "Article Preview Component" do Frontend Mentor. O objetivo do desafio é recriar um componente de pré-visualização de artigo responsivo e com interações de compartilhamento em redes sociais.

## Índice
- [Visão Geral](#visão-geral)
- [O desafio](#o-desafio)
- [Screenshot](#screenshot)
- [Links](#links)
- [Meu processo](#meu-processo)
- [Construído com](#construído-com)
- [O que eu aprendi](#o-que-eu-aprendi)
- [Desenvolvimento contínuo](#desenvolvimento-contínuo)
- [Recursos úteis](#recursos-úteis)
- [Autor](#autor)
- [Agradecimentos](#agradecimentos)

## Visão Geral
Componente simples de pré-visualização de artigo com:
- Layout responsivo (mobile-first).
- Ícone de compartilhamento que revela opções de redes sociais.
- Estilização moderna com sombras, bordas arredondadas e tipografia legível.

## O desafio
Os usuários devem ser capazes de:
- Ver o layout ideal para o componente, dependendo do tamanho da tela do dispositivo.
- Ver os links de compartilhamento de mídia social ao clicar no ícone de compartilhamento.

## Screenshot
(Substitua o caminho abaixo pelo caminho para a imagem do seu projeto pronto)
- Imagem do componente (desktop): ./screenshots/desktop.png
- Imagem do componente (mobile): ./screenshots/mobile.png

## Links
- URL da Solução (repositório): https://github.com/kayky-ctrl/frontendTreino
- URL do Site ao Vivo: https://kayky-ctrl.github.io/frontendTreino

(Substitua os links acima pelos links reais do seu projeto.)

## Meu processo
Comecei com um layout mobile-first e criei a estrutura HTML semântica do componente. Em seguida, estilizei usando CSS moderno (variáveis CSS e flexbox). Por fim, implementei a lógica de compartilhamento com JavaScript para alternar a visibilidade do painel de redes sociais e garantir bom posicionamento em diferentes tamanhos de tela.

Como passos principais:
1. Estrutura HTML semântica (article, header, footer).
2. Estilização mobile-first com variáveis CSS e uso de flexbox.
3. Adição de media queries para versão desktop.
4. Implementação do botão de compartilhar com evento de clique e acessibilidade básica (aria-attributes).

## Construído com
- HTML5 semântico
- CSS3 (variáveis CSS personalizadas)
- Flexbox
- Mobile-first workflow
- JavaScript (vanilla) para interações simples

## O que eu aprendi
Neste projeto, aprendi a criar um menu de compartilhamento flutuante usando JavaScript e CSS. O maior desafio foi posicioná-lo corretamente em relação ao ícone, tanto no desktop quanto no mobile.

Exemplo do trecho de JavaScript do qual me orgulho:
```javascript
const shareButton = document.querySelector('.share-button');
const sharePanel = document.querySelector('.share-panel');

shareButton.addEventListener('click', () => {
  const isOpen = sharePanel.classList.toggle('open');
  // Alterna atributo aria para acessibilidade
  shareButton.setAttribute('aria-expanded', isOpen);
});
```

Exemplo de CSS para posicionamento responsivo do painel de compartilhamento:
```css
.share-panel {
  position: absolute;
  bottom: calc(100% + 12px);
  right: 0;
  transform-origin: bottom right;
  opacity: 0;
  pointer-events: none;
  transition: opacity .2s ease, transform .2s ease;
}
.share-panel.open {
  opacity: 1;
  pointer-events: auto;
  transform: translateY(0);
}
@media (min-width: 768px) {
  .share-panel {
    bottom: 50%;
    left: calc(100% + 12px);
    right: auto;
    transform-origin: center left;
  }
}
```

## Desenvolvimento contínuo
Coisas que quero melhorar e praticar:
- Tornar o componente mais acessível (melhor uso de teclas, foco e leitores de tela).
- Recriar o mesmo componente com um framework (React ou Vue) para praticar componentização.
- Adicionar testes visuais ou snapshots para garantir regressões de layout.

## Recursos úteis
- Artigo sobre posicionamento e tooltips em CSS — ajudou a entender transform-origin e posicionamento absoluto.
- Guia de Flexbox — útil para centralizar itens e construir layouts responsivos.
- Documentação de ARIA — para melhorar a acessibilidade de componentes interativos.

(Adicione aqui quaisquer links de tutoriais ou guias que te ajudaram.)

## Autor
- Frontend Mentor - @kayky-ctrl
