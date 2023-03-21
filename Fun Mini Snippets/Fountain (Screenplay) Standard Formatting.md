# Fountain Standard Formatting
> Screenplay in image below: [fountain.io](https://fountain.io/syntax#section-example)
> 
> **Table of Content**
>1. [Changes](https://github.com/Bluemoondragon07/Obsidian-amazing-snippets/edit/main/Fun%20Mini%20Snippets/Fountain%20(Screenplay)%20Standard%20Formatting.md#changes)
>2. [Code](https://github.com/Bluemoondragon07/Obsidian-amazing-snippets/edit/main/Fun%20Mini%20Snippets/Fountain%20(Screenplay)%20Standard%20Formatting.md#code)


This snippet tweaks the appearance of the Fountain plug-in in both reading and preview mode to look more consistent with the standard format for screenplays.

![](https://github.com/Bluemoondragon07/Obsidian-amazing-snippets/blob/main/Screenshots/fountain.png)



## Changes

1. Margins
    1. Mimics the standard that screenplays are to have 1-inch top, bottom, and right margins as well as a left margin of 1.5 inches.
2. Action lines
    1. Typically, you don't want to have a giant block of action lines with no spacing in-between. Typically, screenwriters will break up these blocks by inserting an empty line every 3 or 4 lines. With this snippet, determining where you should break up action lines is much easier. Pasting from a software like Celtx or Studio Binder produce identical breaks.
2. Scene Headings and Character Names
    1. This snippet shrinks the size of Scene Headings and Character names for more readability, and also to be consistent with what the final exported script will look like. Colors still follow theme heading colors, though.
4. Font
     1. This snippet includes **Courier Prime**, embedded from [CDN Fonts](https://www.cdnfonts.com/courier-prime.font). This font is used when there is a wi-fi connection. If there is no Wi-Fi connection, the current theme's monospace font is used instead (unless you have **Courier Screenplay** or **Courier Final Draft** already installed on your system).

## Code

```css
/* import font */
@import url('https://fonts.cdnfonts.com/css/courier-prime?styles=21757');

/* Fountain Code Mirror */

.fountain-source-view>.CodeMirror-wrap>.CodeMirror-scroll {
    padding: 20px !important;
    position: unset;
}

.screenplay {
    margin: 0;
    padding: 0;
    border: 0;
    font-size: 100%;
    font: inherit;
    overflow-y: hidden;
    vertical-align: baseline;
}

.screenplay {
    display: block;
}


/* Styles for Screenplain */

.screenplay {
    margin: auto !important;
    text-align: left !important;
    font-size: 12pt !important;
    font-family: 'Courier Final Draft', 'Courier Screenplay', 'Courier Prime', var(--font-monospace), Courier;
    padding: 1in 1in 1in 1.5in !important;
    width: 8in !important;
    max-width: 8in !important;
    min-width: 8in !important;
    line-height: 1 !important;

}
.screenplay > * {
    text-indent: 0px !important;
}

.screenplay>header {
    margin-bottom: 1em;
    border-bottom: 1px solid black;
}

.screenplay>footer {
    margin-top: 1em;
}

.screenplay .italic {
    font-style: italic !important;
}

.screenplay>p .bold {
    font-weight: bold !important;
}



.screenplay>br {
    clear: both;
}

.screenplay>div.action p {
    margin-top: 1em;
}


/* Dialogue */

.screenplay>.dialogue h4 {
    text-align: center;
    text-transform: uppercase;
    color: var(--h2-color) !important;
    font-weight: 600 !important;
    font-size: 12pt !important;
    margin-left: 0.5in !important;
    padding: 0px !important;
    font-family: inherit !important;
}

.screenplay>.dialogue p {
    text-align: left;
    margin-left: 1in !important;
    padding: 0px !important;
}

.underline {
    text-decoration: underline;
}

.screenplay>.dialogue .parenthetical {
    margin-left: 2.7in !important;
    padding: 0px !important;
}


/* Headers */

.screenplay>h3 {
    padding: 0px !important;
    text-transform: uppercase;
    font-weight: 700 !important;
    font-size: 12pt !important;
    text-align: left !important;
    color: var(--h1-color) !important;
    font-family: inherit !important;
}
.screenplay>h2 {
padding: 0px !important;
text-transform: uppercase;
font-weight: 600 !important;
font-size: 12pt !important;
text-align: right !important;
font-family: inherit !important;
}

/* Change mode button */

.fountain-button {
    background-color: transparent;
    margin: none;
    padding: 0px;
}

.fountain-button:hover {
    color: var(--text-a);
    background-color: transparent;
}


.markdown-reading-view:has(.screenplay) {
    --file-line-width: 100% !important;
}
.HyperMD-codeblock {
    text-align: left !important;
    font-size: 12pt !important;
    padding: 5px 1in 5px 1.5in !important;
    position: relative;
    word-wrap: break-word;
    white-space:initial;
    display: block;
    width: 8in !important;
    min-width: 8in !important;
    max-width: 8in !important;
    line-height: 1.3 !important;
}
 .cm-hmd-codeblock {
    font-family: 'Courier Prime', 'Courier New', Courier, monospace;
}
```
