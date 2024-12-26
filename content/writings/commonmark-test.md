+++
title = "CommonMark and Pulldown-cmark Comprehensive Test Template"
description = "A comprehensive test file for all CommonMark elements and Pulldown-cmark extensions"
date = 2024-11-09
[taxonomies]
tags = ["commonmark", "pulldown-cmark", "first"]
+++

<!-- 
This test template covers:
1. All CommonMark standard elements
2. Pulldown-cmark extensions (GFM tables, footnotes, task lists, strikethrough)
3. Edge cases and nested combinations
4. Various formatting scenarios
-->

# Headings

<!-- Testing all heading levels -->
# Heading Level 1
## Heading Level 2
### Heading Level 3
#### Heading Level 4
##### Heading Level 5
###### Heading Level 6

<!-- Testing alternate heading syntax -->
Heading Level 1
==============

Heading Level 2
--------------

# Paragraphs and Text Formatting

<!-- Testing basic paragraph separation -->
This is the first paragraph with plain text.

This is the second paragraph with plain text.

<!-- Testing inline formatting -->
*This text is italicized* and _this is also italicized_

**This text is bold** and __this is also bold__

***This text is bold and italic*** and ___this is also bold and italic___

<!-- Testing strikethrough (Pulldown-cmark extension) -->
~~This text is struck through~~

<!-- Testing code spans -->
Use `inline code` within text

<!-- Testing combinations -->
**Bold text with `inline code` inside**
*Italic text with `inline code` inside*
~~Strikethrough text with `inline code` inside~~
***`code` bold italic*** and ***bold italic `code`***

# Links and References

<!-- Testing various link types -->
[Basic link](https://example.com)
[Link with title](https://example.com "Link title")
<https://example.com>
<user@example.com>

<!-- Testing reference-style links -->
[Reference link][1]
[Reference link with text][reference text]
[Shorthand reference]

[1]: https://example.com
[reference text]: https://example.com "Optional title"
[shorthand reference]: https://example.com

# Lists

<!-- Testing unordered lists -->
* First item
* Second item
* Third item

<!-- Testing ordered lists -->
1. First item
2. Second item
3. Third item

<!-- Testing nested lists -->
* First level
  * Second level
    * Third level
      * Fourth level
        * Fifth level
          * Sixth level

<!-- Testing mixed nested lists -->
1. First ordered item
   * Unordered sub-item
     1. Ordered sub-sub-item
        * Mixed nesting
2. Second ordered item
   1. Ordered sub-item
      * Unordered sub-sub-item

<!-- Testing task lists (Pulldown-cmark extension) -->
- [ ] Unchecked task
- [x] Checked task
  - [ ] Nested unchecked task
  - [x] Nested checked task

# Code Blocks

<!-- Testing fenced code blocks with language -->
```rust
fn main() {
    println!("Hello, world!");
    let x = 42;
    let y = String::from("Test");
}
```

<!-- Testing fenced code block without language -->
```
Plain code block
No syntax highlighting
Multiple lines
```

<!-- Testing indented code blocks -->
    This is an indented code block
    It continues here
    And here

# Blockquotes

<!-- Testing basic blockquotes -->
> This is a blockquote
> It continues here

<!-- Testing nested blockquotes -->
> First level
>> Second level
>>> Third level
>>>> Fourth level

<!-- Testing blockquotes with other elements -->
> # Heading in blockquote
> 
> * List in blockquote
> * Second item
> 
> ```
> Code block in blockquote
> ```

# Tables (GFM Extension)

<!-- Testing basic table -->
| Header 1 | Header 2 | Header 3 |
|----------|----------|----------|
| Cell 1   | Cell 2   | Cell 3   |
| Cell 4   | Cell 5   | Cell 6   |

<!-- Testing aligned table -->
| Left | Center | Right | AAA | BBB | CCC | DDD | EEE | FFF | GGG | HHH | III | JJJ | KKK | LLL | MMM | NNN | OOO | PPP | QQQ | RRR | SSS | TTT | UUU | VVV | WWW | XXX | YYY | ZZZ |
|:-----|:------:|------:|:--|:--|:--|:--|:--|:--|:--|:--|:--|:--|:--|:--|:--|:--|:--|:--|:--|:--|:--|:--|:--|:--|:--|:--|:--|:--|
| Left | Center | Right | A | B | C | D | E | F | G | H | I | J | K | L | M | N | O | P | Q | R | S | T | U | V | W | X | Y | Z |

<!-- Testing complex table -->
| Format | In | Table |
|--------|:--:|-------|
| *Italic* | `code` | **Bold** |
| ~~Strike~~ | [Link](url) | > Quote |
| ==Mark== | `{color: red}` | *Mixed* **Styles** |

# Horizontal Rules

<!-- Testing various horizontal rule syntaxes -->
***

---

___

<!-- Testing horizontal rules with spacing -->
Text above

---

Text below

# Images

<!-- Testing basic image -->
![Alt text](https://example.com/image.jpg)

<!-- Testing image with title -->
![Alt text](https://example.com/image.jpg "Image title")

<!-- Testing reference-style image -->
![Alt text][image-1]

[image-1]: https://example.com/image.jpg "Reference style image"

# Footnotes (Pulldown-cmark Extension)

<!-- Testing footnotes -->
Here's a sentence with a footnote[^1].

Here's another sentence with a longer footnote[^2].

[^1]: This is the footnote.
[^2]: This is a longer footnote with multiple paragraphs.

    Subsequent paragraphs are indented to be part of the footnote.

    ```
    Even code blocks can be in footnotes
    ```

# Special Characters and Escaping

<!-- Testing escaping markdown characters -->
\*Not italic\*
\**Not bold\**
\[Not a link\](http://example.com)
\`Not code\`

<!-- Testing HTML entities -->
&copy; Copyright
&nbsp; Non-breaking space
&lt; Less than
&gt; Greater than
&amp; Ampersand

# HTML Tags (if supported by your configuration)

<!-- Testing basic HTML -->
<div class="custom-class">
  <p>Custom HTML paragraph</p>
  <span>Inline HTML</span>
</div>

<!-- Testing HTML with markdown inside -->
<div>
  *This markdown should be processed*
  
  **This too**
</div>

# Edge Cases and Complex Combinations

<!-- Testing deeply nested combinations -->
> * First level list in blockquote
>   1. Ordered sublist
>      * Unordered sub-sublist
>        ```
>        Code block in deep nest
>        ```
>        > Blockquote in list
>        > * List in blockquote in list
>        >   * Deeper nesting

<!-- Testing inline combinations -->
***~~`code in bold italic strikethrough`~~***

**_`code in bold italic different syntax`_**

[*Italic link*](https://example.com)

[**Bold link with `code` and *italic***](https://example.com)

<!-- Testing list item continuation -->
1. First item
   
   Second paragraph in first item

2. Second item
   > Blockquote in list
   ```
   Code block in list
   ```

# Mathematical Notations (if supported)

<!-- Testing inline math -->
This is an inline equation: $E = mc^2$

<!-- Testing block math -->
$$
\frac{d}{dx}\left( \int_{0}^{x} f(u)\,du\right)=f(x)
$$

<!-- END OF TEST TEMPLATE -->

<!--
This template includes all standard CommonMark elements and Pulldown-cmark extensions.
When styling your theme, make sure to test:
1. All elements in light and dark mode (if applicable)
2. Mobile responsiveness
3. Print stylesheets
4. Accessibility features
5. Different viewport sizes
-->
