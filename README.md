# cmderdev.github.io
The cmder.net page.

[![CI](https://github.com/cmderdev/cmderdev.github.io/actions/workflows/ci.yml/badge.svg)](https://github.com/cmderdev/cmderdev.github.io/actions/workflows/ci.yml)

## Development

### Building CSS

This project uses SCSS for styling. The source files are in `_sass/` and the compiled CSS is generated in `css/`.

To build the CSS:
```bash
npm install
npm run build:css
```

To watch for changes and rebuild automatically:
```bash
npm run watch:css
```

### Building the Site

The site uses Jekyll for static site generation:
```bash
bundle install
bundle exec jekyll build
```

The built site will be in the `_site/` directory.
