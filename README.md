# Flash Player Emulator (TypeScript)

## Overview

This project aims to provide a modern Flash Player emulator written in **TypeScript**.  
It allows executing SWF files directly in a browser without depending on the legacy Flash plugin.  
The adopted approach focuses on **maintainability**, **progressive compatibility**, and openness to **community contribution**.

## Project Goals

- Execute Flash animations, games, and applications directly in modern browsers
- Provide a modular and extensible architecture
- Ensure good performance using TypeScript and modern web APIs
- Serve as an educational and technical foundation for understanding Flash internals

## Installation

### Prerequisites

- [Node.js](https://nodejs.org/) (version 18 or higher recommended)
- [npm](https://www.npmjs.com/) (included with Node.js)

### Steps

```bash
# Clone the repository
git clone https://github.com/<organization>/<repo>.git
cd <repo>

# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build
```

## Available Scripts

- `npm run dev` : starts the development server with hot-reload
- `npm run build` : generates the optimized production bundle
- `npm run lint` : analyzes code with ESLint
- `npm run test` : runs unit tests
- `npm run format` : applies Prettier for code formatting

## Project Structure

```
.
├── src/              # Main source code
│   ├── core/         # Execution engine (parsing, VM, rendering)
│   ├── swf/          # SWF file handling and parsing
│   ├── render/       # Graphics rendering (Canvas, WebGL, DOM)
│   ├── audio/        # Audio management
│   └── utils/        # Utility functions
├── tests/            # Unit and integration tests
├── public/           # Static files (HTML, CSS, example SWF files)
├── package.json
├── tsconfig.json
└── README.md
```

## Development Conventions

### Branches

- `main` : stable version ready for deployment
- `develop` : main development branch
- `feature/<name>` : for each new feature
- `fix/<name>` : for bug fixes
- `release/<version>` : preparing a stable release

### Commits

Follow this format:

```
<type>(<scope>): <message>
```

**Examples:**

- `feat(core): add SWF tag parsing`
- `fix(audio): fix audio desynchronization`
- `docs(readme): add installation instructions`

**Common types:**

- `feat` : new feature
- `fix` : bug fix
- `docs` : documentation
- `test` : adding or modifying tests
- `refactor` : code improvement without adding functionality
- `chore` : maintenance

### Push Rules

- Always create a dedicated branch before developing
- Create pull requests to `develop`
- Pull requests must be reviewed and approved by at least one team member
- Squash & merge recommended to maintain clean history

## Contributing

### Process

1. Fork the project
2. Create a branch `feature/my-feature`
3. Develop and add associated tests
4. Check code style with `npm run lint && npm run format`
5. Create a pull request to `develop`

### Best Practices

- Code in strict TypeScript
- Add unit tests for each new feature
- Document code with clear comments
- Verify compatibility with existing examples

## Testing

Tests are written with **Jest**.

Run tests:

```bash
npm run test
```

## License

This project is licensed under the **MIT License**.  
This means you can use, modify, and distribute it freely, provided you retain the license notice and copyright.

## Roadmap

- [ ] SWF file parsing (binary format, tags, metadata)
- [ ] Display engine implementation (Canvas then WebGL)
- [ ] Audio management
- [ ] ActionScript Virtual Machine implementation
- [ ] Cross-browser compatibility
- [ ] Integrated debugging tools