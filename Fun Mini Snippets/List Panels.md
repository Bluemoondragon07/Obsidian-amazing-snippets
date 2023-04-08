# List Panels
> Adapted from the `mado-panels` CSS class in hydescarf's Mado Miniflow theme


This is a slightly modified version of hydescarf's `mado-panels` css class in the Mado Miniflow theme. It turns bulleted and numbered lists, as well as tasks, into panels.
It has been modified allow long, nested lines of text without overflowing.

![](https://github.com/Bluemoondragon07/Obsidian-amazing-snippets/blob/main/Screenshots/Panels.png?raw=true)

# How to Use
Just type `mado-panel` or `panel` in `cssClasses` in the frontmatter of a note.
## Example
```
---
cssClasses: panel
---
rest of note
```
# Code
```
/* --- adapted from the Mado Miniflow theme by hydescarf --- */

.mado-panel, .panel {
	--indentation-guide-color: transparent;
}
.mado-panel .markdown-preview-sizer>div ul,
.panel .markdown-preview-sizer>div ul{
	display:flex;
	flex-wrap:wrap;
	width:100%;
	gap:10px;
	transition:height 0.2s, opacity 0.2s;
	padding-inline:23px;
	padding-block:7px;
}

.mado-panel .markdown-preview-sizer>div ul li,
.panel .markdown-preview-sizer>div ul li {
	font-weight: normal;
	display:flexbox;
	align-items: center;
	padding-block:15px;
	padding-inline:20px;
	background: rgba(255, 255, 255, 0.03);
	border: 1px solid var(--background-modifier-border);
	transition:0.1s background, 0.1s box-shadow, transform 0.1s;
	text-align: center;
	width:flex;
	flex:auto;
	height: flex;
	max-width: flex;
	overflow:hidden;
	border-radius: var(--radius-m);
	margin-right: auto;
	margin-left: auto;
}
.theme-light .mado-panel .markdown-preview-sizer>div ul li,
.theme-light .panel .markdown-preview-sizer>div ul li{
	background: rgba(255, 255, 255, 0.16);
}

.mado-panel .markdown-preview-sizer>div ul li a:not(.tag),
.panel .markdown-preview-sizer>div ul li a:not(.tag){
	text-decoration: none;
	font-size: var(--h5-size);
}


[class*="mado-panel"] .markdown-preview-sizer>div ul li .list-bullet,
[class*="panel"] .markdown-preview-sizer>div ul li .list-bullet{
	display:none;
}
[class*="mado-panel"] .markdown-preview-sizer>div ul li:hover,
[class*="panel"] .markdown-preview-sizer>div ul li:hover{
	background:var(--background-secondary-alt);
	transform:translateY(-2px);
	transition: 0.1s background, 0.2 transform, opacity 1s;
}




[class*="mado-panel"] .markdown-preview-sizer>div li.task-list-item,
[class*="panel"] .markdown-preview-sizer>div li.task-list-item{
	position:relative;
}
[class*="mado-panel"] .markdown-preview-sizer>div li.task-list-item>input,
[class*="panel"] .markdown-preview-sizer>div li.task-list-item>input{
	padding:0px;
	position:absolute;
	left:unset;
	bottom:unset;
	top: 0;
	right:0;
	margin: 5px;
	border: 1px solid var(--checkbox-border-color);
}
[class*="mado-panel"] .markdown-preview-sizer>div li.task-list-item.is-checked,
[class*="panel"] .markdown-preview-sizer>div li.task-list-item.is-checked{
	background:var(--background-secondary-alt);
	opacity: 0.5;
}
```
