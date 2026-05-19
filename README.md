# FlagAI – Chrome Extension

> Flag YouTube channels that publish AI-generated music.

FlagAI is an open-source Chrome extension that automatically marks YouTube channels known for publishing AI-generated music, sourced from a dedicated backend API.

## Stack

| Layer | Tech |
|---|---|
| Language | TypeScript |
| Bundler | Vite + CRXJS |
| Manifest | V3 |
| Package manager | pnpm |

## Project structure

```
flagAI/
├── src/
│   ├── background/   # Service worker (MV3)
│   ├── content/      # Content scripts injected on youtube.com
│   ├── popup/        # Browser action popup
│   ├── options/      # Extension options page
│   ├── types/        # Shared TypeScript types
│   └── utils/        # Shared utilities
├── public/
│   └── icons/        # Extension icons (16, 32, 48, 128px)
├── manifest.json     # Chrome Extension Manifest V3
├── vite.config.ts
└── tsconfig.json
```

## Getting started

```bash
# Install dependencies
pnpm install

# Development build with watch mode
pnpm dev

# Production build
pnpm build
```

Then load `dist/` as an unpacked extension in `chrome://extensions`.

## Environment variables

Copy `.env.example` to `.env` and fill in the values:

```bash
cp .env.example .env
```

## Contributing

Pull requests are welcome. Please open an issue first to discuss what you would like to change.

## License

[MIT](./LICENSE)
