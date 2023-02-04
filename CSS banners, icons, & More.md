# CSS Banners, Icons (Experimental), and other Image Options

This snippet will allow you to use banner images in your notes. It has 3 types of banner styles—Fade, Fancy Title, and Notion—that can be toggled with the Style Settings plug-in. You can also turn an image into an icon that floats near the title of your note (**WARNING:** may look wonky in themes with custom readable line widths).


## How it Works
### Css Classes
- `obsidian-banner` - type this in the frontmatter after `cssClasses` to enable the banner image.
- `obsidian-icon` - type this in the frontmatter after `cssClasses` to enable the icon image.
### Image Alts 
-  `banner` - makes the image the banner image.
- `higher` - positions the background image higher.
- `lower` - positions the background image lower.
-  `circle`, `profile`, or `round` - typing any of these will make the image circular in shape, like a profile picture.
-  `left` - floats the image left.
- `right` - floats the image right
- `icon` - turns the image into a title icon.
#### **A Warning About the Icon Feature**
I am still a beginner in CSS, and the icon feature did not turn out as good as I'd like. For the most part, it works fine. **BUT**, when viewing multiple panes at the same time, it drifts into a weird position, and a theme with a custom readable line length may disrupt its placement on the page.
You *can* still use the icons feature, but be warned: it can act a bit wonky.
## Screenshots

```css

/* ----- banner image variants ----- */
/* ---- majority done by efemkay ---- */

/* --- CSS CLASSES and IMAGE ALTS: --- 
(css class) obsidian-banner - type this in the frontmatter after `cssClasses` to enable the banner image.
(css class, experimental) obsidian-icon - type this in the frontmatter after `cssClasses` to enable the icon image.
(img alt) banner - makes the image the banner image.
(img alt) higher - positions the background image higher
(img alt) lower - positions the background image lower
(img alt) circle, profile, OR round - typing any of these will make the image circular in shape, like a profile picture
(img alt) left - floats the image left
(img alt) right - floats the image right
(img alt, experimental) icon - turns the image into a title icon.



/* ---- the code below is a slightly modified version of emkay's banner image in this forum post: https://forum.obsidian.md/t/css-how-to-style-the-first-image-in-a-note/52839/ ---- */

/* banner using css only -- https://forum.obsidian.md/t/css-how-to-style-the-first-image-in-a-note/52839/ */

    /* make the div (in LP) containing the image doesn't control the css box-sizing */
    .internal-embed.image-embed[alt*="banner"] { 
        display: contents; 
    }
    /* original forum post snippet with minor tweak */
    .obsidian-banner img[alt*="banner"] {
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        height: 200px;
        width: 100%;
        margin-right: auto;
        margin-left: auto;
        object-fit: cover;
        object-position: 50% 50%;
        overflow: hidden;
        user-select: none;
        border-radius: 0px;  
     }
     /* add option to adjust vertical position by adding the alt metadata "higher" or "lower" */
     .obsidian-banner img[alt*="banner"][alt*="higher"] { object-position: 50% 30%; }
     .obsidian-banner img[alt*="banner"][alt*="lower"] { object-position: 50% 70%; }
    
     

     /* ---- note title placements --- */
     .banner-title .obsidian-banner .inline-title {
         position: relative;
         margin-top: 3.94em;
         margin-bottom: 30px !important;
         font-size:  30px;
         line-height: 1.2em ;
         text-align: center;
         color: white;
         padding: 7px 0px 7px 20px !important;
         background: radial-gradient(circle, rgba(0, 0, 0, 0.416) 0%, rgba(0, 0, 0, 0.233) 53%, rgba(0,0,0,0) 100%);    
     }
     
     .obsidian-banner .inline-title, .banner-fade .obsidian-banner .inline-title{
        position: relative;
        padding-top: 150px;
        z-index: 1;
     }
     .obsidian-banner img[alt*="banner"], .banner-fade .obsidian-banner img[alt*="banner"]{
        -webkit-mask-image: -webkit-gradient(linear, left top, left bottom, from(rgba(0,0,0,1)), to(rgba(0,0,0,0)));
        mask-image: linear-gradient(to bottom, rgba(0,0,0,1), rgba(0,0,0,0));
    }
     .banner-title .obsidian-banner img[alt*="banner"]{
        -webkit-mask-image: none;
        mask-image: none;
     }


     .banner-notion .obsidian-banner img[alt*="banner"] {
        -webkit-mask-image: none;
        mask-image: none;
     }
     .banner-notion .obsidian-banner .inline-title{
        position: relative;
        margin-top: 1.5em !important;
        line-height: 1em !important;
        font-size: 2em !important;
        padding-bottom: 0.3em;
        z-index: 1;
     }

    

/* --- profile image --- */
img[alt*="circle"], 
img[alt*="profile"],
img[alt*="round"] {
    display: block;
    border-radius: 100%;
    aspect-ratio: 1/1;
    object-fit: cover;
    width: 60%;
    position: 50% 50%;
    margin-right: auto;
    margin-left: auto;
}

/* --- float images --- */
.markdown-rendered img[alt*="right"] {
    display: flexbox;
    float: right;
    clear:right;
    max-width: 40%;
    margin-left: 15px;
}
.markdown-rendered img[alt*="left"] {
    display: flexbox;
    float: left;
    clear:left;
    max-width: 40%;
    margin-right: 15px;
}


/* --- EXPERIMENTAL: icon image feature --- */
/* To use, type `obsidian-icon` in the frontmatter
 and use the alt `icon` on an image. 
 WARNING: icons may not respond to custom page widths in certain themes.
 */


.obsidian-icon .inline-title {
    position: relative;
    margin-top: 175px;
    z-index: 1;
}

.obsidian-icon img[alt*="icon"] {
    position: absolute;
    top: 2em;
    left: 1.8em;
    right: unset;
    width: 9% !important;
    object-fit: cover;
    border-radius: 100%;
    aspect-ratio: 1/1;
    z-index: 1;
}
.obsidian-icon.is-readable-line-width img[alt*="icon"] {
    top: 2em;
    left: 26em;
    width: 9%;
}



.obsidian-banner.obsidian-icon .inline-title,
.banner-fade .obsidian-banner.obsidian-icon .inline-title {
    margin-top: 0px;
}
.obsidian-banner.obsidian-icon img[alt*="icon"], .banner-fade .obsidian-banner.obsidian-icon img[alt*="icon"]{
    position: absolute;
    top: 1.2em;
    left: 1.8em;
}
.obsidian-banner.obsidian-icon.obsidian-icon.is-readable-line-width img[alt*="icon"], 
.banner-fade .obsidian-banner.obsidian-icon.is-readable-line-width img[alt*="icon"] {
    position: absolute;
    top: 2.5em;
    left: 26em;
    width: 7% !important;
}
 


.banner-title .obsidian-banner.obsidian-icon .inline-title {
    margin-top: 3.94em;
}
.banner-title .obsidian-banner.obsidian-icon img[alt*="icon"] {
    top: 1.1em;
    width: 10% !important;
    left: 1.5em;
}
.banner-title .obsidian-banner.obsidian-icon.obsidian-icon.is-readable-line-width img[alt*="icon"] {
    top: 5.5em;
    left: 25em;
}


.banner-notion .obsidian-banner.obsidian-icon img[alt*="icon"] {
    top: 6.65em;
    width: 6% !important;
    left: 1.5em;
}
.banner-notion .obsidian-banner.obsidian-icon.obsidian-icon.is-readable-line-width img[alt*="icon"] {
    top: 6.7em;
    left: 25em;
    width: 6% !important;
}


/*

 | --- scrapped attempt  at icons --- |

.obsidian-banner img[alt*="circle"][alt*="icon"], 
.obsidian-banner img[alt*="profile"][alt*="icon"],
.obsidian-banner img[alt*="round"][alt*="icon"] {
    position: absolute;
    top: 15px;
    left: 25px;
    right: unset;
    width: 9%;
    object-fit: cover;
    overflow: hidden;
    user-select: none;
}
.obsidian-banner.is-readable-line-width img[alt*="circle"][alt*="icon"], 
.obsidian-banner.is-readable-line-width img[alt*="profile"][alt*="icon"],
.obsidian-banner.is-readable-line-width img[alt*="round"][alt*="icon"] {
    position: absolute;
    top: 15px;
    left: 470px;
    right: unset;
    width: 9%;
    object-fit: cover;
    overflow: hidden;
    user-select: none;
}
*/


/* @settings

name: Image Features
id: image-features
description: Change the banner style.
settings:
    - 
        id: banner-type
        title: Banner Style
        type: class-select
        allowEmpty: false
        default: banner-fade
        options:
            - 
                label: Fancy Title
                value: banner-title
            -
                label: Fade
                value: banner-fade
            - 
                label: Notion
                value: banner-notion
   

*/
```
