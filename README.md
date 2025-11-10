# Cmder Website

[![CI](https://github.com/cmderdev/cmderdev.github.io/actions/workflows/ci.yml/badge.svg)](https://github.com/cmderdev/cmderdev.github.io/actions/workflows/ci.yml)

The official website for Cmder - a portable console emulator for Windows.

Visit us at: **[https://cmder.app](https://cmder.app)**

## About Cmder

Cmder is a software package created out of pure frustration over the absence of nice console emulators on Windows. It is based on amazing software, and spiced up with the Monokai color scheme and a custom prompt layout, looking sexy from the start.

## About This Repository

This repository contains the source code for the Cmder website, built as a static GitHub Pages site using:

- **Bootstrap 5** - Modern responsive framework
- **SCSS** - Structured stylesheets with CSS variables
- **Jekyll** - Static site generation
- **GitHub Actions** - Automated CI/CD pipeline

## Development Setup

### Prerequisites

- **Ruby** 3.x or higher (for Jekyll)
- **Node.js** 18.x or higher (for SCSS build tools)
- **Bundler** (Ruby gem manager)
- **npm** (Node package manager)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/cmderdev/cmderdev.github.io.git
   cd cmderdev.github.io
   ```

2. **Install Ruby dependencies**
   ```bash
   bundle install
   ```

3. **Install Node.js dependencies**
   ```bash
   npm install
   ```

### Building the Site

**Build CSS from SCSS:**
```bash
npm run build
```

This will:
1. Compile SCSS to CSS
2. Add vendor prefixes with Autoprefixer
3. Minify the CSS output

**Build Jekyll site:**
```bash
bundle exec jekyll build
```

The site will be generated in the `_site` directory.

**Serve locally for development:**
```bash
bundle exec jekyll serve
```

Visit `http://localhost:4000` to view the site.

### Development Workflow

**Watch SCSS files for changes:**
```bash
npm run watch
```

This will automatically rebuild CSS when SCSS files are modified.

**Run linters:**
```bash
npm run lint:scss   # Lint SCSS files
npm run lint:html   # Lint HTML files
npm test           # Run all linters and build CSS
```

## Project Structure

```
cmderdev.github.io/
├── .github/
│   └── workflows/
│       └── ci.yml          # GitHub Actions CI pipeline
├── css/
│   ├── main.css           # Compiled CSS (expanded)
│   └── main.min.css       # Compiled CSS (minified)
├── scss/
│   └── main.scss          # Source SCSS with CSS variables
├── img/                   # Images and assets
├── script/
│   └── cibuild           # CI build script
├── index.html            # Main HTML page
├── package.json          # Node.js dependencies
├── Gemfile              # Ruby dependencies
└── README.md            # This file
```

## CSS Architecture

The site uses modern CSS practices:

- **CSS Variables** - All colors, spacing, and typography use CSS variables for easy theming
- **No Vendor Prefixes** - Autoprefixer automatically adds them during build
- **Smooth Transitions** - Performant animations on hover and interactions
- **Dark Mode** - Automatic dark mode support via `prefers-color-scheme`
- **Mobile-First** - Responsive design for all screen sizes

## Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Make your changes
4. Run tests (`npm test`)
5. Commit your changes (`git commit -m 'Add amazing feature'`)
6. Push to the branch (`git push origin feature/amazing-feature`)
7. Open a Pull Request

### Contribution Guidelines

- Follow the existing code style
- Test your changes locally before submitting
- Ensure all linters pass
- Update documentation if needed
- Keep commits focused and atomic

## Testing

The CI pipeline automatically runs:

1. **SCSS Linting** - Validates SCSS syntax and style
2. **HTML Linting** - Validates HTML structure
3. **CSS Build** - Ensures CSS compiles without errors
4. **Jekyll Build** - Validates site generation
5. **Link Checking** - Verifies all links work (html-proofer)

Run tests locally:
```bash
npm test                      # Run all linters
bundle exec jekyll build      # Build site
bundle exec htmlproofer ./_site --disable-external  # Check links
```

## Browser Support

We target all modern browsers:

- Chrome (last 2 versions)
- Firefox (last 2 versions)
- Safari (last 2 versions)
- Edge (last 2 versions)

Legacy browser support (IE11 and below) is not provided.

## License

This website is part of the Cmder project. For information about Cmder itself, visit the [main repository](https://github.com/cmderdev/cmder).

## Maintainers

- [Samuel Vasko](https://github.com/samvasko) - Creator
- [Martin Kemp](https://github.com/MartiUK) - Maintainer
- [The cmderdev team](https://github.com/cmderdev) - Core team
- [All contributors](https://github.com/cmderdev/cmder/graphs/contributors)

## Links

- **Website**: [https://cmder.app](https://cmder.app)
- **Main Repository**: [https://github.com/cmderdev/cmder](https://github.com/cmderdev/cmder)
- **Issues**: [https://github.com/cmderdev/cmder/issues](https://github.com/cmderdev/cmder/issues)
- **Wiki**: [https://github.com/cmderdev/cmder/wiki](https://github.com/cmderdev/cmder/wiki)

---

Made with ❤️ by the Cmder community
