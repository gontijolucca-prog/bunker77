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

- Health packs no mapa (+30 vida) e +15 vida por onda sobrevivida.
- Armas para apanhar: metralhadora, raio laser, bazooka (explosão em área).
- Boss gigante a cada 10 ondas (+1000 pontos).
- Em multiplayer: respawn em 5 s com balas cheias; se morrerem todos ao mesmo tempo, a equipa recua uma onda.
- Música procedural com botão de mute (🔊 / tecla M).

## Tecnologia

Ficheiro único (`index.html`), sem build. Motor raycasting próprio em Canvas 2D, som procedural WebAudio, netcode host-autoritativo com previsão local e interpolação.
