# HW Engineer Portfolio

A portfolio website for Hardware Engineers, powered by **Notion as CMS**. Write projects in Notion, and they automatically appear on the website.

## Tech Stack

- **Framework**: Next.js 15.5.3 (App Router + Turbopack)
- **Language**: TypeScript 5
- **Styling**: TailwindCSS v4 + shadcn/ui
- **CMS**: Notion API (@notionhq/client)
- **Icons**: Lucide React
- **Deployment**: Vercel

## Features

- Notion database as content management system
- Project listing with thumbnail, title, category, and tags
- Category filtering and keyword search
- Project detail page with full Notion block rendering (text, images, code, YouTube embeds)
- Fully responsive design (mobile / tablet / desktop)

## Getting Started

### Prerequisites

- Node.js 18+
- Notion API key and database ID

### Installation

```bash
npm install
```

### Environment Variables

Create a `.env.local` file:

```env
NOTION_API_KEY=your_notion_api_key
NOTION_DATABASE_ID=your_notion_database_id
```

### Development

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

### Build

```bash
npm run build
```

### Lint & Format

```bash
npm run check-all    # typecheck + lint + format check
```

## Notion Database Schema

| Property  | Type           | Description                              |
|-----------|----------------|------------------------------------------|
| Title     | Title          | Project title                            |
| Category  | Select         | e.g., PCB Design, Firmware, Testing      |
| Tags      | Multi-select   | e.g., Arduino, FPGA, Oscilloscope        |
| Published | Checkbox       | Whether to show on the website           |
| Status    | Select         | Completed, In Progress, etc.             |
| Thumbnail | Files & media  | Project cover image                      |

## Project Structure

```
src/
├── app/              # Next.js App Router pages
├── components/       # React components
│   ├── ui/           # shadcn/ui components
│   └── ...           # Feature components
├── lib/              # Utilities and configurations
└── styles/           # Global styles
```

## Documentation

- [PRD (Product Requirements Document)](./docs/PRD.md)
- [Project Structure Guide](./docs/guides/project-structure.md)
- [Styling Guide](./docs/guides/styling-guide.md)
- [Component Patterns](./docs/guides/component-patterns.md)

## License

Private
