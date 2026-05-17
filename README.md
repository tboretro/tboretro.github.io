# Local Setup

## Tool Installation

```bash
sudo apt install git ruby-full build-essential zlib1g-dev
gem install bundler
```

## Cloning project

Requires SSL key added to GitHub account

```bash
git clone git@github.com:tboretro/tboretro.github.io.git
```

## Start local server

```bash
bundle install
bundle exec jekyll serve
```

## URL

http://127.0.0.1:4000

## Deployment

Deployment erfolgt automatisch über GitHub Pages.

## Notes

- Theme basiert auf minima
- Custom CSS in assets/css/
