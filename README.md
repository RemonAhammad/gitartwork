# gitartwork on user's contribution graph

gitartwork on user's contribution graph, make a SVG image of it and finally push it back to your repository.

<!-- An example result:
[![RemonAhammad/gitartwork](gitartwork.svg)](https://github.com/RemonAhammad/gitartwork) -->

An example result:
[![RemonAhammad/gitartwork](gitartwork.svg)](https://github.com/RemonAhammad/gitartwork)
## Usage:

### Option #1: Use gitartwork as a GitHub Action
1. Copy the workflow code into a `.github/workflows/gitartwork.yml` file in your repository.

        name: gitartwork from a contribution graph
        on: 
          push:
          schedule:
            - cron: '* */24 * * *'
        workflow_dispatch:
        jobs:
          build:
            name: Make gitartwork SVG
            runs-on: ubuntu-latest
            steps:
              - uses: actions/checkout@v2
              - uses: RemonAhammad/gitartwork@v1
                with:
                   # Use this username's contribution graph  
                   user_name: RemonAhammad
                   # Text on contribution graph 
                   text: Remon
              - uses: RemonAhammad/simple-push-action@v1

2. A few moments later it will generate `gitartwork.svg` image in your repository, so then you can include it in your `README.md` like `![gitartwork](gitartwork.svg)`
3. Have fun :)

### Option #2: Make gitartwork locally on your environment
Still in progress...