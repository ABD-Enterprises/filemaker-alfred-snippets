# FileMaker Alfred Snippets

Alfred snippets for common Claris FileMaker functions and syntax patterns.

## What is this?
This repository provides a collection of Alfred snippets designed specifically for Claris FileMaker developers. It allows you to quickly insert common FileMaker calculation functions, SQL syntax, JSON patterns, and more, directly into the FileMaker calculation dialog or any code editor.

## Who is it for?
Claris FileMaker developers using macOS and the [Alfred](https://www.alfredapp.com/) productivity app (with the Powerpack enabled) who want to speed up their workflow by typing short triggers instead of writing out full function names or syntax.

## Installation

1. Download the [`FileMaker_Functions.alfredsnippets`](FileMaker_Functions.alfredsnippets) file from this repository.
2. Double-click the file to import it into Alfred.
3. Ensure the Snippets feature is enabled in Alfred's preferences.

For more detailed instructions, see [INSTALL.md](docs/INSTALL.md).

## Example Triggers

Here are a few examples of what you can type to trigger the snippets:

- `;fmlet` → Inserts a multi-line `Let ( [ var = value ] ; result )` statement.
- `;fmcase` → Inserts a multi-line `Case ( test1 ; result1 ; test2 ; result2 ; defaultResult )` block.
- `;fmif` → Inserts `If ( test ; resultIfTrue ; resultIfFalse )`.
- `;fmsql` → Inserts `ExecuteSQL ( "SELECT field FROM table WHERE id = ?" ; "" ; "" ; id )`.

For a full list and usage guide, see [USAGE.md](docs/USAGE.md).

## Disclaimer

**Note:** This is an unofficial community utility. It is not affiliated with, endorsed by, or associated with Claris International Inc. or FileMaker. "FileMaker" and "Claris" are trademarks of Claris International Inc.

## Helpful Links
- [Alfred Snippets Documentation](https://www.alfredapp.com/help/features/snippets/)
- [Claris FileMaker Function Reference](https://help.claris.com/en/pro-help/content/functions-reference.html)

## Contributing
Want to add a snippet or improve an existing one? See [CONTRIBUTING.md](docs/CONTRIBUTING.md).

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
