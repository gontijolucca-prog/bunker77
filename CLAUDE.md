# CLAUDE.md

## Auto-learned Rules

<!-- claude-evolve:managed-start -->

<!-- claude-evolve:rule id=r_mq9spw3x_er2i score=5.9 created=2026-06-11 source=observation complexity=simple -->
- When using macOS Vision framework for background removal, write a Swift CLI to /tmp, compile with swiftc, and run it — do not use Python/shell-only alternatives which lack VisionKit access
<!-- /claude-evolve:rule -->

<!-- claude-evolve:rule id=r_mq9spw4s_xruv score=5 created=2026-06-11 source=observation complexity=simple -->
- After pushing to GitHub Pages, poll the CDN URL in a loop (curl -w "%{http_code}") with sleep intervals until 200 — do not assume the asset is live immediately after push
<!-- /claude-evolve:rule -->

<!-- claude-evolve:rule id=r_mq9spw5i_an8k score=5.3 created=2026-06-11 source=observation complexity=simple -->
- After background removal, Read the output PNG before using it in downstream edits — verify the asset exists and is non-empty before wiring it into HTML/JS
<!-- /claude-evolve:rule -->

<!-- claude-evolve:rule id=r_mq9spw68_g7cj score=5.9 created=2026-06-11 source=observation complexity=simple -->
- When replacing a sprite in a canvas game, use lazy-loading with Image().onload and a null fallback — never block rendering on asset load
<!-- /claude-evolve:rule -->

<!-- claude-evolve:rule id=r_mq9spw6x_2kjz score=5.9 created=2026-06-11 source=observation complexity=simple -->
- Use Playwright with chromium.launch({ channel: 'chrome' }) for headless screenshots of local HTML — write the screenshot script to content-machine as a .mjs file for reuse
<!-- /claude-evolve:rule -->

<!-- claude-evolve:managed-end -->
