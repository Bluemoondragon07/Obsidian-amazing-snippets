# Popular Color Schemes (with Style Settings)

This snippet creates a color scheme selector in Style Settings that will let you select a color scheme for your vault. 
The code is taken from the *Serenity* theme.

Included Color Schemes:
- Ayu
- Catppuccin
- Nord
- Solarized
- Everforest
- Gruvbox
- Rose Pine

The snippet also allows you to choose accent, light mode contrast, and dark mode contrast. 

My personal favorite is Ayu with medium contrast (light mode) and low contrast (dark mode).

```css
/* color scheme variable systen */
body {
    --custom-theme-tint-l: 15;
    --custom-theme-sat-l: 100%;
    --custom-theme-tint-secondary-l: 15;
    --custom-theme-sat-secondary-l: 77%;
    --custom-theme-tint-text-l: 205;
    --custom-theme-sat-text-l: 25%;
    --custom-theme-tint-d: 0;
    --custom-theme-sat-d: 20%;
    --custom-theme-tint-secondary-d: 0;
    --custom-theme-sat-secondary-d: 25%;
    --custom-theme-tint-text-d: 10;
    --custom-theme-sat-text-d: 10%;
    --custom-base-c-l: 99%;
    --custom-c-20-l: 97%;
    --custom-border-c-l: 82%;
    --custom-text-c-l: 43%;
    --custom-base-c-d: 10%;
    --custom-c-20-d: 14%;
    --custom-border-c-d: 50%;
    --custom-text-c-d: 90%;
    
}


body {

    /* base color */
    --theme-tint: 0; /* an hsl "h" value that determines the tint of the base */
    --theme-sat: 0%; /* an hsl "s" value that determines the saturation of the base tint. */

    /* secondary (sidebar, border) colors */
    --theme-tint-secondary: 0; /* hsl "h" value that determines the tint of the sidebars and borders. */
    --theme-sat-secondary: 0%; /* hsl "s" value that determines the saturation of the secondary tint */

    /* text colors */
    --theme-tint-text: 0; /* hsl "h" value that determines the tint of the text */
    --theme-sat-text: 0%; /* hsl "s" value that determines the saturation of the text color */
}

/* ==== custom color scheme =====  */

.custom-color-scheme-light.theme-light,
.custom-color-scheme-light.medium-contrast-light.theme-light,
.custom-color-scheme-light.low-contrast-light.theme-light,
.custom-color-scheme-light.high-contrast-light.theme-light {
        --theme-tint: var(--custom-theme-tint-l) !important;
        --theme-sat: var(--custom-theme-sat-l);
        --theme-tint-secondary:var(--custom-theme-tint-secondary-l) !important;
        --theme-sat-secondary:var(--custom-theme-sat-secondary-l) !important;
        --theme-tint-text: var(--custom-theme-tint-text-l) !important;
        --theme-sat-text: var(--custom-theme-sat-text-l) !important; 
        --base-c: var(--custom-base-c-l) !important;
        --c-00: var(--custom-base-c-l) !important;
        --c-05: calc(var(--custom-base-c-l) - 1.5%) !important;
        --c-10: calc(var(--custom-base-c-l) - 2%) !important;
        --c-20: var(--custom-c-20-l) !important;
        --c-25: var(--custom-border-c-l) !important;
        --c-30: var(--custom-border-c-l) !important;
        --background-modifier-border: hsl(var(--theme-tint), calc(var(--theme-sat-text) - 5%), var(--c-30)) !important;
        --c-40: var(--custom-border-c-l) !important;
        --c-50: calc(var(--custom-text-c-l) + 45%) !important;
        --c-60: calc(var(--custom-text-c-l) + 30%) !important;
        --c-70: calc(var(--custom-text-c-l) + 15%) !important;
        --c-100: var(--custom-text-c-l) !important;

}
.custom-color-scheme-dark.theme-dark,
.custom-color-scheme-dark.medium-contrast-dark.theme-dark,
.custom-color-scheme-dark.low-contrast-dark.theme-dark,
.custom-color-scheme-dark.high-contrast-dark.theme-dark {
    --theme-tint: var(--custom-theme-tint-text-d) !important;
    --theme-sat: var(--custom-theme-sat-text-d);
    --theme-tint-secondary:var(--custom-theme-tint-secondary-d) !important;
    --theme-sat-secondary:var(--custom-theme-sat-secondary-d) !important;
    --theme-tint-text: var(--custom-theme-tint-d) !important;
    --theme-sat-text: var(--custom-theme-sat-d) !important; 
    --base-c: var(--custom-base-c-d) !important;
    --c-00:  var(--custom-base-c-d) !important;
    --c-05: calc(var(--custom-base-c-d) + 2%) !important;
    --c-10: calc(var(--custom-base-c-d) + 2.5%) !important;
    --c-20: var(--custom-c-20-d) !important;
    --c-25: var(--custom-border-c-d) !important;
    --c-30: var(--custom-border-c-d) !important;
    --background-modifier-border: hsl(var(--custom-theme-tint-d), var(--custom-theme-sat-text-d), var(--c-30)) !important;
    --background-modifier-border-hover: hsl(var(--custom-theme-tint-d), calc(var(--custom-theme-sat-text-d) - 5%), var(--c-30)) !important;
    --background-modifier-border-focus: hsl(var(--custom-theme-tint-d), calc(var(--custon-theme-sat-text-d) - 5%), var(--c-30)) !important;
    --c-40: var(--custom-border-c-d) !important;
    --c-50: calc(var(--custom-text-c-d) - 20%) !important;
    --c-60: calc(var(--custom-text-c-d) - 15%) !important;
    --c-70: calc(var(--custom-text-c-d) - 10%) !important;
    --c-100: var(--custom-text-c-d) !important;
    --color-base-40: hsl(var(--custom-theme-tint-d), var(--custom-theme-sat-d), var(--custom-border-c-d)) !important;
    --background-secondary: hsl(var(--theme-tint-secondary), var(--theme-sat-secondary), var(--c-20)) !important;
}


    /* =====  contrast levels ===== */

/* == Light Mode Contrast == */

    /* low contrast */

    .theme-light.low-contrast-light {
        /* base contrast */
        /* this is the lightest "l" value */
        --base-c: 100%;
        --base-c-low: calc(var(--base-c) - 1%);
    
        /* these represent hsl "l" values. */
        --c-00:  var(--base-c-low);
    
        --c-05: calc(var(--base-c-low) - 1%);
        --c-10: calc(var(--base-c-low) - 2%);
        --c-20: calc(var(--base-c-low) - 3.5%);
    
        --c-25: calc(var(--base-c-low) - 19%);
        --c-30: calc(var(--base-c-low) - 80%);
        --c-35: calc(var(--base-c-low) - 80%);
        --c-40: calc(var(--base-c-low) - 10%);
    
        --c-50: calc(var(--text-base) + 28%);
        --c-60: calc(var(--text-base) + 19%);
        --c-70: calc(var(--text-base) + 14%);
        --c-100: calc(var(--text-base) + 7% );

        --color-base-10: hsl(var(--theme-tint), calc(var(--theme-sat) / 1.2) , var(--c-10)) !important;
        --color-base-20: hsl(var(--theme-tint-secondary), calc(var(--theme-sat-secondary) * 1.2) , var(--c-20));
        --color-base-30:  hsl(var(--theme-tint), calc(var(--theme-sat-text) + 5%), 85%) !important;
        --color-base-35:  hsl(var(--theme-tint), calc(var(--theme-sat-text) + 5%), 50%, 0.18) !important;
    }


    /* medium contrast */

.theme-light:not(.low-contrast-light):not(.high-contrast-light), .theme-light.medium-contrast-light {
    --color-accent-2: hsl(calc(var(--accent-h) - 4), calc(var(--accent-s) + 4%), calc(var(--accent-l) + 7%));

    /* base contrast */
    /* this is the lightest "l" value */
    --base-c-bg: calc(var(--base-c) + 3.2%);

    /* these represent hsl "l" values. */

    --c-00:  var(--base-c-bg);
    --c-05: calc(var(--base-c-bg) - 2%);
    --c-10: calc(var(--base-c-bg) - 6%);
    --c-20: calc(var(--base-c-bg) - 7%);

    --c-25: calc(var(--base-c) - 8%);
    --c-30: calc(var(--base-c) - 70%);
    --c-35: calc(var(--base-c) - 70%);
    --c-40: calc(var(--base-c) - 10%);

    --c-50: calc(var(--text-base) + 20%);
    --c-60: calc(var(--text-base) + 15%);
    --c-70: calc(var(--text-base) + 12%);
    --c-100: calc(var(--text-base) + 5%);

    --color-base-30:  hsl(var(--theme-tint), calc(var(--theme-sat-text) + 5%), 85%) !important;
    --color-base-35:  hsl(var(--theme-tint), calc(var(--theme-sat-text) + 5%), 50%, 0.28) !important;
    --c-20: calc(var(--base-c-bg) - 5%);
}



/* high contrast  */

.theme-light.high-contrast-light {
    --color-accent-2: hsl(calc(var(--accent-h) - 6), calc(var(--accent-s) + 10%), calc(var(--accent-l) - 5%));
    --color-accent-1: hsl(calc(var(--accent-h) - 6), calc(var(--accent-s) + 10%), calc(var(--accent-l) - 3%));

    /* base contrast */
    /* this is the lightest "l" value */
    --base-c: 100%;
    --base-c-high: calc(var(--base-c) + 5%);

    /* these represent hsl "l" values. */
    --c-00:  var(--base-c-high);
    --c-05: calc(var(--base-c-high) - 5%);
    --c-10: calc(var(--base-c-high) - 7%);
    --c-20: calc(var(--base-c-high) - 7%);

    --c-25: calc(var(--base-c) - 26%);
    --c-30: calc(var(--base-c) - 27%);
    --c-35: calc(var(--base-c) - 28%);
    --c-40: calc(var(--base-c) - 20%);

    --c-50: calc(var(--text-base) + 18%);
    --c-60: calc(var(--text-base) + 12%);
    --c-70: calc(var(--text-base) + 26%);
    --c-100: calc(var(--text-base) - 1%);

    


}

/* ==== dark theme contrast == */

/* medium contrast */
.theme-dark:not(.low-contrast-dark):not(.high-contrast-dark), .theme-dark.medium-contrast-dark,
.theme-dark {
    /* base contrast */
    /* this is the lightest "l" value */
    --base-c-m: calc(var(--base-c) - 10%);

    /* these represent hsl "l" values. */
    /* the higher the contrast, the greater the range between values. */
    --c-00:  var(--base-c-m);
    --c-05: calc(var(--base-c-m) + 1%);
    --c-10: calc(var(--base-c-m) + 5%);
    --c-20: calc(var(--base-c-m) - 4%);

    --c-25: calc(var(--base-c-m) + 3%);
    --c-30: calc(var(--base-c-m) + 3%);
    --c-35: calc(var(--base-c-m) + 19%);
    --c-40: calc(var(--base-c-m) + 18%);

    --c-50: calc(var(--base-c-m) + 60%);
    --c-60: calc(var(--base-c-m) + 64%);
    --c-70: calc(var(--base-c-m) + 66%);
    --c-100: calc(var(--base-c-m) + 68%);


}

/* high contrast */
.theme-dark.high-contrast-dark {
    /* base contrast */
    /* this is the lightest "l" value */
    --base-c-m: calc(var(--base-c) - 12%);

    /* these represent hsl "l" values. */
    /* the higher the contrast, the greater the range between values. */
    --c-00:  var(--base-c-m);
    --c-05: calc(var(--base-c-m) + 1%);
    --c-10: calc(var(--base-c-m) + 10%);
    --c-20: calc(var(--base-c-m) - 2.7%);
    --c-25: calc(var(--base-c-m) + 3%);
    --c-30: calc(var(--base-c-m) + 6%);
    --c-35: calc(var(--base-c-m) + 25%);
    --c-40: calc(var(--base-c-m) + 30%);

    --c-50: calc(var(--base-c-m) + 75%);
    --c-60: calc(var(--base-c-m) + 78%);
    --c-70: calc(var(--base-c-m) + 79%);
    --c-100: calc(var(--base-c-m) + 84%);
}


/* low contrast */
.theme-dark.low-contrast-dark {
    /* base contrast */
    /* this is the lightest "l" value */
    --base-c: 0%;
    --base-c-m: calc(var(--base-c));

    /* these represent hsl "l" values. */
    /* the higher the contrast, the greater the range between values. */
    --c-00:  var(--base-c-m);
    --c-05: calc(var(--base-c-m) + 1%);
    --c-10: calc(var(--base-c-m) + 5%);
    --c-20: calc(var(--base-c-m) - 3%) !important;

    --c-25: calc(var(--base-c-m) +  2%);
    --c-30: calc(var(--base-c-m) + 3%);
    --c-35: calc(var(--base-c-m) + 15%);
    --c-40: calc(var(--base-c-m) + 12%);

    --c-50: calc(var(--base-c-m) + 47%);
    --c-60: calc(var(--base-c-m) + 50%);
    --c-70: calc(var(--base-c-m) + 55%);
    --c-100: calc(var(--base-c-m) + 60%);
}


/* higher contrast (jet black) */
.theme-dark.true-black-dark {
    /* base contrast */
     /* this is the lightest "l" value */
     --base-c-m: 1% !important; 
 
     /* these represent hsl "l" values. */
     /* the higher the contrast, the greater the range between values. */
     --c-00:  var(--base-c-m);
     --c-05: calc(var(--base-c-m) + 2%);
     --c-10: calc(var(--base-c-m) + 15%);
     --c-20: calc(var(--base-c-m) + 8%) !important;
 
     --c-25: calc(var(--base-c-m) + 3%);
     --c-30: calc(var(--base-c-m) + 10%) !important;
     --c-35: calc(var(--base-c-m) + 50%) !important;
     --c-40: calc(var(--base-c-m) + 30%);
 
     --c-50: calc(var(--base-c-m) + 79%) !important;
     --c-60: calc(var(--base-c-m) + 80%) !important;
     --c-70: calc(var(--base-c-m) + 82%) !important;
     --c-100: 80% !important;

 }
 
 

/* == light theme == */
/* this structure is used for all color schemes. */

.theme-light {
--background-modifier-hover: rgba(var(--mono-rgb-100), 0.05);
--interactive-accent: vaR(--color-accent-1);

/* base colors */
  --color-base-00: hsl(var(--theme-tint), var(--theme-sat), var(--c-00));
  --color-base-05: hsl(var(--theme-tint), var(--theme-sat-secondary), var(--c-05));
  --color-base-10: hsl(var(--theme-tint), var(--theme-sat-secondary), var(--c-10));

/* secondary colors */
--color-base-20: hsl(var(--theme-tint-secondary), var(--theme-sat-secondary), var(--c-20));
  --color-base-25: hsl(var(--theme-tint-secondary), var(--theme-sat-secondary), var(--c-25));
  --color-base-30:  hsl(var(--theme-tint), calc(var(--theme-sat-text) - 5%), var(--c-30));
 --color-base-35:  hsl(var(--theme-tint), calc(var(--theme-sat-text) - 5%), var(--c-35));
  --color-base-40:  hsl(var(--theme-tint), var(--theme-sat-text), var(--c-40));

  /* text colors */
  --color-base-50:  hsl(var(--theme-tint-text), var(--theme-sat-text), var(--c-50));
  --color-base-60: hsl(var(--theme-tint-text), var(--theme-sat-text), var(--c-60));
  --color-base-70: hsl(var(--theme-tint-text), var(--theme-sat-text), var(--c-70));
  --color-base-100: hsl(var(--theme-tint-text), var(--theme-sat-text), var(--c-100));

  --background-modifier-message: var(--color-accent-1);

  --text-base: 15%;
		/* muted colors */
    --color-muted: #797593;
    --color-muted-rgb: 121, 117, 147;
}

/* == dark theme == */
/* this is the base used for all dark color schemes */

.theme-dark,
.is-mobile.theme-dark {
--color-accent-2: hsl(calc(var(--accent-h) - 4), calc(var(--accent-s) + 4%), calc(var(--accent-l) + 5%));
--color-accent-1: hsl(calc(var(--accent-h) + 4), calc(var(--accent-s) + 4%), calc(var(--accent-l) + 6%));


  /* base colors */
--color-base-00: hsl(var(--theme-tint-text), var(--theme-sat-text), var(--c-00));
--color-base-05: hsl(var(--theme-tint-text), var(--theme-sat-text), var(--c-05));
--color-base-10: hsl(var(--theme-tint-text), var(--theme-sat-text), var(--c-10));
--color-base-20: hsl(var(--theme-tint-text), var(--theme-sat-text), var(--c-20));

/* secondary colors */
--color-base-25: hsl(var(--theme-tint-text), var(--theme-sat-text), var(--c-25));
--color-base-30:  hsl(var(--theme-tint-text), var(--theme-sat-text), var(--c-30));
--color-base-35:  hsl(var(--theme-tint-secondary), var(--theme-sat-secondary), var(--c-35));
--color-base-40:  hsl(var(--theme-tint-secondary), var(--theme-sat-secondary), var(--c-40));

/* text colors */
--color-base-50:  hsl(var(--theme-tint-text), var(--theme-sat), var(--c-50));
--color-base-60: hsl(var(--theme-tint), var(--theme-sat), var(--c-60));
--color-base-70: hsl(var(--theme-tint), var(--theme-sat), var(--c-70));
--color-base-100: hsl(var(--theme-tint), var(--theme-sat), var(--c-100));

--text-muted: var(--color-base-50) !important;
--background-modifier-form-field: var(--color-base-10);
--background-modifier-message: var(--color-accent-1);
--background-modifier-border: var(--color-base-35);

		/* muted colors */
    --color-muted: #908caa;
    --color-muted-rgb: 144, 140, 170;
}


/* == default light theme == */
.theme-light, .theme-normal.theme-light {
    --base-c: 100%;
    --accent-h: 228;
    --accent-s: 70%;
    --accent-l: 66%;
    --color-red: #f45757;
    --color-red-rgb: 244, 87, 87;
}
.theme-normal.blue-accent {
    --color-accent-hsl: 193, 85%, 50% !important;
    --color-accent: rgb(21, 189, 236) !important;
    --color-accent-1: hsl(193, 85%, 50%) !important;
    --color-accent-2: rgb(21, 189, 236) !important;
    --link-decoration-color: rgba(8, 187, 237, 0.42);
    --link-unresolved-decoration-color: rgba(21, 189, 236, 0.265);
}
.theme-normal.green-accent {
    --color-accent: #38ab70 !important;
    --color-accent-1: #2aaf6a !important;
    --color-accent-2: #26d37a !important;
    --link-decoration-color: #29c87652 !important;
    --link-unresolved-decoration-color: #29c87652;
}
.theme-normal.yellow-accent {
    --color-accent: #ffb700 !important;
    --color-accent-1: #ffb700 !important;
    --color-accent-2: #ffb700 !important;
    --link-decoration-color: #ffb7005e;
    --link-unresolved-decoration-color: #ffb7005e;
}

/* == default dark theme == */
.theme-dark, .theme-normal.theme-dark {
    --base-c: 15%;
    --accent-h: 238;
    --accent-s: 100%;
    --accent-l: 70%;
}
/* == default theme colorful headings == */
.colorful-headings-s {
    --h1-color: var(--text-accent);
    --h2-color: var(--text-accent);
    --h3-color: var(--text-accent);
    --h4-color: var(--text-accent);
    --h5-color: var(--text-accent);
    --h6-color: var(--text-accent);
}


/* == solarized theme == */
.theme-solarized-s {
    --theme-tint: 48.5;
    --theme-sat: 100%;
    --theme-tint-secondary: 43;
    --theme-sat-secondary: 52%;
    --theme-tint-text: 194;
    --theme-sat-text: 22%;
    --accent-h: 175 !important;
    --accent-s: 59% !important;
    --accent-l: 40% !important;

    --color-red: #dc322f;
    --color-green-rgb: 133, 153, 0;
    --color-green: #859900;
    --color-orange-rgb: 203, 75, 22;
    --color-orange: #cb4b16;
    --color-yellow-rgb: 181, 137, 0;
    --color-yellow: #b58900;
    --color-cyan-rgb: 42, 161, 152;
    --color-cyan: #2aa198;
    --color-blue-rgb: 38, 139, 210;
    --color-blue: #268bd2;
    --color-purple-rgb:108, 113, 196;
    --color-purple: #6c71c4;
    --color-pink-rgb: 211, 54, 130;
    --color-pink: #d33682;
    --text-base: 30%;

}
.theme-light.theme-solarized-s {
    --base-c: 92.8%;
}
.theme-light.low-contrast-light.theme-solarized-s {
    --theme-tint-secondary:47;
    --theme-sat-secondary: 70%;
}
.theme-dark.theme-solarized-s {
    --base-c: 20%;
    --theme-sat: 20%;
    --theme-tint: 180;
    --theme-tint-secondary: 194;
    --theme-sat-text: 100%;
    --accent-h: 18 !important;
    --accent-s: 80% !important;
    --accent-l: 44% !important;
    --text-normal: rgb(145, 189, 192) !important;
    --text-muted: rgb(85, 148, 165) !important;
    --text-faint: rgb(73, 133, 149) !important;
}
.theme-dark.theme-solarized-s.low-contrast-dark {
    --base-c: 14%;
}
.theme-dark.theme-solarized-s.low-contrast-dark,
.theme-dark.theme-solarized-s.medium-contrast-dark {
    --color-red: #d86866;
    --accent-h: 18 !important;
    --accent-s: 80% !important;
    --accent-l: 55% !important;
}
.theme-solarized-s.colorful-headings-s {
    --h1-color: var(--color-cyan);
    --h2-color: var(--color-cyan);
    --h3-color: var(--color-cyan);
    --h4-color: var(--color-cyan);
    --h5-color: var(--color-cyan);
    --h6-color: var(--color-cyan);
}

/* == rose pine theme == */
.theme-rose-pine {
    --theme-tint: 32;
    --theme-sat: 57%;
    --theme-tint-secondary: 31.5;
    --theme-sat-secondary: 40%;
    --theme-tint-text: 248;
    --theme-sat-text: 18%;
}
.theme-light.theme-rose-pine {
    --base-c: 89%;
    --accent-h: 3 !important;
    --accent-s: 53% !important;
    --accent-l: 67% !important;
    --text-base: 25%;

    --color-muted: #797593;
    --color-red: #b4637a;
    --color-pink: #d7827e;
    --color-orange: #ea9d34;
    --color-yellow: #eacc34;
    --color-green: #719756; 
    --color-cyan: #56949f;
    --color-blue: #286983;
    --color-purple: rgb(144, 122, 169);
    --color-muted-rgb: 121, 117, 147;
    --color-red-rgb: 180, 99, 122;
    --color-pink-rgb: 215, 130, 126;
    --color-orange-rgb: 234, 157, 52;
    --color-yellow-rgb: 230, 180, 50;
    --color-green-rgb: 113, 151, 86; 
    --color-cyan-rgb: 86, 148, 159;
    --color-blue-rgb: 40, 105, 131;
    --color-purple-rgb: 144, 122, 169;
}
.theme-light.low-contrast-light.theme-rose-pine {
    --base-c: 92%;
}
.theme-dark.theme-rose-pine {
    --base-c: 20%;
    --theme-tint: 285;
    --theme-tint-secondary: 248;
    --theme-sat-secondary: 13%;
    --theme-sat: 10%;
    --accent-h: 267 !important;
    --accent-s: 57% !important;
    --accent-l: 78% !important;
    --theme-tint-text: 265;

    --color-muted: #908caa;
    --color-red: #eb6f92;
    --color-pink: #ebbcba;
    --color-orange: #f6ac77;
    --color-yellow: #f6ce77;
    --color-green: #b8d89c;
    --color-cyan: #9ccfd8;
    --color-blue: #569ebb;
    --color-purple: #c4a7e7;
    --color-muted-rgb: 144, 140, 170;
    --color-red-rgb: 235, 111, 146;
    --color-pink-rgb: 235, 188, 186;
    --color-orange-rgb:246, 172, 119;
    --color-yellow-rgb: 246, 206, 119;
    --color-green-rgb: 184, 216, 156;
    --color-cyan-rgb: 156, 207, 216;
    --color-blue-rgb: 49, 116, 143;
    --color-purple-rgb: 196, 167, 231;
} 
.theme-rose-pine.theme-dark:not(.low-contrast-dark):not(.high-contrast-dark) {
    --c-100: 60%;
}
.theme-rose-pine.theme-dark.colorful-headings-s {
    --h6-color: var(--color-purple);
    --h1-color: var(--color-pink);
    --h2-color: var(--color-orange);
    --h3-color: var(--color-yellow);
    --h4-color: var(--color-green);
    --h5-color: var(--color-cyan);
}
.theme-rose-pine.theme-light.colorful-headings-s {
    --h1-color: var(--color-red);
    --h2-color: var(--color-purple);
    --h3-color: var(--color-cyan);
    --h4-color: var(--color-green);
    --h5-color: var(--color-orange);
    --h6-color: var(--color-pink);

}

/* == everforest theme == */
.theme-everforest {
    --accent-h: 68 !important;
    --accent-s: 99% !important;
    --accent-l: 32% !important;

    --theme-tint: 54;
    --theme-sat: 55%;
    --theme-tint-secondary: 55;
    --theme-sat-secondary: 40%;
    --theme-tint-text: 170;
    --theme-sat-text: 15%;

    --color-red: rgb(234, 93, 90);
    --color-pink: rgb(248, 105, 162);
    --color-orange: rgb(245, 125, 38);
    --color-yellow: rgb(223, 160, 0);
    --color-green: rgb(141, 161, 1); 
    --color-cyan: rgb(53, 167, 124);
    --color-blue: rgb(58, 148, 197);
    --color-purple: rgb(223, 105, 186);
    --color-red-rgb: 247, 84, 82;
    --color-pink-rgb: 248, 105, 162;
    --color-orange-rgb: 245, 125, 38;
    --color-yellow-rgb: 223, 160, 0;
    --color-green-rgb:141, 161, 1; 
    --color-cyan-rgb: 53, 167, 124;
    --color-blue-rgb: 58, 148, 197;
    --color-purple-rgb: 223, 105, 186;
}
.theme-light.theme-everforest {
    --base-c: 89%;
    --text-base: 25%;
}
.theme-light.theme-everforest.low-contrast-light {
    --base-c: 91%;
    --theme-sat: 50%;
    --theme-sat-secondary: 32%;
    --theme-tint-secondary: 55;
    --theme-tint: 55;
}
.theme-light.theme-everforest.high-contrast-light {
    --theme-tint: 55;
    --base-c: 90%;
    --theme-tint-secondary: 55;
}
.theme-dark.theme-everforest {
    --accent-h: 68 !important;
    --accent-s: 99% !important;
    --accent-l: 32% !important;

    --base-c: 25%;
    --theme-tint-text: 203;
    --theme-sat-text: 15%;
    --theme-tint: 47;
    --theme-sat: 20%;
    --theme-sat-secondary: 7%;
    --theme-tint-secondary: 159;

    --color-red: rgb(247, 84, 82);
    --color-pink: rgb(248, 105, 162);
    --color-orange: rgb(245, 125, 38);
    --color-yellow: rgb(223, 160, 0);
    --color-green: hsl(68, 99%, 32%); 
    --color-cyan: rgb(53, 167, 124);
    --color-blue: rgb(58, 148, 197);
    --color-purple: rgb(223, 105, 186);
    --color-red-rgb: 247, 84, 82;
    --color-pink-rgb: 248, 105, 162;
    --color-orange-rgb: 245, 125, 38;
    --color-yellow-rgb: 223, 160, 0;
    --color-green-rgb:141, 161, 1; 
    --color-cyan-rgb: 53, 167, 124;
    --color-blue-rgb: 58, 148, 197;
    --color-purple-rgb: 223, 105, 186;
}
.theme-dark.theme-everforest.low-contrast-dark {
    --base-c: 17%;
}
.theme-dark.theme-everforest.high-contrast-dark {
    --base-c: 26%;
}
/* ==== Gruvbox Theme ==== */

.theme-gruvbox-s {
    --accent-h: 12 !important;
    --accent-s: 57% !important;
    --accent-l: 50% !important;

    --theme-tint: 48;
    --theme-sat: 87%;
    --theme-tint-secondary: 46;
    --theme-sat-secondary: 73%;
    --theme-tint-text: 27;
    --theme-sat-text: 20%;
    
    --color-red-rgb:251, 73, 52;
    --color-red: hsl(6, 64%, 52%);
    --color-green-rgb: 184, 186, 38;
    --color-green: #9d9f12;
    --color-orange-rgb: 255, 135, 55;
    --color-orange: hsl(24, 87%, 47%);
    --color-yellow-rgb: 215, 153, 33;
    --color-yellow: #fabd2f;
    --color-cyan-rgb: 142, 192, 124;
    --color-cyan: #649751;
    --color-blue-rgb: 131, 165, 152;
    --color-blue: #5b8374;
    --color-purple-rgb: 211, 134, 155;
    --color-purple: hsl(344, 37%, 59%);
    --color-pink-rgb: 241, 168, 203;
    --color-pink: #d383aa;
}
.theme-light.theme-gruvbox-s {
    --base-c: 88%;
}
.theme-light.theme-gruvbox-s.low-contrast-light {
    --color-base-35:  hsl(var(--theme-tint), calc(var(--theme-sat-text) + 5%), 50%, 0.18) !important;
    --color-base-30:  hsl(var(--theme-tint), 60%, 75%) !important;
}
.theme-dark.theme-gruvbox-s{
    --accent-h: 24 !important;
    --accent-s: 100% !important;
    --accent-l: 61% !important;
   
    --base-c: 18%;
    --theme-tint: 36;
    --theme-sat: 19%;
    --theme-tint-text: 0;
    --theme-sat-text: 2%;
    --theme-tint-secondary: 30;
    --theme-sat-secondary: 3%;
}
.theme-gruvbox-s.colorful-headings-s {
    --h2-color: var(--color-orange);
    --h1-color: var(--color-red);
    --h3-color: var(--color-green);
    --h4-color: var(--color-cyan);
    --h5-color: var(--color-blue);
    --h6-color: var(--color-purple);
}
/* === Nord Theme === */

.theme-nord-s {
    --checkbox-color: var(--color-orange);
    --checkbox-color-hover: var(--color-orange);
    --accent-h: 210 !important;
    --accent-s: 34% !important;
    --accent-l: 63% !important; 
    
    --theme-tint: 213;
    --theme-sat: 25%;
    --theme-tint-secondary: 213;
    --theme-sat-secondary: 30%;
    --theme-tint-text: 222;
    --theme-sat-text: 15%;

    /* --color-base-00: hsl(210, 20%, 96%);
    --color-base-20: hsl(213, 31%, 93%);
    --color-base-70: hsl(222, 10%, 51%);
    --color-base-100: hsl(219, 15%, 34%); */

    --color-red-rgb: 191, 97, 106;
    --color-red: #BF616A;
    --color-green-rgb: 163, 190, 140;
    --color-green: #A3be8c;
    --color-orange-rgb: 208, 135, 112;
    --color-orange: #d08770;
    --color-yellow-rgb: 235, 203, 139;
    --color-yellow: #ebcb8b;
    --color-cyan-rgb: 136, 192, 208;
    --color-cyan: #88c0d0;
    --color-blue-rgb: 129, 161, 193;
    --color-blue: hsl(210, 34%, 63%);
    --color-purple-rgb: 94, 129, 172;
    --color-purple: #5e81AC;
    --color-pink-rgb: 180, 142, 173;
    --color-pink: #b48ead;
}
.theme-light.theme-nord-s {
    --base-c: 98%;
}
.theme-dark.theme-nord-s {
    --base-c:30%;
    --theme-tint-text: 218;
    --theme-sat-text: 17%;
    --theme-sat-secondary: 15%;
    --accent-h: 193 !important;
    --accent-s: 43% !important;
    --accent-l: 67% !important; 
    --color-red-rgb: 191, 97, 106;
    --color-red: #dc8890;
    --color-green-rgb: 163, 190, 140;
    --color-green: #A3be8c;
    --color-orange-rgb: 208, 135, 112;
    --color-orange: #db9681;
    --color-yellow-rgb: 235, 203, 139;
    --color-yellow: #ebcb8b;
    --color-cyan-rgb: 136, 192, 208;
    --color-cyan: hsl(193, 43%, 67%);
    --color-blue-rgb: 129, 161, 193;
    --color-blue: #81a1c1;
    --color-purple-rgb: 94, 129, 172;
    --color-purple: #6e8fb6;
    --color-pink-rgb: 180, 142, 173;
    --color-pink: #b48ead;
}
.theme-dark.theme-nord-s.low-contrast-dark {
    --base-c: 28%;
    --theme-sat-text: 20%;
    --color-red: #e19199;
    --color-orange: #e6a18b;
    --color-purple: #aab2cd;
}
.theme-nord-s.colorful-headings-s,
.theme-everforest.colorful-headings-s {
    --h1-color: var(--color-red);
    --h2-color: var(--color-orange);
    --h3-color: var(--color-yellow);
    --h4-color: var(--color-green);
    --h5-color: var(--color-cyan);
    --h6-color: var(--color-blue);
}

/* == catppuccin theme == */
.theme-catpp.theme-light.low-contrast-light {
    --theme-sat: 30%;
    --theme-sat-secondary: 30%;
    --base-c: 95%;
}
.theme-catpp.theme-light.high-contrast-light {
    --base-c: 93.5%;
}

.theme-catpp {
    --theme-tint: 220;
    --theme-sat: 45%;
    --theme-tint-secondary: 220;
    --theme-sat-secondary: 35%;
    --theme-tint-text: 234;
    --theme-sat-text: 24%;
    --background-modifier-hover: rgba(var(--color-purple-rgb), 0.25);
    --checkbox-color: var(--color-green);
    --checkbox-color-hover: var(--color-cyan);
    --accent-h: 231 !important;
    --accent-s: 97% !important;
    --accent-l: 72% !important; 
}
.theme-catpp:not(.red-accent):not(.orange-accent):not(.yellow-accent):not(.green-accent):not(.cyan-accent):not(.blue-accent):not(.purple-accent):not(.pink-accent) {
    --color-accent-1: var(--color-purple);
    --color-accent-2: var(--color-pink);
    --interactive-accent: var(--rose);
    --text-on-accent: var(--background-primary) !important;
    --text-accent: var(--color-green);
    --link-color: var(--color-purple);
    --link-color-hover: var(--color-pink);
    --link-unresolved-color: var(--color-cyan);
}
.theme-light.theme-catpp {
    --base-c: 94%;
    --color-red: hsl(347, 87%, 44%);
    --color-red-rgb: 210, 15, 57;
    --color-orange: #dd7878;
    --color-orange-rgb: 220, 138, 120;
    --color-yellow:#df8e1d;
    --color-yellow-rgb: 223, 142, 29;
    --color-green: #179299;
    --color-green-rgb: 23, 146, 153;
    --color-cyan: #04a5e5;
    --color-cyan-rgb: 4, 165, 229;
    --color-blue: #1e66f5;
    --color-blue-rgb: 30, 102, 245;
    --color-purple: #637afa;
    --color-purple-rgb: 114, 135, 253;
    --color-pink: #ea76cb;
    --color-pink-rgb: 234, 118, 203;
    --rose: #dc8a78;
}
.theme-catpp.theme-light.colorful-headings-s {
    --h1-color: var(--color-purple);
    --h2-color: var(--color-blue);
    --h3-color: var(--color-cyan);
    --h4-color: var(--color-green);
    --h5-color: #40a02b;
    --h6-color: var(--color-orange);
}
.theme-dark.theme-catpp {
    --base-c: 23%;

    --theme-tint-text: 230;
    --theme-sat-text: 22%;
    --theme-sat-secondary: 17%;
    --theme-tint: 230;
    --theme-sat: 80%;

    --accent-h: 193 !important;
    --accent-s: 43% !important;
    --accent-l: 67% !important; 
    
    --color-red-rgb: 238, 153, 160;
    --color-red: #ee99a0;
    --color-green-rgb:166, 218, 149;
    --color-green: #a6da95;
    --color-orange-rgb:245, 169, 127;
    --color-orange: #f5a97f;
    --color-yellow-rgb: 238, 212, 159;
    --color-yellow: #eed49f;
    --color-cyan-rgb: 145, 215, 227;
    --color-cyan: #91d7e3;
    --color-blue-rgb:138, 173, 244;
    --color-blue: #8aadf4;
    --color-purple-rgb: 183, 189, 248;
    --color-purple: #b7bdf8;
    --color-pink-rgb: 245, 189, 230;
    --color-pink: #f5bde6;  
    --rose: #f4dbd6;
}
.theme-catpp.theme-dark.low-contrast-dark {
    --base-c: 18%; 
    --theme-sat-text: 17%;
    --theme-tint-text: 228;
    --theme-sat: 40%;
}
.theme-catpp.theme-dark.high-contrast-dark {
    --base-c: 25%;
    --theme-sat-text: 20%;
    --theme-tint-text: 240;
    --theme-sat: 80%;
    --c-100: 90% !important;
}
.theme-catpp.theme-dark.colorful-headings-s {
    --h1-color: #7dc4e4;
    --h2-color: var(--color-blue);
    --h3-color: #c6a0f6;
    --h4-color: var(--color-pink);
    --h5-color: var(--color-red);
    --h6-color: var(--color-orange);

}

/* === Ayu Theme === */



.theme-light.theme-ayu-s {
    --text-base: 40%;
    --theme-tint: 210;
    --theme-sat: 50%;
    --theme-tint-secondary: 210;
    --theme-sat-secondary: 25%;
    --theme-tint-text: 210;
    --theme-sat-text: 10%;
    --accent-h: 35 !important;
    --accent-s: 100% !important;
    --accent-l: 60% !important; 
    --base-c: 100%;
    --color-red-rgb: 240, 113, 113;
    --color-red: rgb(240, 113, 113);
    --color-green-rgb: 156, 208, 0;
    --color-green: rgb(141, 187, 0);
    --color-orange-rgb: 250, 141, 62;
    --color-orange: rgb(250, 141, 62);
    --color-yellow-rgb: 242, 174, 73;
    --color-yellow: rgb(242, 174, 73);
    --color-cyan-rgb: 76, 191, 153;
    --color-cyan: rgb(76, 191, 153);
    --color-blue-rgb: 85, 180, 212;
    --color-blue: rgb(85, 180, 212);
    --color-purple-rgb: 71, 138, 204;
    --color-purple: rgb(71, 138, 204);
    --color-pink-rgb: 180, 142, 173;
    --color-pink: hsl(270, 45%, 64%);
}
.theme-dark.theme-ayu-s {
    --text-on-accent: black;
    --accent-h: 40 !important;
    --accent-s: 100% !important;
    --accent-l: 70% !important;
    --base-c: 25%;
    --theme-tint-text: 223;
    --theme-sat-text: 30%;
    --theme-tint-secondary: 223;
    --theme-sat-secondary: 27%;
    --theme-sat: 10%;
    --theme-tint:100;
    --color-red-rgb: 242, 135, 121;
    --color-red: rgb(242, 135, 121);
    --color-green-rgb: 213, 255, 128;
    --color-green: rgb(213, 255, 128);
    --color-orange-rgb: 255, 173, 102;
    --color-orange: rgb(255, 173, 102);
    --color-yellow-rgb: 255, 209, 115;
    --color-yellow: rgb(255, 209, 115);
    --color-cyan-rgb: 149, 230, 203;
    --color-cyan: rgb(149, 230, 203);
    --color-blue-rgb: 92, 207, 230;
    --color-blue: #5ccfe6;
    --color-purple-rgb: 128, 191, 255;
    --color-purple: rgb(128, 191, 255);
    --color-pink-rgb: 223, 191, 255;
    --color-pink: rgb(223, 191, 255);
    
} .theme-dark.theme-ayu-s:not(.low-contrast-dark):not(high-contrast-dark) {
    --c-100: 75%;
} .theme-dark.theme-ayu-slow-contrast-dark {
    --c-00: 5% !important;
}

/* colorful headings */
.theme-ayu-s.colorful-headings-s {
    --h1-color: var(--color-purple);
    --h2-color: var(--color-blue);
    --h3-color: var(--color-green);
    --h4-color: var(--color-yellow);
    --h5-color: var(--color-orange);
    --h6-color: var(--color-red);
}

/* Color Accents */
.red-accent {
    --color-accent: var(--color-red) !important;
    --color-accent-1: var(--color-red) !important;
    --color-accent-2: rgba(var(--color-red-rgb), 0.8) !important;
    --link-decoration-color: rgba(var(--color-red-rgb), 0.4);
    --link-unresolved-decoration-color: rgba(var(--color-red-rgb), 0.4);
}
.orange-accent {
    --color-accent: var(--color-orange !important);
    --color-accent-1: var(--color-orange) !important;
    --color-accent-2: rgba(var(--color-orange-rgb), 0.8) !important;
    --link-decoration-color: rgba(var(--color-orange-rgb), 0.4);
    --link-unresolved-decoration-color: rgba(var(--color-orange-rgb), 0.4);
}
.yellow-accent {
    --color-accent: var(--color-yellow) !important;
    --color-accent-1: var(--color-yellow) !important;
    --color-accent-2: rgba(var(--color-yellow-rgb), 0.8) !important;
    --link-decoration-color: rgba(var(--color-yellow-rgb), 0.4);
    --link-unresolved-decoration-color: rgba(var(--color-yellow-rgb), 0.4);
}
.green-accent {
    --color-accent: var(--color-green) !important;
    --color-accent-1: var(--color-green) !important;
    --color-accent-2: rgba(var(--color-green-rgb), 0.8) !important;
    --link-decoration-color: rgba(var(--color-green-rgb), 0.4);
    --link-unresolved-decoration-color: rgba(var(--color-green-rgb), 0.4);
}
.cyan-accent {
    --color-accent: var(--color-cyan) !important;
    --color-accent-1: var(--color-cyan) !important;
    --color-accent-2: rgba(var(--color-cyan-rgb), 0.8) !important;
    --link-decoration-color: rgba(var(--color-cyan-rgb), 0.4);
    --link-unresolved-decoration-color: rgba(var(--color-cyan-rgb), 0.4);
}
.blue-accent {
    --color-accent: var(--color-blue) !important;
    --color-accent-1: var(--color-blue) !important;
    --color-accent-2: rgba(var(--color-blue-rgb), 0.8) !important;
    --link-decoration-color: rgba(var(--color-blue-rgb), 0.4);
    --link-unresolved-decoration-color: rgba(var(--color-blue-rgb), 0.4);
}
.purple-accent {
    --color-accent: var(--color-purple) !important;
    --color-accent-1: var(--color-purple) !important;
    --color-accent-2: rgba(var(--color-purple-rgb), 0.8) !important;
    --link-decoration-color: rgba(var(--color-purple-rgb), 0.4);
    --link-unresolved-decoration-color: rgba(var(--color-purple-rgb), 0.4);
}
.pink-accent {
    --color-accent: var(--color-pink) !important;
    --color-accent-1: var(--color-pink) !important;
    --color-accent-2: rgba(var(--color-pink-rgb), 0.8) !important;
    --link-decoration-color: rgba(var(--color-pink-rgb), 0.4);
    --link-unresolved-decoration-color: rgba(var(--color-pink-rgb), 0.4);
}

/* @settings

name: Serenity Color Schemes
id: serenity-color-schemes
settings:
    -
        id: colors-heading
        title: Colors
        type: heading
        level: 2
        collapsed: true
    -
        id: color-scheme-select
        title: Color Scheme
        type: class-select
        allowEmpty: false
        default: theme-normal
        options: 
            -
                label: Obsidian
                value: theme-normal
            -
                label: Ayu
                value: theme-ayu-s
            -
                label: Catppuccin
                value: theme-catpp
            -
                label: Nord 
                value: theme-nord-s
            -  
                label: Solarized
                value: theme-solarized-s
            -
               label: Rose Pine
               value: theme-rose-pine
            -
                label: Everforest
                value: theme-everforest

            -
                label: Gruvbox
                value: theme-gruvbox-s
    -
        id: color-accent-class-select
        title: Accent Color
        type: class-select
        default: Auto
        options:
            -
                label: Auto
                value: auto-accent
            -
                label: Red
                value: red-accent
            -
                label: Orange
                value: orange-accent
            -
                label: Yellow
                value: yellow-accent
            -   
                label: Green
                value: green-accent 
            -   
                label: Cyan
                value: cyan-accent
            -
                label: Blue
                value: blue-accent
            -
                label: Purple
                value: purple-accent
            -
                label: Pink
                value: pink-accent
    -
        id: contrast-light
        title: Light Mode Contrast
        type: class-select
        default: medium-contrast-light
        options: 
            -
                label: Low Contrast
                value: low-contrast-light
            -
                label: Medium Contrast
                value: medium-contrast-light
            -
                label: High Contrast
                value: high-contrast-light
    -
        id: contrast-dark
        title: Dark Mode Contrast
        type: class-select
        default: medium-contrast-dark
        options: 
            -
                label: Low Contrast
                value: low-contrast-dark
            -
                label: Medium Contrast
                value: medium-contrast-dark
            -
                label: High Contrast
                value: high-contrast-dark
            -
                label: Jet Black
                value: true-black-dark
    -
        id: advanced-heading
        title: Advanced
        type: heading
        level: 3
        collapsed: true
    -
        id: custom-color-scheme-heading-light
        title: Custom Light Theme
        type: heading
        level: 4
        collapsed: true
    -
        id: custom-color-scheme-light
        title: Use Custom Light Theme
        type: class-toggle
        default: false
    -
        id: custom-theme-tint-l
        title: Base Tint
        type: variable-number-slider
        min: 0
        max: 360
        step: 1
        default: 15
    -
        id: custom-theme-sat-l
        title: Base Saturation
        type: variable-number-slider
        min: 0
        format: '%'
        max: 100
        step: 0.25
        default: 100
    -
        id: custom-base-c-l
        title: Base Brightness
        type: variable-number-slider
        min: 0
        format: '%'
        max: 100
        step: 0.25
        default: 99
    -
        id: custom-theme-tint-secondary-l
        title: Secondary Tint
        type: variable-number-slider
        min: 0
        max: 360
        step: 1
        default: 15
    -
        id: custom-theme-sat-secondary-l
        title: Secondary Saturation
        type: variable-number-slider
        min: 0
        format: '%'
        max: 100
        step: 0.25
        default: 77
    -
        id: custom-c-20-l
        title: Secondary Brightness
        type: variable-number-slider
        min: 0
        format: '%'
        max: 100
        step: 0.25
        default: 97
    -
        id: custom-theme-tint-text-l
        title: Text Tint
        type: variable-number-slider
        min: 0
        max: 360
        step: 1
        default: 205
    -
        id: custom-theme-sat-text-l
        title: Text Saturation
        type: variable-number-slider
        min: 0
        format: '%'
        max: 100
        step: 0.25
        default: 25
    -
        id: custom-text-c-l
        title: Text Contrast
        type: variable-number-slider
        min: 0
        format: '%'
        max: 100
        step: 0.25
        default: 43
    -
        id: custom-border-c-l
        title: Border Contrast
        type: variable-number-slider
        min: 0
        format: '%'
        max: 100
        step: 0.25
        default: 82
    -
-
        id: custom-color-scheme-heading-dark
        title: Custom Dark Theme
        type: heading
        level: 4
        collapsed: true
    -
        id: custom-color-scheme-dark
        title: Use Custom Dark Theme
        type: class-toggle
        default: false
    -
        id: custom-theme-tint-d
        title: Base Tint
        type: variable-number-slider
        min: 0
        max: 360
        step: 1

    -
        id: custom-theme-sat-d
        title: Base Saturation
        type: variable-number-slider
        min: 0
        format: '%'
        max: 100
        step: 0.25
        default: 63
    -
        id: custom-base-c-d
        title: Base Brightness
        type: variable-number-slider
        min: 0
        format: '%'
        max: 100
        step: 0.25
        default: 9
    -
        id: custom-theme-tint-secondary-d
        title: Secondary Tint
        type: variable-number-slider
        min: 0
        max: 360
        step: 1
        default: 225
    -
        id: custom-theme-sat-secondary-d
        title: Secondary Saturation
        type: variable-number-slider
        min: 0
        format: '%'
        max: 100
        step: 0.25
        default: 50
    -
        id: custom-c-20-d
        title: Secondary Brightness
        type: variable-number-slider
        min: 0
        format: '%'
        max: 100
        step: 0.25
        default: 13
    -
        id: custom-theme-tint-text-d
        title: Text Tint
        type: variable-number-slider
        min: 0
        max: 360
        step: 1
        default: 223
    -
        id: custom-theme-sat-text-d
        title: Text Saturation
        type: variable-number-slider
        min: 0
        format: '%'
        max: 100
        step: 0.25
        default: 19
    -
        id: custom-text-c-d
        title: Text Contrast
        type: variable-number-slider
        min: 0
        format: '%'
        max: 100
        step: 0.25
        default: 73
    -
        id: custom-border-c-d
        title: Border Contrast
        type: variable-number-slider
        min: 0
        format: '%'
        max: 100
        step: 0.25
        default: 31
    -
*/
```
