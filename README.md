# Deploy to Neocities

A GitHub Action for deploying a folder to [Neocities](https://neocities.org) using [`neocities-red`](https://github.com/o-200/neocities-red).

This action is useful for giant website, static sites built with tools like Hugo, Jekyll, Eleventy, Astro, VitePress, or plain HTML/CSS/JS projects.

## Usage

### Basic example

1) place this code in .github/workflows

```yaml
name: Deploy to neocities.org

on:
  push:
    branches:
      - main

jobs:
  test:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout
        uses: actions/checkout@v4

      - name: Run your action
        uses: o-200/deploy-sites-neocities-red@v1
        with:
          key: ${{ secrets.NEOCITIES_API_TOKEN }}
```

2) place your neocities api token into github secrets

3) Now, it ready to work!

### How to get API TOKEN? 
1) Open your account settings in neocities
2) Open "Manage Site Settings" in "Sites"
3) Go to "API" and take your API token

### How to place api token in github secrets?
1) Open your website's github repository 
2) Settings 
3) Secrets And Variables 
4) New Repository Secret
5) Name - "NEOCITIES_API_TOKEN" (without quotes), put your api key in Secret
6) Done!





