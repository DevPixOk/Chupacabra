# Chupacabra

**Multilingual web, SEO and document intelligence auditor.**

Chupacabra crawls website structures, checks URL availability, identifies broken or suspicious links, analyzes digital marketing and SEO signals, discovers downloadable resources, maps document collections, downloads selected files, and generates clear reports for technical and non-technical users.

Chupacabra Marketing Community is designed to make a website audit understandable, not just exhaustive. The goal is to show **what was found, what is wrong, why it matters, and what can be done next**.

## Main capabilities

### Web crawling and URL auditing

- Crawls internal HTML pages starting from a user-defined URL.
- Records HTTP status codes and final URLs.
- Detects redirects.
- Identifies 404/410 responses, 4xx and 5xx errors.
- Reports timeouts, DNS failures, SSL/TLS errors and connection failures.
- Flags suspected soft 404 pages.
- Records where a link was discovered.
- Measures response time.
- Reports crawl coverage and distinguishes discovered URLs from effectively tested resources.
- Supports unlimited crawling when the page limit is blank or set to `0`.

### Digital Marketing and SEO

Chupacabra can collect and review signals such as:

- Page title and title length.
- Meta description and description length.
- H1 structure.
- Declared HTML language.
- Canonical URL.
- Meta robots directives.
- Internal and external links.
- Images without ALT text.
- Crawl depth.
- Indexability-related signals.
- Objective problems separated from improvement opportunities.

An HTTP `200` response means that a resource is available. It does **not** automatically mean that the page has no SEO, content or accessibility issues.

## Document intelligence

Chupacabra is not limited to HTML pages. It can discover and organize many types of resources, including:

- PDF
- Word and OpenDocument files
- Excel, CSV and spreadsheet formats
- PowerPoint and presentation formats
- Images
- ZIP and other compressed files
- Text, XML, JSON, YAML and other data formats
- Audio and video
- E-books

The application builds a hierarchical view of the discovered website and document collection, showing how pages and files are related.

## File downloads

Discovered files can be selected and downloaded while preserving the website's logical structure.

The downloader:

- Follows redirects.
- Uses server-provided filenames when available.
- Handles URLs where the visible path does not end with the real filename.
- Verifies downloaded byte counts when the server provides a content length.
- Avoids silently overwriting different files.
- Logs successful and failed downloads.
- Can create a ZIP archive of downloaded resources.
- Remembers recently used download folders locally.

## Reports and exports

Chupacabra can produce:

- HTML audit reports
- Excel workbooks
- CSV audit data
- TXT site/document structures
- Detailed execution logs
- An AI analysis prompt based on the audit data

Generated reports are intended to be self-explanatory. Findings can include the affected URL, problem category, severity, evidence or observed condition, explanation and recommended action.

Exported files follow a consistent naming pattern:

```text
Relatório_<site>_<type>_<date_time>.<extension>
```

Reports and logs include the Chupacabra version and audit date/time where supported.

## AI analysis prompt

Chupacabra can generate a structured prompt for use with an AI assistant.

The prompt can include:

- Audit scope and metadata.
- Crawl coverage and limitations.
- Inaccessible URLs and reasons.
- Objective technical problems.
- Marketing and SEO findings.
- Document inventory and structure.
- Suggested prioritization and manual checks.

The generated prompt explicitly distinguishes metadata from document content. Listing a PDF or other file does not imply that the AI has read its contents.

## Multilingual design

Chupacabra uses the **Grimoire** localization layer and is being prepared for a broad multilingual interface. The project target is **30 languages**, including full coverage of interface messages, help, audit terminology, reports and user guidance.

Translations are maintained separately from the application logic so that new audit features can be localized consistently.

## Community Edition and sponsorship

Chupacabra Marketing Community is intended to remain useful as a free edition.

The interface can display a small sponsorship area. When no external sponsor is configured, the area can promote and link back to the Chupacabra project on GitHub.

Advertising is not intended to be embedded inside professional audit reports.

## Privacy

Chupacabra's URL and download-folder histories are local convenience features. Local history, temporary files, partial downloads and environment-specific configuration should not be committed to the public repository.

Users should review organizational policies before auditing authenticated, restricted, confidential or third-party websites.

## Current limitations

Crawl coverage cannot prove that every URL existing on a server has been discovered. A website may contain resources that are:

- Orphaned and not linked from crawled pages.
- Listed only in XML sitemaps.
- Generated through JavaScript.
- Available only after form submission.
- Protected by authentication.
- Excluded by crawl scope or site rules.

Future development may expand sitemap comparison, JavaScript-aware discovery, crawl comparison and deeper technical SEO checks.

## Running from source

The current development version is a Python desktop application.

Typical dependencies include:

```text
requests
beautifulsoup4
lxml
pandas
Pillow
```

Optional Excel support can use `openpyxl`. Current development versions also include a fallback XLSX writer for environments where `openpyxl` is not installed.

Keep the project files, assets, localization catalog and `grimoire.py` together according to the repository structure.

A typical development run is:

```powershell
py main.py
```

The exact filename may change between development versions until a stable release package is published.

## Responsible use

Only crawl websites and resources that you are authorized to access. Respect applicable website terms, authentication requirements, infrastructure limits and organizational security policies.

For large websites, operators should consider crawl load, server capacity and request frequency before running unrestricted audits.

## Project status

Chupacabra is under active development. Features, report formats and localization coverage may change before a stable release.

Issues and suggestions are welcome through the repository's issue tracker.

## License

Chupacabra is distributed under the **GNU General Public License v3.0 (GPL-3.0)**. See the `LICENSE` file in this repository for the complete terms.

## Repository

**DevPixOk / Chupacabra**

Project home: https://github.com/DevPixOk/Chupacabra

---

Built as a DevPixOk community project for clearer web, SEO and document intelligence auditing.
