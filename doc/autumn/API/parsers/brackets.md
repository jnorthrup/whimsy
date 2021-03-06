# Matching Bracketed and Comma-Separated Content

These parsers are defined in the file [Brackets.kt].

[Brackets.kt]: /norswap/autumn/parsers/Brackets.kt

### `brackets`

    inline fun Grammar.brackets(left: String, right: String, crossinline p: Parser): Boolean
    
Matches `p` bracketed by `left` and `right`. Uses [`word`] to match `left` and `right`.

### `angles`

    inline fun Grammar.angles (crossinline p: Parser): Boolean
    
Matches `p` bracketed by angle brackets. Uses [`word`] for matching the brackets.

### `squares`

    inline fun Grammar.angles (crossinline p: Parser): Boolean

Matches `p` bracketed by square brackets. Uses [`word`] for matching the brackets.

### `curlies`

    inline fun Grammar.curlies (crossinline p: Parser): Boolean

Matches `p` bracketed by curly brackets. Uses [`word`] for matching the brackets.

### `parens`

    inline fun Grammar.parens (crossinline p: Parser): Boolean

Matches `p` bracketed by parens. Uses [`word`] for matching the parens.

### `angles` (empty)

    fun Grammar.angles(): Boolean
    
Matches an empty set of angles brackets, potentially separated and/or followed by whitespace.

### `squares` (empty)

    fun Grammar.squares(): Boolean

Matches an empty set of square brackets, potentially separated and/or followed by whitespace.

### `curlies` (empty)

    fun Grammar.curlies(): Boolean

Matches an empty set of curly brackets, potentially separated and/or followed by whitespace.

### `parens` (empty)

    fun Grammar.parens(): Boolean

Matches an empty set of parens, potentially separated and/or followed by whitespace.

### `comma_list0`

    inline fun Grammar.comma_list0 (crossinline item: Parser): Boolean
    
Matches a possibly-empty comma-separated list of `item`. Uses [`word`] to match the commas.

### `comma_list1`

    inline fun Grammar.comma_list1 (crossinline item: Parser): Boolean
    
Matches a non-empty comma-separated list of `item`. Uses [`word`] to match the commas.

### `comma_list_term0`

    inline fun Grammar.comma_list_term0 (crossinline item: Parser): Boolean

Matches a possibly-empty comma-separated list of `item`. Uses [`word`] to match the commas.
An additional comma is allowed at the end.

### `comma_list_term1`

    inline fun Grammar.comma_list_term1 (crossinline item: Parser): Boolean
    
Matches a non-empty comma-separated list of `item`. Uses [`word`] to match the commas.
An additional comma is allowed at the end.

[`word`]: chars.md#word