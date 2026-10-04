# Quitanderia Gourmet — Landing Page

React + Vite + Framer Motion.

    npm install
    npm run dev      # desenvolvimento
    npm run build    # gera /dist para publicar

## Onde editar (sem mexer nos componentes)
- `src/data/business.js`  WhatsApp (só dígitos, ex.: 5534999999999), Instagram, Facebook, link do Google Maps, link das avaliações, horário.
  Campo vazio = o elemento não aparece (botão de WhatsApp, por exemplo).
- `src/data/menu.js`      cardápio (bebidas frias, quentes e lanches). Preços lidos do cardápio digital: conferir com o original.
- `src/data/reviews.js`   avaliações reais do Google. Vazio = a seção e o link do menu não aparecem.
- `src/data/gallery.js`   fotos da galeria (áreas: a, b, c, d; `pos` escolhe o recorte). Com menos de 3 fotos a seção não aparece.
- `src/data/photos.js`    fotos do bloco "Sobre" (salão) e do Café Colonial (mesa de salgados).

## Hero e calda do bolo
`src/components/GlazeCanvas.jsx` + `src/data/glaze.js`. A calda é medida na foto `src/assets/bolo.jpg`.
Se trocar a foto do hero, os números de `glaze.js` precisam ser medidos de novo.
Com `prefers-reduced-motion`, a calda fica parada.

## Prévia em arquivo único
`VITE_EMBED_MAP=0 npx vite build --config vite.preview.config.js` gera `dist-preview/index.html`
(sem o mapa embutido, que não carrega em ambientes isolados).
