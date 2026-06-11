# BUNKER 77

FPS cooperativo no browser. Sobrevive às ondas de demónios — sozinho ou com amigos.

**Jogar:** https://gontijolucca-prog.github.io/bunker77/

## Multiplayer

1. Um jogador clica **CRIAR SALA ONLINE** — o link da sala é copiado automaticamente.
2. Envia o link aos amigos (até 6 jogadores).
3. Os amigos abrem o link e clicam **ENTRAR NA SALA**.

A ligação é direta entre browsers (WebRTC via PeerJS) — não há servidor de jogo.

## Controlos

| Tecla | Ação |
|---|---|
| WASD | Mover |
| Rato | Apontar |
| Clique | Disparar |
| R | Recarregar |
| Shift | Correr |
| M | Som on/off |
| Esc | Pausa |

**Telemóvel:** controlos touch automáticos — joystick à esquerda, arrastar à direita para apontar, botão FOGO.

## Jogo

- Health packs e armas aparecem constantemente no mapa; +15 vida por onda sobrevivida.
- Armas para apanhar: metralhadora, raio laser (feixe contínuo) e bazooka (explosão em área). Troca com 1-4, scroll ou toque na munição. Morrer = perder as armas (voltam a aparecer no mapa).
- Boss gigante a cada 10 ondas (+1000 pontos) e mudança de mapa (3 mapas em rotação).
- Em multiplayer: respawn em 5 s com balas cheias; se morrerem todos ao mesmo tempo, a equipa recua uma onda.
- Música procedural com botão de mute (🔊 / tecla M).

## Tecnologia

Ficheiro único (`index.html`), sem build. Motor raycasting próprio em Canvas 2D, som procedural WebAudio, netcode host-autoritativo com previsão local e interpolação.
- O jogo atualiza-se sozinho entre ondas quando há versão nova — sem refresh manual.
