# CLAUDE.md

## Auto-learned Rules

<!-- claude-evolve:managed-start -->

<!-- claude-evolve:rule id=r_mq9spw3x_er2i score=5.6 created=2026-06-11 source=observation complexity=simple -->
- When using macOS Vision framework for background removal, write a Swift CLI to /tmp, compile with swiftc, and run it — do not use Python/shell-only alternatives which lack VisionKit access
<!-- /claude-evolve:rule -->

<!-- claude-evolve:rule id=r_mq9spw4s_xruv score=5 created=2026-06-11 source=observation complexity=simple -->
- After pushing to GitHub Pages, poll the CDN URL in a loop (curl -w "%{http_code}") with sleep intervals until 200 — do not assume the asset is live immediately after push
<!-- /claude-evolve:rule -->

<!-- claude-evolve:rule id=r_mq9spw5i_an8k score=5.5 created=2026-06-11 source=observation complexity=simple -->
- After background removal, Read the output PNG before using it in downstream edits — verify the asset exists and is non-empty before wiring it into HTML/JS
<!-- /claude-evolve:rule -->

<!-- claude-evolve:rule id=r_mq9spw68_g7cj score=6.5 created=2026-06-11 source=observation complexity=simple -->
- When replacing a sprite in a canvas game, use lazy-loading with Image().onload and a null fallback — never block rendering on asset load
<!-- /claude-evolve:rule -->

<!-- claude-evolve:rule id=r_mq9spw6x_2kjz score=6.5 created=2026-06-11 source=observation complexity=simple -->
- Use Playwright with chromium.launch({ channel: 'chrome' }) for headless screenshots of local HTML — write the screenshot script to content-machine as a .mjs file for reuse
<!-- /claude-evolve:rule -->

<!-- claude-evolve:rule id=r_mq9tedde_knuf score=5.9 created=2026-06-11 source=observation complexity=simple -->
- When adding mobile support to a canvas/web game, define a single MOBILE constant at module top using matchMedia('(pointer:coarse)').matches and gate ALL mobile-specific branches on it — never scatter individual feature-detect checks across the codebase
<!-- /claude-evolve:rule -->

<!-- claude-evolve:rule id=r_mq9tede9_gfly score=5.3 created=2026-06-11 source=observation complexity=simple -->
- When multiple related hardcoded constants appear together (mag=8, MAG=8, rate=.28, etc.), consolidate them into a config object (WEAPONS={shotgun:{...}, mg:{...}}) before adding more features — prevents constant drift as feature count grows
<!-- /claude-evolve:rule -->

<!-- claude-evolve:rule id=r_mq9tedf0_20h5 score=5.9 created=2026-06-11 source=observation complexity=simple -->
- When a game damage function will be called over a network path, accept damage as a parameter with an explicit server-side cap (Math.min(maxVal, +m.dmg||fallback)) rather than hardcoding — prevents exploit amplification on the client
<!-- /claude-evolve:rule -->

<!-- claude-evolve:rule id=r_mq9tedfq_w58u score=5.9 created=2026-06-11 source=observation complexity=simple -->
- Add touch controls as a position:fixed display:none overlay with pointer-events:none on the container, shown only when MOBILE===true — keeps desktop DOM path clean and avoids CSS conflicts
<!-- /claude-evolve:rule -->

<!-- claude-evolve:rule id=r_mq9tedgg_dzqu score=5.9 created=2026-06-11 source=anti_pattern complexity=simple -->
- Do not hardcode damage values in game functions that will later be networked — design hitEnemy(e, dmg) from the start when multiplayer is already present
<!-- /claude-evolve:rule -->

<!-- claude-evolve:managed-end -->
