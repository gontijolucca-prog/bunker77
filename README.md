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
| Esc | Pausa |

## Tecnologia

Ficheiro único (`index.html`), sem build. Motor raycasting próprio em Canvas 2D, som procedural WebAudio, netcode host-autoritativo com previsão local e interpolação.
