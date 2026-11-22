# Reader

View and print `.ptrn` patterns in the browser. Think of it as what Adobe Reader originally was for PDFs: a free, simple way to open the file and get it onto paper.

Planned home: [read.ptrnformat.org](https://read.ptrnformat.org) · Status: **planning**

## What it does

- Opens a `.ptrn` file in the browser and displays the pattern for the person making it.
- Prints the pattern. Printing is the main use, so the print layout matters as much as the screen layout.
- Shows the shared envelope for any craft: title, designer, materials, gauge, sizes, text and images.
- Shows the pattern body for crochet and knitting. Specialty forms (Tunisian, loom knitting and so on) come later.
- Shows stitch names in US or UK terms, whichever the reader picks.
- Shows the written rows when a file has no stitch graph, so a file with no graph still reads and prints.

## What it doesn't do

- **No checking.** It doesn't recount rows or flag mismatches. Correct counts are the designer's job, and Writer handles them.
- **No row tracking.** No progress, counters or notes. Reader is a viewer, not a project tracker.
- **No editing.** Use [Writer](https://github.com/ptrnformat/writer).
- **No offline promise.** It's a web tool.

## How it works

- Browser-first. The file is opened locally and is not uploaded anywhere. This matters to designers who worry about their patterns being copied.
- Reads files through [`ptrn-js`](https://github.com/ptrnformat/ptrn-js), so it shares parsing with the other tools.

## Open questions

- **Print layout.** The spec says readers decide how a pattern looks. Reader's layout will probably become the one people think of as "what PTRN looks like", so it needs careful design.
- **Spec conflict on recounting.** The spec currently says readers *must* recount and flag mismatches. It needs to say *may*, or Reader won't conform.
- **Draft files.** Whether Reader should show a notice for files that came straight from Converter or were saved without a graph. This depends on whether the spec adds a draft flag (see Writer).
- **Charts and symbols.** How charts and CYC symbols render in print.

## Decisions

Decisions and the reasons behind them are logged in [DECISIONS.md](DECISIONS.md).

## License

[Apache 2.0](LICENSE)
