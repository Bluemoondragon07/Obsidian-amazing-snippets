# CSS Banners, Icons (Experimental), and other Image Options
> Adapted from [efemkay's banner code](https://forum.obsidian.md/t/css-how-to-style-the-first-image-in-a-note/52839/9)

This snippet will allow you to use banner images in your notes using css classes and image alts. There are 3 banner styles—Fade, Fancy Title, and Notion—that can be toggled with the [Style Settings](https://github.com/mgmeyers/obsidian-style-settings/blob/main/obsidian-default-theme.css) plug-in. You can also control the banner height, similar to the height options in the [Banners plug-in](https://github.com/noatpad/obsidian-banners).

If you uncomment the marked section in the code, you can also turn an image into an icon positioned near the title of your note (**Warning: experimental**).

In addition, images can be floated to either side, and their shape can be changed with alts.


## How it Works
> **NOTE** 
> 
> In order to use the icons feature, you must first uncomment the **Icons** section in the code by deleting the `/*` and `*/` that is wrapped around the section.
### Css Classes
- `obsidian-banner` - type this in the frontmatter after `cssClasses` to enable the banner image.
- `obsidian-icon` - type this in the frontmatter after `cssClasses` to enable the icon image.
### Image Alts 
>**Example of an image alt** ***(banner):***`![image-alt|banner](image.png)`

-  `banner` - makes the image the banner image.
- `higher` - positions the banner image higher.
- `lower` - positions the banner image lower.
-  `circle`, `profile`, or `round` - typing any of these will make the image circular in shape, like a profile picture.
-  `left` - floats the image left.
- `right` - floats the image right
- `icon` (**Uncomment the Icons part of the code to use**) - turns the image into a title icon.
#### **A Warning About the Icon Feature**
I am still a beginner in CSS, and the icon feature did not turn out as good as I'd like. For the most part, it works fine. **BUT**, when viewing multiple panes at the same time, it drifts into a weird position, and a theme with a custom readable line length may disrupt its placement on the page.
You *can* still use the icons feature, but be warned: it can act a bit wonky.
## Screenshots
![](https://github.com/Bluemoondragon07/Obsidian-amazing-snippets/blob/main/Screenshots/Banners1.png)
![](https://github.com/Bluemoondragon07/Obsidian-amazing-snippets/blob/main/Screenshots/Banners2.png)
![](https://github.com/Bluemoondragon07/Obsidian-amazing-snippets/blob/main/Screenshots/Banners3.png)
![](https://github.com/Bluemoondragon07/Obsidian-amazing-snippets/blob/main/Screenshots/Banners4.png)

# Code
Copy the code below and paste it into a `.css` file in `.obsidian/snippets`.
```


/* ----- banner image variants ----- */
/* ---- majority done by efemkay ---- */

body {
    --banner-height: 250px;
   }
   
   /* ---- the code below is a slightly modified version of efemkay's banner image in this forum post: https://forum.obsidian.md/t/css-how-to-style-the-first-image-in-a-note/52839/ ---- */
   
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
           height: var(--banner-height);
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
            margin-top: calc(var(--banner-height) - 100px);
            margin-bottom: 50px !important;
            line-height: 1.2em ;
            text-align: center;
            color: white;
            padding: 7px 0px 7px 20px !important;
            background: radial-gradient(circle, rgba(0, 0, 0, 0.416) 0%, rgba(0, 0, 0, 0.233) 53%, rgba(0,0,0,0) 100%);    
        }
        
        .obsidian-banner .mod-header, .banner-fade .obsidian-banner .mod-header {
           position: relative;
           padding-top: calc(var(--banner-height) - 60px);
           z-index: 1;
        }
        .obsidian-banner img[alt*="banner"], .banner-fade .obsidian-banner img[alt*="banner"]{
           -webkit-mask-image: -webkit-gradient(linear, 50% 60%, 50% 100%, from(rgba(0,0,0,1)), to(rgba(0,0,0,0)));
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
           padding-top: calc(var(--banner-height) + 5px) !important;
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
   /* Uncomment the section below if you want to try it out */
   /* To use, type `obsidian-icon` in the frontmatter and use the alt `icon` on an image. 
    WARNING: icons may not respond to custom page widths in certain themes.*/
   
   
   
   /*
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
    -
        id: banner-height
        title: Banner Height
        type: variable-number-slider
        default: 250
        min: 100
        max: 350
        step: 5
        format: px
*/


```

# Credits
Special thanks to efemkay, who did most of the banner code in [this Obsidian thread](https://forum.obsidian.md/t/css-how-to-style-the-first-image-in-a-note/52839/)!
