# Usage Guide

This collection uses a consistent naming convention to make snippets easy to remember and prevent accidental triggers during normal typing.

## Naming Convention

All triggers in this collection start with `;fm` followed by the function name or category abbreviation. 

The semicolon (`;`) is used as a prefix because it is rarely typed immediately before letters in normal prose, reducing the chance of accidental expansion.

**Example:** `;fmlet` for the `Let` function.

## Examples by Category

### Logic
- `;fmif` → `If ( test ; result1 {; result2} )`
- `;fmcase` → `Case ( test1 ; result1 {; test2 ; result2 ; ... ; defaultResult} )`
- `;fmlet` → `Let ( {[} var1 = expression1 {; var2 = expression2...]} ; calculation )`

### Text
- `;fmsub` → `Substitute ( text ; searchString ; replaceString )`
- `;fmpos` → `Position ( text ; searchString ; start ; occurrence )`
- `;fmmiddle` → `Middle ( text ; start ; numberOfCharacters )`

### JSON
- `;fmjsonset` → `JSONSetElement ( json ; keyOrIndexOrPath ; value ; type )`
- `;fmjsonget` → `JSONGetElement ( json ; keyOrIndexOrPath )`
- `;fmjsonlist` → `JSONListKeys ( json ; keyOrIndexOrPath )`

### SQL
- `;fmsql` → `ExecuteSQL ( sqlQuery ; fieldSeparator ; rowSeparator {; arguments...} )`

### Variables
- `;fmgv` → `$$GlobalVariable`
- `;fmlv` → `$LocalVariable`

### Dates
- `;fmdate` → `Date ( month ; day ; year )`
- `;fmgcdc` → `Get ( CurrentDate )`

### Lists
- `;fmgetv` → `GetValue ( listOfValues ; valueNumber )`
- `;fmvc` → `ValueCount ( listOfValues )`

## Editing Snippets

If you want to customize the snippets or change the triggers after importing them:
1. Open **Alfred Preferences**.
2. Navigate to **Features** > **Snippets**.
3. Select the `FileMaker Functions` collection.
4. Double-click any snippet to edit its name, keyword (trigger), or snippet text.
