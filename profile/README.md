<!-- If you have a banner image from Canva, uncomment and replace the URL:
<p align="center">
  <img src="https://raw.githubusercontent.com/VitaeFlow/.github/main/profile/banner.png" alt="VitaeFlow" width="100%" />
</p>
-->

<h1 align="center">VitaeFlow</h1>

<p align="center">
  <strong>Open standard for machine-readable resumes in PDF</strong>
</p>

<p align="center">
  <a href="https://vitaeflow.org">Website</a> &nbsp;&bull;&nbsp;
  <a href="https://vitaeflow.org/docs/">Getting Started</a> &nbsp;&bull;&nbsp;
  <a href="https://vitaeflow.org/tools/">Try the Tools</a>
</p>

---

A VitaeFlow PDF looks like any normal resume to a human reader, but it also contains structured JSON data that ATS, job boards, and HR tools can extract instantly — no parsing heuristics, no guessing.

```
  Resume PDF  +  Structured JSON  →  .vf.pdf
  (visual)       (machine-readable)   (both)
```

The `.vf.pdf` suffix is recommended for discoverability, but not required.

## How it works

VitaeFlow embeds a JSON file inside the PDF using the PDF/A-3 standard — the same mechanism used by [Factur-X](https://fnfe-mpe.org/factur-x/) for electronic invoices. The PDF remains readable by any viewer. Tools that understand VitaeFlow extract the data; others simply ignore it.

## Repositories

| Repository | Description | |
|---|---|---|
| [vitaeflow-spec](https://github.com/VitaeFlow/vitaeflow-spec) | JSON schema and PDF embedding standard | [![Schema: Draft v0.1](https://img.shields.io/badge/schema-draft_v0.1-teal.svg)](https://github.com/VitaeFlow/vitaeflow-spec) |
| [vitaeflow-js](https://github.com/VitaeFlow/vitaeflow-js) | JavaScript/TypeScript SDK — validate, embed, extract | [![npm](https://img.shields.io/npm/v/@vitaeflow/sdk.svg)](https://www.npmjs.com/package/@vitaeflow/sdk) |
| [vitaeflow-cli](https://github.com/VitaeFlow/vitaeflow-cli) | Command-line tool | [![npm](https://img.shields.io/npm/v/vitaeflow.svg)](https://www.npmjs.com/package/vitaeflow) |
| [vitaeflow-web](https://github.com/VitaeFlow/vitaeflow-web) | Website and interactive tools | [vitaeflow.org](https://vitaeflow.org) |

## Quick start

```bash
npm install @vitaeflow/sdk
```

```ts
import { embedResume, extractResume } from '@vitaeflow/sdk';

// Embed structured data into a PDF
const vfPdf = await embedResume(pdfBytes, {
  version: '0.1',
  profile: 'standard',
  basics: { givenName: 'Marie', familyName: 'Laurent', email: 'marie@example.com' },
});

// Extract it back
const result = await extractResume(vfPdf);
console.log(result.resume.basics.givenName); // "Marie"
```

## Contributing

VitaeFlow is open source and contributions are welcome. Check out the individual repos above or open a discussion if you have ideas.

## License

All VitaeFlow projects are released under the [MIT License](https://opensource.org/licenses/MIT).
