# slack

A [Dive](https://github.com/loon-rocks/dive) pack for posting messages to Slack channels and threads, so a plan can report what it found where the team reads it.

## Install

```bash
dive pack add slack
```

That installs the pack into the project's `.dive/packs/slack`. Add `--global` to install it for every project.

## Requirements

- macOS or Linux.
- Dive v0.17 or later.
- `bash`, `curl` and `jq` on your `PATH`.
- `SLACK_BOT_TOKEN` in the environment.

## Setup

1. Create a Slack app with the `chat:write` bot scope. [`app-manifest.json`](app-manifest.json) has this configuration.
2. Install the app to your workspace.
3. Invite it to each channel you post to: `/invite @your-app`.
4. Export its bot token (`xoxb-…`) as `SLACK_BOT_TOKEN`.

## Tools

| Tool | What it does |
|---|---|
| `slack__tool__slack_post_message` | Posts a message to a Slack channel, or as a reply in a thread when given `thread_ts`. Returns `{channel, ts, permalink}` |

## Develop

| Command | What it does |
|---|---|
| `dive pack check` | loads the pack the way an install would and reports every problem |
| `dive pack run tool__slack_post_message --input channel=#test --input text=hello` | posts a message with the tool |
| `dive pack test` | runs `check`, then each migration over its sample files |
| `dive pack release <major\|minor\|patch>` | compares the public interface with the previous tag and creates the next tag |
