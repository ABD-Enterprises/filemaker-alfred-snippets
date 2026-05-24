# Contributing

We welcome contributions to the FileMaker Alfred Snippets collection! If you have ideas for new snippets or improvements to existing ones, please follow these guidelines.

## How to Propose New Snippets

1. **Fork the Repository:** Create your own fork of this project.
2. **Edit the Source Data:** All snippet data is maintained in the CSV file located at `data/FileMaker_Functions_Alfred_Snippets.csv`. Please make your additions or modifications in this file.
3. **Submit a Pull Request (PR):** Submit your PR against the CSV file. 

*Note: You do not need to generate the `.alfredsnippets` bundle yourself. Once the PR is approved and merged, the maintainers will regenerate and update the Alfred bundle in the repository.*

## Guidelines for Snippets

### Keyword Naming Rules
- All snippet triggers **must** start with `;fm`.
- Keep the suffix short but descriptive (e.g., `;fmlet`, `;fmjsonset`).
- Use all lowercase for the trigger.

### Avoid Conflicts
- Before submitting a new snippet, check the existing list (or CSV) to ensure the trigger keyword isn't already in use.
- Avoid creating triggers that are extremely similar and might cause confusion.

### Prefer Canonical Syntax
- Snippets should use standard Claris FileMaker syntax exactly as it appears in the official documentation (e.g., matching capitalization and spacing).
- Include optional parameters enclosed in curly braces `{}` where appropriate, mimicking FileMaker's calculation dialog auto-complete format.

## Regenerating the Alfred Bundle (Maintainers Only)
If you are a maintainer, you can generate a new `.alfredsnippets` file by importing the updated CSV into an Alfred collection, exporting the collection, and committing the new binary file to the repository.
