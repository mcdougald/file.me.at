<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/assets/hero-dark.png">
    <img src=".github/assets/hero.png" alt="file.me.at landing page" width="880">
  </picture>
</p>

# file.me.at

Edit PDFs without uploading them.

File is a PDF toolbox that runs in your browser. Merge, split, compress, rotate, protect and clean PDFs on your own device: the tools make no request carrying your file, there is no sign-in or server queue, and nothing is stored after you close the tab. For scripts and servers, a separate conversion API does the same work server-side.

## Features

- **14 browser tools**: merge, split, extract pages, delete pages, reorder and rotate; compress (lossless, balanced or small), optimise and strip metadata; protect (AES-256 with permissions) and unlock; watermark and page numbers; images (JPEG/PNG) to PDF.
- **Files never leave your device**: every tool runs in a Web Worker on an MIT-licensed PDF engine. No account, no upload, and it works offline.
- **The same checks as the server sandbox**: the PDF header check, page and object limits and password rules used for untrusted files run before a file is opened.
- **Passwords are never silently stripped**: a locked PDF opened with its password comes back locked with the same password. Only the Unlock tool removes encryption.
- **A conversion matrix you can trust**: a format pair is listed only when a written acceptance contract says what a correct conversion preserves and the engine passes it. Nothing is greyed out as coming soon.
- **Conversion API**: a stateless endpoint that takes a file and answers with the result (one file, or a ZIP for several), with nothing written to disk. In the hosted mode it is metered in credits with a spend cap and usage alerts; a self-host mode runs it without identity or metering.
- **Self-hostable**: the identical toolbox can run inside your own network.

## Screenshots

<table>
  <tr>
    <td width="50%"><picture><source media="(prefers-color-scheme: dark)" srcset=".github/assets/formats-dark.png"><img src=".github/assets/formats.png" alt="Formats"></picture><br><sub>Formats: the conversion matrix, accepted pairs only</sub></td>
    <td width="50%"><picture><source media="(prefers-color-scheme: dark)" srcset=".github/assets/pricing-dark.png"><img src=".github/assets/pricing.png" alt="Pricing"></picture><br><sub>Pricing: free tools, a paid API, and self-hosting</sub></td>
  </tr>
</table>

## Built with

- Next.js 16 (App Router), React 19, TypeScript
- Tailwind CSS 4
- `@cantoo/pdf-lib` running in a Web Worker
- oRPC with TanStack Query
- Drizzle ORM with Postgres
- Better Auth
- next-intl

## Part of the me.at family

file.me.at is one of my [`*.me.at`](https://me.at) apps. They share one design system, account, and app shell. Development happens in a private monorepo; this repository is the project's public-facing home.

## License

See [LICENSE](LICENSE).
