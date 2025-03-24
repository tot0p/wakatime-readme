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


## Result

<!--WAKATIME-->
<!--/WAKATIME-->