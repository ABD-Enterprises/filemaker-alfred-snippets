# Usage Guide

This collection uses a consistent naming convention to make snippets easy to remember and prevent accidental triggers during normal typing.

## Naming Convention

All triggers in this collection start with `;fm` followed by the function name or category abbreviation. 

The semicolon (`;`) is used as a prefix because it is rarely typed immediately before letters in normal prose, reducing the chance of accidental expansion.

**Example:** `;fmlet` for the `Let` function.

## Examples by Category

The expansions below are copied from `data/FileMaker_Functions_Alfred_Snippets.csv`, the source of the bundle. Some snippets expand to the function name with empty parentheses, such as `JSONSetElement (  )`.

### Logic
- `;fmif` → `If ( test ; resultIfTrue ; resultIfFalse )`
- `;fmcase` → a multi-line `Case ( test1 ; result1 ; test2 ; result2 ; defaultResult )` block
- `;fmlet` → a multi-line `Let ( [ var = value ] ; result )` block

### Text
- `;fmsub` → `Substitute ( text ; [ searchString ; replacementString ] )`
- `;fmpos` → `Position ( text ; searchString ; start ; occurrence )`
- `;fmmiddlewords` → `MiddleWords (  )`

### JSON
- `;fmjsonsetelement` → `JSONSetElement (  )`
- `;fmjsongetelement` → `JSONGetElement (  )`
- `;fmjsonlistkeys` → `JSONListKeys (  )`

### SQL
- `;fmsql` → `ExecuteSQL ( "SELECT field FROM table WHERE id = ?" ; "" ; "" ; id )`

### Dates
- `;fmdatefn` → `Date ( month ; day ; year )`
- `;fmgetcurrentdate` → `Get ( CurrentDate )`

### Lists
- `;fmgetvalue` → `GetValue ( listOfValues ; valueNumber )`
- `;fmvaluecount` → `ValueCount ( listOfValues )`

## Editing Snippets

If you want to customize the snippets or change the triggers after importing them:
1. Open **Alfred Preferences**.
2. Navigate to **Features** > **Snippets**.
3. Select the `FileMaker Functions` collection.
4. Double-click any snippet to edit its name, keyword (trigger), or snippet text.
