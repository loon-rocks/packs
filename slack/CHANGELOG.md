# Changelog

## v1.0.1

- Graph is now Dive, and this pack's home is now `github.com/loon-rocks/packs`. The pack requires Dive v0.17 or later and installs with `dive pack add slack`. The tool is unchanged, and the Slack app in `app-manifest.json` is now named Dive CI.

## v1.0.0

- `slack_post_message`, which shipped inside graph up to v0.15 as `builtin__slack_post_message`, unchanged, now installed with `graph pack add slack` and called as `slack__tool__slack_post_message`.
