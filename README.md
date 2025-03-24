# WAKATIME-README

## What is this?

This is a simple script that generates a README.md file with your Wakatime stats.

## Inputs

### `WAKATIME_API_KEY`

**Required** Your Wakatime API key. You can find it [here](https://wakatime.com/settings/account).

### `CHAR1`

**Optional** The character you want to use to draw the graph. Default `▇`.

### `CHAR2`

**Optional** The character you want to use to draw the graph. Default `░`.

### `name_of_balise`

**Optional** The name of the balise you want to use to draw the graph. Default `WAKATIME`.

### `commit_message`

**Optional** The commit message. Default `wakatime update`.

### `draw_graph`

**Optional** If you want to draw the graph. Default `false`.


## Outputs

You need to have a `README.md` file in the root of your repository.

And you need to have the following balise in your `README.md` file:

```md
<!--WAKATIME-->
<!--/WAKATIME-->
```

> The name of the balise can be changed with the `name_of_balise` input. Default is `"WAKATIME"`.

⚠️**WARNING**⚠️ : this action need Read and write permissions (Settings > Actions > General)


## Example usage

```yaml
name: Update Wakatime stats

on:
  schedule:
    - cron: '0 0 * * *'
  push:
    branches:
      - main
  
jobs:
  update_wakatime_stats:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout repository
        uses: actions/checkout@v3

      - name: Update Wakatime stats
        uses: tot0p/wakatime-readme@v1
        with:
          WAKATIME_API_KEY: ${{ secrets.WAKATIME_API_KEY }}
          CHAR1: ">"
          CHAR2: "-"
          name_of_balise: "WAKATIME"
          commit_message: "wakatime update"
          draw_graph: "true"
```

## Result

<!--WAKATIME-->
## Work Time of last 7 days

```text
🌐 Time zone: Europe/Paris

🗓️ From 2025-03-16T23:00:00Z to 2025-03-23T22:59:59Z

⌚ Total time: 52 mins

💬 Languages:

Go       23 mins ▓▓▓▓▓░░░░░ 44.98 %
Docker   17 mins ▓▓▓▓░░░░░░ 33.18 %
Markdown 7 mins  ▓▓░░░░░░░░ 14.7 %
YAML     2 mins  ▓░░░░░░░░░ 4.63 %
Other    1 min   ▓░░░░░░░░░ 2.34 %
go.mod   0 secs  ▓░░░░░░░░░ 0.18 %

🔥 IDE:

GoLand 52 mins ▓▓▓▓▓▓▓▓▓▓ 100.0 %

💻 OS:

Windows 52 mins ▓▓▓▓▓▓▓▓▓▓ 100.0 %
```
<!--/WAKATIME-->