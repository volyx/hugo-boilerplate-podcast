# hugo-boilerplate-podcast

Podcast theme for Hugo.

## Prerequisite

You have to install the newest version of Hugo before using.

```bash
$ brew install hugo
```

## Usage

```bash
# Clone this repository
$ git clone git@github.com:1000ch/hugo-boilerplate-podcast.git

# Install dependencies
$ cd hugo-boilerplate-podcast
$ npm install

# Build and watch
$ npm start
```

## Wercker Integration

See [Automated deployments with Wercker](http://gohugo.io/tutorials/automated-deployments/).

`wercker.yml` example:

```yml
box: node:latest
build:
  steps:
    - npm-install
    - arjen/hugo-build:
        version: "0.18"
    - code: npm run build
deploy:
  steps:
    - lukevivier/gh-pages@0.2.1:
        token: $GITHUB_TOKEN
        domain: 1000ch.github.io
        basedir: docs
```

## License

[MIT](https://1000ch.mit-license.org) © [Shogo Sensui](https://github.com/1000ch)