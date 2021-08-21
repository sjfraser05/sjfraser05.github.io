layout: post
title: "TEST POST"
date: 2021-08-21 07:23:00 -0000
categories: CATEGORY-1 CATEGORY-2

<!DOCTYPE html>
<html>
<head><meta charset="utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Covid SVM Classifier</title><script src="https://cdnjs.cloudflare.com/ajax/libs/require.js/2.1.10/require.min.js"></script>




<style type="text/css">
    pre { line-height: 125%; }
td.linenos .normal { color: inherit; background-color: transparent; padding-left: 5px; padding-right: 5px; }
span.linenos { color: inherit; background-color: transparent; padding-left: 5px; padding-right: 5px; }
td.linenos .special { color: #000000; background-color: #ffffc0; padding-left: 5px; padding-right: 5px; }
span.linenos.special { color: #000000; background-color: #ffffc0; padding-left: 5px; padding-right: 5px; }
.highlight .hll { background-color: var(--jp-cell-editor-active-background) }
.highlight { background: var(--jp-cell-editor-background); color: var(--jp-mirror-editor-variable-color) }
.highlight .c { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment */
.highlight .err { color: var(--jp-mirror-editor-error-color) } /* Error */
.highlight .k { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword */
.highlight .o { color: var(--jp-mirror-editor-operator-color); font-weight: bold } /* Operator */
.highlight .p { color: var(--jp-mirror-editor-punctuation-color) } /* Punctuation */
.highlight .ch { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Hashbang */
.highlight .cm { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Multiline */
.highlight .cp { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Preproc */
.highlight .cpf { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.PreprocFile */
.highlight .c1 { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Single */
.highlight .cs { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Special */
.highlight .kc { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Constant */
.highlight .kd { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Declaration */
.highlight .kn { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Namespace */
.highlight .kp { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Pseudo */
.highlight .kr { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Reserved */
.highlight .kt { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Type */
.highlight .m { color: var(--jp-mirror-editor-number-color) } /* Literal.Number */
.highlight .s { color: var(--jp-mirror-editor-string-color) } /* Literal.String */
.highlight .ow { color: var(--jp-mirror-editor-operator-color); font-weight: bold } /* Operator.Word */
.highlight .w { color: var(--jp-mirror-editor-variable-color) } /* Text.Whitespace */
.highlight .mb { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Bin */
.highlight .mf { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Float */
.highlight .mh { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Hex */
.highlight .mi { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Integer */
.highlight .mo { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Oct */
.highlight .sa { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Affix */
.highlight .sb { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Backtick */
.highlight .sc { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Char */
.highlight .dl { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Delimiter */
.highlight .sd { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Doc */
.highlight .s2 { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Double */
.highlight .se { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Escape */
.highlight .sh { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Heredoc */
.highlight .si { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Interpol */
.highlight .sx { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Other */
.highlight .sr { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Regex */
.highlight .s1 { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Single */
.highlight .ss { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Symbol */
.highlight .il { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Integer.Long */
  </style>



<style type="text/css">
/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*
 * Mozilla scrollbar styling
 */

/* use standard opaque scrollbars for most nodes */
[data-jp-theme-scrollbars='true'] {
  scrollbar-color: rgb(var(--jp-scrollbar-thumb-color))
    var(--jp-scrollbar-background-color);
}

/* for code nodes, use a transparent style of scrollbar. These selectors
 * will match lower in the tree, and so will override the above */
[data-jp-theme-scrollbars='true'] .CodeMirror-hscrollbar,
[data-jp-theme-scrollbars='true'] .CodeMirror-vscrollbar {
  scrollbar-color: rgba(var(--jp-scrollbar-thumb-color), 0.5) transparent;
}

/* tiny scrollbar */

.jp-scrollbar-tiny {
  scrollbar-color: rgba(var(--jp-scrollbar-thumb-color), 0.5) transparent;
  scrollbar-width: thin;
}

/*
 * Webkit scrollbar styling
 */

/* use standard opaque scrollbars for most nodes */

[data-jp-theme-scrollbars='true'] ::-webkit-scrollbar,
[data-jp-theme-scrollbars='true'] ::-webkit-scrollbar-corner {
  background: var(--jp-scrollbar-background-color);
}

[data-jp-theme-scrollbars='true'] ::-webkit-scrollbar-thumb {
  background: rgb(var(--jp-scrollbar-thumb-color));
  border: var(--jp-scrollbar-thumb-margin) solid transparent;
  background-clip: content-box;
  border-radius: var(--jp-scrollbar-thumb-radius);
}

[data-jp-theme-scrollbars='true'] ::-webkit-scrollbar-track:horizontal {
  border-left: var(--jp-scrollbar-endpad) solid
    var(--jp-scrollbar-background-color);
  border-right: var(--jp-scrollbar-endpad) solid
    var(--jp-scrollbar-background-color);
}

[data-jp-theme-scrollbars='true'] ::-webkit-scrollbar-track:vertical {
  border-top: var(--jp-scrollbar-endpad) solid
    var(--jp-scrollbar-background-color);
  border-bottom: var(--jp-scrollbar-endpad) solid
    var(--jp-scrollbar-background-color);
}

/* for code nodes, use a transparent style of scrollbar */

[data-jp-theme-scrollbars='true'] .CodeMirror-hscrollbar::-webkit-scrollbar,
[data-jp-theme-scrollbars='true'] .CodeMirror-vscrollbar::-webkit-scrollbar,
[data-jp-theme-scrollbars='true']
  .CodeMirror-hscrollbar::-webkit-scrollbar-corner,
[data-jp-theme-scrollbars='true']
  .CodeMirror-vscrollbar::-webkit-scrollbar-corner {
  background-color: transparent;
}

[data-jp-theme-scrollbars='true']
  .CodeMirror-hscrollbar::-webkit-scrollbar-thumb,
[data-jp-theme-scrollbars='true']
  .CodeMirror-vscrollbar::-webkit-scrollbar-thumb {
  background: rgba(var(--jp-scrollbar-thumb-color), 0.5);
  border: var(--jp-scrollbar-thumb-margin) solid transparent;
  background-clip: content-box;
  border-radius: var(--jp-scrollbar-thumb-radius);
}

[data-jp-theme-scrollbars='true']
  .CodeMirror-hscrollbar::-webkit-scrollbar-track:horizontal {
  border-left: var(--jp-scrollbar-endpad) solid transparent;
  border-right: var(--jp-scrollbar-endpad) solid transparent;
}

[data-jp-theme-scrollbars='true']
  .CodeMirror-vscrollbar::-webkit-scrollbar-track:vertical {
  border-top: var(--jp-scrollbar-endpad) solid transparent;
  border-bottom: var(--jp-scrollbar-endpad) solid transparent;
}

/* tiny scrollbar */

.jp-scrollbar-tiny::-webkit-scrollbar,
.jp-scrollbar-tiny::-webkit-scrollbar-corner {
  background-color: transparent;
  height: 4px;
  width: 4px;
}

.jp-scrollbar-tiny::-webkit-scrollbar-thumb {
  background: rgba(var(--jp-scrollbar-thumb-color), 0.5);
}

.jp-scrollbar-tiny::-webkit-scrollbar-track:horizontal {
  border-left: 0px solid transparent;
  border-right: 0px solid transparent;
}

.jp-scrollbar-tiny::-webkit-scrollbar-track:vertical {
  border-top: 0px solid transparent;
  border-bottom: 0px solid transparent;
}

/*
 * Phosphor
 */

.lm-ScrollBar[data-orientation='horizontal'] {
  min-height: 16px;
  max-height: 16px;
  min-width: 45px;
  border-top: 1px solid #a0a0a0;
}

.lm-ScrollBar[data-orientation='vertical'] {
  min-width: 16px;
  max-width: 16px;
  min-height: 45px;
  border-left: 1px solid #a0a0a0;
}

.lm-ScrollBar-button {
  background-color: #f0f0f0;
  background-position: center center;
  min-height: 15px;
  max-height: 15px;
  min-width: 15px;
  max-width: 15px;
}

.lm-ScrollBar-button:hover {
  background-color: #dadada;
}

.lm-ScrollBar-button.lm-mod-active {
  background-color: #cdcdcd;
}

.lm-ScrollBar-track {
  background: #f0f0f0;
}

.lm-ScrollBar-thumb {
  background: #cdcdcd;
}

.lm-ScrollBar-thumb:hover {
  background: #bababa;
}

.lm-ScrollBar-thumb.lm-mod-active {
  background: #a0a0a0;
}

.lm-ScrollBar[data-orientation='horizontal'] .lm-ScrollBar-thumb {
  height: 100%;
  min-width: 15px;
  border-left: 1px solid #a0a0a0;
  border-right: 1px solid #a0a0a0;
}

.lm-ScrollBar[data-orientation='vertical'] .lm-ScrollBar-thumb {
  width: 100%;
  min-height: 15px;
  border-top: 1px solid #a0a0a0;
  border-bottom: 1px solid #a0a0a0;
}

.lm-ScrollBar[data-orientation='horizontal']
  .lm-ScrollBar-button[data-action='decrement'] {
  background-image: var(--jp-icon-caret-left);
  background-size: 17px;
}

.lm-ScrollBar[data-orientation='horizontal']
  .lm-ScrollBar-button[data-action='increment'] {
  background-image: var(--jp-icon-caret-right);
  background-size: 17px;
}

.lm-ScrollBar[data-orientation='vertical']
  .lm-ScrollBar-button[data-action='decrement'] {
  background-image: var(--jp-icon-caret-up);
  background-size: 17px;
}

.lm-ScrollBar[data-orientation='vertical']
  .lm-ScrollBar-button[data-action='increment'] {
  background-image: var(--jp-icon-caret-down);
  background-size: 17px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-Widget, /* </DEPRECATED> */
.lm-Widget {
  box-sizing: border-box;
  position: relative;
  overflow: hidden;
  cursor: default;
}


/* <DEPRECATED> */ .p-Widget.p-mod-hidden, /* </DEPRECATED> */
.lm-Widget.lm-mod-hidden {
  display: none !important;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-CommandPalette, /* </DEPRECATED> */
.lm-CommandPalette {
  display: flex;
  flex-direction: column;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}


/* <DEPRECATED> */ .p-CommandPalette-search, /* </DEPRECATED> */
.lm-CommandPalette-search {
  flex: 0 0 auto;
}


/* <DEPRECATED> */ .p-CommandPalette-content, /* </DEPRECATED> */
.lm-CommandPalette-content {
  flex: 1 1 auto;
  margin: 0;
  padding: 0;
  min-height: 0;
  overflow: auto;
  list-style-type: none;
}


/* <DEPRECATED> */ .p-CommandPalette-header, /* </DEPRECATED> */
.lm-CommandPalette-header {
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}


/* <DEPRECATED> */ .p-CommandPalette-item, /* </DEPRECATED> */
.lm-CommandPalette-item {
  display: flex;
  flex-direction: row;
}


/* <DEPRECATED> */ .p-CommandPalette-itemIcon, /* </DEPRECATED> */
.lm-CommandPalette-itemIcon {
  flex: 0 0 auto;
}


/* <DEPRECATED> */ .p-CommandPalette-itemContent, /* </DEPRECATED> */
.lm-CommandPalette-itemContent {
  flex: 1 1 auto;
  overflow: hidden;
}


/* <DEPRECATED> */ .p-CommandPalette-itemShortcut, /* </DEPRECATED> */
.lm-CommandPalette-itemShortcut {
  flex: 0 0 auto;
}


/* <DEPRECATED> */ .p-CommandPalette-itemLabel, /* </DEPRECATED> */
.lm-CommandPalette-itemLabel {
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}

.lm-close-icon {
	border:1px solid transparent;
  background-color: transparent;
  position: absolute;
	z-index:1;
	right:3%;
	top: 0;
	bottom: 0;
	margin: auto;
	padding: 7px 0;
	display: none;
	vertical-align: middle;
  outline: 0;
  cursor: pointer;
}
.lm-close-icon:after {
	content: "X";
	display: block;
	width: 15px;
	height: 15px;
	text-align: center;
	color:#000;
	font-weight: normal;
	font-size: 12px;
	cursor: pointer;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-DockPanel, /* </DEPRECATED> */
.lm-DockPanel {
  z-index: 0;
}


/* <DEPRECATED> */ .p-DockPanel-widget, /* </DEPRECATED> */
.lm-DockPanel-widget {
  z-index: 0;
}


/* <DEPRECATED> */ .p-DockPanel-tabBar, /* </DEPRECATED> */
.lm-DockPanel-tabBar {
  z-index: 1;
}


/* <DEPRECATED> */ .p-DockPanel-handle, /* </DEPRECATED> */
.lm-DockPanel-handle {
  z-index: 2;
}


/* <DEPRECATED> */ .p-DockPanel-handle.p-mod-hidden, /* </DEPRECATED> */
.lm-DockPanel-handle.lm-mod-hidden {
  display: none !important;
}


/* <DEPRECATED> */ .p-DockPanel-handle:after, /* </DEPRECATED> */
.lm-DockPanel-handle:after {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  content: '';
}


/* <DEPRECATED> */
.p-DockPanel-handle[data-orientation='horizontal'],
/* </DEPRECATED> */
.lm-DockPanel-handle[data-orientation='horizontal'] {
  cursor: ew-resize;
}


/* <DEPRECATED> */
.p-DockPanel-handle[data-orientation='vertical'],
/* </DEPRECATED> */
.lm-DockPanel-handle[data-orientation='vertical'] {
  cursor: ns-resize;
}


/* <DEPRECATED> */
.p-DockPanel-handle[data-orientation='horizontal']:after,
/* </DEPRECATED> */
.lm-DockPanel-handle[data-orientation='horizontal']:after {
  left: 50%;
  min-width: 8px;
  transform: translateX(-50%);
}


/* <DEPRECATED> */
.p-DockPanel-handle[data-orientation='vertical']:after,
/* </DEPRECATED> */
.lm-DockPanel-handle[data-orientation='vertical']:after {
  top: 50%;
  min-height: 8px;
  transform: translateY(-50%);
}


/* <DEPRECATED> */ .p-DockPanel-overlay, /* </DEPRECATED> */
.lm-DockPanel-overlay {
  z-index: 3;
  box-sizing: border-box;
  pointer-events: none;
}


/* <DEPRECATED> */ .p-DockPanel-overlay.p-mod-hidden, /* </DEPRECATED> */
.lm-DockPanel-overlay.lm-mod-hidden {
  display: none !important;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-Menu, /* </DEPRECATED> */
.lm-Menu {
  z-index: 10000;
  position: absolute;
  white-space: nowrap;
  overflow-x: hidden;
  overflow-y: auto;
  outline: none;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}


/* <DEPRECATED> */ .p-Menu-content, /* </DEPRECATED> */
.lm-Menu-content {
  margin: 0;
  padding: 0;
  display: table;
  list-style-type: none;
}


/* <DEPRECATED> */ .p-Menu-item, /* </DEPRECATED> */
.lm-Menu-item {
  display: table-row;
}


/* <DEPRECATED> */
.p-Menu-item.p-mod-hidden,
.p-Menu-item.p-mod-collapsed,
/* </DEPRECATED> */
.lm-Menu-item.lm-mod-hidden,
.lm-Menu-item.lm-mod-collapsed {
  display: none !important;
}


/* <DEPRECATED> */
.p-Menu-itemIcon,
.p-Menu-itemSubmenuIcon,
/* </DEPRECATED> */
.lm-Menu-itemIcon,
.lm-Menu-itemSubmenuIcon {
  display: table-cell;
  text-align: center;
}


/* <DEPRECATED> */ .p-Menu-itemLabel, /* </DEPRECATED> */
.lm-Menu-itemLabel {
  display: table-cell;
  text-align: left;
}


/* <DEPRECATED> */ .p-Menu-itemShortcut, /* </DEPRECATED> */
.lm-Menu-itemShortcut {
  display: table-cell;
  text-align: right;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-MenuBar, /* </DEPRECATED> */
.lm-MenuBar {
  outline: none;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}


/* <DEPRECATED> */ .p-MenuBar-content, /* </DEPRECATED> */
.lm-MenuBar-content {
  margin: 0;
  padding: 0;
  display: flex;
  flex-direction: row;
  list-style-type: none;
}


/* <DEPRECATED> */ .p--MenuBar-item, /* </DEPRECATED> */
.lm-MenuBar-item {
  box-sizing: border-box;
}


/* <DEPRECATED> */
.p-MenuBar-itemIcon,
.p-MenuBar-itemLabel,
/* </DEPRECATED> */
.lm-MenuBar-itemIcon,
.lm-MenuBar-itemLabel {
  display: inline-block;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-ScrollBar, /* </DEPRECATED> */
.lm-ScrollBar {
  display: flex;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}


/* <DEPRECATED> */
.p-ScrollBar[data-orientation='horizontal'],
/* </DEPRECATED> */
.lm-ScrollBar[data-orientation='horizontal'] {
  flex-direction: row;
}


/* <DEPRECATED> */
.p-ScrollBar[data-orientation='vertical'],
/* </DEPRECATED> */
.lm-ScrollBar[data-orientation='vertical'] {
  flex-direction: column;
}


/* <DEPRECATED> */ .p-ScrollBar-button, /* </DEPRECATED> */
.lm-ScrollBar-button {
  box-sizing: border-box;
  flex: 0 0 auto;
}


/* <DEPRECATED> */ .p-ScrollBar-track, /* </DEPRECATED> */
.lm-ScrollBar-track {
  box-sizing: border-box;
  position: relative;
  overflow: hidden;
  flex: 1 1 auto;
}


/* <DEPRECATED> */ .p-ScrollBar-thumb, /* </DEPRECATED> */
.lm-ScrollBar-thumb {
  box-sizing: border-box;
  position: absolute;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-SplitPanel-child, /* </DEPRECATED> */
.lm-SplitPanel-child {
  z-index: 0;
}


/* <DEPRECATED> */ .p-SplitPanel-handle, /* </DEPRECATED> */
.lm-SplitPanel-handle {
  z-index: 1;
}


/* <DEPRECATED> */ .p-SplitPanel-handle.p-mod-hidden, /* </DEPRECATED> */
.lm-SplitPanel-handle.lm-mod-hidden {
  display: none !important;
}


/* <DEPRECATED> */ .p-SplitPanel-handle:after, /* </DEPRECATED> */
.lm-SplitPanel-handle:after {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  content: '';
}


/* <DEPRECATED> */
.p-SplitPanel[data-orientation='horizontal'] > .p-SplitPanel-handle,
/* </DEPRECATED> */
.lm-SplitPanel[data-orientation='horizontal'] > .lm-SplitPanel-handle {
  cursor: ew-resize;
}


/* <DEPRECATED> */
.p-SplitPanel[data-orientation='vertical'] > .p-SplitPanel-handle,
/* </DEPRECATED> */
.lm-SplitPanel[data-orientation='vertical'] > .lm-SplitPanel-handle {
  cursor: ns-resize;
}


/* <DEPRECATED> */
.p-SplitPanel[data-orientation='horizontal'] > .p-SplitPanel-handle:after,
/* </DEPRECATED> */
.lm-SplitPanel[data-orientation='horizontal'] > .lm-SplitPanel-handle:after {
  left: 50%;
  min-width: 8px;
  transform: translateX(-50%);
}


/* <DEPRECATED> */
.p-SplitPanel[data-orientation='vertical'] > .p-SplitPanel-handle:after,
/* </DEPRECATED> */
.lm-SplitPanel[data-orientation='vertical'] > .lm-SplitPanel-handle:after {
  top: 50%;
  min-height: 8px;
  transform: translateY(-50%);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-TabBar, /* </DEPRECATED> */
.lm-TabBar {
  display: flex;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}


/* <DEPRECATED> */ .p-TabBar[data-orientation='horizontal'], /* </DEPRECATED> */
.lm-TabBar[data-orientation='horizontal'] {
  flex-direction: row;
}


/* <DEPRECATED> */ .p-TabBar[data-orientation='vertical'], /* </DEPRECATED> */
.lm-TabBar[data-orientation='vertical'] {
  flex-direction: column;
}


/* <DEPRECATED> */ .p-TabBar-content, /* </DEPRECATED> */
.lm-TabBar-content {
  margin: 0;
  padding: 0;
  display: flex;
  flex: 1 1 auto;
  list-style-type: none;
}


/* <DEPRECATED> */
.p-TabBar[data-orientation='horizontal'] > .p-TabBar-content,
/* </DEPRECATED> */
.lm-TabBar[data-orientation='horizontal'] > .lm-TabBar-content {
  flex-direction: row;
}


/* <DEPRECATED> */
.p-TabBar[data-orientation='vertical'] > .p-TabBar-content,
/* </DEPRECATED> */
.lm-TabBar[data-orientation='vertical'] > .lm-TabBar-content {
  flex-direction: column;
}


/* <DEPRECATED> */ .p-TabBar-tab, /* </DEPRECATED> */
.lm-TabBar-tab {
  display: flex;
  flex-direction: row;
  box-sizing: border-box;
  overflow: hidden;
}


/* <DEPRECATED> */
.p-TabBar-tabIcon,
.p-TabBar-tabCloseIcon,
/* </DEPRECATED> */
.lm-TabBar-tabIcon,
.lm-TabBar-tabCloseIcon {
  flex: 0 0 auto;
}


/* <DEPRECATED> */ .p-TabBar-tabLabel, /* </DEPRECATED> */
.lm-TabBar-tabLabel {
  flex: 1 1 auto;
  overflow: hidden;
  white-space: nowrap;
}


.lm-TabBar-tabInput {
  user-select: all;
  width: 100%;
  box-sizing : border-box;
}


/* <DEPRECATED> */ .p-TabBar-tab.p-mod-hidden, /* </DEPRECATED> */
.lm-TabBar-tab.lm-mod-hidden {
  display: none !important;
}


/* <DEPRECATED> */ .p-TabBar.p-mod-dragging .p-TabBar-tab, /* </DEPRECATED> */
.lm-TabBar.lm-mod-dragging .lm-TabBar-tab {
  position: relative;
}


/* <DEPRECATED> */
.p-TabBar.p-mod-dragging[data-orientation='horizontal'] .p-TabBar-tab,
/* </DEPRECATED> */
.lm-TabBar.lm-mod-dragging[data-orientation='horizontal'] .lm-TabBar-tab {
  left: 0;
  transition: left 150ms ease;
}


/* <DEPRECATED> */
.p-TabBar.p-mod-dragging[data-orientation='vertical'] .p-TabBar-tab,
/* </DEPRECATED> */
.lm-TabBar.lm-mod-dragging[data-orientation='vertical'] .lm-TabBar-tab {
  top: 0;
  transition: top 150ms ease;
}


/* <DEPRECATED> */
.p-TabBar.p-mod-dragging .p-TabBar-tab.p-mod-dragging,
/* </DEPRECATED> */
.lm-TabBar.lm-mod-dragging .lm-TabBar-tab.lm-mod-dragging {
  transition: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-TabPanel-tabBar, /* </DEPRECATED> */
.lm-TabPanel-tabBar {
  z-index: 1;
}


/* <DEPRECATED> */ .p-TabPanel-stackedPanel, /* </DEPRECATED> */
.lm-TabPanel-stackedPanel {
  z-index: 0;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/

@charset "UTF-8";
html{
  -webkit-box-sizing:border-box;
          box-sizing:border-box; }

*,
*::before,
*::after{
  -webkit-box-sizing:inherit;
          box-sizing:inherit; }

body{
  font-size:14px;
  font-weight:400;
  letter-spacing:0;
  line-height:1.28581;
  text-transform:none;
  color:#182026;
  font-family:-apple-system, "BlinkMacSystemFont", "Segoe UI", "Roboto", "Oxygen", "Ubuntu", "Cantarell", "Open Sans", "Helvetica Neue", "Icons16", sans-serif; }

p{
  margin-bottom:10px;
  margin-top:0; }

small{
  font-size:12px; }

strong{
  font-weight:600; }

::-moz-selection{
  background:rgba(125, 188, 255, 0.6); }

::selection{
  background:rgba(125, 188, 255, 0.6); }
.bp3-heading{
  color:#182026;
  font-weight:600;
  margin:0 0 10px;
  padding:0; }
  .bp3-dark .bp3-heading{
    color:#f5f8fa; }

h1.bp3-heading, .bp3-running-text h1{
  font-size:36px;
  line-height:40px; }

h2.bp3-heading, .bp3-running-text h2{
  font-size:28px;
  line-height:32px; }

h3.bp3-heading, .bp3-running-text h3{
  font-size:22px;
  line-height:25px; }

h4.bp3-heading, .bp3-running-text h4{
  font-size:18px;
  line-height:21px; }

h5.bp3-heading, .bp3-running-text h5{
  font-size:16px;
  line-height:19px; }

h6.bp3-heading, .bp3-running-text h6{
  font-size:14px;
  line-height:16px; }
.bp3-ui-text{
  font-size:14px;
  font-weight:400;
  letter-spacing:0;
  line-height:1.28581;
  text-transform:none; }

.bp3-monospace-text{
  font-family:monospace;
  text-transform:none; }

.bp3-text-muted{
  color:#5c7080; }
  .bp3-dark .bp3-text-muted{
    color:#a7b6c2; }

.bp3-text-disabled{
  color:rgba(92, 112, 128, 0.6); }
  .bp3-dark .bp3-text-disabled{
    color:rgba(167, 182, 194, 0.6); }

.bp3-text-overflow-ellipsis{
  overflow:hidden;
  text-overflow:ellipsis;
  white-space:nowrap;
  word-wrap:normal; }
.bp3-running-text{
  font-size:14px;
  line-height:1.5; }
  .bp3-running-text h1{
    color:#182026;
    font-weight:600;
    margin-bottom:20px;
    margin-top:40px; }
    .bp3-dark .bp3-running-text h1{
      color:#f5f8fa; }
  .bp3-running-text h2{
    color:#182026;
    font-weight:600;
    margin-bottom:20px;
    margin-top:40px; }
    .bp3-dark .bp3-running-text h2{
      color:#f5f8fa; }
  .bp3-running-text h3{
    color:#182026;
    font-weight:600;
    margin-bottom:20px;
    margin-top:40px; }
    .bp3-dark .bp3-running-text h3{
      color:#f5f8fa; }
  .bp3-running-text h4{
    color:#182026;
    font-weight:600;
    margin-bottom:20px;
    margin-top:40px; }
    .bp3-dark .bp3-running-text h4{
      color:#f5f8fa; }
  .bp3-running-text h5{
    color:#182026;
    font-weight:600;
    margin-bottom:20px;
    margin-top:40px; }
    .bp3-dark .bp3-running-text h5{
      color:#f5f8fa; }
  .bp3-running-text h6{
    color:#182026;
    font-weight:600;
    margin-bottom:20px;
    margin-top:40px; }
    .bp3-dark .bp3-running-text h6{
      color:#f5f8fa; }
  .bp3-running-text hr{
    border:none;
    border-bottom:1px solid rgba(16, 22, 26, 0.15);
    margin:20px 0; }
    .bp3-dark .bp3-running-text hr{
      border-color:rgba(255, 255, 255, 0.15); }
  .bp3-running-text p{
    margin:0 0 10px;
    padding:0; }

.bp3-text-large{
  font-size:16px; }

.bp3-text-small{
  font-size:12px; }
a{
  color:#106ba3;
  text-decoration:none; }
  a:hover{
    color:#106ba3;
    cursor:pointer;
    text-decoration:underline; }
  a .bp3-icon, a .bp3-icon-standard, a .bp3-icon-large{
    color:inherit; }
  a code,
  .bp3-dark a code{
    color:inherit; }
  .bp3-dark a,
  .bp3-dark a:hover{
    color:#48aff0; }
    .bp3-dark a .bp3-icon, .bp3-dark a .bp3-icon-standard, .bp3-dark a .bp3-icon-large,
    .bp3-dark a:hover .bp3-icon,
    .bp3-dark a:hover .bp3-icon-standard,
    .bp3-dark a:hover .bp3-icon-large{
      color:inherit; }
.bp3-running-text code, .bp3-code{
  font-family:monospace;
  text-transform:none;
  background:rgba(255, 255, 255, 0.7);
  border-radius:3px;
  -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2);
          box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2);
  color:#5c7080;
  font-size:smaller;
  padding:2px 5px; }
  .bp3-dark .bp3-running-text code, .bp3-running-text .bp3-dark code, .bp3-dark .bp3-code{
    background:rgba(16, 22, 26, 0.3);
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
    color:#a7b6c2; }
  .bp3-running-text a > code, a > .bp3-code{
    color:#137cbd; }
    .bp3-dark .bp3-running-text a > code, .bp3-running-text .bp3-dark a > code, .bp3-dark a > .bp3-code{
      color:inherit; }

.bp3-running-text pre, .bp3-code-block{
  font-family:monospace;
  text-transform:none;
  background:rgba(255, 255, 255, 0.7);
  border-radius:3px;
  -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15);
          box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15);
  color:#182026;
  display:block;
  font-size:13px;
  line-height:1.4;
  margin:10px 0;
  padding:13px 15px 12px;
  word-break:break-all;
  word-wrap:break-word; }
  .bp3-dark .bp3-running-text pre, .bp3-running-text .bp3-dark pre, .bp3-dark .bp3-code-block{
    background:rgba(16, 22, 26, 0.3);
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
    color:#f5f8fa; }
  .bp3-running-text pre > code, .bp3-code-block > code{
    background:none;
    -webkit-box-shadow:none;
            box-shadow:none;
    color:inherit;
    font-size:inherit;
    padding:0; }

.bp3-running-text kbd, .bp3-key{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  background:#ffffff;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
  color:#5c7080;
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex;
  font-family:inherit;
  font-size:12px;
  height:24px;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  line-height:24px;
  min-width:24px;
  padding:3px 6px;
  vertical-align:middle; }
  .bp3-running-text kbd .bp3-icon, .bp3-key .bp3-icon, .bp3-running-text kbd .bp3-icon-standard, .bp3-key .bp3-icon-standard, .bp3-running-text kbd .bp3-icon-large, .bp3-key .bp3-icon-large{
    margin-right:5px; }
  .bp3-dark .bp3-running-text kbd, .bp3-running-text .bp3-dark kbd, .bp3-dark .bp3-key{
    background:#394b59;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
    color:#a7b6c2; }
.bp3-running-text blockquote, .bp3-blockquote{
  border-left:solid 4px rgba(167, 182, 194, 0.5);
  margin:0 0 10px;
  padding:0 20px; }
  .bp3-dark .bp3-running-text blockquote, .bp3-running-text .bp3-dark blockquote, .bp3-dark .bp3-blockquote{
    border-color:rgba(115, 134, 148, 0.5); }
.bp3-running-text ul,
.bp3-running-text ol, .bp3-list{
  margin:10px 0;
  padding-left:30px; }
  .bp3-running-text ul li:not(:last-child), .bp3-running-text ol li:not(:last-child), .bp3-list li:not(:last-child){
    margin-bottom:5px; }
  .bp3-running-text ul ol, .bp3-running-text ol ol, .bp3-list ol,
  .bp3-running-text ul ul,
  .bp3-running-text ol ul,
  .bp3-list ul{
    margin-top:5px; }

.bp3-list-unstyled{
  list-style:none;
  margin:0;
  padding:0; }
  .bp3-list-unstyled li{
    padding:0; }
.bp3-rtl{
  text-align:right; }

.bp3-dark{
  color:#f5f8fa; }

:focus{
  outline:rgba(19, 124, 189, 0.6) auto 2px;
  outline-offset:2px;
  -moz-outline-radius:6px; }

.bp3-focus-disabled :focus{
  outline:none !important; }
  .bp3-focus-disabled :focus ~ .bp3-control-indicator{
    outline:none !important; }

.bp3-alert{
  max-width:400px;
  padding:20px; }

.bp3-alert-body{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex; }
  .bp3-alert-body .bp3-icon{
    font-size:40px;
    margin-right:20px;
    margin-top:0; }

.bp3-alert-contents{
  word-break:break-word; }

.bp3-alert-footer{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:reverse;
      -ms-flex-direction:row-reverse;
          flex-direction:row-reverse;
  margin-top:10px; }
  .bp3-alert-footer .bp3-button{
    margin-left:10px; }
.bp3-breadcrumbs{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  cursor:default;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -ms-flex-wrap:wrap;
      flex-wrap:wrap;
  height:30px;
  list-style:none;
  margin:0;
  padding:0; }
  .bp3-breadcrumbs > li{
    -webkit-box-align:center;
        -ms-flex-align:center;
            align-items:center;
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex; }
    .bp3-breadcrumbs > li::after{
      background:url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 16 16'%3e%3cpath fill-rule='evenodd' clip-rule='evenodd' d='M10.71 7.29l-4-4a1.003 1.003 0 00-1.42 1.42L8.59 8 5.3 11.29c-.19.18-.3.43-.3.71a1.003 1.003 0 001.71.71l4-4c.18-.18.29-.43.29-.71 0-.28-.11-.53-.29-.71z' fill='%235C7080'/%3e%3c/svg%3e");
      content:"";
      display:block;
      height:16px;
      margin:0 5px;
      width:16px; }
    .bp3-breadcrumbs > li:last-of-type::after{
      display:none; }

.bp3-breadcrumb,
.bp3-breadcrumb-current,
.bp3-breadcrumbs-collapsed{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex;
  font-size:16px; }

.bp3-breadcrumb,
.bp3-breadcrumbs-collapsed{
  color:#5c7080; }

.bp3-breadcrumb:hover{
  text-decoration:none; }

.bp3-breadcrumb.bp3-disabled{
  color:rgba(92, 112, 128, 0.6);
  cursor:not-allowed; }

.bp3-breadcrumb .bp3-icon{
  margin-right:5px; }

.bp3-breadcrumb-current{
  color:inherit;
  font-weight:600; }
  .bp3-breadcrumb-current .bp3-input{
    font-size:inherit;
    font-weight:inherit;
    vertical-align:baseline; }

.bp3-breadcrumbs-collapsed{
  background:#ced9e0;
  border:none;
  border-radius:3px;
  cursor:pointer;
  margin-right:2px;
  padding:1px 5px;
  vertical-align:text-bottom; }
  .bp3-breadcrumbs-collapsed::before{
    background:url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 16 16'%3e%3cg fill='%235C7080'%3e%3ccircle cx='2' cy='8.03' r='2'/%3e%3ccircle cx='14' cy='8.03' r='2'/%3e%3ccircle cx='8' cy='8.03' r='2'/%3e%3c/g%3e%3c/svg%3e") center no-repeat;
    content:"";
    display:block;
    height:16px;
    width:16px; }
  .bp3-breadcrumbs-collapsed:hover{
    background:#bfccd6;
    color:#182026;
    text-decoration:none; }

.bp3-dark .bp3-breadcrumb,
.bp3-dark .bp3-breadcrumbs-collapsed{
  color:#a7b6c2; }

.bp3-dark .bp3-breadcrumbs > li::after{
  color:#a7b6c2; }

.bp3-dark .bp3-breadcrumb.bp3-disabled{
  color:rgba(167, 182, 194, 0.6); }

.bp3-dark .bp3-breadcrumb-current{
  color:#f5f8fa; }

.bp3-dark .bp3-breadcrumbs-collapsed{
  background:rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-breadcrumbs-collapsed:hover{
    background:rgba(16, 22, 26, 0.6);
    color:#f5f8fa; }
.bp3-button{
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  border:none;
  border-radius:3px;
  cursor:pointer;
  font-size:14px;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  padding:5px 10px;
  text-align:left;
  vertical-align:middle;
  min-height:30px;
  min-width:30px; }
  .bp3-button > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-button > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-button::before,
  .bp3-button > *{
    margin-right:7px; }
  .bp3-button:empty::before,
  .bp3-button > :last-child{
    margin-right:0; }
  .bp3-button:empty{
    padding:0 !important; }
  .bp3-button:disabled, .bp3-button.bp3-disabled{
    cursor:not-allowed; }
  .bp3-button.bp3-fill{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    width:100%; }
  .bp3-button.bp3-align-right,
  .bp3-align-right .bp3-button{
    text-align:right; }
  .bp3-button.bp3-align-left,
  .bp3-align-left .bp3-button{
    text-align:left; }
  .bp3-button:not([class*="bp3-intent-"]){
    background-color:#f5f8fa;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.8)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    color:#182026; }
    .bp3-button:not([class*="bp3-intent-"]):hover{
      background-clip:padding-box;
      background-color:#ebf1f5;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1); }
    .bp3-button:not([class*="bp3-intent-"]):active, .bp3-button:not([class*="bp3-intent-"]).bp3-active{
      background-color:#d8e1e8;
      background-image:none;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-button:not([class*="bp3-intent-"]):disabled, .bp3-button:not([class*="bp3-intent-"]).bp3-disabled{
      background-color:rgba(206, 217, 224, 0.5);
      background-image:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(92, 112, 128, 0.6);
      cursor:not-allowed;
      outline:none; }
      .bp3-button:not([class*="bp3-intent-"]):disabled.bp3-active, .bp3-button:not([class*="bp3-intent-"]):disabled.bp3-active:hover, .bp3-button:not([class*="bp3-intent-"]).bp3-disabled.bp3-active, .bp3-button:not([class*="bp3-intent-"]).bp3-disabled.bp3-active:hover{
        background:rgba(206, 217, 224, 0.7); }
  .bp3-button.bp3-intent-primary{
    background-color:#137cbd;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    color:#ffffff; }
    .bp3-button.bp3-intent-primary:hover, .bp3-button.bp3-intent-primary:active, .bp3-button.bp3-intent-primary.bp3-active{
      color:#ffffff; }
    .bp3-button.bp3-intent-primary:hover{
      background-color:#106ba3;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2); }
    .bp3-button.bp3-intent-primary:active, .bp3-button.bp3-intent-primary.bp3-active{
      background-color:#0e5a8a;
      background-image:none;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-button.bp3-intent-primary:disabled, .bp3-button.bp3-intent-primary.bp3-disabled{
      background-color:rgba(19, 124, 189, 0.5);
      background-image:none;
      border-color:transparent;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(255, 255, 255, 0.6); }
  .bp3-button.bp3-intent-success{
    background-color:#0f9960;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    color:#ffffff; }
    .bp3-button.bp3-intent-success:hover, .bp3-button.bp3-intent-success:active, .bp3-button.bp3-intent-success.bp3-active{
      color:#ffffff; }
    .bp3-button.bp3-intent-success:hover{
      background-color:#0d8050;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2); }
    .bp3-button.bp3-intent-success:active, .bp3-button.bp3-intent-success.bp3-active{
      background-color:#0a6640;
      background-image:none;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-button.bp3-intent-success:disabled, .bp3-button.bp3-intent-success.bp3-disabled{
      background-color:rgba(15, 153, 96, 0.5);
      background-image:none;
      border-color:transparent;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(255, 255, 255, 0.6); }
  .bp3-button.bp3-intent-warning{
    background-color:#d9822b;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    color:#ffffff; }
    .bp3-button.bp3-intent-warning:hover, .bp3-button.bp3-intent-warning:active, .bp3-button.bp3-intent-warning.bp3-active{
      color:#ffffff; }
    .bp3-button.bp3-intent-warning:hover{
      background-color:#bf7326;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2); }
    .bp3-button.bp3-intent-warning:active, .bp3-button.bp3-intent-warning.bp3-active{
      background-color:#a66321;
      background-image:none;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-button.bp3-intent-warning:disabled, .bp3-button.bp3-intent-warning.bp3-disabled{
      background-color:rgba(217, 130, 43, 0.5);
      background-image:none;
      border-color:transparent;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(255, 255, 255, 0.6); }
  .bp3-button.bp3-intent-danger{
    background-color:#db3737;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    color:#ffffff; }
    .bp3-button.bp3-intent-danger:hover, .bp3-button.bp3-intent-danger:active, .bp3-button.bp3-intent-danger.bp3-active{
      color:#ffffff; }
    .bp3-button.bp3-intent-danger:hover{
      background-color:#c23030;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2); }
    .bp3-button.bp3-intent-danger:active, .bp3-button.bp3-intent-danger.bp3-active{
      background-color:#a82a2a;
      background-image:none;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-button.bp3-intent-danger:disabled, .bp3-button.bp3-intent-danger.bp3-disabled{
      background-color:rgba(219, 55, 55, 0.5);
      background-image:none;
      border-color:transparent;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(255, 255, 255, 0.6); }
  .bp3-button[class*="bp3-intent-"] .bp3-button-spinner .bp3-spinner-head{
    stroke:#ffffff; }
  .bp3-button.bp3-large,
  .bp3-large .bp3-button{
    min-height:40px;
    min-width:40px;
    font-size:16px;
    padding:5px 15px; }
    .bp3-button.bp3-large::before,
    .bp3-button.bp3-large > *,
    .bp3-large .bp3-button::before,
    .bp3-large .bp3-button > *{
      margin-right:10px; }
    .bp3-button.bp3-large:empty::before,
    .bp3-button.bp3-large > :last-child,
    .bp3-large .bp3-button:empty::before,
    .bp3-large .bp3-button > :last-child{
      margin-right:0; }
  .bp3-button.bp3-small,
  .bp3-small .bp3-button{
    min-height:24px;
    min-width:24px;
    padding:0 7px; }
  .bp3-button.bp3-loading{
    position:relative; }
    .bp3-button.bp3-loading[class*="bp3-icon-"]::before{
      visibility:hidden; }
    .bp3-button.bp3-loading .bp3-button-spinner{
      margin:0;
      position:absolute; }
    .bp3-button.bp3-loading > :not(.bp3-button-spinner){
      visibility:hidden; }
  .bp3-button[class*="bp3-icon-"]::before{
    font-family:"Icons16", sans-serif;
    font-size:16px;
    font-style:normal;
    font-weight:400;
    line-height:1;
    -moz-osx-font-smoothing:grayscale;
    -webkit-font-smoothing:antialiased;
    color:#5c7080; }
  .bp3-button .bp3-icon, .bp3-button .bp3-icon-standard, .bp3-button .bp3-icon-large{
    color:#5c7080; }
    .bp3-button .bp3-icon.bp3-align-right, .bp3-button .bp3-icon-standard.bp3-align-right, .bp3-button .bp3-icon-large.bp3-align-right{
      margin-left:7px; }
  .bp3-button .bp3-icon:first-child:last-child,
  .bp3-button .bp3-spinner + .bp3-icon:last-child{
    margin:0 -7px; }
  .bp3-dark .bp3-button:not([class*="bp3-intent-"]){
    background-color:#394b59;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.05)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0));
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
    color:#f5f8fa; }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]):hover, .bp3-dark .bp3-button:not([class*="bp3-intent-"]):active, .bp3-dark .bp3-button:not([class*="bp3-intent-"]).bp3-active{
      color:#f5f8fa; }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]):hover{
      background-color:#30404d;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]):active, .bp3-dark .bp3-button:not([class*="bp3-intent-"]).bp3-active{
      background-color:#202b33;
      background-image:none;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]):disabled, .bp3-dark .bp3-button:not([class*="bp3-intent-"]).bp3-disabled{
      background-color:rgba(57, 75, 89, 0.5);
      background-image:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(167, 182, 194, 0.6); }
      .bp3-dark .bp3-button:not([class*="bp3-intent-"]):disabled.bp3-active, .bp3-dark .bp3-button:not([class*="bp3-intent-"]).bp3-disabled.bp3-active{
        background:rgba(57, 75, 89, 0.7); }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]) .bp3-button-spinner .bp3-spinner-head{
      background:rgba(16, 22, 26, 0.5);
      stroke:#8a9ba8; }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"])[class*="bp3-icon-"]::before{
      color:#a7b6c2; }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]) .bp3-icon, .bp3-dark .bp3-button:not([class*="bp3-intent-"]) .bp3-icon-standard, .bp3-dark .bp3-button:not([class*="bp3-intent-"]) .bp3-icon-large{
      color:#a7b6c2; }
  .bp3-dark .bp3-button[class*="bp3-intent-"]{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-button[class*="bp3-intent-"]:hover{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-button[class*="bp3-intent-"]:active, .bp3-dark .bp3-button[class*="bp3-intent-"].bp3-active{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-dark .bp3-button[class*="bp3-intent-"]:disabled, .bp3-dark .bp3-button[class*="bp3-intent-"].bp3-disabled{
      background-image:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(255, 255, 255, 0.3); }
    .bp3-dark .bp3-button[class*="bp3-intent-"] .bp3-button-spinner .bp3-spinner-head{
      stroke:#8a9ba8; }
  .bp3-button:disabled::before,
  .bp3-button:disabled .bp3-icon, .bp3-button:disabled .bp3-icon-standard, .bp3-button:disabled .bp3-icon-large, .bp3-button.bp3-disabled::before,
  .bp3-button.bp3-disabled .bp3-icon, .bp3-button.bp3-disabled .bp3-icon-standard, .bp3-button.bp3-disabled .bp3-icon-large, .bp3-button[class*="bp3-intent-"]::before,
  .bp3-button[class*="bp3-intent-"] .bp3-icon, .bp3-button[class*="bp3-intent-"] .bp3-icon-standard, .bp3-button[class*="bp3-intent-"] .bp3-icon-large{
    color:inherit !important; }
  .bp3-button.bp3-minimal{
    background:none;
    -webkit-box-shadow:none;
            box-shadow:none; }
    .bp3-button.bp3-minimal:hover{
      background:rgba(167, 182, 194, 0.3);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#182026;
      text-decoration:none; }
    .bp3-button.bp3-minimal:active, .bp3-button.bp3-minimal.bp3-active{
      background:rgba(115, 134, 148, 0.3);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#182026; }
    .bp3-button.bp3-minimal:disabled, .bp3-button.bp3-minimal:disabled:hover, .bp3-button.bp3-minimal.bp3-disabled, .bp3-button.bp3-minimal.bp3-disabled:hover{
      background:none;
      color:rgba(92, 112, 128, 0.6);
      cursor:not-allowed; }
      .bp3-button.bp3-minimal:disabled.bp3-active, .bp3-button.bp3-minimal:disabled:hover.bp3-active, .bp3-button.bp3-minimal.bp3-disabled.bp3-active, .bp3-button.bp3-minimal.bp3-disabled:hover.bp3-active{
        background:rgba(115, 134, 148, 0.3); }
    .bp3-dark .bp3-button.bp3-minimal{
      background:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:inherit; }
      .bp3-dark .bp3-button.bp3-minimal:hover, .bp3-dark .bp3-button.bp3-minimal:active, .bp3-dark .bp3-button.bp3-minimal.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none; }
      .bp3-dark .bp3-button.bp3-minimal:hover{
        background:rgba(138, 155, 168, 0.15); }
      .bp3-dark .bp3-button.bp3-minimal:active, .bp3-dark .bp3-button.bp3-minimal.bp3-active{
        background:rgba(138, 155, 168, 0.3);
        color:#f5f8fa; }
      .bp3-dark .bp3-button.bp3-minimal:disabled, .bp3-dark .bp3-button.bp3-minimal:disabled:hover, .bp3-dark .bp3-button.bp3-minimal.bp3-disabled, .bp3-dark .bp3-button.bp3-minimal.bp3-disabled:hover{
        background:none;
        color:rgba(167, 182, 194, 0.6);
        cursor:not-allowed; }
        .bp3-dark .bp3-button.bp3-minimal:disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal:disabled:hover.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-disabled:hover.bp3-active{
          background:rgba(138, 155, 168, 0.3); }
    .bp3-button.bp3-minimal.bp3-intent-primary{
      color:#106ba3; }
      .bp3-button.bp3-minimal.bp3-intent-primary:hover, .bp3-button.bp3-minimal.bp3-intent-primary:active, .bp3-button.bp3-minimal.bp3-intent-primary.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#106ba3; }
      .bp3-button.bp3-minimal.bp3-intent-primary:hover{
        background:rgba(19, 124, 189, 0.15);
        color:#106ba3; }
      .bp3-button.bp3-minimal.bp3-intent-primary:active, .bp3-button.bp3-minimal.bp3-intent-primary.bp3-active{
        background:rgba(19, 124, 189, 0.3);
        color:#106ba3; }
      .bp3-button.bp3-minimal.bp3-intent-primary:disabled, .bp3-button.bp3-minimal.bp3-intent-primary.bp3-disabled{
        background:none;
        color:rgba(16, 107, 163, 0.5); }
        .bp3-button.bp3-minimal.bp3-intent-primary:disabled.bp3-active, .bp3-button.bp3-minimal.bp3-intent-primary.bp3-disabled.bp3-active{
          background:rgba(19, 124, 189, 0.3); }
      .bp3-button.bp3-minimal.bp3-intent-primary .bp3-button-spinner .bp3-spinner-head{
        stroke:#106ba3; }
      .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary{
        color:#48aff0; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary:hover{
          background:rgba(19, 124, 189, 0.2);
          color:#48aff0; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary:active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary.bp3-active{
          background:rgba(19, 124, 189, 0.3);
          color:#48aff0; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary:disabled, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary.bp3-disabled{
          background:none;
          color:rgba(72, 175, 240, 0.5); }
          .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary:disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary.bp3-disabled.bp3-active{
            background:rgba(19, 124, 189, 0.3); }
    .bp3-button.bp3-minimal.bp3-intent-success{
      color:#0d8050; }
      .bp3-button.bp3-minimal.bp3-intent-success:hover, .bp3-button.bp3-minimal.bp3-intent-success:active, .bp3-button.bp3-minimal.bp3-intent-success.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#0d8050; }
      .bp3-button.bp3-minimal.bp3-intent-success:hover{
        background:rgba(15, 153, 96, 0.15);
        color:#0d8050; }
      .bp3-button.bp3-minimal.bp3-intent-success:active, .bp3-button.bp3-minimal.bp3-intent-success.bp3-active{
        background:rgba(15, 153, 96, 0.3);
        color:#0d8050; }
      .bp3-button.bp3-minimal.bp3-intent-success:disabled, .bp3-button.bp3-minimal.bp3-intent-success.bp3-disabled{
        background:none;
        color:rgba(13, 128, 80, 0.5); }
        .bp3-button.bp3-minimal.bp3-intent-success:disabled.bp3-active, .bp3-button.bp3-minimal.bp3-intent-success.bp3-disabled.bp3-active{
          background:rgba(15, 153, 96, 0.3); }
      .bp3-button.bp3-minimal.bp3-intent-success .bp3-button-spinner .bp3-spinner-head{
        stroke:#0d8050; }
      .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success{
        color:#3dcc91; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success:hover{
          background:rgba(15, 153, 96, 0.2);
          color:#3dcc91; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success:active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success.bp3-active{
          background:rgba(15, 153, 96, 0.3);
          color:#3dcc91; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success:disabled, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success.bp3-disabled{
          background:none;
          color:rgba(61, 204, 145, 0.5); }
          .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success:disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success.bp3-disabled.bp3-active{
            background:rgba(15, 153, 96, 0.3); }
    .bp3-button.bp3-minimal.bp3-intent-warning{
      color:#bf7326; }
      .bp3-button.bp3-minimal.bp3-intent-warning:hover, .bp3-button.bp3-minimal.bp3-intent-warning:active, .bp3-button.bp3-minimal.bp3-intent-warning.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#bf7326; }
      .bp3-button.bp3-minimal.bp3-intent-warning:hover{
        background:rgba(217, 130, 43, 0.15);
        color:#bf7326; }
      .bp3-button.bp3-minimal.bp3-intent-warning:active, .bp3-button.bp3-minimal.bp3-intent-warning.bp3-active{
        background:rgba(217, 130, 43, 0.3);
        color:#bf7326; }
      .bp3-button.bp3-minimal.bp3-intent-warning:disabled, .bp3-button.bp3-minimal.bp3-intent-warning.bp3-disabled{
        background:none;
        color:rgba(191, 115, 38, 0.5); }
        .bp3-button.bp3-minimal.bp3-intent-warning:disabled.bp3-active, .bp3-button.bp3-minimal.bp3-intent-warning.bp3-disabled.bp3-active{
          background:rgba(217, 130, 43, 0.3); }
      .bp3-button.bp3-minimal.bp3-intent-warning .bp3-button-spinner .bp3-spinner-head{
        stroke:#bf7326; }
      .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning{
        color:#ffb366; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning:hover{
          background:rgba(217, 130, 43, 0.2);
          color:#ffb366; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning:active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning.bp3-active{
          background:rgba(217, 130, 43, 0.3);
          color:#ffb366; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning:disabled, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning.bp3-disabled{
          background:none;
          color:rgba(255, 179, 102, 0.5); }
          .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning:disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning.bp3-disabled.bp3-active{
            background:rgba(217, 130, 43, 0.3); }
    .bp3-button.bp3-minimal.bp3-intent-danger{
      color:#c23030; }
      .bp3-button.bp3-minimal.bp3-intent-danger:hover, .bp3-button.bp3-minimal.bp3-intent-danger:active, .bp3-button.bp3-minimal.bp3-intent-danger.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#c23030; }
      .bp3-button.bp3-minimal.bp3-intent-danger:hover{
        background:rgba(219, 55, 55, 0.15);
        color:#c23030; }
      .bp3-button.bp3-minimal.bp3-intent-danger:active, .bp3-button.bp3-minimal.bp3-intent-danger.bp3-active{
        background:rgba(219, 55, 55, 0.3);
        color:#c23030; }
      .bp3-button.bp3-minimal.bp3-intent-danger:disabled, .bp3-button.bp3-minimal.bp3-intent-danger.bp3-disabled{
        background:none;
        color:rgba(194, 48, 48, 0.5); }
        .bp3-button.bp3-minimal.bp3-intent-danger:disabled.bp3-active, .bp3-button.bp3-minimal.bp3-intent-danger.bp3-disabled.bp3-active{
          background:rgba(219, 55, 55, 0.3); }
      .bp3-button.bp3-minimal.bp3-intent-danger .bp3-button-spinner .bp3-spinner-head{
        stroke:#c23030; }
      .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger{
        color:#ff7373; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger:hover{
          background:rgba(219, 55, 55, 0.2);
          color:#ff7373; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger:active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger.bp3-active{
          background:rgba(219, 55, 55, 0.3);
          color:#ff7373; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger:disabled, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger.bp3-disabled{
          background:none;
          color:rgba(255, 115, 115, 0.5); }
          .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger:disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger.bp3-disabled.bp3-active{
            background:rgba(219, 55, 55, 0.3); }
  .bp3-button.bp3-outlined{
    background:none;
    -webkit-box-shadow:none;
            box-shadow:none;
    border:1px solid rgba(24, 32, 38, 0.2);
    -webkit-box-sizing:border-box;
            box-sizing:border-box; }
    .bp3-button.bp3-outlined:hover{
      background:rgba(167, 182, 194, 0.3);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#182026;
      text-decoration:none; }
    .bp3-button.bp3-outlined:active, .bp3-button.bp3-outlined.bp3-active{
      background:rgba(115, 134, 148, 0.3);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#182026; }
    .bp3-button.bp3-outlined:disabled, .bp3-button.bp3-outlined:disabled:hover, .bp3-button.bp3-outlined.bp3-disabled, .bp3-button.bp3-outlined.bp3-disabled:hover{
      background:none;
      color:rgba(92, 112, 128, 0.6);
      cursor:not-allowed; }
      .bp3-button.bp3-outlined:disabled.bp3-active, .bp3-button.bp3-outlined:disabled:hover.bp3-active, .bp3-button.bp3-outlined.bp3-disabled.bp3-active, .bp3-button.bp3-outlined.bp3-disabled:hover.bp3-active{
        background:rgba(115, 134, 148, 0.3); }
    .bp3-dark .bp3-button.bp3-outlined{
      background:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:inherit; }
      .bp3-dark .bp3-button.bp3-outlined:hover, .bp3-dark .bp3-button.bp3-outlined:active, .bp3-dark .bp3-button.bp3-outlined.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none; }
      .bp3-dark .bp3-button.bp3-outlined:hover{
        background:rgba(138, 155, 168, 0.15); }
      .bp3-dark .bp3-button.bp3-outlined:active, .bp3-dark .bp3-button.bp3-outlined.bp3-active{
        background:rgba(138, 155, 168, 0.3);
        color:#f5f8fa; }
      .bp3-dark .bp3-button.bp3-outlined:disabled, .bp3-dark .bp3-button.bp3-outlined:disabled:hover, .bp3-dark .bp3-button.bp3-outlined.bp3-disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-disabled:hover{
        background:none;
        color:rgba(167, 182, 194, 0.6);
        cursor:not-allowed; }
        .bp3-dark .bp3-button.bp3-outlined:disabled.bp3-active, .bp3-dark .bp3-button.bp3-outlined:disabled:hover.bp3-active, .bp3-dark .bp3-button.bp3-outlined.bp3-disabled.bp3-active, .bp3-dark .bp3-button.bp3-outlined.bp3-disabled:hover.bp3-active{
          background:rgba(138, 155, 168, 0.3); }
    .bp3-button.bp3-outlined.bp3-intent-primary{
      color:#106ba3; }
      .bp3-button.bp3-outlined.bp3-intent-primary:hover, .bp3-button.bp3-outlined.bp3-intent-primary:active, .bp3-button.bp3-outlined.bp3-intent-primary.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#106ba3; }
      .bp3-button.bp3-outlined.bp3-intent-primary:hover{
        background:rgba(19, 124, 189, 0.15);
        color:#106ba3; }
      .bp3-button.bp3-outlined.bp3-intent-primary:active, .bp3-button.bp3-outlined.bp3-intent-primary.bp3-active{
        background:rgba(19, 124, 189, 0.3);
        color:#106ba3; }
      .bp3-button.bp3-outlined.bp3-intent-primary:disabled, .bp3-button.bp3-outlined.bp3-intent-primary.bp3-disabled{
        background:none;
        color:rgba(16, 107, 163, 0.5); }
        .bp3-button.bp3-outlined.bp3-intent-primary:disabled.bp3-active, .bp3-button.bp3-outlined.bp3-intent-primary.bp3-disabled.bp3-active{
          background:rgba(19, 124, 189, 0.3); }
      .bp3-button.bp3-outlined.bp3-intent-primary .bp3-button-spinner .bp3-spinner-head{
        stroke:#106ba3; }
      .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary{
        color:#48aff0; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary:hover{
          background:rgba(19, 124, 189, 0.2);
          color:#48aff0; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary:active, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary.bp3-active{
          background:rgba(19, 124, 189, 0.3);
          color:#48aff0; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary:disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary.bp3-disabled{
          background:none;
          color:rgba(72, 175, 240, 0.5); }
          .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary:disabled.bp3-active, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary.bp3-disabled.bp3-active{
            background:rgba(19, 124, 189, 0.3); }
    .bp3-button.bp3-outlined.bp3-intent-success{
      color:#0d8050; }
      .bp3-button.bp3-outlined.bp3-intent-success:hover, .bp3-button.bp3-outlined.bp3-intent-success:active, .bp3-button.bp3-outlined.bp3-intent-success.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#0d8050; }
      .bp3-button.bp3-outlined.bp3-intent-success:hover{
        background:rgba(15, 153, 96, 0.15);
        color:#0d8050; }
      .bp3-button.bp3-outlined.bp3-intent-success:active, .bp3-button.bp3-outlined.bp3-intent-success.bp3-active{
        background:rgba(15, 153, 96, 0.3);
        color:#0d8050; }
      .bp3-button.bp3-outlined.bp3-intent-success:disabled, .bp3-button.bp3-outlined.bp3-intent-success.bp3-disabled{
        background:none;
        color:rgba(13, 128, 80, 0.5); }
        .bp3-button.bp3-outlined.bp3-intent-success:disabled.bp3-active, .bp3-button.bp3-outlined.bp3-intent-success.bp3-disabled.bp3-active{
          background:rgba(15, 153, 96, 0.3); }
      .bp3-button.bp3-outlined.bp3-intent-success .bp3-button-spinner .bp3-spinner-head{
        stroke:#0d8050; }
      .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success{
        color:#3dcc91; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success:hover{
          background:rgba(15, 153, 96, 0.2);
          color:#3dcc91; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success:active, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success.bp3-active{
          background:rgba(15, 153, 96, 0.3);
          color:#3dcc91; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success:disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success.bp3-disabled{
          background:none;
          color:rgba(61, 204, 145, 0.5); }
          .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success:disabled.bp3-active, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success.bp3-disabled.bp3-active{
            background:rgba(15, 153, 96, 0.3); }
    .bp3-button.bp3-outlined.bp3-intent-warning{
      color:#bf7326; }
      .bp3-button.bp3-outlined.bp3-intent-warning:hover, .bp3-button.bp3-outlined.bp3-intent-warning:active, .bp3-button.bp3-outlined.bp3-intent-warning.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#bf7326; }
      .bp3-button.bp3-outlined.bp3-intent-warning:hover{
        background:rgba(217, 130, 43, 0.15);
        color:#bf7326; }
      .bp3-button.bp3-outlined.bp3-intent-warning:active, .bp3-button.bp3-outlined.bp3-intent-warning.bp3-active{
        background:rgba(217, 130, 43, 0.3);
        color:#bf7326; }
      .bp3-button.bp3-outlined.bp3-intent-warning:disabled, .bp3-button.bp3-outlined.bp3-intent-warning.bp3-disabled{
        background:none;
        color:rgba(191, 115, 38, 0.5); }
        .bp3-button.bp3-outlined.bp3-intent-warning:disabled.bp3-active, .bp3-button.bp3-outlined.bp3-intent-warning.bp3-disabled.bp3-active{
          background:rgba(217, 130, 43, 0.3); }
      .bp3-button.bp3-outlined.bp3-intent-warning .bp3-button-spinner .bp3-spinner-head{
        stroke:#bf7326; }
      .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning{
        color:#ffb366; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning:hover{
          background:rgba(217, 130, 43, 0.2);
          color:#ffb366; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning:active, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning.bp3-active{
          background:rgba(217, 130, 43, 0.3);
          color:#ffb366; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning:disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning.bp3-disabled{
          background:none;
          color:rgba(255, 179, 102, 0.5); }
          .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning:disabled.bp3-active, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning.bp3-disabled.bp3-active{
            background:rgba(217, 130, 43, 0.3); }
    .bp3-button.bp3-outlined.bp3-intent-danger{
      color:#c23030; }
      .bp3-button.bp3-outlined.bp3-intent-danger:hover, .bp3-button.bp3-outlined.bp3-intent-danger:active, .bp3-button.bp3-outlined.bp3-intent-danger.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#c23030; }
      .bp3-button.bp3-outlined.bp3-intent-danger:hover{
        background:rgba(219, 55, 55, 0.15);
        color:#c23030; }
      .bp3-button.bp3-outlined.bp3-intent-danger:active, .bp3-button.bp3-outlined.bp3-intent-danger.bp3-active{
        background:rgba(219, 55, 55, 0.3);
        color:#c23030; }
      .bp3-button.bp3-outlined.bp3-intent-danger:disabled, .bp3-button.bp3-outlined.bp3-intent-danger.bp3-disabled{
        background:none;
        color:rgba(194, 48, 48, 0.5); }
        .bp3-button.bp3-outlined.bp3-intent-danger:disabled.bp3-active, .bp3-button.bp3-outlined.bp3-intent-danger.bp3-disabled.bp3-active{
          background:rgba(219, 55, 55, 0.3); }
      .bp3-button.bp3-outlined.bp3-intent-danger .bp3-button-spinner .bp3-spinner-head{
        stroke:#c23030; }
      .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger{
        color:#ff7373; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger:hover{
          background:rgba(219, 55, 55, 0.2);
          color:#ff7373; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger:active, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger.bp3-active{
          background:rgba(219, 55, 55, 0.3);
          color:#ff7373; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger:disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger.bp3-disabled{
          background:none;
          color:rgba(255, 115, 115, 0.5); }
          .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger:disabled.bp3-active, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger.bp3-disabled.bp3-active{
            background:rgba(219, 55, 55, 0.3); }
    .bp3-button.bp3-outlined:disabled, .bp3-button.bp3-outlined.bp3-disabled, .bp3-button.bp3-outlined:disabled:hover, .bp3-button.bp3-outlined.bp3-disabled:hover{
      border-color:rgba(92, 112, 128, 0.1); }
    .bp3-dark .bp3-button.bp3-outlined{
      border-color:rgba(255, 255, 255, 0.4); }
      .bp3-dark .bp3-button.bp3-outlined:disabled, .bp3-dark .bp3-button.bp3-outlined:disabled:hover, .bp3-dark .bp3-button.bp3-outlined.bp3-disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-disabled:hover{
        border-color:rgba(255, 255, 255, 0.2); }
    .bp3-button.bp3-outlined.bp3-intent-primary{
      border-color:rgba(16, 107, 163, 0.6); }
      .bp3-button.bp3-outlined.bp3-intent-primary:disabled, .bp3-button.bp3-outlined.bp3-intent-primary.bp3-disabled{
        border-color:rgba(16, 107, 163, 0.2); }
      .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary{
        border-color:rgba(72, 175, 240, 0.6); }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary:disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary.bp3-disabled{
          border-color:rgba(72, 175, 240, 0.2); }
    .bp3-button.bp3-outlined.bp3-intent-success{
      border-color:rgba(13, 128, 80, 0.6); }
      .bp3-button.bp3-outlined.bp3-intent-success:disabled, .bp3-button.bp3-outlined.bp3-intent-success.bp3-disabled{
        border-color:rgba(13, 128, 80, 0.2); }
      .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success{
        border-color:rgba(61, 204, 145, 0.6); }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success:disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success.bp3-disabled{
          border-color:rgba(61, 204, 145, 0.2); }
    .bp3-button.bp3-outlined.bp3-intent-warning{
      border-color:rgba(191, 115, 38, 0.6); }
      .bp3-button.bp3-outlined.bp3-intent-warning:disabled, .bp3-button.bp3-outlined.bp3-intent-warning.bp3-disabled{
        border-color:rgba(191, 115, 38, 0.2); }
      .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning{
        border-color:rgba(255, 179, 102, 0.6); }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning:disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning.bp3-disabled{
          border-color:rgba(255, 179, 102, 0.2); }
    .bp3-button.bp3-outlined.bp3-intent-danger{
      border-color:rgba(194, 48, 48, 0.6); }
      .bp3-button.bp3-outlined.bp3-intent-danger:disabled, .bp3-button.bp3-outlined.bp3-intent-danger.bp3-disabled{
        border-color:rgba(194, 48, 48, 0.2); }
      .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger{
        border-color:rgba(255, 115, 115, 0.6); }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger:disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger.bp3-disabled{
          border-color:rgba(255, 115, 115, 0.2); }

a.bp3-button{
  text-align:center;
  text-decoration:none;
  -webkit-transition:none;
  transition:none; }
  a.bp3-button, a.bp3-button:hover, a.bp3-button:active{
    color:#182026; }
  a.bp3-button.bp3-disabled{
    color:rgba(92, 112, 128, 0.6); }

.bp3-button-text{
  -webkit-box-flex:0;
      -ms-flex:0 1 auto;
          flex:0 1 auto; }

.bp3-button.bp3-align-left .bp3-button-text, .bp3-button.bp3-align-right .bp3-button-text,
.bp3-button-group.bp3-align-left .bp3-button-text,
.bp3-button-group.bp3-align-right .bp3-button-text{
  -webkit-box-flex:1;
      -ms-flex:1 1 auto;
          flex:1 1 auto; }
.bp3-button-group{
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex; }
  .bp3-button-group .bp3-button{
    -webkit-box-flex:0;
        -ms-flex:0 0 auto;
            flex:0 0 auto;
    position:relative;
    z-index:4; }
    .bp3-button-group .bp3-button:focus{
      z-index:5; }
    .bp3-button-group .bp3-button:hover{
      z-index:6; }
    .bp3-button-group .bp3-button:active, .bp3-button-group .bp3-button.bp3-active{
      z-index:7; }
    .bp3-button-group .bp3-button:disabled, .bp3-button-group .bp3-button.bp3-disabled{
      z-index:3; }
    .bp3-button-group .bp3-button[class*="bp3-intent-"]{
      z-index:9; }
      .bp3-button-group .bp3-button[class*="bp3-intent-"]:focus{
        z-index:10; }
      .bp3-button-group .bp3-button[class*="bp3-intent-"]:hover{
        z-index:11; }
      .bp3-button-group .bp3-button[class*="bp3-intent-"]:active, .bp3-button-group .bp3-button[class*="bp3-intent-"].bp3-active{
        z-index:12; }
      .bp3-button-group .bp3-button[class*="bp3-intent-"]:disabled, .bp3-button-group .bp3-button[class*="bp3-intent-"].bp3-disabled{
        z-index:8; }
  .bp3-button-group:not(.bp3-minimal) > .bp3-popover-wrapper:not(:first-child) .bp3-button,
  .bp3-button-group:not(.bp3-minimal) > .bp3-button:not(:first-child){
    border-bottom-left-radius:0;
    border-top-left-radius:0; }
  .bp3-button-group:not(.bp3-minimal) > .bp3-popover-wrapper:not(:last-child) .bp3-button,
  .bp3-button-group:not(.bp3-minimal) > .bp3-button:not(:last-child){
    border-bottom-right-radius:0;
    border-top-right-radius:0;
    margin-right:-1px; }
  .bp3-button-group.bp3-minimal .bp3-button{
    background:none;
    -webkit-box-shadow:none;
            box-shadow:none; }
    .bp3-button-group.bp3-minimal .bp3-button:hover{
      background:rgba(167, 182, 194, 0.3);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#182026;
      text-decoration:none; }
    .bp3-button-group.bp3-minimal .bp3-button:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-active{
      background:rgba(115, 134, 148, 0.3);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#182026; }
    .bp3-button-group.bp3-minimal .bp3-button:disabled, .bp3-button-group.bp3-minimal .bp3-button:disabled:hover, .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled, .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled:hover{
      background:none;
      color:rgba(92, 112, 128, 0.6);
      cursor:not-allowed; }
      .bp3-button-group.bp3-minimal .bp3-button:disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button:disabled:hover.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled:hover.bp3-active{
        background:rgba(115, 134, 148, 0.3); }
    .bp3-dark .bp3-button-group.bp3-minimal .bp3-button{
      background:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:inherit; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:hover, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:hover{
        background:rgba(138, 155, 168, 0.15); }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-active{
        background:rgba(138, 155, 168, 0.3);
        color:#f5f8fa; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:disabled:hover, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled:hover{
        background:none;
        color:rgba(167, 182, 194, 0.6);
        cursor:not-allowed; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:disabled:hover.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled:hover.bp3-active{
          background:rgba(138, 155, 168, 0.3); }
    .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary{
      color:#106ba3; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:hover, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#106ba3; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:hover{
        background:rgba(19, 124, 189, 0.15);
        color:#106ba3; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-active{
        background:rgba(19, 124, 189, 0.3);
        color:#106ba3; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:disabled, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-disabled{
        background:none;
        color:rgba(16, 107, 163, 0.5); }
        .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-disabled.bp3-active{
          background:rgba(19, 124, 189, 0.3); }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary .bp3-button-spinner .bp3-spinner-head{
        stroke:#106ba3; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary{
        color:#48aff0; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:hover{
          background:rgba(19, 124, 189, 0.2);
          color:#48aff0; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-active{
          background:rgba(19, 124, 189, 0.3);
          color:#48aff0; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-disabled{
          background:none;
          color:rgba(72, 175, 240, 0.5); }
          .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-disabled.bp3-active{
            background:rgba(19, 124, 189, 0.3); }
    .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success{
      color:#0d8050; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:hover, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#0d8050; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:hover{
        background:rgba(15, 153, 96, 0.15);
        color:#0d8050; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-active{
        background:rgba(15, 153, 96, 0.3);
        color:#0d8050; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:disabled, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-disabled{
        background:none;
        color:rgba(13, 128, 80, 0.5); }
        .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-disabled.bp3-active{
          background:rgba(15, 153, 96, 0.3); }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success .bp3-button-spinner .bp3-spinner-head{
        stroke:#0d8050; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success{
        color:#3dcc91; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:hover{
          background:rgba(15, 153, 96, 0.2);
          color:#3dcc91; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-active{
          background:rgba(15, 153, 96, 0.3);
          color:#3dcc91; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-disabled{
          background:none;
          color:rgba(61, 204, 145, 0.5); }
          .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-disabled.bp3-active{
            background:rgba(15, 153, 96, 0.3); }
    .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning{
      color:#bf7326; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:hover, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#bf7326; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:hover{
        background:rgba(217, 130, 43, 0.15);
        color:#bf7326; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-active{
        background:rgba(217, 130, 43, 0.3);
        color:#bf7326; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:disabled, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-disabled{
        background:none;
        color:rgba(191, 115, 38, 0.5); }
        .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-disabled.bp3-active{
          background:rgba(217, 130, 43, 0.3); }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning .bp3-button-spinner .bp3-spinner-head{
        stroke:#bf7326; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning{
        color:#ffb366; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:hover{
          background:rgba(217, 130, 43, 0.2);
          color:#ffb366; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-active{
          background:rgba(217, 130, 43, 0.3);
          color:#ffb366; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-disabled{
          background:none;
          color:rgba(255, 179, 102, 0.5); }
          .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-disabled.bp3-active{
            background:rgba(217, 130, 43, 0.3); }
    .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger{
      color:#c23030; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:hover, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#c23030; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:hover{
        background:rgba(219, 55, 55, 0.15);
        color:#c23030; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-active{
        background:rgba(219, 55, 55, 0.3);
        color:#c23030; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:disabled, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-disabled{
        background:none;
        color:rgba(194, 48, 48, 0.5); }
        .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-disabled.bp3-active{
          background:rgba(219, 55, 55, 0.3); }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger .bp3-button-spinner .bp3-spinner-head{
        stroke:#c23030; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger{
        color:#ff7373; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:hover{
          background:rgba(219, 55, 55, 0.2);
          color:#ff7373; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-active{
          background:rgba(219, 55, 55, 0.3);
          color:#ff7373; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-disabled{
          background:none;
          color:rgba(255, 115, 115, 0.5); }
          .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-disabled.bp3-active{
            background:rgba(219, 55, 55, 0.3); }
  .bp3-button-group .bp3-popover-wrapper,
  .bp3-button-group .bp3-popover-target{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto; }
  .bp3-button-group.bp3-fill{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    width:100%; }
  .bp3-button-group .bp3-button.bp3-fill,
  .bp3-button-group.bp3-fill .bp3-button:not(.bp3-fixed){
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto; }
  .bp3-button-group.bp3-vertical{
    -webkit-box-align:stretch;
        -ms-flex-align:stretch;
            align-items:stretch;
    -webkit-box-orient:vertical;
    -webkit-box-direction:normal;
        -ms-flex-direction:column;
            flex-direction:column;
    vertical-align:top; }
    .bp3-button-group.bp3-vertical.bp3-fill{
      height:100%;
      width:unset; }
    .bp3-button-group.bp3-vertical .bp3-button{
      margin-right:0 !important;
      width:100%; }
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-popover-wrapper:first-child .bp3-button,
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-button:first-child{
      border-radius:3px 3px 0 0; }
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-popover-wrapper:last-child .bp3-button,
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-button:last-child{
      border-radius:0 0 3px 3px; }
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-popover-wrapper:not(:last-child) .bp3-button,
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-button:not(:last-child){
      margin-bottom:-1px; }
  .bp3-button-group.bp3-align-left .bp3-button{
    text-align:left; }
  .bp3-dark .bp3-button-group:not(.bp3-minimal) > .bp3-popover-wrapper:not(:last-child) .bp3-button,
  .bp3-dark .bp3-button-group:not(.bp3-minimal) > .bp3-button:not(:last-child){
    margin-right:1px; }
  .bp3-dark .bp3-button-group.bp3-vertical > .bp3-popover-wrapper:not(:last-child) .bp3-button,
  .bp3-dark .bp3-button-group.bp3-vertical > .bp3-button:not(:last-child){
    margin-bottom:1px; }
.bp3-callout{
  font-size:14px;
  line-height:1.5;
  background-color:rgba(138, 155, 168, 0.15);
  border-radius:3px;
  padding:10px 12px 9px;
  position:relative;
  width:100%; }
  .bp3-callout[class*="bp3-icon-"]{
    padding-left:40px; }
    .bp3-callout[class*="bp3-icon-"]::before{
      font-family:"Icons20", sans-serif;
      font-size:20px;
      font-style:normal;
      font-weight:400;
      line-height:1;
      -moz-osx-font-smoothing:grayscale;
      -webkit-font-smoothing:antialiased;
      color:#5c7080;
      left:10px;
      position:absolute;
      top:10px; }
  .bp3-callout.bp3-callout-icon{
    padding-left:40px; }
    .bp3-callout.bp3-callout-icon > .bp3-icon:first-child{
      color:#5c7080;
      left:10px;
      position:absolute;
      top:10px; }
  .bp3-callout .bp3-heading{
    line-height:20px;
    margin-bottom:5px;
    margin-top:0; }
    .bp3-callout .bp3-heading:last-child{
      margin-bottom:0; }
  .bp3-dark .bp3-callout{
    background-color:rgba(138, 155, 168, 0.2); }
    .bp3-dark .bp3-callout[class*="bp3-icon-"]::before{
      color:#a7b6c2; }
  .bp3-callout.bp3-intent-primary{
    background-color:rgba(19, 124, 189, 0.15); }
    .bp3-callout.bp3-intent-primary[class*="bp3-icon-"]::before,
    .bp3-callout.bp3-intent-primary > .bp3-icon:first-child,
    .bp3-callout.bp3-intent-primary .bp3-heading{
      color:#106ba3; }
    .bp3-dark .bp3-callout.bp3-intent-primary{
      background-color:rgba(19, 124, 189, 0.25); }
      .bp3-dark .bp3-callout.bp3-intent-primary[class*="bp3-icon-"]::before,
      .bp3-dark .bp3-callout.bp3-intent-primary > .bp3-icon:first-child,
      .bp3-dark .bp3-callout.bp3-intent-primary .bp3-heading{
        color:#48aff0; }
  .bp3-callout.bp3-intent-success{
    background-color:rgba(15, 153, 96, 0.15); }
    .bp3-callout.bp3-intent-success[class*="bp3-icon-"]::before,
    .bp3-callout.bp3-intent-success > .bp3-icon:first-child,
    .bp3-callout.bp3-intent-success .bp3-heading{
      color:#0d8050; }
    .bp3-dark .bp3-callout.bp3-intent-success{
      background-color:rgba(15, 153, 96, 0.25); }
      .bp3-dark .bp3-callout.bp3-intent-success[class*="bp3-icon-"]::before,
      .bp3-dark .bp3-callout.bp3-intent-success > .bp3-icon:first-child,
      .bp3-dark .bp3-callout.bp3-intent-success .bp3-heading{
        color:#3dcc91; }
  .bp3-callout.bp3-intent-warning{
    background-color:rgba(217, 130, 43, 0.15); }
    .bp3-callout.bp3-intent-warning[class*="bp3-icon-"]::before,
    .bp3-callout.bp3-intent-warning > .bp3-icon:first-child,
    .bp3-callout.bp3-intent-warning .bp3-heading{
      color:#bf7326; }
    .bp3-dark .bp3-callout.bp3-intent-warning{
      background-color:rgba(217, 130, 43, 0.25); }
      .bp3-dark .bp3-callout.bp3-intent-warning[class*="bp3-icon-"]::before,
      .bp3-dark .bp3-callout.bp3-intent-warning > .bp3-icon:first-child,
      .bp3-dark .bp3-callout.bp3-intent-warning .bp3-heading{
        color:#ffb366; }
  .bp3-callout.bp3-intent-danger{
    background-color:rgba(219, 55, 55, 0.15); }
    .bp3-callout.bp3-intent-danger[class*="bp3-icon-"]::before,
    .bp3-callout.bp3-intent-danger > .bp3-icon:first-child,
    .bp3-callout.bp3-intent-danger .bp3-heading{
      color:#c23030; }
    .bp3-dark .bp3-callout.bp3-intent-danger{
      background-color:rgba(219, 55, 55, 0.25); }
      .bp3-dark .bp3-callout.bp3-intent-danger[class*="bp3-icon-"]::before,
      .bp3-dark .bp3-callout.bp3-intent-danger > .bp3-icon:first-child,
      .bp3-dark .bp3-callout.bp3-intent-danger .bp3-heading{
        color:#ff7373; }
  .bp3-running-text .bp3-callout{
    margin:20px 0; }
.bp3-card{
  background-color:#ffffff;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.15), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.15), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
  padding:20px;
  -webkit-transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), box-shadow 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), box-shadow 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 200ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-card.bp3-dark,
  .bp3-dark .bp3-card{
    background-color:#30404d;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0); }

.bp3-elevation-0{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.15), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.15), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0); }
  .bp3-elevation-0.bp3-dark,
  .bp3-dark .bp3-elevation-0{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0); }

.bp3-elevation-1{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-elevation-1.bp3-dark,
  .bp3-dark .bp3-elevation-1{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4); }

.bp3-elevation-2{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 1px 1px rgba(16, 22, 26, 0.2), 0 2px 6px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 1px 1px rgba(16, 22, 26, 0.2), 0 2px 6px rgba(16, 22, 26, 0.2); }
  .bp3-elevation-2.bp3-dark,
  .bp3-dark .bp3-elevation-2{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.4), 0 2px 6px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.4), 0 2px 6px rgba(16, 22, 26, 0.4); }

.bp3-elevation-3{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2); }
  .bp3-elevation-3.bp3-dark,
  .bp3-dark .bp3-elevation-3{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }

.bp3-elevation-4{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2); }
  .bp3-elevation-4.bp3-dark,
  .bp3-dark .bp3-elevation-4{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4); }

.bp3-card.bp3-interactive:hover{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
  cursor:pointer; }
  .bp3-card.bp3-interactive:hover.bp3-dark,
  .bp3-dark .bp3-card.bp3-interactive:hover{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }

.bp3-card.bp3-interactive:active{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
  opacity:0.9;
  -webkit-transition-duration:0;
          transition-duration:0; }
  .bp3-card.bp3-interactive:active.bp3-dark,
  .bp3-dark .bp3-card.bp3-interactive:active{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4); }

.bp3-collapse{
  height:0;
  overflow-y:hidden;
  -webkit-transition:height 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:height 200ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-collapse .bp3-collapse-body{
    -webkit-transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9); }
    .bp3-collapse .bp3-collapse-body[aria-hidden="true"]{
      display:none; }

.bp3-context-menu .bp3-popover-target{
  display:block; }

.bp3-context-menu-popover-target{
  position:fixed; }

.bp3-divider{
  border-bottom:1px solid rgba(16, 22, 26, 0.15);
  border-right:1px solid rgba(16, 22, 26, 0.15);
  margin:5px; }
  .bp3-dark .bp3-divider{
    border-color:rgba(16, 22, 26, 0.4); }
.bp3-dialog-container{
  opacity:1;
  -webkit-transform:scale(1);
          transform:scale(1);
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  min-height:100%;
  pointer-events:none;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none;
  width:100%; }
  .bp3-dialog-container.bp3-overlay-enter > .bp3-dialog, .bp3-dialog-container.bp3-overlay-appear > .bp3-dialog{
    opacity:0;
    -webkit-transform:scale(0.5);
            transform:scale(0.5); }
  .bp3-dialog-container.bp3-overlay-enter-active > .bp3-dialog, .bp3-dialog-container.bp3-overlay-appear-active > .bp3-dialog{
    opacity:1;
    -webkit-transform:scale(1);
            transform:scale(1);
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-property:opacity, -webkit-transform;
    transition-property:opacity, -webkit-transform;
    transition-property:opacity, transform;
    transition-property:opacity, transform, -webkit-transform;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11); }
  .bp3-dialog-container.bp3-overlay-exit > .bp3-dialog{
    opacity:1;
    -webkit-transform:scale(1);
            transform:scale(1); }
  .bp3-dialog-container.bp3-overlay-exit-active > .bp3-dialog{
    opacity:0;
    -webkit-transform:scale(0.5);
            transform:scale(0.5);
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-property:opacity, -webkit-transform;
    transition-property:opacity, -webkit-transform;
    transition-property:opacity, transform;
    transition-property:opacity, transform, -webkit-transform;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11); }

.bp3-dialog{
  background:#ebf1f5;
  border-radius:6px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  margin:30px 0;
  padding-bottom:20px;
  pointer-events:all;
  -webkit-user-select:text;
     -moz-user-select:text;
      -ms-user-select:text;
          user-select:text;
  width:500px; }
  .bp3-dialog:focus{
    outline:0; }
  .bp3-dialog.bp3-dark,
  .bp3-dark .bp3-dialog{
    background:#293742;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
    color:#f5f8fa; }

.bp3-dialog-header{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  background:#ffffff;
  border-radius:6px 6px 0 0;
  -webkit-box-shadow:0 1px 0 rgba(16, 22, 26, 0.15);
          box-shadow:0 1px 0 rgba(16, 22, 26, 0.15);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  min-height:40px;
  padding-left:20px;
  padding-right:5px; }
  .bp3-dialog-header .bp3-icon-large,
  .bp3-dialog-header .bp3-icon{
    color:#5c7080;
    -webkit-box-flex:0;
        -ms-flex:0 0 auto;
            flex:0 0 auto;
    margin-right:10px; }
  .bp3-dialog-header .bp3-heading{
    overflow:hidden;
    text-overflow:ellipsis;
    white-space:nowrap;
    word-wrap:normal;
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto;
    line-height:inherit;
    margin:0; }
    .bp3-dialog-header .bp3-heading:last-child{
      margin-right:20px; }
  .bp3-dark .bp3-dialog-header{
    background:#30404d;
    -webkit-box-shadow:0 1px 0 rgba(16, 22, 26, 0.4);
            box-shadow:0 1px 0 rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-dialog-header .bp3-icon-large,
    .bp3-dark .bp3-dialog-header .bp3-icon{
      color:#a7b6c2; }

.bp3-dialog-body{
  -webkit-box-flex:1;
      -ms-flex:1 1 auto;
          flex:1 1 auto;
  line-height:18px;
  margin:20px; }

.bp3-dialog-footer{
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  margin:0 20px; }

.bp3-dialog-footer-actions{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-pack:end;
      -ms-flex-pack:end;
          justify-content:flex-end; }
  .bp3-dialog-footer-actions .bp3-button{
    margin-left:10px; }
.bp3-drawer{
  background:#ffffff;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  margin:0;
  padding:0; }
  .bp3-drawer:focus{
    outline:0; }
  .bp3-drawer.bp3-position-top{
    height:50%;
    left:0;
    right:0;
    top:0; }
    .bp3-drawer.bp3-position-top.bp3-overlay-enter, .bp3-drawer.bp3-position-top.bp3-overlay-appear{
      -webkit-transform:translateY(-100%);
              transform:translateY(-100%); }
    .bp3-drawer.bp3-position-top.bp3-overlay-enter-active, .bp3-drawer.bp3-position-top.bp3-overlay-appear-active{
      -webkit-transform:translateY(0);
              transform:translateY(0);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
    .bp3-drawer.bp3-position-top.bp3-overlay-exit{
      -webkit-transform:translateY(0);
              transform:translateY(0); }
    .bp3-drawer.bp3-position-top.bp3-overlay-exit-active{
      -webkit-transform:translateY(-100%);
              transform:translateY(-100%);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-drawer.bp3-position-bottom{
    bottom:0;
    height:50%;
    left:0;
    right:0; }
    .bp3-drawer.bp3-position-bottom.bp3-overlay-enter, .bp3-drawer.bp3-position-bottom.bp3-overlay-appear{
      -webkit-transform:translateY(100%);
              transform:translateY(100%); }
    .bp3-drawer.bp3-position-bottom.bp3-overlay-enter-active, .bp3-drawer.bp3-position-bottom.bp3-overlay-appear-active{
      -webkit-transform:translateY(0);
              transform:translateY(0);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
    .bp3-drawer.bp3-position-bottom.bp3-overlay-exit{
      -webkit-transform:translateY(0);
              transform:translateY(0); }
    .bp3-drawer.bp3-position-bottom.bp3-overlay-exit-active{
      -webkit-transform:translateY(100%);
              transform:translateY(100%);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-drawer.bp3-position-left{
    bottom:0;
    left:0;
    top:0;
    width:50%; }
    .bp3-drawer.bp3-position-left.bp3-overlay-enter, .bp3-drawer.bp3-position-left.bp3-overlay-appear{
      -webkit-transform:translateX(-100%);
              transform:translateX(-100%); }
    .bp3-drawer.bp3-position-left.bp3-overlay-enter-active, .bp3-drawer.bp3-position-left.bp3-overlay-appear-active{
      -webkit-transform:translateX(0);
              transform:translateX(0);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
    .bp3-drawer.bp3-position-left.bp3-overlay-exit{
      -webkit-transform:translateX(0);
              transform:translateX(0); }
    .bp3-drawer.bp3-position-left.bp3-overlay-exit-active{
      -webkit-transform:translateX(-100%);
              transform:translateX(-100%);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-drawer.bp3-position-right{
    bottom:0;
    right:0;
    top:0;
    width:50%; }
    .bp3-drawer.bp3-position-right.bp3-overlay-enter, .bp3-drawer.bp3-position-right.bp3-overlay-appear{
      -webkit-transform:translateX(100%);
              transform:translateX(100%); }
    .bp3-drawer.bp3-position-right.bp3-overlay-enter-active, .bp3-drawer.bp3-position-right.bp3-overlay-appear-active{
      -webkit-transform:translateX(0);
              transform:translateX(0);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
    .bp3-drawer.bp3-position-right.bp3-overlay-exit{
      -webkit-transform:translateX(0);
              transform:translateX(0); }
    .bp3-drawer.bp3-position-right.bp3-overlay-exit-active{
      -webkit-transform:translateX(100%);
              transform:translateX(100%);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
  .bp3-position-right):not(.bp3-vertical){
    bottom:0;
    right:0;
    top:0;
    width:50%; }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-enter, .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-appear{
      -webkit-transform:translateX(100%);
              transform:translateX(100%); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-enter-active, .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-appear-active{
      -webkit-transform:translateX(0);
              transform:translateX(0);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-exit{
      -webkit-transform:translateX(0);
              transform:translateX(0); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-exit-active{
      -webkit-transform:translateX(100%);
              transform:translateX(100%);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
  .bp3-position-right).bp3-vertical{
    bottom:0;
    height:50%;
    left:0;
    right:0; }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-enter, .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-appear{
      -webkit-transform:translateY(100%);
              transform:translateY(100%); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-enter-active, .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-appear-active{
      -webkit-transform:translateY(0);
              transform:translateY(0);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-exit{
      -webkit-transform:translateY(0);
              transform:translateY(0); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-exit-active{
      -webkit-transform:translateY(100%);
              transform:translateY(100%);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-drawer.bp3-dark,
  .bp3-dark .bp3-drawer{
    background:#30404d;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
    color:#f5f8fa; }

.bp3-drawer-header{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  border-radius:0;
  -webkit-box-shadow:0 1px 0 rgba(16, 22, 26, 0.15);
          box-shadow:0 1px 0 rgba(16, 22, 26, 0.15);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  min-height:40px;
  padding:5px;
  padding-left:20px;
  position:relative; }
  .bp3-drawer-header .bp3-icon-large,
  .bp3-drawer-header .bp3-icon{
    color:#5c7080;
    -webkit-box-flex:0;
        -ms-flex:0 0 auto;
            flex:0 0 auto;
    margin-right:10px; }
  .bp3-drawer-header .bp3-heading{
    overflow:hidden;
    text-overflow:ellipsis;
    white-space:nowrap;
    word-wrap:normal;
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto;
    line-height:inherit;
    margin:0; }
    .bp3-drawer-header .bp3-heading:last-child{
      margin-right:20px; }
  .bp3-dark .bp3-drawer-header{
    -webkit-box-shadow:0 1px 0 rgba(16, 22, 26, 0.4);
            box-shadow:0 1px 0 rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-drawer-header .bp3-icon-large,
    .bp3-dark .bp3-drawer-header .bp3-icon{
      color:#a7b6c2; }

.bp3-drawer-body{
  -webkit-box-flex:1;
      -ms-flex:1 1 auto;
          flex:1 1 auto;
  line-height:18px;
  overflow:auto; }

.bp3-drawer-footer{
  -webkit-box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.15);
          box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.15);
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  padding:10px 20px;
  position:relative; }
  .bp3-dark .bp3-drawer-footer{
    -webkit-box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.4);
            box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.4); }
.bp3-editable-text{
  cursor:text;
  display:inline-block;
  max-width:100%;
  position:relative;
  vertical-align:top;
  white-space:nowrap; }
  .bp3-editable-text::before{
    bottom:-3px;
    left:-3px;
    position:absolute;
    right:-3px;
    top:-3px;
    border-radius:3px;
    content:"";
    -webkit-transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9), box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9), box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-editable-text:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15); }
  .bp3-editable-text.bp3-editable-text-editing::before{
    background-color:#ffffff;
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-editable-text.bp3-disabled::before{
    -webkit-box-shadow:none;
            box-shadow:none; }
  .bp3-editable-text.bp3-intent-primary .bp3-editable-text-input,
  .bp3-editable-text.bp3-intent-primary .bp3-editable-text-content{
    color:#137cbd; }
  .bp3-editable-text.bp3-intent-primary:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(19, 124, 189, 0.4);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(19, 124, 189, 0.4); }
  .bp3-editable-text.bp3-intent-primary.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-editable-text.bp3-intent-success .bp3-editable-text-input,
  .bp3-editable-text.bp3-intent-success .bp3-editable-text-content{
    color:#0f9960; }
  .bp3-editable-text.bp3-intent-success:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px rgba(15, 153, 96, 0.4);
            box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px rgba(15, 153, 96, 0.4); }
  .bp3-editable-text.bp3-intent-success.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-editable-text.bp3-intent-warning .bp3-editable-text-input,
  .bp3-editable-text.bp3-intent-warning .bp3-editable-text-content{
    color:#d9822b; }
  .bp3-editable-text.bp3-intent-warning:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px rgba(217, 130, 43, 0.4);
            box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px rgba(217, 130, 43, 0.4); }
  .bp3-editable-text.bp3-intent-warning.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-editable-text.bp3-intent-danger .bp3-editable-text-input,
  .bp3-editable-text.bp3-intent-danger .bp3-editable-text-content{
    color:#db3737; }
  .bp3-editable-text.bp3-intent-danger:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px rgba(219, 55, 55, 0.4);
            box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px rgba(219, 55, 55, 0.4); }
  .bp3-editable-text.bp3-intent-danger.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-dark .bp3-editable-text:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(255, 255, 255, 0.15);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(255, 255, 255, 0.15); }
  .bp3-dark .bp3-editable-text.bp3-editable-text-editing::before{
    background-color:rgba(16, 22, 26, 0.3);
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-disabled::before{
    -webkit-box-shadow:none;
            box-shadow:none; }
  .bp3-dark .bp3-editable-text.bp3-intent-primary .bp3-editable-text-content{
    color:#48aff0; }
  .bp3-dark .bp3-editable-text.bp3-intent-primary:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(72, 175, 240, 0), 0 0 0 0 rgba(72, 175, 240, 0), inset 0 0 0 1px rgba(72, 175, 240, 0.4);
            box-shadow:0 0 0 0 rgba(72, 175, 240, 0), 0 0 0 0 rgba(72, 175, 240, 0), inset 0 0 0 1px rgba(72, 175, 240, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-primary.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #48aff0, 0 0 0 3px rgba(72, 175, 240, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #48aff0, 0 0 0 3px rgba(72, 175, 240, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-success .bp3-editable-text-content{
    color:#3dcc91; }
  .bp3-dark .bp3-editable-text.bp3-intent-success:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(61, 204, 145, 0), 0 0 0 0 rgba(61, 204, 145, 0), inset 0 0 0 1px rgba(61, 204, 145, 0.4);
            box-shadow:0 0 0 0 rgba(61, 204, 145, 0), 0 0 0 0 rgba(61, 204, 145, 0), inset 0 0 0 1px rgba(61, 204, 145, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-success.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #3dcc91, 0 0 0 3px rgba(61, 204, 145, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #3dcc91, 0 0 0 3px rgba(61, 204, 145, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-warning .bp3-editable-text-content{
    color:#ffb366; }
  .bp3-dark .bp3-editable-text.bp3-intent-warning:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(255, 179, 102, 0), 0 0 0 0 rgba(255, 179, 102, 0), inset 0 0 0 1px rgba(255, 179, 102, 0.4);
            box-shadow:0 0 0 0 rgba(255, 179, 102, 0), 0 0 0 0 rgba(255, 179, 102, 0), inset 0 0 0 1px rgba(255, 179, 102, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-warning.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #ffb366, 0 0 0 3px rgba(255, 179, 102, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #ffb366, 0 0 0 3px rgba(255, 179, 102, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-danger .bp3-editable-text-content{
    color:#ff7373; }
  .bp3-dark .bp3-editable-text.bp3-intent-danger:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(255, 115, 115, 0), 0 0 0 0 rgba(255, 115, 115, 0), inset 0 0 0 1px rgba(255, 115, 115, 0.4);
            box-shadow:0 0 0 0 rgba(255, 115, 115, 0), 0 0 0 0 rgba(255, 115, 115, 0), inset 0 0 0 1px rgba(255, 115, 115, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-danger.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #ff7373, 0 0 0 3px rgba(255, 115, 115, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #ff7373, 0 0 0 3px rgba(255, 115, 115, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }

.bp3-editable-text-input,
.bp3-editable-text-content{
  color:inherit;
  display:inherit;
  font:inherit;
  letter-spacing:inherit;
  max-width:inherit;
  min-width:inherit;
  position:relative;
  resize:none;
  text-transform:inherit;
  vertical-align:top; }

.bp3-editable-text-input{
  background:none;
  border:none;
  -webkit-box-shadow:none;
          box-shadow:none;
  padding:0;
  white-space:pre-wrap;
  width:100%; }
  .bp3-editable-text-input::-webkit-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-editable-text-input::-moz-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-editable-text-input:-ms-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-editable-text-input::-ms-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-editable-text-input::placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-editable-text-input:focus{
    outline:none; }
  .bp3-editable-text-input::-ms-clear{
    display:none; }

.bp3-editable-text-content{
  overflow:hidden;
  padding-right:2px;
  text-overflow:ellipsis;
  white-space:pre; }
  .bp3-editable-text-editing > .bp3-editable-text-content{
    left:0;
    position:absolute;
    visibility:hidden; }
  .bp3-editable-text-placeholder > .bp3-editable-text-content{
    color:rgba(92, 112, 128, 0.6); }
    .bp3-dark .bp3-editable-text-placeholder > .bp3-editable-text-content{
      color:rgba(167, 182, 194, 0.6); }

.bp3-editable-text.bp3-multiline{
  display:block; }
  .bp3-editable-text.bp3-multiline .bp3-editable-text-content{
    overflow:auto;
    white-space:pre-wrap;
    word-wrap:break-word; }
.bp3-divider{
  border-bottom:1px solid rgba(16, 22, 26, 0.15);
  border-right:1px solid rgba(16, 22, 26, 0.15);
  margin:5px; }
  .bp3-dark .bp3-divider{
    border-color:rgba(16, 22, 26, 0.4); }
.bp3-control-group{
  -webkit-transform:translateZ(0);
          transform:translateZ(0);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:stretch;
      -ms-flex-align:stretch;
          align-items:stretch; }
  .bp3-control-group > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-control-group > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-control-group .bp3-button,
  .bp3-control-group .bp3-html-select,
  .bp3-control-group .bp3-input,
  .bp3-control-group .bp3-select{
    position:relative; }
  .bp3-control-group .bp3-input{
    border-radius:inherit;
    z-index:2; }
    .bp3-control-group .bp3-input:focus{
      border-radius:3px;
      z-index:14; }
    .bp3-control-group .bp3-input[class*="bp3-intent"]{
      z-index:13; }
      .bp3-control-group .bp3-input[class*="bp3-intent"]:focus{
        z-index:15; }
    .bp3-control-group .bp3-input[readonly], .bp3-control-group .bp3-input:disabled, .bp3-control-group .bp3-input.bp3-disabled{
      z-index:1; }
  .bp3-control-group .bp3-input-group[class*="bp3-intent"] .bp3-input{
    z-index:13; }
    .bp3-control-group .bp3-input-group[class*="bp3-intent"] .bp3-input:focus{
      z-index:15; }
  .bp3-control-group .bp3-button,
  .bp3-control-group .bp3-html-select select,
  .bp3-control-group .bp3-select select{
    -webkit-transform:translateZ(0);
            transform:translateZ(0);
    border-radius:inherit;
    z-index:4; }
    .bp3-control-group .bp3-button:focus,
    .bp3-control-group .bp3-html-select select:focus,
    .bp3-control-group .bp3-select select:focus{
      z-index:5; }
    .bp3-control-group .bp3-button:hover,
    .bp3-control-group .bp3-html-select select:hover,
    .bp3-control-group .bp3-select select:hover{
      z-index:6; }
    .bp3-control-group .bp3-button:active,
    .bp3-control-group .bp3-html-select select:active,
    .bp3-control-group .bp3-select select:active{
      z-index:7; }
    .bp3-control-group .bp3-button[readonly], .bp3-control-group .bp3-button:disabled, .bp3-control-group .bp3-button.bp3-disabled,
    .bp3-control-group .bp3-html-select select[readonly],
    .bp3-control-group .bp3-html-select select:disabled,
    .bp3-control-group .bp3-html-select select.bp3-disabled,
    .bp3-control-group .bp3-select select[readonly],
    .bp3-control-group .bp3-select select:disabled,
    .bp3-control-group .bp3-select select.bp3-disabled{
      z-index:3; }
    .bp3-control-group .bp3-button[class*="bp3-intent"],
    .bp3-control-group .bp3-html-select select[class*="bp3-intent"],
    .bp3-control-group .bp3-select select[class*="bp3-intent"]{
      z-index:9; }
      .bp3-control-group .bp3-button[class*="bp3-intent"]:focus,
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"]:focus,
      .bp3-control-group .bp3-select select[class*="bp3-intent"]:focus{
        z-index:10; }
      .bp3-control-group .bp3-button[class*="bp3-intent"]:hover,
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"]:hover,
      .bp3-control-group .bp3-select select[class*="bp3-intent"]:hover{
        z-index:11; }
      .bp3-control-group .bp3-button[class*="bp3-intent"]:active,
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"]:active,
      .bp3-control-group .bp3-select select[class*="bp3-intent"]:active{
        z-index:12; }
      .bp3-control-group .bp3-button[class*="bp3-intent"][readonly], .bp3-control-group .bp3-button[class*="bp3-intent"]:disabled, .bp3-control-group .bp3-button[class*="bp3-intent"].bp3-disabled,
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"][readonly],
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"]:disabled,
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"].bp3-disabled,
      .bp3-control-group .bp3-select select[class*="bp3-intent"][readonly],
      .bp3-control-group .bp3-select select[class*="bp3-intent"]:disabled,
      .bp3-control-group .bp3-select select[class*="bp3-intent"].bp3-disabled{
        z-index:8; }
  .bp3-control-group .bp3-input-group > .bp3-icon,
  .bp3-control-group .bp3-input-group > .bp3-button,
  .bp3-control-group .bp3-input-group > .bp3-input-action{
    z-index:16; }
  .bp3-control-group .bp3-select::after,
  .bp3-control-group .bp3-html-select::after,
  .bp3-control-group .bp3-select > .bp3-icon,
  .bp3-control-group .bp3-html-select > .bp3-icon{
    z-index:17; }
  .bp3-control-group .bp3-select:focus-within{
    z-index:5; }
  .bp3-control-group:not(.bp3-vertical) > *:not(.bp3-divider){
    margin-right:-1px; }
  .bp3-control-group:not(.bp3-vertical) > .bp3-divider:not(:first-child){
    margin-left:6px; }
  .bp3-dark .bp3-control-group:not(.bp3-vertical) > *:not(.bp3-divider){
    margin-right:0; }
  .bp3-dark .bp3-control-group:not(.bp3-vertical) > .bp3-button + .bp3-button{
    margin-left:1px; }
  .bp3-control-group .bp3-popover-wrapper,
  .bp3-control-group .bp3-popover-target{
    border-radius:inherit; }
  .bp3-control-group > :first-child{
    border-radius:3px 0 0 3px; }
  .bp3-control-group > :last-child{
    border-radius:0 3px 3px 0;
    margin-right:0; }
  .bp3-control-group > :only-child{
    border-radius:3px;
    margin-right:0; }
  .bp3-control-group .bp3-input-group .bp3-button{
    border-radius:3px; }
  .bp3-control-group .bp3-numeric-input:not(:first-child) .bp3-input-group{
    border-bottom-left-radius:0;
    border-top-left-radius:0; }
  .bp3-control-group.bp3-fill{
    width:100%; }
  .bp3-control-group > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto; }
  .bp3-control-group.bp3-fill > *:not(.bp3-fixed){
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto; }
  .bp3-control-group.bp3-vertical{
    -webkit-box-orient:vertical;
    -webkit-box-direction:normal;
        -ms-flex-direction:column;
            flex-direction:column; }
    .bp3-control-group.bp3-vertical > *{
      margin-top:-1px; }
    .bp3-control-group.bp3-vertical > :first-child{
      border-radius:3px 3px 0 0;
      margin-top:0; }
    .bp3-control-group.bp3-vertical > :last-child{
      border-radius:0 0 3px 3px; }
.bp3-control{
  cursor:pointer;
  display:block;
  margin-bottom:10px;
  position:relative;
  text-transform:none; }
  .bp3-control input:checked ~ .bp3-control-indicator{
    background-color:#137cbd;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    color:#ffffff; }
  .bp3-control:hover input:checked ~ .bp3-control-indicator{
    background-color:#106ba3;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2); }
  .bp3-control input:not(:disabled):active:checked ~ .bp3-control-indicator{
    background:#0e5a8a;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
  .bp3-control input:disabled:checked ~ .bp3-control-indicator{
    background:rgba(19, 124, 189, 0.5);
    -webkit-box-shadow:none;
            box-shadow:none; }
  .bp3-dark .bp3-control input:checked ~ .bp3-control-indicator{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control:hover input:checked ~ .bp3-control-indicator{
    background-color:#106ba3;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control input:not(:disabled):active:checked ~ .bp3-control-indicator{
    background-color:#0e5a8a;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
  .bp3-dark .bp3-control input:disabled:checked ~ .bp3-control-indicator{
    background:rgba(14, 90, 138, 0.5);
    -webkit-box-shadow:none;
            box-shadow:none; }
  .bp3-control:not(.bp3-align-right){
    padding-left:26px; }
    .bp3-control:not(.bp3-align-right) .bp3-control-indicator{
      margin-left:-26px; }
  .bp3-control.bp3-align-right{
    padding-right:26px; }
    .bp3-control.bp3-align-right .bp3-control-indicator{
      margin-right:-26px; }
  .bp3-control.bp3-disabled{
    color:rgba(92, 112, 128, 0.6);
    cursor:not-allowed; }
  .bp3-control.bp3-inline{
    display:inline-block;
    margin-right:20px; }
  .bp3-control input{
    left:0;
    opacity:0;
    position:absolute;
    top:0;
    z-index:-1; }
  .bp3-control .bp3-control-indicator{
    background-clip:padding-box;
    background-color:#f5f8fa;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.8)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
    border:none;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    cursor:pointer;
    display:inline-block;
    font-size:16px;
    height:1em;
    margin-right:10px;
    margin-top:-3px;
    position:relative;
    -webkit-user-select:none;
       -moz-user-select:none;
        -ms-user-select:none;
            user-select:none;
    vertical-align:middle;
    width:1em; }
    .bp3-control .bp3-control-indicator::before{
      content:"";
      display:block;
      height:1em;
      width:1em; }
  .bp3-control:hover .bp3-control-indicator{
    background-color:#ebf1f5; }
  .bp3-control input:not(:disabled):active ~ .bp3-control-indicator{
    background:#d8e1e8;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
  .bp3-control input:disabled ~ .bp3-control-indicator{
    background:rgba(206, 217, 224, 0.5);
    -webkit-box-shadow:none;
            box-shadow:none;
    cursor:not-allowed; }
  .bp3-control input:focus ~ .bp3-control-indicator{
    outline:rgba(19, 124, 189, 0.6) auto 2px;
    outline-offset:2px;
    -moz-outline-radius:6px; }
  .bp3-control.bp3-align-right .bp3-control-indicator{
    float:right;
    margin-left:10px;
    margin-top:1px; }
  .bp3-control.bp3-large{
    font-size:16px; }
    .bp3-control.bp3-large:not(.bp3-align-right){
      padding-left:30px; }
      .bp3-control.bp3-large:not(.bp3-align-right) .bp3-control-indicator{
        margin-left:-30px; }
    .bp3-control.bp3-large.bp3-align-right{
      padding-right:30px; }
      .bp3-control.bp3-large.bp3-align-right .bp3-control-indicator{
        margin-right:-30px; }
    .bp3-control.bp3-large .bp3-control-indicator{
      font-size:20px; }
    .bp3-control.bp3-large.bp3-align-right .bp3-control-indicator{
      margin-top:0; }
  .bp3-control.bp3-checkbox input:indeterminate ~ .bp3-control-indicator{
    background-color:#137cbd;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    color:#ffffff; }
  .bp3-control.bp3-checkbox:hover input:indeterminate ~ .bp3-control-indicator{
    background-color:#106ba3;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2); }
  .bp3-control.bp3-checkbox input:not(:disabled):active:indeterminate ~ .bp3-control-indicator{
    background:#0e5a8a;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
  .bp3-control.bp3-checkbox input:disabled:indeterminate ~ .bp3-control-indicator{
    background:rgba(19, 124, 189, 0.5);
    -webkit-box-shadow:none;
            box-shadow:none; }
  .bp3-dark .bp3-control.bp3-checkbox input:indeterminate ~ .bp3-control-indicator{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control.bp3-checkbox:hover input:indeterminate ~ .bp3-control-indicator{
    background-color:#106ba3;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control.bp3-checkbox input:not(:disabled):active:indeterminate ~ .bp3-control-indicator{
    background-color:#0e5a8a;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
  .bp3-dark .bp3-control.bp3-checkbox input:disabled:indeterminate ~ .bp3-control-indicator{
    background:rgba(14, 90, 138, 0.5);
    -webkit-box-shadow:none;
            box-shadow:none; }
  .bp3-control.bp3-checkbox .bp3-control-indicator{
    border-radius:3px; }
  .bp3-control.bp3-checkbox input:checked ~ .bp3-control-indicator::before{
    background-image:url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 16 16'%3e%3cpath fill-rule='evenodd' clip-rule='evenodd' d='M12 5c-.28 0-.53.11-.71.29L7 9.59l-2.29-2.3a1.003 1.003 0 00-1.42 1.42l3 3c.18.18.43.29.71.29s.53-.11.71-.29l5-5A1.003 1.003 0 0012 5z' fill='white'/%3e%3c/svg%3e"); }
  .bp3-control.bp3-checkbox input:indeterminate ~ .bp3-control-indicator::before{
    background-image:url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 16 16'%3e%3cpath fill-rule='evenodd' clip-rule='evenodd' d='M11 7H5c-.55 0-1 .45-1 1s.45 1 1 1h6c.55 0 1-.45 1-1s-.45-1-1-1z' fill='white'/%3e%3c/svg%3e"); }
  .bp3-control.bp3-radio .bp3-control-indicator{
    border-radius:50%; }
  .bp3-control.bp3-radio input:checked ~ .bp3-control-indicator::before{
    background-image:radial-gradient(#ffffff, #ffffff 28%, transparent 32%); }
  .bp3-control.bp3-radio input:checked:disabled ~ .bp3-control-indicator::before{
    opacity:0.5; }
  .bp3-control.bp3-radio input:focus ~ .bp3-control-indicator{
    -moz-outline-radius:16px; }
  .bp3-control.bp3-switch input ~ .bp3-control-indicator{
    background:rgba(167, 182, 194, 0.5); }
  .bp3-control.bp3-switch:hover input ~ .bp3-control-indicator{
    background:rgba(115, 134, 148, 0.5); }
  .bp3-control.bp3-switch input:not(:disabled):active ~ .bp3-control-indicator{
    background:rgba(92, 112, 128, 0.5); }
  .bp3-control.bp3-switch input:disabled ~ .bp3-control-indicator{
    background:rgba(206, 217, 224, 0.5); }
    .bp3-control.bp3-switch input:disabled ~ .bp3-control-indicator::before{
      background:rgba(255, 255, 255, 0.8); }
  .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator{
    background:#137cbd; }
  .bp3-control.bp3-switch:hover input:checked ~ .bp3-control-indicator{
    background:#106ba3; }
  .bp3-control.bp3-switch input:checked:not(:disabled):active ~ .bp3-control-indicator{
    background:#0e5a8a; }
  .bp3-control.bp3-switch input:checked:disabled ~ .bp3-control-indicator{
    background:rgba(19, 124, 189, 0.5); }
    .bp3-control.bp3-switch input:checked:disabled ~ .bp3-control-indicator::before{
      background:rgba(255, 255, 255, 0.8); }
  .bp3-control.bp3-switch:not(.bp3-align-right){
    padding-left:38px; }
    .bp3-control.bp3-switch:not(.bp3-align-right) .bp3-control-indicator{
      margin-left:-38px; }
  .bp3-control.bp3-switch.bp3-align-right{
    padding-right:38px; }
    .bp3-control.bp3-switch.bp3-align-right .bp3-control-indicator{
      margin-right:-38px; }
  .bp3-control.bp3-switch .bp3-control-indicator{
    border:none;
    border-radius:1.75em;
    -webkit-box-shadow:none !important;
            box-shadow:none !important;
    min-width:1.75em;
    -webkit-transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
    width:auto; }
    .bp3-control.bp3-switch .bp3-control-indicator::before{
      background:#ffffff;
      border-radius:50%;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
      height:calc(1em - 4px);
      left:0;
      margin:2px;
      position:absolute;
      -webkit-transition:left 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
      transition:left 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
      width:calc(1em - 4px); }
  .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator::before{
    left:calc(100% - 1em); }
  .bp3-control.bp3-switch.bp3-large:not(.bp3-align-right){
    padding-left:45px; }
    .bp3-control.bp3-switch.bp3-large:not(.bp3-align-right) .bp3-control-indicator{
      margin-left:-45px; }
  .bp3-control.bp3-switch.bp3-large.bp3-align-right{
    padding-right:45px; }
    .bp3-control.bp3-switch.bp3-large.bp3-align-right .bp3-control-indicator{
      margin-right:-45px; }
  .bp3-dark .bp3-control.bp3-switch input ~ .bp3-control-indicator{
    background:rgba(16, 22, 26, 0.5); }
  .bp3-dark .bp3-control.bp3-switch:hover input ~ .bp3-control-indicator{
    background:rgba(16, 22, 26, 0.7); }
  .bp3-dark .bp3-control.bp3-switch input:not(:disabled):active ~ .bp3-control-indicator{
    background:rgba(16, 22, 26, 0.9); }
  .bp3-dark .bp3-control.bp3-switch input:disabled ~ .bp3-control-indicator{
    background:rgba(57, 75, 89, 0.5); }
    .bp3-dark .bp3-control.bp3-switch input:disabled ~ .bp3-control-indicator::before{
      background:rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator{
    background:#137cbd; }
  .bp3-dark .bp3-control.bp3-switch:hover input:checked ~ .bp3-control-indicator{
    background:#106ba3; }
  .bp3-dark .bp3-control.bp3-switch input:checked:not(:disabled):active ~ .bp3-control-indicator{
    background:#0e5a8a; }
  .bp3-dark .bp3-control.bp3-switch input:checked:disabled ~ .bp3-control-indicator{
    background:rgba(14, 90, 138, 0.5); }
    .bp3-dark .bp3-control.bp3-switch input:checked:disabled ~ .bp3-control-indicator::before{
      background:rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control.bp3-switch .bp3-control-indicator::before{
    background:#394b59;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator::before{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-control.bp3-switch .bp3-switch-inner-text{
    font-size:0.7em;
    text-align:center; }
  .bp3-control.bp3-switch .bp3-control-indicator-child:first-child{
    line-height:0;
    margin-left:0.5em;
    margin-right:1.2em;
    visibility:hidden; }
  .bp3-control.bp3-switch .bp3-control-indicator-child:last-child{
    line-height:1em;
    margin-left:1.2em;
    margin-right:0.5em;
    visibility:visible; }
  .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator .bp3-control-indicator-child:first-child{
    line-height:1em;
    visibility:visible; }
  .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator .bp3-control-indicator-child:last-child{
    line-height:0;
    visibility:hidden; }
  .bp3-dark .bp3-control{
    color:#f5f8fa; }
    .bp3-dark .bp3-control.bp3-disabled{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-control .bp3-control-indicator{
      background-color:#394b59;
      background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.05)), to(rgba(255, 255, 255, 0)));
      background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0));
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-control:hover .bp3-control-indicator{
      background-color:#30404d; }
    .bp3-dark .bp3-control input:not(:disabled):active ~ .bp3-control-indicator{
      background:#202b33;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-dark .bp3-control input:disabled ~ .bp3-control-indicator{
      background:rgba(57, 75, 89, 0.5);
      -webkit-box-shadow:none;
              box-shadow:none;
      cursor:not-allowed; }
    .bp3-dark .bp3-control.bp3-checkbox input:disabled:checked ~ .bp3-control-indicator, .bp3-dark .bp3-control.bp3-checkbox input:disabled:indeterminate ~ .bp3-control-indicator{
      color:rgba(167, 182, 194, 0.6); }
.bp3-file-input{
  cursor:pointer;
  display:inline-block;
  height:30px;
  position:relative; }
  .bp3-file-input input{
    margin:0;
    min-width:200px;
    opacity:0; }
    .bp3-file-input input:disabled + .bp3-file-upload-input,
    .bp3-file-input input.bp3-disabled + .bp3-file-upload-input{
      background:rgba(206, 217, 224, 0.5);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(92, 112, 128, 0.6);
      cursor:not-allowed;
      resize:none; }
      .bp3-file-input input:disabled + .bp3-file-upload-input::after,
      .bp3-file-input input.bp3-disabled + .bp3-file-upload-input::after{
        background-color:rgba(206, 217, 224, 0.5);
        background-image:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:rgba(92, 112, 128, 0.6);
        cursor:not-allowed;
        outline:none; }
        .bp3-file-input input:disabled + .bp3-file-upload-input::after.bp3-active, .bp3-file-input input:disabled + .bp3-file-upload-input::after.bp3-active:hover,
        .bp3-file-input input.bp3-disabled + .bp3-file-upload-input::after.bp3-active,
        .bp3-file-input input.bp3-disabled + .bp3-file-upload-input::after.bp3-active:hover{
          background:rgba(206, 217, 224, 0.7); }
      .bp3-dark .bp3-file-input input:disabled + .bp3-file-upload-input, .bp3-dark
      .bp3-file-input input.bp3-disabled + .bp3-file-upload-input{
        background:rgba(57, 75, 89, 0.5);
        -webkit-box-shadow:none;
                box-shadow:none;
        color:rgba(167, 182, 194, 0.6); }
        .bp3-dark .bp3-file-input input:disabled + .bp3-file-upload-input::after, .bp3-dark
        .bp3-file-input input.bp3-disabled + .bp3-file-upload-input::after{
          background-color:rgba(57, 75, 89, 0.5);
          background-image:none;
          -webkit-box-shadow:none;
                  box-shadow:none;
          color:rgba(167, 182, 194, 0.6); }
          .bp3-dark .bp3-file-input input:disabled + .bp3-file-upload-input::after.bp3-active, .bp3-dark
          .bp3-file-input input.bp3-disabled + .bp3-file-upload-input::after.bp3-active{
            background:rgba(57, 75, 89, 0.7); }
  .bp3-file-input.bp3-file-input-has-selection .bp3-file-upload-input{
    color:#182026; }
  .bp3-dark .bp3-file-input.bp3-file-input-has-selection .bp3-file-upload-input{
    color:#f5f8fa; }
  .bp3-file-input.bp3-fill{
    width:100%; }
  .bp3-file-input.bp3-large,
  .bp3-large .bp3-file-input{
    height:40px; }
  .bp3-file-input .bp3-file-upload-input-custom-text::after{
    content:attr(bp3-button-text); }

.bp3-file-upload-input{
  -webkit-appearance:none;
     -moz-appearance:none;
          appearance:none;
  background:#ffffff;
  border:none;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
  color:#182026;
  font-size:14px;
  font-weight:400;
  height:30px;
  line-height:30px;
  outline:none;
  padding:0 10px;
  -webkit-transition:-webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:-webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  vertical-align:middle;
  overflow:hidden;
  text-overflow:ellipsis;
  white-space:nowrap;
  word-wrap:normal;
  color:rgba(92, 112, 128, 0.6);
  left:0;
  padding-right:80px;
  position:absolute;
  right:0;
  top:0;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-file-upload-input::-webkit-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-file-upload-input::-moz-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-file-upload-input:-ms-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-file-upload-input::-ms-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-file-upload-input::placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-file-upload-input:focus, .bp3-file-upload-input.bp3-active{
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-file-upload-input[type="search"], .bp3-file-upload-input.bp3-round{
    border-radius:30px;
    -webkit-box-sizing:border-box;
            box-sizing:border-box;
    padding-left:10px; }
  .bp3-file-upload-input[readonly]{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15); }
  .bp3-file-upload-input:disabled, .bp3-file-upload-input.bp3-disabled{
    background:rgba(206, 217, 224, 0.5);
    -webkit-box-shadow:none;
            box-shadow:none;
    color:rgba(92, 112, 128, 0.6);
    cursor:not-allowed;
    resize:none; }
  .bp3-file-upload-input::after{
    background-color:#f5f8fa;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.8)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    color:#182026;
    min-height:24px;
    min-width:24px;
    overflow:hidden;
    text-overflow:ellipsis;
    white-space:nowrap;
    word-wrap:normal;
    border-radius:3px;
    content:"Browse";
    line-height:24px;
    margin:3px;
    position:absolute;
    right:0;
    text-align:center;
    top:0;
    width:70px; }
    .bp3-file-upload-input::after:hover{
      background-clip:padding-box;
      background-color:#ebf1f5;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1); }
    .bp3-file-upload-input::after:active, .bp3-file-upload-input::after.bp3-active{
      background-color:#d8e1e8;
      background-image:none;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-file-upload-input::after:disabled, .bp3-file-upload-input::after.bp3-disabled{
      background-color:rgba(206, 217, 224, 0.5);
      background-image:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(92, 112, 128, 0.6);
      cursor:not-allowed;
      outline:none; }
      .bp3-file-upload-input::after:disabled.bp3-active, .bp3-file-upload-input::after:disabled.bp3-active:hover, .bp3-file-upload-input::after.bp3-disabled.bp3-active, .bp3-file-upload-input::after.bp3-disabled.bp3-active:hover{
        background:rgba(206, 217, 224, 0.7); }
  .bp3-file-upload-input:hover::after{
    background-clip:padding-box;
    background-color:#ebf1f5;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1); }
  .bp3-file-upload-input:active::after{
    background-color:#d8e1e8;
    background-image:none;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
  .bp3-large .bp3-file-upload-input{
    font-size:16px;
    height:40px;
    line-height:40px;
    padding-right:95px; }
    .bp3-large .bp3-file-upload-input[type="search"], .bp3-large .bp3-file-upload-input.bp3-round{
      padding:0 15px; }
    .bp3-large .bp3-file-upload-input::after{
      min-height:30px;
      min-width:30px;
      line-height:30px;
      margin:5px;
      width:85px; }
  .bp3-dark .bp3-file-upload-input{
    background:rgba(16, 22, 26, 0.3);
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
    color:#f5f8fa;
    color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input::-webkit-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input::-moz-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input:-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input::-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input::placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input:focus{
      -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-file-upload-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-file-upload-input:disabled, .bp3-dark .bp3-file-upload-input.bp3-disabled{
      background:rgba(57, 75, 89, 0.5);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input::after{
      background-color:#394b59;
      background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.05)), to(rgba(255, 255, 255, 0)));
      background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0));
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
      color:#f5f8fa; }
      .bp3-dark .bp3-file-upload-input::after:hover, .bp3-dark .bp3-file-upload-input::after:active, .bp3-dark .bp3-file-upload-input::after.bp3-active{
        color:#f5f8fa; }
      .bp3-dark .bp3-file-upload-input::after:hover{
        background-color:#30404d;
        -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
                box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-file-upload-input::after:active, .bp3-dark .bp3-file-upload-input::after.bp3-active{
        background-color:#202b33;
        background-image:none;
        -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
                box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
      .bp3-dark .bp3-file-upload-input::after:disabled, .bp3-dark .bp3-file-upload-input::after.bp3-disabled{
        background-color:rgba(57, 75, 89, 0.5);
        background-image:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:rgba(167, 182, 194, 0.6); }
        .bp3-dark .bp3-file-upload-input::after:disabled.bp3-active, .bp3-dark .bp3-file-upload-input::after.bp3-disabled.bp3-active{
          background:rgba(57, 75, 89, 0.7); }
      .bp3-dark .bp3-file-upload-input::after .bp3-button-spinner .bp3-spinner-head{
        background:rgba(16, 22, 26, 0.5);
        stroke:#8a9ba8; }
    .bp3-dark .bp3-file-upload-input:hover::after{
      background-color:#30404d;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-file-upload-input:active::after{
      background-color:#202b33;
      background-image:none;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
.bp3-file-upload-input::after{
  -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
          box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1); }
.bp3-form-group{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  margin:0 0 15px; }
  .bp3-form-group label.bp3-label{
    margin-bottom:5px; }
  .bp3-form-group .bp3-control{
    margin-top:7px; }
  .bp3-form-group .bp3-form-helper-text{
    color:#5c7080;
    font-size:12px;
    margin-top:5px; }
  .bp3-form-group.bp3-intent-primary .bp3-form-helper-text{
    color:#106ba3; }
  .bp3-form-group.bp3-intent-success .bp3-form-helper-text{
    color:#0d8050; }
  .bp3-form-group.bp3-intent-warning .bp3-form-helper-text{
    color:#bf7326; }
  .bp3-form-group.bp3-intent-danger .bp3-form-helper-text{
    color:#c23030; }
  .bp3-form-group.bp3-inline{
    -webkit-box-align:start;
        -ms-flex-align:start;
            align-items:flex-start;
    -webkit-box-orient:horizontal;
    -webkit-box-direction:normal;
        -ms-flex-direction:row;
            flex-direction:row; }
    .bp3-form-group.bp3-inline.bp3-large label.bp3-label{
      line-height:40px;
      margin:0 10px 0 0; }
    .bp3-form-group.bp3-inline label.bp3-label{
      line-height:30px;
      margin:0 10px 0 0; }
  .bp3-form-group.bp3-disabled .bp3-label,
  .bp3-form-group.bp3-disabled .bp3-text-muted,
  .bp3-form-group.bp3-disabled .bp3-form-helper-text{
    color:rgba(92, 112, 128, 0.6) !important; }
  .bp3-dark .bp3-form-group.bp3-intent-primary .bp3-form-helper-text{
    color:#48aff0; }
  .bp3-dark .bp3-form-group.bp3-intent-success .bp3-form-helper-text{
    color:#3dcc91; }
  .bp3-dark .bp3-form-group.bp3-intent-warning .bp3-form-helper-text{
    color:#ffb366; }
  .bp3-dark .bp3-form-group.bp3-intent-danger .bp3-form-helper-text{
    color:#ff7373; }
  .bp3-dark .bp3-form-group .bp3-form-helper-text{
    color:#a7b6c2; }
  .bp3-dark .bp3-form-group.bp3-disabled .bp3-label,
  .bp3-dark .bp3-form-group.bp3-disabled .bp3-text-muted,
  .bp3-dark .bp3-form-group.bp3-disabled .bp3-form-helper-text{
    color:rgba(167, 182, 194, 0.6) !important; }
.bp3-input-group{
  display:block;
  position:relative; }
  .bp3-input-group .bp3-input{
    position:relative;
    width:100%; }
    .bp3-input-group .bp3-input:not(:first-child){
      padding-left:30px; }
    .bp3-input-group .bp3-input:not(:last-child){
      padding-right:30px; }
  .bp3-input-group .bp3-input-action,
  .bp3-input-group > .bp3-input-left-container,
  .bp3-input-group > .bp3-button,
  .bp3-input-group > .bp3-icon{
    position:absolute;
    top:0; }
    .bp3-input-group .bp3-input-action:first-child,
    .bp3-input-group > .bp3-input-left-container:first-child,
    .bp3-input-group > .bp3-button:first-child,
    .bp3-input-group > .bp3-icon:first-child{
      left:0; }
    .bp3-input-group .bp3-input-action:last-child,
    .bp3-input-group > .bp3-input-left-container:last-child,
    .bp3-input-group > .bp3-button:last-child,
    .bp3-input-group > .bp3-icon:last-child{
      right:0; }
  .bp3-input-group .bp3-button{
    min-height:24px;
    min-width:24px;
    margin:3px;
    padding:0 7px; }
    .bp3-input-group .bp3-button:empty{
      padding:0; }
  .bp3-input-group > .bp3-input-left-container,
  .bp3-input-group > .bp3-icon{
    z-index:1; }
  .bp3-input-group > .bp3-input-left-container > .bp3-icon,
  .bp3-input-group > .bp3-icon{
    color:#5c7080; }
    .bp3-input-group > .bp3-input-left-container > .bp3-icon:empty,
    .bp3-input-group > .bp3-icon:empty{
      font-family:"Icons16", sans-serif;
      font-size:16px;
      font-style:normal;
      font-weight:400;
      line-height:1;
      -moz-osx-font-smoothing:grayscale;
      -webkit-font-smoothing:antialiased; }
  .bp3-input-group > .bp3-input-left-container > .bp3-icon,
  .bp3-input-group > .bp3-icon,
  .bp3-input-group .bp3-input-action > .bp3-spinner{
    margin:7px; }
  .bp3-input-group .bp3-tag{
    margin:5px; }
  .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:not(:hover):not(:focus),
  .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:not(:hover):not(:focus){
    color:#5c7080; }
    .bp3-dark .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:not(:hover):not(:focus), .bp3-dark
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:not(:hover):not(:focus){
      color:#a7b6c2; }
    .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon, .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon-standard, .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon-large,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon-standard,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon-large{
      color:#5c7080; }
  .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:disabled,
  .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:disabled{
    color:rgba(92, 112, 128, 0.6) !important; }
    .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:disabled .bp3-icon, .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:disabled .bp3-icon-standard, .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:disabled .bp3-icon-large,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:disabled .bp3-icon,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:disabled .bp3-icon-standard,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:disabled .bp3-icon-large{
      color:rgba(92, 112, 128, 0.6) !important; }
  .bp3-input-group.bp3-disabled{
    cursor:not-allowed; }
    .bp3-input-group.bp3-disabled .bp3-icon{
      color:rgba(92, 112, 128, 0.6); }
  .bp3-input-group.bp3-large .bp3-button{
    min-height:30px;
    min-width:30px;
    margin:5px; }
  .bp3-input-group.bp3-large > .bp3-input-left-container > .bp3-icon,
  .bp3-input-group.bp3-large > .bp3-icon,
  .bp3-input-group.bp3-large .bp3-input-action > .bp3-spinner{
    margin:12px; }
  .bp3-input-group.bp3-large .bp3-input{
    font-size:16px;
    height:40px;
    line-height:40px; }
    .bp3-input-group.bp3-large .bp3-input[type="search"], .bp3-input-group.bp3-large .bp3-input.bp3-round{
      padding:0 15px; }
    .bp3-input-group.bp3-large .bp3-input:not(:first-child){
      padding-left:40px; }
    .bp3-input-group.bp3-large .bp3-input:not(:last-child){
      padding-right:40px; }
  .bp3-input-group.bp3-small .bp3-button{
    min-height:20px;
    min-width:20px;
    margin:2px; }
  .bp3-input-group.bp3-small .bp3-tag{
    min-height:20px;
    min-width:20px;
    margin:2px; }
  .bp3-input-group.bp3-small > .bp3-input-left-container > .bp3-icon,
  .bp3-input-group.bp3-small > .bp3-icon,
  .bp3-input-group.bp3-small .bp3-input-action > .bp3-spinner{
    margin:4px; }
  .bp3-input-group.bp3-small .bp3-input{
    font-size:12px;
    height:24px;
    line-height:24px;
    padding-left:8px;
    padding-right:8px; }
    .bp3-input-group.bp3-small .bp3-input[type="search"], .bp3-input-group.bp3-small .bp3-input.bp3-round{
      padding:0 12px; }
    .bp3-input-group.bp3-small .bp3-input:not(:first-child){
      padding-left:24px; }
    .bp3-input-group.bp3-small .bp3-input:not(:last-child){
      padding-right:24px; }
  .bp3-input-group.bp3-fill{
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto;
    width:100%; }
  .bp3-input-group.bp3-round .bp3-button,
  .bp3-input-group.bp3-round .bp3-input,
  .bp3-input-group.bp3-round .bp3-tag{
    border-radius:30px; }
  .bp3-dark .bp3-input-group .bp3-icon{
    color:#a7b6c2; }
  .bp3-dark .bp3-input-group.bp3-disabled .bp3-icon{
    color:rgba(167, 182, 194, 0.6); }
  .bp3-input-group.bp3-intent-primary .bp3-input{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-primary .bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-primary .bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #137cbd;
              box-shadow:inset 0 0 0 1px #137cbd; }
    .bp3-input-group.bp3-intent-primary .bp3-input:disabled, .bp3-input-group.bp3-intent-primary .bp3-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-input-group.bp3-intent-primary > .bp3-icon{
    color:#106ba3; }
    .bp3-dark .bp3-input-group.bp3-intent-primary > .bp3-icon{
      color:#48aff0; }
  .bp3-input-group.bp3-intent-success .bp3-input{
    -webkit-box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-success .bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-success .bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #0f9960;
              box-shadow:inset 0 0 0 1px #0f9960; }
    .bp3-input-group.bp3-intent-success .bp3-input:disabled, .bp3-input-group.bp3-intent-success .bp3-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-input-group.bp3-intent-success > .bp3-icon{
    color:#0d8050; }
    .bp3-dark .bp3-input-group.bp3-intent-success > .bp3-icon{
      color:#3dcc91; }
  .bp3-input-group.bp3-intent-warning .bp3-input{
    -webkit-box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-warning .bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-warning .bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #d9822b;
              box-shadow:inset 0 0 0 1px #d9822b; }
    .bp3-input-group.bp3-intent-warning .bp3-input:disabled, .bp3-input-group.bp3-intent-warning .bp3-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-input-group.bp3-intent-warning > .bp3-icon{
    color:#bf7326; }
    .bp3-dark .bp3-input-group.bp3-intent-warning > .bp3-icon{
      color:#ffb366; }
  .bp3-input-group.bp3-intent-danger .bp3-input{
    -webkit-box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-danger .bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-danger .bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #db3737;
              box-shadow:inset 0 0 0 1px #db3737; }
    .bp3-input-group.bp3-intent-danger .bp3-input:disabled, .bp3-input-group.bp3-intent-danger .bp3-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-input-group.bp3-intent-danger > .bp3-icon{
    color:#c23030; }
    .bp3-dark .bp3-input-group.bp3-intent-danger > .bp3-icon{
      color:#ff7373; }
.bp3-input{
  -webkit-appearance:none;
     -moz-appearance:none;
          appearance:none;
  background:#ffffff;
  border:none;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
  color:#182026;
  font-size:14px;
  font-weight:400;
  height:30px;
  line-height:30px;
  outline:none;
  padding:0 10px;
  -webkit-transition:-webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:-webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  vertical-align:middle; }
  .bp3-input::-webkit-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input::-moz-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input:-ms-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input::-ms-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input::placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input:focus, .bp3-input.bp3-active{
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-input[type="search"], .bp3-input.bp3-round{
    border-radius:30px;
    -webkit-box-sizing:border-box;
            box-sizing:border-box;
    padding-left:10px; }
  .bp3-input[readonly]{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15); }
  .bp3-input:disabled, .bp3-input.bp3-disabled{
    background:rgba(206, 217, 224, 0.5);
    -webkit-box-shadow:none;
            box-shadow:none;
    color:rgba(92, 112, 128, 0.6);
    cursor:not-allowed;
    resize:none; }
  .bp3-input.bp3-large{
    font-size:16px;
    height:40px;
    line-height:40px; }
    .bp3-input.bp3-large[type="search"], .bp3-input.bp3-large.bp3-round{
      padding:0 15px; }
  .bp3-input.bp3-small{
    font-size:12px;
    height:24px;
    line-height:24px;
    padding-left:8px;
    padding-right:8px; }
    .bp3-input.bp3-small[type="search"], .bp3-input.bp3-small.bp3-round{
      padding:0 12px; }
  .bp3-input.bp3-fill{
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto;
    width:100%; }
  .bp3-dark .bp3-input{
    background:rgba(16, 22, 26, 0.3);
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
    color:#f5f8fa; }
    .bp3-dark .bp3-input::-webkit-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-input::-moz-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-input:-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-input::-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-input::placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-input:disabled, .bp3-dark .bp3-input.bp3-disabled{
      background:rgba(57, 75, 89, 0.5);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(167, 182, 194, 0.6); }
  .bp3-input.bp3-intent-primary{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-primary:focus{
      -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-primary[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #137cbd;
              box-shadow:inset 0 0 0 1px #137cbd; }
    .bp3-input.bp3-intent-primary:disabled, .bp3-input.bp3-intent-primary.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
    .bp3-dark .bp3-input.bp3-intent-primary{
      -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-primary:focus{
        -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
                box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-primary[readonly]{
        -webkit-box-shadow:inset 0 0 0 1px #137cbd;
                box-shadow:inset 0 0 0 1px #137cbd; }
      .bp3-dark .bp3-input.bp3-intent-primary:disabled, .bp3-dark .bp3-input.bp3-intent-primary.bp3-disabled{
        -webkit-box-shadow:none;
                box-shadow:none; }
  .bp3-input.bp3-intent-success{
    -webkit-box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-success:focus{
      -webkit-box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-success[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #0f9960;
              box-shadow:inset 0 0 0 1px #0f9960; }
    .bp3-input.bp3-intent-success:disabled, .bp3-input.bp3-intent-success.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
    .bp3-dark .bp3-input.bp3-intent-success{
      -webkit-box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-success:focus{
        -webkit-box-shadow:0 0 0 1px #0f9960, 0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
                box-shadow:0 0 0 1px #0f9960, 0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-success[readonly]{
        -webkit-box-shadow:inset 0 0 0 1px #0f9960;
                box-shadow:inset 0 0 0 1px #0f9960; }
      .bp3-dark .bp3-input.bp3-intent-success:disabled, .bp3-dark .bp3-input.bp3-intent-success.bp3-disabled{
        -webkit-box-shadow:none;
                box-shadow:none; }
  .bp3-input.bp3-intent-warning{
    -webkit-box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-warning:focus{
      -webkit-box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-warning[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #d9822b;
              box-shadow:inset 0 0 0 1px #d9822b; }
    .bp3-input.bp3-intent-warning:disabled, .bp3-input.bp3-intent-warning.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
    .bp3-dark .bp3-input.bp3-intent-warning{
      -webkit-box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-warning:focus{
        -webkit-box-shadow:0 0 0 1px #d9822b, 0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
                box-shadow:0 0 0 1px #d9822b, 0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-warning[readonly]{
        -webkit-box-shadow:inset 0 0 0 1px #d9822b;
                box-shadow:inset 0 0 0 1px #d9822b; }
      .bp3-dark .bp3-input.bp3-intent-warning:disabled, .bp3-dark .bp3-input.bp3-intent-warning.bp3-disabled{
        -webkit-box-shadow:none;
                box-shadow:none; }
  .bp3-input.bp3-intent-danger{
    -webkit-box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-danger:focus{
      -webkit-box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-danger[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #db3737;
              box-shadow:inset 0 0 0 1px #db3737; }
    .bp3-input.bp3-intent-danger:disabled, .bp3-input.bp3-intent-danger.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
    .bp3-dark .bp3-input.bp3-intent-danger{
      -webkit-box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-danger:focus{
        -webkit-box-shadow:0 0 0 1px #db3737, 0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
                box-shadow:0 0 0 1px #db3737, 0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-danger[readonly]{
        -webkit-box-shadow:inset 0 0 0 1px #db3737;
                box-shadow:inset 0 0 0 1px #db3737; }
      .bp3-dark .bp3-input.bp3-intent-danger:disabled, .bp3-dark .bp3-input.bp3-intent-danger.bp3-disabled{
        -webkit-box-shadow:none;
                box-shadow:none; }
  .bp3-input::-ms-clear{
    display:none; }
textarea.bp3-input{
  max-width:100%;
  padding:10px; }
  textarea.bp3-input, textarea.bp3-input.bp3-large, textarea.bp3-input.bp3-small{
    height:auto;
    line-height:inherit; }
  textarea.bp3-input.bp3-small{
    padding:8px; }
  .bp3-dark textarea.bp3-input{
    background:rgba(16, 22, 26, 0.3);
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
    color:#f5f8fa; }
    .bp3-dark textarea.bp3-input::-webkit-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark textarea.bp3-input::-moz-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark textarea.bp3-input:-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark textarea.bp3-input::-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark textarea.bp3-input::placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark textarea.bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark textarea.bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark textarea.bp3-input:disabled, .bp3-dark textarea.bp3-input.bp3-disabled{
      background:rgba(57, 75, 89, 0.5);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(167, 182, 194, 0.6); }
label.bp3-label{
  display:block;
  margin-bottom:15px;
  margin-top:0; }
  label.bp3-label .bp3-html-select,
  label.bp3-label .bp3-input,
  label.bp3-label .bp3-select,
  label.bp3-label .bp3-slider,
  label.bp3-label .bp3-popover-wrapper{
    display:block;
    margin-top:5px;
    text-transform:none; }
  label.bp3-label .bp3-button-group{
    margin-top:5px; }
  label.bp3-label .bp3-select select,
  label.bp3-label .bp3-html-select select{
    font-weight:400;
    vertical-align:top;
    width:100%; }
  label.bp3-label.bp3-disabled,
  label.bp3-label.bp3-disabled .bp3-text-muted{
    color:rgba(92, 112, 128, 0.6); }
  label.bp3-label.bp3-inline{
    line-height:30px; }
    label.bp3-label.bp3-inline .bp3-html-select,
    label.bp3-label.bp3-inline .bp3-input,
    label.bp3-label.bp3-inline .bp3-input-group,
    label.bp3-label.bp3-inline .bp3-select,
    label.bp3-label.bp3-inline .bp3-popover-wrapper{
      display:inline-block;
      margin:0 0 0 5px;
      vertical-align:top; }
    label.bp3-label.bp3-inline .bp3-button-group{
      margin:0 0 0 5px; }
    label.bp3-label.bp3-inline .bp3-input-group .bp3-input{
      margin-left:0; }
    label.bp3-label.bp3-inline.bp3-large{
      line-height:40px; }
  label.bp3-label:not(.bp3-inline) .bp3-popover-target{
    display:block; }
  .bp3-dark label.bp3-label{
    color:#f5f8fa; }
    .bp3-dark label.bp3-label.bp3-disabled,
    .bp3-dark label.bp3-label.bp3-disabled .bp3-text-muted{
      color:rgba(167, 182, 194, 0.6); }
.bp3-numeric-input .bp3-button-group.bp3-vertical > .bp3-button{
  -webkit-box-flex:1;
      -ms-flex:1 1 14px;
          flex:1 1 14px;
  min-height:0;
  padding:0;
  width:30px; }
  .bp3-numeric-input .bp3-button-group.bp3-vertical > .bp3-button:first-child{
    border-radius:0 3px 0 0; }
  .bp3-numeric-input .bp3-button-group.bp3-vertical > .bp3-button:last-child{
    border-radius:0 0 3px 0; }

.bp3-numeric-input .bp3-button-group.bp3-vertical:first-child > .bp3-button:first-child{
  border-radius:3px 0 0 0; }

.bp3-numeric-input .bp3-button-group.bp3-vertical:first-child > .bp3-button:last-child{
  border-radius:0 0 0 3px; }

.bp3-numeric-input.bp3-large .bp3-button-group.bp3-vertical > .bp3-button{
  width:40px; }

form{
  display:block; }
.bp3-html-select select,
.bp3-select select{
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  border:none;
  border-radius:3px;
  cursor:pointer;
  font-size:14px;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  padding:5px 10px;
  text-align:left;
  vertical-align:middle;
  background-color:#f5f8fa;
  background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.8)), to(rgba(255, 255, 255, 0)));
  background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
  -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
          box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
  color:#182026;
  -moz-appearance:none;
  -webkit-appearance:none;
  border-radius:3px;
  height:30px;
  padding:0 25px 0 10px;
  width:100%; }
  .bp3-html-select select > *, .bp3-select select > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-html-select select > .bp3-fill, .bp3-select select > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-html-select select::before,
  .bp3-select select::before, .bp3-html-select select > *, .bp3-select select > *{
    margin-right:7px; }
  .bp3-html-select select:empty::before,
  .bp3-select select:empty::before,
  .bp3-html-select select > :last-child,
  .bp3-select select > :last-child{
    margin-right:0; }
  .bp3-html-select select:hover,
  .bp3-select select:hover{
    background-clip:padding-box;
    background-color:#ebf1f5;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1); }
  .bp3-html-select select:active,
  .bp3-select select:active, .bp3-html-select select.bp3-active,
  .bp3-select select.bp3-active{
    background-color:#d8e1e8;
    background-image:none;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
  .bp3-html-select select:disabled,
  .bp3-select select:disabled, .bp3-html-select select.bp3-disabled,
  .bp3-select select.bp3-disabled{
    background-color:rgba(206, 217, 224, 0.5);
    background-image:none;
    -webkit-box-shadow:none;
            box-shadow:none;
    color:rgba(92, 112, 128, 0.6);
    cursor:not-allowed;
    outline:none; }
    .bp3-html-select select:disabled.bp3-active,
    .bp3-select select:disabled.bp3-active, .bp3-html-select select:disabled.bp3-active:hover,
    .bp3-select select:disabled.bp3-active:hover, .bp3-html-select select.bp3-disabled.bp3-active,
    .bp3-select select.bp3-disabled.bp3-active, .bp3-html-select select.bp3-disabled.bp3-active:hover,
    .bp3-select select.bp3-disabled.bp3-active:hover{
      background:rgba(206, 217, 224, 0.7); }

.bp3-html-select.bp3-minimal select,
.bp3-select.bp3-minimal select{
  background:none;
  -webkit-box-shadow:none;
          box-shadow:none; }
  .bp3-html-select.bp3-minimal select:hover,
  .bp3-select.bp3-minimal select:hover{
    background:rgba(167, 182, 194, 0.3);
    -webkit-box-shadow:none;
            box-shadow:none;
    color:#182026;
    text-decoration:none; }
  .bp3-html-select.bp3-minimal select:active,
  .bp3-select.bp3-minimal select:active, .bp3-html-select.bp3-minimal select.bp3-active,
  .bp3-select.bp3-minimal select.bp3-active{
    background:rgba(115, 134, 148, 0.3);
    -webkit-box-shadow:none;
            box-shadow:none;
    color:#182026; }
  .bp3-html-select.bp3-minimal select:disabled,
  .bp3-select.bp3-minimal select:disabled, .bp3-html-select.bp3-minimal select:disabled:hover,
  .bp3-select.bp3-minimal select:disabled:hover, .bp3-html-select.bp3-minimal select.bp3-disabled,
  .bp3-select.bp3-minimal select.bp3-disabled, .bp3-html-select.bp3-minimal select.bp3-disabled:hover,
  .bp3-select.bp3-minimal select.bp3-disabled:hover{
    background:none;
    color:rgba(92, 112, 128, 0.6);
    cursor:not-allowed; }
    .bp3-html-select.bp3-minimal select:disabled.bp3-active,
    .bp3-select.bp3-minimal select:disabled.bp3-active, .bp3-html-select.bp3-minimal select:disabled:hover.bp3-active,
    .bp3-select.bp3-minimal select:disabled:hover.bp3-active, .bp3-html-select.bp3-minimal select.bp3-disabled.bp3-active,
    .bp3-select.bp3-minimal select.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal select.bp3-disabled:hover.bp3-active,
    .bp3-select.bp3-minimal select.bp3-disabled:hover.bp3-active{
      background:rgba(115, 134, 148, 0.3); }
  .bp3-dark .bp3-html-select.bp3-minimal select, .bp3-html-select.bp3-minimal .bp3-dark select,
  .bp3-dark .bp3-select.bp3-minimal select, .bp3-select.bp3-minimal .bp3-dark select{
    background:none;
    -webkit-box-shadow:none;
            box-shadow:none;
    color:inherit; }
    .bp3-dark .bp3-html-select.bp3-minimal select:hover, .bp3-html-select.bp3-minimal .bp3-dark select:hover,
    .bp3-dark .bp3-select.bp3-minimal select:hover, .bp3-select.bp3-minimal .bp3-dark select:hover, .bp3-dark .bp3-html-select.bp3-minimal select:active, .bp3-html-select.bp3-minimal .bp3-dark select:active,
    .bp3-dark .bp3-select.bp3-minimal select:active, .bp3-select.bp3-minimal .bp3-dark select:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-active,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-active{
      background:none;
      -webkit-box-shadow:none;
              box-shadow:none; }
    .bp3-dark .bp3-html-select.bp3-minimal select:hover, .bp3-html-select.bp3-minimal .bp3-dark select:hover,
    .bp3-dark .bp3-select.bp3-minimal select:hover, .bp3-select.bp3-minimal .bp3-dark select:hover{
      background:rgba(138, 155, 168, 0.15); }
    .bp3-dark .bp3-html-select.bp3-minimal select:active, .bp3-html-select.bp3-minimal .bp3-dark select:active,
    .bp3-dark .bp3-select.bp3-minimal select:active, .bp3-select.bp3-minimal .bp3-dark select:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-active,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-active{
      background:rgba(138, 155, 168, 0.3);
      color:#f5f8fa; }
    .bp3-dark .bp3-html-select.bp3-minimal select:disabled, .bp3-html-select.bp3-minimal .bp3-dark select:disabled,
    .bp3-dark .bp3-select.bp3-minimal select:disabled, .bp3-select.bp3-minimal .bp3-dark select:disabled, .bp3-dark .bp3-html-select.bp3-minimal select:disabled:hover, .bp3-html-select.bp3-minimal .bp3-dark select:disabled:hover,
    .bp3-dark .bp3-select.bp3-minimal select:disabled:hover, .bp3-select.bp3-minimal .bp3-dark select:disabled:hover, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-disabled,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-disabled, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-disabled:hover, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-disabled:hover,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-disabled:hover, .bp3-select.bp3-minimal .bp3-dark select.bp3-disabled:hover{
      background:none;
      color:rgba(167, 182, 194, 0.6);
      cursor:not-allowed; }
      .bp3-dark .bp3-html-select.bp3-minimal select:disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select:disabled.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select:disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select:disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select:disabled:hover.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select:disabled:hover.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select:disabled:hover.bp3-active, .bp3-select.bp3-minimal .bp3-dark select:disabled:hover.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-disabled.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-disabled:hover.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-disabled:hover.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-disabled:hover.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-disabled:hover.bp3-active{
        background:rgba(138, 155, 168, 0.3); }
  .bp3-html-select.bp3-minimal select.bp3-intent-primary,
  .bp3-select.bp3-minimal select.bp3-intent-primary{
    color:#106ba3; }
    .bp3-html-select.bp3-minimal select.bp3-intent-primary:hover,
    .bp3-select.bp3-minimal select.bp3-intent-primary:hover, .bp3-html-select.bp3-minimal select.bp3-intent-primary:active,
    .bp3-select.bp3-minimal select.bp3-intent-primary:active, .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-active{
      background:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#106ba3; }
    .bp3-html-select.bp3-minimal select.bp3-intent-primary:hover,
    .bp3-select.bp3-minimal select.bp3-intent-primary:hover{
      background:rgba(19, 124, 189, 0.15);
      color:#106ba3; }
    .bp3-html-select.bp3-minimal select.bp3-intent-primary:active,
    .bp3-select.bp3-minimal select.bp3-intent-primary:active, .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-active{
      background:rgba(19, 124, 189, 0.3);
      color:#106ba3; }
    .bp3-html-select.bp3-minimal select.bp3-intent-primary:disabled,
    .bp3-select.bp3-minimal select.bp3-intent-primary:disabled, .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-disabled,
    .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-disabled{
      background:none;
      color:rgba(16, 107, 163, 0.5); }
      .bp3-html-select.bp3-minimal select.bp3-intent-primary:disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-primary:disabled.bp3-active, .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-disabled.bp3-active{
        background:rgba(19, 124, 189, 0.3); }
    .bp3-html-select.bp3-minimal select.bp3-intent-primary .bp3-button-spinner .bp3-spinner-head, .bp3-select.bp3-minimal select.bp3-intent-primary .bp3-button-spinner .bp3-spinner-head{
      stroke:#106ba3; }
    .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary{
      color:#48aff0; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary:hover, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary:hover,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary:hover, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary:hover{
        background:rgba(19, 124, 189, 0.2);
        color:#48aff0; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary:active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary:active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary:active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-active{
        background:rgba(19, 124, 189, 0.3);
        color:#48aff0; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary:disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary:disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary:disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary:disabled, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-disabled{
        background:none;
        color:rgba(72, 175, 240, 0.5); }
        .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary:disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary:disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary:disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary:disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-disabled.bp3-active{
          background:rgba(19, 124, 189, 0.3); }
  .bp3-html-select.bp3-minimal select.bp3-intent-success,
  .bp3-select.bp3-minimal select.bp3-intent-success{
    color:#0d8050; }
    .bp3-html-select.bp3-minimal select.bp3-intent-success:hover,
    .bp3-select.bp3-minimal select.bp3-intent-success:hover, .bp3-html-select.bp3-minimal select.bp3-intent-success:active,
    .bp3-select.bp3-minimal select.bp3-intent-success:active, .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-success.bp3-active{
      background:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#0d8050; }
    .bp3-html-select.bp3-minimal select.bp3-intent-success:hover,
    .bp3-select.bp3-minimal select.bp3-intent-success:hover{
      background:rgba(15, 153, 96, 0.15);
      color:#0d8050; }
    .bp3-html-select.bp3-minimal select.bp3-intent-success:active,
    .bp3-select.bp3-minimal select.bp3-intent-success:active, .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-success.bp3-active{
      background:rgba(15, 153, 96, 0.3);
      color:#0d8050; }
    .bp3-html-select.bp3-minimal select.bp3-intent-success:disabled,
    .bp3-select.bp3-minimal select.bp3-intent-success:disabled, .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-disabled,
    .bp3-select.bp3-minimal select.bp3-intent-success.bp3-disabled{
      background:none;
      color:rgba(13, 128, 80, 0.5); }
      .bp3-html-select.bp3-minimal select.bp3-intent-success:disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-success:disabled.bp3-active, .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-success.bp3-disabled.bp3-active{
        background:rgba(15, 153, 96, 0.3); }
    .bp3-html-select.bp3-minimal select.bp3-intent-success .bp3-button-spinner .bp3-spinner-head, .bp3-select.bp3-minimal select.bp3-intent-success .bp3-button-spinner .bp3-spinner-head{
      stroke:#0d8050; }
    .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success{
      color:#3dcc91; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success:hover, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success:hover,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success:hover, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success:hover{
        background:rgba(15, 153, 96, 0.2);
        color:#3dcc91; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success:active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success:active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success:active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-active{
        background:rgba(15, 153, 96, 0.3);
        color:#3dcc91; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success:disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success:disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success:disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success:disabled, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success.bp3-disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-disabled{
        background:none;
        color:rgba(61, 204, 145, 0.5); }
        .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success:disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success:disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success:disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success:disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success.bp3-disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-disabled.bp3-active{
          background:rgba(15, 153, 96, 0.3); }
  .bp3-html-select.bp3-minimal select.bp3-intent-warning,
  .bp3-select.bp3-minimal select.bp3-intent-warning{
    color:#bf7326; }
    .bp3-html-select.bp3-minimal select.bp3-intent-warning:hover,
    .bp3-select.bp3-minimal select.bp3-intent-warning:hover, .bp3-html-select.bp3-minimal select.bp3-intent-warning:active,
    .bp3-select.bp3-minimal select.bp3-intent-warning:active, .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-active{
      background:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#bf7326; }
    .bp3-html-select.bp3-minimal select.bp3-intent-warning:hover,
    .bp3-select.bp3-minimal select.bp3-intent-warning:hover{
      background:rgba(217, 130, 43, 0.15);
      color:#bf7326; }
    .bp3-html-select.bp3-minimal select.bp3-intent-warning:active,
    .bp3-select.bp3-minimal select.bp3-intent-warning:active, .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-active{
      background:rgba(217, 130, 43, 0.3);
      color:#bf7326; }
    .bp3-html-select.bp3-minimal select.bp3-intent-warning:disabled,
    .bp3-select.bp3-minimal select.bp3-intent-warning:disabled, .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-disabled,
    .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-disabled{
      background:none;
      color:rgba(191, 115, 38, 0.5); }
      .bp3-html-select.bp3-minimal select.bp3-intent-warning:disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-warning:disabled.bp3-active, .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-disabled.bp3-active{
        background:rgba(217, 130, 43, 0.3); }
    .bp3-html-select.bp3-minimal select.bp3-intent-warning .bp3-button-spinner .bp3-spinner-head, .bp3-select.bp3-minimal select.bp3-intent-warning .bp3-button-spinner .bp3-spinner-head{
      stroke:#bf7326; }
    .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning{
      color:#ffb366; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning:hover, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning:hover,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning:hover, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning:hover{
        background:rgba(217, 130, 43, 0.2);
        color:#ffb366; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning:active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning:active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning:active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-active{
        background:rgba(217, 130, 43, 0.3);
        color:#ffb366; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning:disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning:disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning:disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning:disabled, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-disabled{
        background:none;
        color:rgba(255, 179, 102, 0.5); }
        .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning:disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning:disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning:disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning:disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-disabled.bp3-active{
          background:rgba(217, 130, 43, 0.3); }
  .bp3-html-select.bp3-minimal select.bp3-intent-danger,
  .bp3-select.bp3-minimal select.bp3-intent-danger{
    color:#c23030; }
    .bp3-html-select.bp3-minimal select.bp3-intent-danger:hover,
    .bp3-select.bp3-minimal select.bp3-intent-danger:hover, .bp3-html-select.bp3-minimal select.bp3-intent-danger:active,
    .bp3-select.bp3-minimal select.bp3-intent-danger:active, .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-active{
      background:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#c23030; }
    .bp3-html-select.bp3-minimal select.bp3-intent-danger:hover,
    .bp3-select.bp3-minimal select.bp3-intent-danger:hover{
      background:rgba(219, 55, 55, 0.15);
      color:#c23030; }
    .bp3-html-select.bp3-minimal select.bp3-intent-danger:active,
    .bp3-select.bp3-minimal select.bp3-intent-danger:active, .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-active{
      background:rgba(219, 55, 55, 0.3);
      color:#c23030; }
    .bp3-html-select.bp3-minimal select.bp3-intent-danger:disabled,
    .bp3-select.bp3-minimal select.bp3-intent-danger:disabled, .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-disabled,
    .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-disabled{
      background:none;
      color:rgba(194, 48, 48, 0.5); }
      .bp3-html-select.bp3-minimal select.bp3-intent-danger:disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-danger:disabled.bp3-active, .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-disabled.bp3-active{
        background:rgba(219, 55, 55, 0.3); }
    .bp3-html-select.bp3-minimal select.bp3-intent-danger .bp3-button-spinner .bp3-spinner-head, .bp3-select.bp3-minimal select.bp3-intent-danger .bp3-button-spinner .bp3-spinner-head{
      stroke:#c23030; }
    .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger{
      color:#ff7373; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger:hover, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger:hover,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger:hover, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger:hover{
        background:rgba(219, 55, 55, 0.2);
        color:#ff7373; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger:active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger:active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger:active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-active{
        background:rgba(219, 55, 55, 0.3);
        color:#ff7373; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger:disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger:disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger:disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger:disabled, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-disabled{
        background:none;
        color:rgba(255, 115, 115, 0.5); }
        .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger:disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger:disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger:disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger:disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-disabled.bp3-active{
          background:rgba(219, 55, 55, 0.3); }

.bp3-html-select.bp3-large select,
.bp3-select.bp3-large select{
  font-size:16px;
  height:40px;
  padding-right:35px; }

.bp3-dark .bp3-html-select select, .bp3-dark .bp3-select select{
  background-color:#394b59;
  background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.05)), to(rgba(255, 255, 255, 0)));
  background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0));
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
  color:#f5f8fa; }
  .bp3-dark .bp3-html-select select:hover, .bp3-dark .bp3-select select:hover, .bp3-dark .bp3-html-select select:active, .bp3-dark .bp3-select select:active, .bp3-dark .bp3-html-select select.bp3-active, .bp3-dark .bp3-select select.bp3-active{
    color:#f5f8fa; }
  .bp3-dark .bp3-html-select select:hover, .bp3-dark .bp3-select select:hover{
    background-color:#30404d;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-html-select select:active, .bp3-dark .bp3-select select:active, .bp3-dark .bp3-html-select select.bp3-active, .bp3-dark .bp3-select select.bp3-active{
    background-color:#202b33;
    background-image:none;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
  .bp3-dark .bp3-html-select select:disabled, .bp3-dark .bp3-select select:disabled, .bp3-dark .bp3-html-select select.bp3-disabled, .bp3-dark .bp3-select select.bp3-disabled{
    background-color:rgba(57, 75, 89, 0.5);
    background-image:none;
    -webkit-box-shadow:none;
            box-shadow:none;
    color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-html-select select:disabled.bp3-active, .bp3-dark .bp3-select select:disabled.bp3-active, .bp3-dark .bp3-html-select select.bp3-disabled.bp3-active, .bp3-dark .bp3-select select.bp3-disabled.bp3-active{
      background:rgba(57, 75, 89, 0.7); }
  .bp3-dark .bp3-html-select select .bp3-button-spinner .bp3-spinner-head, .bp3-dark .bp3-select select .bp3-button-spinner .bp3-spinner-head{
    background:rgba(16, 22, 26, 0.5);
    stroke:#8a9ba8; }

.bp3-html-select select:disabled,
.bp3-select select:disabled{
  background-color:rgba(206, 217, 224, 0.5);
  -webkit-box-shadow:none;
          box-shadow:none;
  color:rgba(92, 112, 128, 0.6);
  cursor:not-allowed; }

.bp3-html-select .bp3-icon,
.bp3-select .bp3-icon, .bp3-select::after{
  color:#5c7080;
  pointer-events:none;
  position:absolute;
  right:7px;
  top:7px; }
  .bp3-html-select .bp3-disabled.bp3-icon,
  .bp3-select .bp3-disabled.bp3-icon, .bp3-disabled.bp3-select::after{
    color:rgba(92, 112, 128, 0.6); }
.bp3-html-select,
.bp3-select{
  display:inline-block;
  letter-spacing:normal;
  position:relative;
  vertical-align:middle; }
  .bp3-html-select select::-ms-expand,
  .bp3-select select::-ms-expand{
    display:none; }
  .bp3-html-select .bp3-icon,
  .bp3-select .bp3-icon{
    color:#5c7080; }
    .bp3-html-select .bp3-icon:hover,
    .bp3-select .bp3-icon:hover{
      color:#182026; }
    .bp3-dark .bp3-html-select .bp3-icon, .bp3-dark
    .bp3-select .bp3-icon{
      color:#a7b6c2; }
      .bp3-dark .bp3-html-select .bp3-icon:hover, .bp3-dark
      .bp3-select .bp3-icon:hover{
        color:#f5f8fa; }
  .bp3-html-select.bp3-large::after,
  .bp3-html-select.bp3-large .bp3-icon,
  .bp3-select.bp3-large::after,
  .bp3-select.bp3-large .bp3-icon{
    right:12px;
    top:12px; }
  .bp3-html-select.bp3-fill,
  .bp3-html-select.bp3-fill select,
  .bp3-select.bp3-fill,
  .bp3-select.bp3-fill select{
    width:100%; }
  .bp3-dark .bp3-html-select option, .bp3-dark
  .bp3-select option{
    background-color:#30404d;
    color:#f5f8fa; }
  .bp3-dark .bp3-html-select option:disabled, .bp3-dark
  .bp3-select option:disabled{
    color:rgba(167, 182, 194, 0.6); }
  .bp3-dark .bp3-html-select::after, .bp3-dark
  .bp3-select::after{
    color:#a7b6c2; }

.bp3-select::after{
  font-family:"Icons16", sans-serif;
  font-size:16px;
  font-style:normal;
  font-weight:400;
  line-height:1;
  -moz-osx-font-smoothing:grayscale;
  -webkit-font-smoothing:antialiased;
  content:""; }
.bp3-running-text table, table.bp3-html-table{
  border-spacing:0;
  font-size:14px; }
  .bp3-running-text table th, table.bp3-html-table th,
  .bp3-running-text table td,
  table.bp3-html-table td{
    padding:11px;
    text-align:left;
    vertical-align:top; }
  .bp3-running-text table th, table.bp3-html-table th{
    color:#182026;
    font-weight:600; }
  
  .bp3-running-text table td,
  table.bp3-html-table td{
    color:#182026; }
  .bp3-running-text table tbody tr:first-child th, table.bp3-html-table tbody tr:first-child th,
  .bp3-running-text table tbody tr:first-child td,
  table.bp3-html-table tbody tr:first-child td{
    -webkit-box-shadow:inset 0 1px 0 0 rgba(16, 22, 26, 0.15);
            box-shadow:inset 0 1px 0 0 rgba(16, 22, 26, 0.15); }
  .bp3-dark .bp3-running-text table th, .bp3-running-text .bp3-dark table th, .bp3-dark table.bp3-html-table th{
    color:#f5f8fa; }
  .bp3-dark .bp3-running-text table td, .bp3-running-text .bp3-dark table td, .bp3-dark table.bp3-html-table td{
    color:#f5f8fa; }
  .bp3-dark .bp3-running-text table tbody tr:first-child th, .bp3-running-text .bp3-dark table tbody tr:first-child th, .bp3-dark table.bp3-html-table tbody tr:first-child th,
  .bp3-dark .bp3-running-text table tbody tr:first-child td,
  .bp3-running-text .bp3-dark table tbody tr:first-child td,
  .bp3-dark table.bp3-html-table tbody tr:first-child td{
    -webkit-box-shadow:inset 0 1px 0 0 rgba(255, 255, 255, 0.15);
            box-shadow:inset 0 1px 0 0 rgba(255, 255, 255, 0.15); }

table.bp3-html-table.bp3-html-table-condensed th,
table.bp3-html-table.bp3-html-table-condensed td, table.bp3-html-table.bp3-small th,
table.bp3-html-table.bp3-small td{
  padding-bottom:6px;
  padding-top:6px; }

table.bp3-html-table.bp3-html-table-striped tbody tr:nth-child(odd) td{
  background:rgba(191, 204, 214, 0.15); }

table.bp3-html-table.bp3-html-table-bordered th:not(:first-child){
  -webkit-box-shadow:inset 1px 0 0 0 rgba(16, 22, 26, 0.15);
          box-shadow:inset 1px 0 0 0 rgba(16, 22, 26, 0.15); }

table.bp3-html-table.bp3-html-table-bordered tbody tr td{
  -webkit-box-shadow:inset 0 1px 0 0 rgba(16, 22, 26, 0.15);
          box-shadow:inset 0 1px 0 0 rgba(16, 22, 26, 0.15); }
  table.bp3-html-table.bp3-html-table-bordered tbody tr td:not(:first-child){
    -webkit-box-shadow:inset 1px 1px 0 0 rgba(16, 22, 26, 0.15);
            box-shadow:inset 1px 1px 0 0 rgba(16, 22, 26, 0.15); }

table.bp3-html-table.bp3-html-table-bordered.bp3-html-table-striped tbody tr:not(:first-child) td{
  -webkit-box-shadow:none;
          box-shadow:none; }
  table.bp3-html-table.bp3-html-table-bordered.bp3-html-table-striped tbody tr:not(:first-child) td:not(:first-child){
    -webkit-box-shadow:inset 1px 0 0 0 rgba(16, 22, 26, 0.15);
            box-shadow:inset 1px 0 0 0 rgba(16, 22, 26, 0.15); }

table.bp3-html-table.bp3-interactive tbody tr:hover td{
  background-color:rgba(191, 204, 214, 0.3);
  cursor:pointer; }

table.bp3-html-table.bp3-interactive tbody tr:active td{
  background-color:rgba(191, 204, 214, 0.4); }

.bp3-dark table.bp3-html-table{ }
  .bp3-dark table.bp3-html-table.bp3-html-table-striped tbody tr:nth-child(odd) td{
    background:rgba(92, 112, 128, 0.15); }
  .bp3-dark table.bp3-html-table.bp3-html-table-bordered th:not(:first-child){
    -webkit-box-shadow:inset 1px 0 0 0 rgba(255, 255, 255, 0.15);
            box-shadow:inset 1px 0 0 0 rgba(255, 255, 255, 0.15); }
  .bp3-dark table.bp3-html-table.bp3-html-table-bordered tbody tr td{
    -webkit-box-shadow:inset 0 1px 0 0 rgba(255, 255, 255, 0.15);
            box-shadow:inset 0 1px 0 0 rgba(255, 255, 255, 0.15); }
    .bp3-dark table.bp3-html-table.bp3-html-table-bordered tbody tr td:not(:first-child){
      -webkit-box-shadow:inset 1px 1px 0 0 rgba(255, 255, 255, 0.15);
              box-shadow:inset 1px 1px 0 0 rgba(255, 255, 255, 0.15); }
  .bp3-dark table.bp3-html-table.bp3-html-table-bordered.bp3-html-table-striped tbody tr:not(:first-child) td{
    -webkit-box-shadow:inset 1px 0 0 0 rgba(255, 255, 255, 0.15);
            box-shadow:inset 1px 0 0 0 rgba(255, 255, 255, 0.15); }
    .bp3-dark table.bp3-html-table.bp3-html-table-bordered.bp3-html-table-striped tbody tr:not(:first-child) td:first-child{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-dark table.bp3-html-table.bp3-interactive tbody tr:hover td{
    background-color:rgba(92, 112, 128, 0.3);
    cursor:pointer; }
  .bp3-dark table.bp3-html-table.bp3-interactive tbody tr:active td{
    background-color:rgba(92, 112, 128, 0.4); }

.bp3-key-combo{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center; }
  .bp3-key-combo > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-key-combo > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-key-combo::before,
  .bp3-key-combo > *{
    margin-right:5px; }
  .bp3-key-combo:empty::before,
  .bp3-key-combo > :last-child{
    margin-right:0; }

.bp3-hotkey-dialog{
  padding-bottom:0;
  top:40px; }
  .bp3-hotkey-dialog .bp3-dialog-body{
    margin:0;
    padding:0; }
  .bp3-hotkey-dialog .bp3-hotkey-label{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1; }

.bp3-hotkey-column{
  margin:auto;
  max-height:80vh;
  overflow-y:auto;
  padding:30px; }
  .bp3-hotkey-column .bp3-heading{
    margin-bottom:20px; }
    .bp3-hotkey-column .bp3-heading:not(:first-child){
      margin-top:40px; }

.bp3-hotkey{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-pack:justify;
      -ms-flex-pack:justify;
          justify-content:space-between;
  margin-left:0;
  margin-right:0; }
  .bp3-hotkey:not(:last-child){
    margin-bottom:10px; }
.bp3-icon{
  display:inline-block;
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  vertical-align:text-bottom; }
  .bp3-icon:not(:empty)::before{
    content:"" !important;
    content:unset !important; }
  .bp3-icon > svg{
    display:block; }
    .bp3-icon > svg:not([fill]){
      fill:currentColor; }

.bp3-icon.bp3-intent-primary, .bp3-icon-standard.bp3-intent-primary, .bp3-icon-large.bp3-intent-primary{
  color:#106ba3; }
  .bp3-dark .bp3-icon.bp3-intent-primary, .bp3-dark .bp3-icon-standard.bp3-intent-primary, .bp3-dark .bp3-icon-large.bp3-intent-primary{
    color:#48aff0; }

.bp3-icon.bp3-intent-success, .bp3-icon-standard.bp3-intent-success, .bp3-icon-large.bp3-intent-success{
  color:#0d8050; }
  .bp3-dark .bp3-icon.bp3-intent-success, .bp3-dark .bp3-icon-standard.bp3-intent-success, .bp3-dark .bp3-icon-large.bp3-intent-success{
    color:#3dcc91; }

.bp3-icon.bp3-intent-warning, .bp3-icon-standard.bp3-intent-warning, .bp3-icon-large.bp3-intent-warning{
  color:#bf7326; }
  .bp3-dark .bp3-icon.bp3-intent-warning, .bp3-dark .bp3-icon-standard.bp3-intent-warning, .bp3-dark .bp3-icon-large.bp3-intent-warning{
    color:#ffb366; }

.bp3-icon.bp3-intent-danger, .bp3-icon-standard.bp3-intent-danger, .bp3-icon-large.bp3-intent-danger{
  color:#c23030; }
  .bp3-dark .bp3-icon.bp3-intent-danger, .bp3-dark .bp3-icon-standard.bp3-intent-danger, .bp3-dark .bp3-icon-large.bp3-intent-danger{
    color:#ff7373; }

span.bp3-icon-standard{
  font-family:"Icons16", sans-serif;
  font-size:16px;
  font-style:normal;
  font-weight:400;
  line-height:1;
  -moz-osx-font-smoothing:grayscale;
  -webkit-font-smoothing:antialiased;
  display:inline-block; }

span.bp3-icon-large{
  font-family:"Icons20", sans-serif;
  font-size:20px;
  font-style:normal;
  font-weight:400;
  line-height:1;
  -moz-osx-font-smoothing:grayscale;
  -webkit-font-smoothing:antialiased;
  display:inline-block; }

span.bp3-icon:empty{
  font-family:"Icons20";
  font-size:inherit;
  font-style:normal;
  font-weight:400;
  line-height:1; }
  span.bp3-icon:empty::before{
    -moz-osx-font-smoothing:grayscale;
    -webkit-font-smoothing:antialiased; }

.bp3-icon-add::before{
  content:""; }

.bp3-icon-add-column-left::before{
  content:""; }

.bp3-icon-add-column-right::before{
  content:""; }

.bp3-icon-add-row-bottom::before{
  content:""; }

.bp3-icon-add-row-top::before{
  content:""; }

.bp3-icon-add-to-artifact::before{
  content:""; }

.bp3-icon-add-to-folder::before{
  content:""; }

.bp3-icon-airplane::before{
  content:""; }

.bp3-icon-align-center::before{
  content:""; }

.bp3-icon-align-justify::before{
  content:""; }

.bp3-icon-align-left::before{
  content:""; }

.bp3-icon-align-right::before{
  content:""; }

.bp3-icon-alignment-bottom::before{
  content:""; }

.bp3-icon-alignment-horizontal-center::before{
  content:""; }

.bp3-icon-alignment-left::before{
  content:""; }

.bp3-icon-alignment-right::before{
  content:""; }

.bp3-icon-alignment-top::before{
  content:""; }

.bp3-icon-alignment-vertical-center::before{
  content:""; }

.bp3-icon-annotation::before{
  content:""; }

.bp3-icon-application::before{
  content:""; }

.bp3-icon-applications::before{
  content:""; }

.bp3-icon-archive::before{
  content:""; }

.bp3-icon-arrow-bottom-left::before{
  content:"↙"; }

.bp3-icon-arrow-bottom-right::before{
  content:"↘"; }

.bp3-icon-arrow-down::before{
  content:"↓"; }

.bp3-icon-arrow-left::before{
  content:"←"; }

.bp3-icon-arrow-right::before{
  content:"→"; }

.bp3-icon-arrow-top-left::before{
  content:"↖"; }

.bp3-icon-arrow-top-right::before{
  content:"↗"; }

.bp3-icon-arrow-up::before{
  content:"↑"; }

.bp3-icon-arrows-horizontal::before{
  content:"↔"; }

.bp3-icon-arrows-vertical::before{
  content:"↕"; }

.bp3-icon-asterisk::before{
  content:"*"; }

.bp3-icon-automatic-updates::before{
  content:""; }

.bp3-icon-badge::before{
  content:""; }

.bp3-icon-ban-circle::before{
  content:""; }

.bp3-icon-bank-account::before{
  content:""; }

.bp3-icon-barcode::before{
  content:""; }

.bp3-icon-blank::before{
  content:""; }

.bp3-icon-blocked-person::before{
  content:""; }

.bp3-icon-bold::before{
  content:""; }

.bp3-icon-book::before{
  content:""; }

.bp3-icon-bookmark::before{
  content:""; }

.bp3-icon-box::before{
  content:""; }

.bp3-icon-briefcase::before{
  content:""; }

.bp3-icon-bring-data::before{
  content:""; }

.bp3-icon-build::before{
  content:""; }

.bp3-icon-calculator::before{
  content:""; }

.bp3-icon-calendar::before{
  content:""; }

.bp3-icon-camera::before{
  content:""; }

.bp3-icon-caret-down::before{
  content:"⌄"; }

.bp3-icon-caret-left::before{
  content:"〈"; }

.bp3-icon-caret-right::before{
  content:"〉"; }

.bp3-icon-caret-up::before{
  content:"⌃"; }

.bp3-icon-cell-tower::before{
  content:""; }

.bp3-icon-changes::before{
  content:""; }

.bp3-icon-chart::before{
  content:""; }

.bp3-icon-chat::before{
  content:""; }

.bp3-icon-chevron-backward::before{
  content:""; }

.bp3-icon-chevron-down::before{
  content:""; }

.bp3-icon-chevron-forward::before{
  content:""; }

.bp3-icon-chevron-left::before{
  content:""; }

.bp3-icon-chevron-right::before{
  content:""; }

.bp3-icon-chevron-up::before{
  content:""; }

.bp3-icon-circle::before{
  content:""; }

.bp3-icon-circle-arrow-down::before{
  content:""; }

.bp3-icon-circle-arrow-left::before{
  content:""; }

.bp3-icon-circle-arrow-right::before{
  content:""; }

.bp3-icon-circle-arrow-up::before{
  content:""; }

.bp3-icon-citation::before{
  content:""; }

.bp3-icon-clean::before{
  content:""; }

.bp3-icon-clipboard::before{
  content:""; }

.bp3-icon-cloud::before{
  content:"☁"; }

.bp3-icon-cloud-download::before{
  content:""; }

.bp3-icon-cloud-upload::before{
  content:""; }

.bp3-icon-code::before{
  content:""; }

.bp3-icon-code-block::before{
  content:""; }

.bp3-icon-cog::before{
  content:""; }

.bp3-icon-collapse-all::before{
  content:""; }

.bp3-icon-column-layout::before{
  content:""; }

.bp3-icon-comment::before{
  content:""; }

.bp3-icon-comparison::before{
  content:""; }

.bp3-icon-compass::before{
  content:""; }

.bp3-icon-compressed::before{
  content:""; }

.bp3-icon-confirm::before{
  content:""; }

.bp3-icon-console::before{
  content:""; }

.bp3-icon-contrast::before{
  content:""; }

.bp3-icon-control::before{
  content:""; }

.bp3-icon-credit-card::before{
  content:""; }

.bp3-icon-cross::before{
  content:"✗"; }

.bp3-icon-crown::before{
  content:""; }

.bp3-icon-cube::before{
  content:""; }

.bp3-icon-cube-add::before{
  content:""; }

.bp3-icon-cube-remove::before{
  content:""; }

.bp3-icon-curved-range-chart::before{
  content:""; }

.bp3-icon-cut::before{
  content:""; }

.bp3-icon-dashboard::before{
  content:""; }

.bp3-icon-data-lineage::before{
  content:""; }

.bp3-icon-database::before{
  content:""; }

.bp3-icon-delete::before{
  content:""; }

.bp3-icon-delta::before{
  content:"Δ"; }

.bp3-icon-derive-column::before{
  content:""; }

.bp3-icon-desktop::before{
  content:""; }

.bp3-icon-diagnosis::before{
  content:""; }

.bp3-icon-diagram-tree::before{
  content:""; }

.bp3-icon-direction-left::before{
  content:""; }

.bp3-icon-direction-right::before{
  content:""; }

.bp3-icon-disable::before{
  content:""; }

.bp3-icon-document::before{
  content:""; }

.bp3-icon-document-open::before{
  content:""; }

.bp3-icon-document-share::before{
  content:""; }

.bp3-icon-dollar::before{
  content:"$"; }

.bp3-icon-dot::before{
  content:"•"; }

.bp3-icon-double-caret-horizontal::before{
  content:""; }

.bp3-icon-double-caret-vertical::before{
  content:""; }

.bp3-icon-double-chevron-down::before{
  content:""; }

.bp3-icon-double-chevron-left::before{
  content:""; }

.bp3-icon-double-chevron-right::before{
  content:""; }

.bp3-icon-double-chevron-up::before{
  content:""; }

.bp3-icon-doughnut-chart::before{
  content:""; }

.bp3-icon-download::before{
  content:""; }

.bp3-icon-drag-handle-horizontal::before{
  content:""; }

.bp3-icon-drag-handle-vertical::before{
  content:""; }

.bp3-icon-draw::before{
  content:""; }

.bp3-icon-drive-time::before{
  content:""; }

.bp3-icon-duplicate::before{
  content:""; }

.bp3-icon-edit::before{
  content:"✎"; }

.bp3-icon-eject::before{
  content:"⏏"; }

.bp3-icon-endorsed::before{
  content:""; }

.bp3-icon-envelope::before{
  content:"✉"; }

.bp3-icon-equals::before{
  content:""; }

.bp3-icon-eraser::before{
  content:""; }

.bp3-icon-error::before{
  content:""; }

.bp3-icon-euro::before{
  content:"€"; }

.bp3-icon-exchange::before{
  content:""; }

.bp3-icon-exclude-row::before{
  content:""; }

.bp3-icon-expand-all::before{
  content:""; }

.bp3-icon-export::before{
  content:""; }

.bp3-icon-eye-off::before{
  content:""; }

.bp3-icon-eye-on::before{
  content:""; }

.bp3-icon-eye-open::before{
  content:""; }

.bp3-icon-fast-backward::before{
  content:""; }

.bp3-icon-fast-forward::before{
  content:""; }

.bp3-icon-feed::before{
  content:""; }

.bp3-icon-feed-subscribed::before{
  content:""; }

.bp3-icon-film::before{
  content:""; }

.bp3-icon-filter::before{
  content:""; }

.bp3-icon-filter-keep::before{
  content:""; }

.bp3-icon-filter-list::before{
  content:""; }

.bp3-icon-filter-open::before{
  content:""; }

.bp3-icon-filter-remove::before{
  content:""; }

.bp3-icon-flag::before{
  content:"⚑"; }

.bp3-icon-flame::before{
  content:""; }

.bp3-icon-flash::before{
  content:""; }

.bp3-icon-floppy-disk::before{
  content:""; }

.bp3-icon-flow-branch::before{
  content:""; }

.bp3-icon-flow-end::before{
  content:""; }

.bp3-icon-flow-linear::before{
  content:""; }

.bp3-icon-flow-review::before{
  content:""; }

.bp3-icon-flow-review-branch::before{
  content:""; }

.bp3-icon-flows::before{
  content:""; }

.bp3-icon-folder-close::before{
  content:""; }

.bp3-icon-folder-new::before{
  content:""; }

.bp3-icon-folder-open::before{
  content:""; }

.bp3-icon-folder-shared::before{
  content:""; }

.bp3-icon-folder-shared-open::before{
  content:""; }

.bp3-icon-follower::before{
  content:""; }

.bp3-icon-following::before{
  content:""; }

.bp3-icon-font::before{
  content:""; }

.bp3-icon-fork::before{
  content:""; }

.bp3-icon-form::before{
  content:""; }

.bp3-icon-full-circle::before{
  content:""; }

.bp3-icon-full-stacked-chart::before{
  content:""; }

.bp3-icon-fullscreen::before{
  content:""; }

.bp3-icon-function::before{
  content:""; }

.bp3-icon-gantt-chart::before{
  content:""; }

.bp3-icon-geolocation::before{
  content:""; }

.bp3-icon-geosearch::before{
  content:""; }

.bp3-icon-git-branch::before{
  content:""; }

.bp3-icon-git-commit::before{
  content:""; }

.bp3-icon-git-merge::before{
  content:""; }

.bp3-icon-git-new-branch::before{
  content:""; }

.bp3-icon-git-pull::before{
  content:""; }

.bp3-icon-git-push::before{
  content:""; }

.bp3-icon-git-repo::before{
  content:""; }

.bp3-icon-glass::before{
  content:""; }

.bp3-icon-globe::before{
  content:""; }

.bp3-icon-globe-network::before{
  content:""; }

.bp3-icon-graph::before{
  content:""; }

.bp3-icon-graph-remove::before{
  content:""; }

.bp3-icon-greater-than::before{
  content:""; }

.bp3-icon-greater-than-or-equal-to::before{
  content:""; }

.bp3-icon-grid::before{
  content:""; }

.bp3-icon-grid-view::before{
  content:""; }

.bp3-icon-group-objects::before{
  content:""; }

.bp3-icon-grouped-bar-chart::before{
  content:""; }

.bp3-icon-hand::before{
  content:""; }

.bp3-icon-hand-down::before{
  content:""; }

.bp3-icon-hand-left::before{
  content:""; }

.bp3-icon-hand-right::before{
  content:""; }

.bp3-icon-hand-up::before{
  content:""; }

.bp3-icon-header::before{
  content:""; }

.bp3-icon-header-one::before{
  content:""; }

.bp3-icon-header-two::before{
  content:""; }

.bp3-icon-headset::before{
  content:""; }

.bp3-icon-heart::before{
  content:"♥"; }

.bp3-icon-heart-broken::before{
  content:""; }

.bp3-icon-heat-grid::before{
  content:""; }

.bp3-icon-heatmap::before{
  content:""; }

.bp3-icon-help::before{
  content:"?"; }

.bp3-icon-helper-management::before{
  content:""; }

.bp3-icon-highlight::before{
  content:""; }

.bp3-icon-history::before{
  content:""; }

.bp3-icon-home::before{
  content:"⌂"; }

.bp3-icon-horizontal-bar-chart::before{
  content:""; }

.bp3-icon-horizontal-bar-chart-asc::before{
  content:""; }

.bp3-icon-horizontal-bar-chart-desc::before{
  content:""; }

.bp3-icon-horizontal-distribution::before{
  content:""; }

.bp3-icon-id-number::before{
  content:""; }

.bp3-icon-image-rotate-left::before{
  content:""; }

.bp3-icon-image-rotate-right::before{
  content:""; }

.bp3-icon-import::before{
  content:""; }

.bp3-icon-inbox::before{
  content:""; }

.bp3-icon-inbox-filtered::before{
  content:""; }

.bp3-icon-inbox-geo::before{
  content:""; }

.bp3-icon-inbox-search::before{
  content:""; }

.bp3-icon-inbox-update::before{
  content:""; }

.bp3-icon-info-sign::before{
  content:"ℹ"; }

.bp3-icon-inheritance::before{
  content:""; }

.bp3-icon-inner-join::before{
  content:""; }

.bp3-icon-insert::before{
  content:""; }

.bp3-icon-intersection::before{
  content:""; }

.bp3-icon-ip-address::before{
  content:""; }

.bp3-icon-issue::before{
  content:""; }

.bp3-icon-issue-closed::before{
  content:""; }

.bp3-icon-issue-new::before{
  content:""; }

.bp3-icon-italic::before{
  content:""; }

.bp3-icon-join-table::before{
  content:""; }

.bp3-icon-key::before{
  content:""; }

.bp3-icon-key-backspace::before{
  content:""; }

.bp3-icon-key-command::before{
  content:""; }

.bp3-icon-key-control::before{
  content:""; }

.bp3-icon-key-delete::before{
  content:""; }

.bp3-icon-key-enter::before{
  content:""; }

.bp3-icon-key-escape::before{
  content:""; }

.bp3-icon-key-option::before{
  content:""; }

.bp3-icon-key-shift::before{
  content:""; }

.bp3-icon-key-tab::before{
  content:""; }

.bp3-icon-known-vehicle::before{
  content:""; }

.bp3-icon-lab-test::before{
  content:""; }

.bp3-icon-label::before{
  content:""; }

.bp3-icon-layer::before{
  content:""; }

.bp3-icon-layers::before{
  content:""; }

.bp3-icon-layout::before{
  content:""; }

.bp3-icon-layout-auto::before{
  content:""; }

.bp3-icon-layout-balloon::before{
  content:""; }

.bp3-icon-layout-circle::before{
  content:""; }

.bp3-icon-layout-grid::before{
  content:""; }

.bp3-icon-layout-group-by::before{
  content:""; }

.bp3-icon-layout-hierarchy::before{
  content:""; }

.bp3-icon-layout-linear::before{
  content:""; }

.bp3-icon-layout-skew-grid::before{
  content:""; }

.bp3-icon-layout-sorted-clusters::before{
  content:""; }

.bp3-icon-learning::before{
  content:""; }

.bp3-icon-left-join::before{
  content:""; }

.bp3-icon-less-than::before{
  content:""; }

.bp3-icon-less-than-or-equal-to::before{
  content:""; }

.bp3-icon-lifesaver::before{
  content:""; }

.bp3-icon-lightbulb::before{
  content:""; }

.bp3-icon-link::before{
  content:""; }

.bp3-icon-list::before{
  content:"☰"; }

.bp3-icon-list-columns::before{
  content:""; }

.bp3-icon-list-detail-view::before{
  content:""; }

.bp3-icon-locate::before{
  content:""; }

.bp3-icon-lock::before{
  content:""; }

.bp3-icon-log-in::before{
  content:""; }

.bp3-icon-log-out::before{
  content:""; }

.bp3-icon-manual::before{
  content:""; }

.bp3-icon-manually-entered-data::before{
  content:""; }

.bp3-icon-map::before{
  content:""; }

.bp3-icon-map-create::before{
  content:""; }

.bp3-icon-map-marker::before{
  content:""; }

.bp3-icon-maximize::before{
  content:""; }

.bp3-icon-media::before{
  content:""; }

.bp3-icon-menu::before{
  content:""; }

.bp3-icon-menu-closed::before{
  content:""; }

.bp3-icon-menu-open::before{
  content:""; }

.bp3-icon-merge-columns::before{
  content:""; }

.bp3-icon-merge-links::before{
  content:""; }

.bp3-icon-minimize::before{
  content:""; }

.bp3-icon-minus::before{
  content:"−"; }

.bp3-icon-mobile-phone::before{
  content:""; }

.bp3-icon-mobile-video::before{
  content:""; }

.bp3-icon-moon::before{
  content:""; }

.bp3-icon-more::before{
  content:""; }

.bp3-icon-mountain::before{
  content:""; }

.bp3-icon-move::before{
  content:""; }

.bp3-icon-mugshot::before{
  content:""; }

.bp3-icon-multi-select::before{
  content:""; }

.bp3-icon-music::before{
  content:""; }

.bp3-icon-new-drawing::before{
  content:""; }

.bp3-icon-new-grid-item::before{
  content:""; }

.bp3-icon-new-layer::before{
  content:""; }

.bp3-icon-new-layers::before{
  content:""; }

.bp3-icon-new-link::before{
  content:""; }

.bp3-icon-new-object::before{
  content:""; }

.bp3-icon-new-person::before{
  content:""; }

.bp3-icon-new-prescription::before{
  content:""; }

.bp3-icon-new-text-box::before{
  content:""; }

.bp3-icon-ninja::before{
  content:""; }

.bp3-icon-not-equal-to::before{
  content:""; }

.bp3-icon-notifications::before{
  content:""; }

.bp3-icon-notifications-updated::before{
  content:""; }

.bp3-icon-numbered-list::before{
  content:""; }

.bp3-icon-numerical::before{
  content:""; }

.bp3-icon-office::before{
  content:""; }

.bp3-icon-offline::before{
  content:""; }

.bp3-icon-oil-field::before{
  content:""; }

.bp3-icon-one-column::before{
  content:""; }

.bp3-icon-outdated::before{
  content:""; }

.bp3-icon-page-layout::before{
  content:""; }

.bp3-icon-panel-stats::before{
  content:""; }

.bp3-icon-panel-table::before{
  content:""; }

.bp3-icon-paperclip::before{
  content:""; }

.bp3-icon-paragraph::before{
  content:""; }

.bp3-icon-path::before{
  content:""; }

.bp3-icon-path-search::before{
  content:""; }

.bp3-icon-pause::before{
  content:""; }

.bp3-icon-people::before{
  content:""; }

.bp3-icon-percentage::before{
  content:""; }

.bp3-icon-person::before{
  content:""; }

.bp3-icon-phone::before{
  content:"☎"; }

.bp3-icon-pie-chart::before{
  content:""; }

.bp3-icon-pin::before{
  content:""; }

.bp3-icon-pivot::before{
  content:""; }

.bp3-icon-pivot-table::before{
  content:""; }

.bp3-icon-play::before{
  content:""; }

.bp3-icon-plus::before{
  content:"+"; }

.bp3-icon-polygon-filter::before{
  content:""; }

.bp3-icon-power::before{
  content:""; }

.bp3-icon-predictive-analysis::before{
  content:""; }

.bp3-icon-prescription::before{
  content:""; }

.bp3-icon-presentation::before{
  content:""; }

.bp3-icon-print::before{
  content:"⎙"; }

.bp3-icon-projects::before{
  content:""; }

.bp3-icon-properties::before{
  content:""; }

.bp3-icon-property::before{
  content:""; }

.bp3-icon-publish-function::before{
  content:""; }

.bp3-icon-pulse::before{
  content:""; }

.bp3-icon-random::before{
  content:""; }

.bp3-icon-record::before{
  content:""; }

.bp3-icon-redo::before{
  content:""; }

.bp3-icon-refresh::before{
  content:""; }

.bp3-icon-regression-chart::before{
  content:""; }

.bp3-icon-remove::before{
  content:""; }

.bp3-icon-remove-column::before{
  content:""; }

.bp3-icon-remove-column-left::before{
  content:""; }

.bp3-icon-remove-column-right::before{
  content:""; }

.bp3-icon-remove-row-bottom::before{
  content:""; }

.bp3-icon-remove-row-top::before{
  content:""; }

.bp3-icon-repeat::before{
  content:""; }

.bp3-icon-reset::before{
  content:""; }

.bp3-icon-resolve::before{
  content:""; }

.bp3-icon-rig::before{
  content:""; }

.bp3-icon-right-join::before{
  content:""; }

.bp3-icon-ring::before{
  content:""; }

.bp3-icon-rotate-document::before{
  content:""; }

.bp3-icon-rotate-page::before{
  content:""; }

.bp3-icon-satellite::before{
  content:""; }

.bp3-icon-saved::before{
  content:""; }

.bp3-icon-scatter-plot::before{
  content:""; }

.bp3-icon-search::before{
  content:""; }

.bp3-icon-search-around::before{
  content:""; }

.bp3-icon-search-template::before{
  content:""; }

.bp3-icon-search-text::before{
  content:""; }

.bp3-icon-segmented-control::before{
  content:""; }

.bp3-icon-select::before{
  content:""; }

.bp3-icon-selection::before{
  content:"⦿"; }

.bp3-icon-send-to::before{
  content:""; }

.bp3-icon-send-to-graph::before{
  content:""; }

.bp3-icon-send-to-map::before{
  content:""; }

.bp3-icon-series-add::before{
  content:""; }

.bp3-icon-series-configuration::before{
  content:""; }

.bp3-icon-series-derived::before{
  content:""; }

.bp3-icon-series-filtered::before{
  content:""; }

.bp3-icon-series-search::before{
  content:""; }

.bp3-icon-settings::before{
  content:""; }

.bp3-icon-share::before{
  content:""; }

.bp3-icon-shield::before{
  content:""; }

.bp3-icon-shop::before{
  content:""; }

.bp3-icon-shopping-cart::before{
  content:""; }

.bp3-icon-signal-search::before{
  content:""; }

.bp3-icon-sim-card::before{
  content:""; }

.bp3-icon-slash::before{
  content:""; }

.bp3-icon-small-cross::before{
  content:""; }

.bp3-icon-small-minus::before{
  content:""; }

.bp3-icon-small-plus::before{
  content:""; }

.bp3-icon-small-tick::before{
  content:""; }

.bp3-icon-snowflake::before{
  content:""; }

.bp3-icon-social-media::before{
  content:""; }

.bp3-icon-sort::before{
  content:""; }

.bp3-icon-sort-alphabetical::before{
  content:""; }

.bp3-icon-sort-alphabetical-desc::before{
  content:""; }

.bp3-icon-sort-asc::before{
  content:""; }

.bp3-icon-sort-desc::before{
  content:""; }

.bp3-icon-sort-numerical::before{
  content:""; }

.bp3-icon-sort-numerical-desc::before{
  content:""; }

.bp3-icon-split-columns::before{
  content:""; }

.bp3-icon-square::before{
  content:""; }

.bp3-icon-stacked-chart::before{
  content:""; }

.bp3-icon-star::before{
  content:"★"; }

.bp3-icon-star-empty::before{
  content:"☆"; }

.bp3-icon-step-backward::before{
  content:""; }

.bp3-icon-step-chart::before{
  content:""; }

.bp3-icon-step-forward::before{
  content:""; }

.bp3-icon-stop::before{
  content:""; }

.bp3-icon-stopwatch::before{
  content:""; }

.bp3-icon-strikethrough::before{
  content:""; }

.bp3-icon-style::before{
  content:""; }

.bp3-icon-swap-horizontal::before{
  content:""; }

.bp3-icon-swap-vertical::before{
  content:""; }

.bp3-icon-symbol-circle::before{
  content:""; }

.bp3-icon-symbol-cross::before{
  content:""; }

.bp3-icon-symbol-diamond::before{
  content:""; }

.bp3-icon-symbol-square::before{
  content:""; }

.bp3-icon-symbol-triangle-down::before{
  content:""; }

.bp3-icon-symbol-triangle-up::before{
  content:""; }

.bp3-icon-tag::before{
  content:""; }

.bp3-icon-take-action::before{
  content:""; }

.bp3-icon-taxi::before{
  content:""; }

.bp3-icon-text-highlight::before{
  content:""; }

.bp3-icon-th::before{
  content:""; }

.bp3-icon-th-derived::before{
  content:""; }

.bp3-icon-th-disconnect::before{
  content:""; }

.bp3-icon-th-filtered::before{
  content:""; }

.bp3-icon-th-list::before{
  content:""; }

.bp3-icon-thumbs-down::before{
  content:""; }

.bp3-icon-thumbs-up::before{
  content:""; }

.bp3-icon-tick::before{
  content:"✓"; }

.bp3-icon-tick-circle::before{
  content:""; }

.bp3-icon-time::before{
  content:"⏲"; }

.bp3-icon-timeline-area-chart::before{
  content:""; }

.bp3-icon-timeline-bar-chart::before{
  content:""; }

.bp3-icon-timeline-events::before{
  content:""; }

.bp3-icon-timeline-line-chart::before{
  content:""; }

.bp3-icon-tint::before{
  content:""; }

.bp3-icon-torch::before{
  content:""; }

.bp3-icon-tractor::before{
  content:""; }

.bp3-icon-train::before{
  content:""; }

.bp3-icon-translate::before{
  content:""; }

.bp3-icon-trash::before{
  content:""; }

.bp3-icon-tree::before{
  content:""; }

.bp3-icon-trending-down::before{
  content:""; }

.bp3-icon-trending-up::before{
  content:""; }

.bp3-icon-truck::before{
  content:""; }

.bp3-icon-two-columns::before{
  content:""; }

.bp3-icon-unarchive::before{
  content:""; }

.bp3-icon-underline::before{
  content:"⎁"; }

.bp3-icon-undo::before{
  content:"⎌"; }

.bp3-icon-ungroup-objects::before{
  content:""; }

.bp3-icon-unknown-vehicle::before{
  content:""; }

.bp3-icon-unlock::before{
  content:""; }

.bp3-icon-unpin::before{
  content:""; }

.bp3-icon-unresolve::before{
  content:""; }

.bp3-icon-updated::before{
  content:""; }

.bp3-icon-upload::before{
  content:""; }

.bp3-icon-user::before{
  content:""; }

.bp3-icon-variable::before{
  content:""; }

.bp3-icon-vertical-bar-chart-asc::before{
  content:""; }

.bp3-icon-vertical-bar-chart-desc::before{
  content:""; }

.bp3-icon-vertical-distribution::before{
  content:""; }

.bp3-icon-video::before{
  content:""; }

.bp3-icon-volume-down::before{
  content:""; }

.bp3-icon-volume-off::before{
  content:""; }

.bp3-icon-volume-up::before{
  content:""; }

.bp3-icon-walk::before{
  content:""; }

.bp3-icon-warning-sign::before{
  content:""; }

.bp3-icon-waterfall-chart::before{
  content:""; }

.bp3-icon-widget::before{
  content:""; }

.bp3-icon-widget-button::before{
  content:""; }

.bp3-icon-widget-footer::before{
  content:""; }

.bp3-icon-widget-header::before{
  content:""; }

.bp3-icon-wrench::before{
  content:""; }

.bp3-icon-zoom-in::before{
  content:""; }

.bp3-icon-zoom-out::before{
  content:""; }

.bp3-icon-zoom-to-fit::before{
  content:""; }
.bp3-submenu > .bp3-popover-wrapper{
  display:block; }

.bp3-submenu .bp3-popover-target{
  display:block; }
  .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-menu-item{ }

.bp3-submenu.bp3-popover{
  -webkit-box-shadow:none;
          box-shadow:none;
  padding:0 5px; }
  .bp3-submenu.bp3-popover > .bp3-popover-content{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2); }
  .bp3-dark .bp3-submenu.bp3-popover, .bp3-submenu.bp3-popover.bp3-dark{
    -webkit-box-shadow:none;
            box-shadow:none; }
    .bp3-dark .bp3-submenu.bp3-popover > .bp3-popover-content, .bp3-submenu.bp3-popover.bp3-dark > .bp3-popover-content{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }
.bp3-menu{
  background:#ffffff;
  border-radius:3px;
  color:#182026;
  list-style:none;
  margin:0;
  min-width:180px;
  padding:5px;
  text-align:left; }

.bp3-menu-divider{
  border-top:1px solid rgba(16, 22, 26, 0.15);
  display:block;
  margin:5px; }
  .bp3-dark .bp3-menu-divider{
    border-top-color:rgba(255, 255, 255, 0.15); }

.bp3-menu-item{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:start;
      -ms-flex-align:start;
          align-items:flex-start;
  border-radius:2px;
  color:inherit;
  line-height:20px;
  padding:5px 7px;
  text-decoration:none;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-menu-item > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-menu-item > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-menu-item::before,
  .bp3-menu-item > *{
    margin-right:7px; }
  .bp3-menu-item:empty::before,
  .bp3-menu-item > :last-child{
    margin-right:0; }
  .bp3-menu-item > .bp3-fill{
    word-break:break-word; }
  .bp3-menu-item:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-menu-item{
    background-color:rgba(167, 182, 194, 0.3);
    cursor:pointer;
    text-decoration:none; }
  .bp3-menu-item.bp3-disabled{
    background-color:inherit;
    color:rgba(92, 112, 128, 0.6);
    cursor:not-allowed; }
  .bp3-dark .bp3-menu-item{
    color:inherit; }
    .bp3-dark .bp3-menu-item:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-menu-item{
      background-color:rgba(138, 155, 168, 0.15);
      color:inherit; }
    .bp3-dark .bp3-menu-item.bp3-disabled{
      background-color:inherit;
      color:rgba(167, 182, 194, 0.6); }
  .bp3-menu-item.bp3-intent-primary{
    color:#106ba3; }
    .bp3-menu-item.bp3-intent-primary .bp3-icon{
      color:inherit; }
    .bp3-menu-item.bp3-intent-primary::before, .bp3-menu-item.bp3-intent-primary::after,
    .bp3-menu-item.bp3-intent-primary .bp3-menu-item-label{
      color:#106ba3; }
    .bp3-menu-item.bp3-intent-primary:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-menu-item.bp3-intent-primary.bp3-active{
      background-color:#137cbd; }
    .bp3-menu-item.bp3-intent-primary:active{
      background-color:#106ba3; }
    .bp3-menu-item.bp3-intent-primary:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-menu-item.bp3-intent-primary:hover::before, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::before, .bp3-menu-item.bp3-intent-primary:hover::after, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::after,
    .bp3-menu-item.bp3-intent-primary:hover .bp3-menu-item-label,
    .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item .bp3-menu-item-label, .bp3-menu-item.bp3-intent-primary:active, .bp3-menu-item.bp3-intent-primary:active::before, .bp3-menu-item.bp3-intent-primary:active::after,
    .bp3-menu-item.bp3-intent-primary:active .bp3-menu-item-label, .bp3-menu-item.bp3-intent-primary.bp3-active, .bp3-menu-item.bp3-intent-primary.bp3-active::before, .bp3-menu-item.bp3-intent-primary.bp3-active::after,
    .bp3-menu-item.bp3-intent-primary.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-menu-item.bp3-intent-success{
    color:#0d8050; }
    .bp3-menu-item.bp3-intent-success .bp3-icon{
      color:inherit; }
    .bp3-menu-item.bp3-intent-success::before, .bp3-menu-item.bp3-intent-success::after,
    .bp3-menu-item.bp3-intent-success .bp3-menu-item-label{
      color:#0d8050; }
    .bp3-menu-item.bp3-intent-success:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-menu-item.bp3-intent-success.bp3-active{
      background-color:#0f9960; }
    .bp3-menu-item.bp3-intent-success:active{
      background-color:#0d8050; }
    .bp3-menu-item.bp3-intent-success:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-menu-item.bp3-intent-success:hover::before, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::before, .bp3-menu-item.bp3-intent-success:hover::after, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::after,
    .bp3-menu-item.bp3-intent-success:hover .bp3-menu-item-label,
    .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item .bp3-menu-item-label, .bp3-menu-item.bp3-intent-success:active, .bp3-menu-item.bp3-intent-success:active::before, .bp3-menu-item.bp3-intent-success:active::after,
    .bp3-menu-item.bp3-intent-success:active .bp3-menu-item-label, .bp3-menu-item.bp3-intent-success.bp3-active, .bp3-menu-item.bp3-intent-success.bp3-active::before, .bp3-menu-item.bp3-intent-success.bp3-active::after,
    .bp3-menu-item.bp3-intent-success.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-menu-item.bp3-intent-warning{
    color:#bf7326; }
    .bp3-menu-item.bp3-intent-warning .bp3-icon{
      color:inherit; }
    .bp3-menu-item.bp3-intent-warning::before, .bp3-menu-item.bp3-intent-warning::after,
    .bp3-menu-item.bp3-intent-warning .bp3-menu-item-label{
      color:#bf7326; }
    .bp3-menu-item.bp3-intent-warning:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-menu-item.bp3-intent-warning.bp3-active{
      background-color:#d9822b; }
    .bp3-menu-item.bp3-intent-warning:active{
      background-color:#bf7326; }
    .bp3-menu-item.bp3-intent-warning:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-menu-item.bp3-intent-warning:hover::before, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::before, .bp3-menu-item.bp3-intent-warning:hover::after, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::after,
    .bp3-menu-item.bp3-intent-warning:hover .bp3-menu-item-label,
    .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item .bp3-menu-item-label, .bp3-menu-item.bp3-intent-warning:active, .bp3-menu-item.bp3-intent-warning:active::before, .bp3-menu-item.bp3-intent-warning:active::after,
    .bp3-menu-item.bp3-intent-warning:active .bp3-menu-item-label, .bp3-menu-item.bp3-intent-warning.bp3-active, .bp3-menu-item.bp3-intent-warning.bp3-active::before, .bp3-menu-item.bp3-intent-warning.bp3-active::after,
    .bp3-menu-item.bp3-intent-warning.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-menu-item.bp3-intent-danger{
    color:#c23030; }
    .bp3-menu-item.bp3-intent-danger .bp3-icon{
      color:inherit; }
    .bp3-menu-item.bp3-intent-danger::before, .bp3-menu-item.bp3-intent-danger::after,
    .bp3-menu-item.bp3-intent-danger .bp3-menu-item-label{
      color:#c23030; }
    .bp3-menu-item.bp3-intent-danger:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-menu-item.bp3-intent-danger.bp3-active{
      background-color:#db3737; }
    .bp3-menu-item.bp3-intent-danger:active{
      background-color:#c23030; }
    .bp3-menu-item.bp3-intent-danger:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-menu-item.bp3-intent-danger:hover::before, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::before, .bp3-menu-item.bp3-intent-danger:hover::after, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::after,
    .bp3-menu-item.bp3-intent-danger:hover .bp3-menu-item-label,
    .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item .bp3-menu-item-label, .bp3-menu-item.bp3-intent-danger:active, .bp3-menu-item.bp3-intent-danger:active::before, .bp3-menu-item.bp3-intent-danger:active::after,
    .bp3-menu-item.bp3-intent-danger:active .bp3-menu-item-label, .bp3-menu-item.bp3-intent-danger.bp3-active, .bp3-menu-item.bp3-intent-danger.bp3-active::before, .bp3-menu-item.bp3-intent-danger.bp3-active::after,
    .bp3-menu-item.bp3-intent-danger.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-menu-item::before{
    font-family:"Icons16", sans-serif;
    font-size:16px;
    font-style:normal;
    font-weight:400;
    line-height:1;
    -moz-osx-font-smoothing:grayscale;
    -webkit-font-smoothing:antialiased;
    margin-right:7px; }
  .bp3-menu-item::before,
  .bp3-menu-item > .bp3-icon{
    color:#5c7080;
    margin-top:2px; }
  .bp3-menu-item .bp3-menu-item-label{
    color:#5c7080; }
  .bp3-menu-item:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-menu-item{
    color:inherit; }
  .bp3-menu-item.bp3-active, .bp3-menu-item:active{
    background-color:rgba(115, 134, 148, 0.3); }
  .bp3-menu-item.bp3-disabled{
    background-color:inherit !important;
    color:rgba(92, 112, 128, 0.6) !important;
    cursor:not-allowed !important;
    outline:none !important; }
    .bp3-menu-item.bp3-disabled::before,
    .bp3-menu-item.bp3-disabled > .bp3-icon,
    .bp3-menu-item.bp3-disabled .bp3-menu-item-label{
      color:rgba(92, 112, 128, 0.6) !important; }
  .bp3-large .bp3-menu-item{
    font-size:16px;
    line-height:22px;
    padding:9px 7px; }
    .bp3-large .bp3-menu-item .bp3-icon{
      margin-top:3px; }
    .bp3-large .bp3-menu-item::before{
      font-family:"Icons20", sans-serif;
      font-size:20px;
      font-style:normal;
      font-weight:400;
      line-height:1;
      -moz-osx-font-smoothing:grayscale;
      -webkit-font-smoothing:antialiased;
      margin-right:10px;
      margin-top:1px; }

button.bp3-menu-item{
  background:none;
  border:none;
  text-align:left;
  width:100%; }
.bp3-menu-header{
  border-top:1px solid rgba(16, 22, 26, 0.15);
  display:block;
  margin:5px;
  cursor:default;
  padding-left:2px; }
  .bp3-dark .bp3-menu-header{
    border-top-color:rgba(255, 255, 255, 0.15); }
  .bp3-menu-header:first-of-type{
    border-top:none; }
  .bp3-menu-header > h6{
    color:#182026;
    font-weight:600;
    overflow:hidden;
    text-overflow:ellipsis;
    white-space:nowrap;
    word-wrap:normal;
    line-height:17px;
    margin:0;
    padding:10px 7px 0 1px; }
    .bp3-dark .bp3-menu-header > h6{
      color:#f5f8fa; }
  .bp3-menu-header:first-of-type > h6{
    padding-top:0; }
  .bp3-large .bp3-menu-header > h6{
    font-size:18px;
    padding-bottom:5px;
    padding-top:15px; }
  .bp3-large .bp3-menu-header:first-of-type > h6{
    padding-top:0; }

.bp3-dark .bp3-menu{
  background:#30404d;
  color:#f5f8fa; }

.bp3-dark .bp3-menu-item{ }
  .bp3-dark .bp3-menu-item.bp3-intent-primary{
    color:#48aff0; }
    .bp3-dark .bp3-menu-item.bp3-intent-primary .bp3-icon{
      color:inherit; }
    .bp3-dark .bp3-menu-item.bp3-intent-primary::before, .bp3-dark .bp3-menu-item.bp3-intent-primary::after,
    .bp3-dark .bp3-menu-item.bp3-intent-primary .bp3-menu-item-label{
      color:#48aff0; }
    .bp3-dark .bp3-menu-item.bp3-intent-primary:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-primary.bp3-active{
      background-color:#137cbd; }
    .bp3-dark .bp3-menu-item.bp3-intent-primary:active{
      background-color:#106ba3; }
    .bp3-dark .bp3-menu-item.bp3-intent-primary:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-primary:hover::before, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::before, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::before, .bp3-dark .bp3-menu-item.bp3-intent-primary:hover::after, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::after, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::after,
    .bp3-dark .bp3-menu-item.bp3-intent-primary:hover .bp3-menu-item-label,
    .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item .bp3-menu-item-label,
    .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-primary:active, .bp3-dark .bp3-menu-item.bp3-intent-primary:active::before, .bp3-dark .bp3-menu-item.bp3-intent-primary:active::after,
    .bp3-dark .bp3-menu-item.bp3-intent-primary:active .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-primary.bp3-active, .bp3-dark .bp3-menu-item.bp3-intent-primary.bp3-active::before, .bp3-dark .bp3-menu-item.bp3-intent-primary.bp3-active::after,
    .bp3-dark .bp3-menu-item.bp3-intent-primary.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-dark .bp3-menu-item.bp3-intent-success{
    color:#3dcc91; }
    .bp3-dark .bp3-menu-item.bp3-intent-success .bp3-icon{
      color:inherit; }
    .bp3-dark .bp3-menu-item.bp3-intent-success::before, .bp3-dark .bp3-menu-item.bp3-intent-success::after,
    .bp3-dark .bp3-menu-item.bp3-intent-success .bp3-menu-item-label{
      color:#3dcc91; }
    .bp3-dark .bp3-menu-item.bp3-intent-success:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-success.bp3-active{
      background-color:#0f9960; }
    .bp3-dark .bp3-menu-item.bp3-intent-success:active{
      background-color:#0d8050; }
    .bp3-dark .bp3-menu-item.bp3-intent-success:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-success:hover::before, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::before, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::before, .bp3-dark .bp3-menu-item.bp3-intent-success:hover::after, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::after, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::after,
    .bp3-dark .bp3-menu-item.bp3-intent-success:hover .bp3-menu-item-label,
    .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item .bp3-menu-item-label,
    .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-success:active, .bp3-dark .bp3-menu-item.bp3-intent-success:active::before, .bp3-dark .bp3-menu-item.bp3-intent-success:active::after,
    .bp3-dark .bp3-menu-item.bp3-intent-success:active .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-success.bp3-active, .bp3-dark .bp3-menu-item.bp3-intent-success.bp3-active::before, .bp3-dark .bp3-menu-item.bp3-intent-success.bp3-active::after,
    .bp3-dark .bp3-menu-item.bp3-intent-success.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-dark .bp3-menu-item.bp3-intent-warning{
    color:#ffb366; }
    .bp3-dark .bp3-menu-item.bp3-intent-warning .bp3-icon{
      color:inherit; }
    .bp3-dark .bp3-menu-item.bp3-intent-warning::before, .bp3-dark .bp3-menu-item.bp3-intent-warning::after,
    .bp3-dark .bp3-menu-item.bp3-intent-warning .bp3-menu-item-label{
      color:#ffb366; }
    .bp3-dark .bp3-menu-item.bp3-intent-warning:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-warning.bp3-active{
      background-color:#d9822b; }
    .bp3-dark .bp3-menu-item.bp3-intent-warning:active{
      background-color:#bf7326; }
    .bp3-dark .bp3-menu-item.bp3-intent-warning:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-warning:hover::before, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::before, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::before, .bp3-dark .bp3-menu-item.bp3-intent-warning:hover::after, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::after, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::after,
    .bp3-dark .bp3-menu-item.bp3-intent-warning:hover .bp3-menu-item-label,
    .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item .bp3-menu-item-label,
    .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-warning:active, .bp3-dark .bp3-menu-item.bp3-intent-warning:active::before, .bp3-dark .bp3-menu-item.bp3-intent-warning:active::after,
    .bp3-dark .bp3-menu-item.bp3-intent-warning:active .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-warning.bp3-active, .bp3-dark .bp3-menu-item.bp3-intent-warning.bp3-active::before, .bp3-dark .bp3-menu-item.bp3-intent-warning.bp3-active::after,
    .bp3-dark .bp3-menu-item.bp3-intent-warning.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-dark .bp3-menu-item.bp3-intent-danger{
    color:#ff7373; }
    .bp3-dark .bp3-menu-item.bp3-intent-danger .bp3-icon{
      color:inherit; }
    .bp3-dark .bp3-menu-item.bp3-intent-danger::before, .bp3-dark .bp3-menu-item.bp3-intent-danger::after,
    .bp3-dark .bp3-menu-item.bp3-intent-danger .bp3-menu-item-label{
      color:#ff7373; }
    .bp3-dark .bp3-menu-item.bp3-intent-danger:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-danger.bp3-active{
      background-color:#db3737; }
    .bp3-dark .bp3-menu-item.bp3-intent-danger:active{
      background-color:#c23030; }
    .bp3-dark .bp3-menu-item.bp3-intent-danger:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-danger:hover::before, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::before, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::before, .bp3-dark .bp3-menu-item.bp3-intent-danger:hover::after, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::after, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::after,
    .bp3-dark .bp3-menu-item.bp3-intent-danger:hover .bp3-menu-item-label,
    .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item .bp3-menu-item-label,
    .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-danger:active, .bp3-dark .bp3-menu-item.bp3-intent-danger:active::before, .bp3-dark .bp3-menu-item.bp3-intent-danger:active::after,
    .bp3-dark .bp3-menu-item.bp3-intent-danger:active .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-danger.bp3-active, .bp3-dark .bp3-menu-item.bp3-intent-danger.bp3-active::before, .bp3-dark .bp3-menu-item.bp3-intent-danger.bp3-active::after,
    .bp3-dark .bp3-menu-item.bp3-intent-danger.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-dark .bp3-menu-item::before,
  .bp3-dark .bp3-menu-item > .bp3-icon{
    color:#a7b6c2; }
  .bp3-dark .bp3-menu-item .bp3-menu-item-label{
    color:#a7b6c2; }
  .bp3-dark .bp3-menu-item.bp3-active, .bp3-dark .bp3-menu-item:active{
    background-color:rgba(138, 155, 168, 0.3); }
  .bp3-dark .bp3-menu-item.bp3-disabled{
    color:rgba(167, 182, 194, 0.6) !important; }
    .bp3-dark .bp3-menu-item.bp3-disabled::before,
    .bp3-dark .bp3-menu-item.bp3-disabled > .bp3-icon,
    .bp3-dark .bp3-menu-item.bp3-disabled .bp3-menu-item-label{
      color:rgba(167, 182, 194, 0.6) !important; }

.bp3-dark .bp3-menu-divider,
.bp3-dark .bp3-menu-header{
  border-color:rgba(255, 255, 255, 0.15); }

.bp3-dark .bp3-menu-header > h6{
  color:#f5f8fa; }

.bp3-label .bp3-menu{
  margin-top:5px; }
.bp3-navbar{
  background-color:#ffffff;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
  height:50px;
  padding:0 15px;
  position:relative;
  width:100%;
  z-index:10; }
  .bp3-navbar.bp3-dark,
  .bp3-dark .bp3-navbar{
    background-color:#394b59; }
  .bp3-navbar.bp3-dark{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-navbar{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-navbar.bp3-fixed-top{
    left:0;
    position:fixed;
    right:0;
    top:0; }

.bp3-navbar-heading{
  font-size:16px;
  margin-right:15px; }

.bp3-navbar-group{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  height:50px; }
  .bp3-navbar-group.bp3-align-left{
    float:left; }
  .bp3-navbar-group.bp3-align-right{
    float:right; }

.bp3-navbar-divider{
  border-left:1px solid rgba(16, 22, 26, 0.15);
  height:20px;
  margin:0 10px; }
  .bp3-dark .bp3-navbar-divider{
    border-left-color:rgba(255, 255, 255, 0.15); }
.bp3-non-ideal-state{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  height:100%;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  text-align:center;
  width:100%; }
  .bp3-non-ideal-state > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-non-ideal-state > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-non-ideal-state::before,
  .bp3-non-ideal-state > *{
    margin-bottom:20px; }
  .bp3-non-ideal-state:empty::before,
  .bp3-non-ideal-state > :last-child{
    margin-bottom:0; }
  .bp3-non-ideal-state > *{
    max-width:400px; }

.bp3-non-ideal-state-visual{
  color:rgba(92, 112, 128, 0.6);
  font-size:60px; }
  .bp3-dark .bp3-non-ideal-state-visual{
    color:rgba(167, 182, 194, 0.6); }

.bp3-overflow-list{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -ms-flex-wrap:nowrap;
      flex-wrap:nowrap;
  min-width:0; }

.bp3-overflow-list-spacer{
  -ms-flex-negative:1;
      flex-shrink:1;
  width:1px; }

body.bp3-overlay-open{
  overflow:hidden; }

.bp3-overlay{
  bottom:0;
  left:0;
  position:static;
  right:0;
  top:0;
  z-index:20; }
  .bp3-overlay:not(.bp3-overlay-open){
    pointer-events:none; }
  .bp3-overlay.bp3-overlay-container{
    overflow:hidden;
    position:fixed; }
    .bp3-overlay.bp3-overlay-container.bp3-overlay-inline{
      position:absolute; }
  .bp3-overlay.bp3-overlay-scroll-container{
    overflow:auto;
    position:fixed; }
    .bp3-overlay.bp3-overlay-scroll-container.bp3-overlay-inline{
      position:absolute; }
  .bp3-overlay.bp3-overlay-inline{
    display:inline;
    overflow:visible; }

.bp3-overlay-content{
  position:fixed;
  z-index:20; }
  .bp3-overlay-inline .bp3-overlay-content,
  .bp3-overlay-scroll-container .bp3-overlay-content{
    position:absolute; }

.bp3-overlay-backdrop{
  bottom:0;
  left:0;
  position:fixed;
  right:0;
  top:0;
  opacity:1;
  background-color:rgba(16, 22, 26, 0.7);
  overflow:auto;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none;
  z-index:20; }
  .bp3-overlay-backdrop.bp3-overlay-enter, .bp3-overlay-backdrop.bp3-overlay-appear{
    opacity:0; }
  .bp3-overlay-backdrop.bp3-overlay-enter-active, .bp3-overlay-backdrop.bp3-overlay-appear-active{
    opacity:1;
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:200ms;
            transition-duration:200ms;
    -webkit-transition-property:opacity;
    transition-property:opacity;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-overlay-backdrop.bp3-overlay-exit{
    opacity:1; }
  .bp3-overlay-backdrop.bp3-overlay-exit-active{
    opacity:0;
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:200ms;
            transition-duration:200ms;
    -webkit-transition-property:opacity;
    transition-property:opacity;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-overlay-backdrop:focus{
    outline:none; }
  .bp3-overlay-inline .bp3-overlay-backdrop{
    position:absolute; }
.bp3-panel-stack{
  overflow:hidden;
  position:relative; }

.bp3-panel-stack-header{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  -webkit-box-shadow:0 1px rgba(16, 22, 26, 0.15);
          box-shadow:0 1px rgba(16, 22, 26, 0.15);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -ms-flex-negative:0;
      flex-shrink:0;
  height:30px;
  z-index:1; }
  .bp3-dark .bp3-panel-stack-header{
    -webkit-box-shadow:0 1px rgba(255, 255, 255, 0.15);
            box-shadow:0 1px rgba(255, 255, 255, 0.15); }
  .bp3-panel-stack-header > span{
    -webkit-box-align:stretch;
        -ms-flex-align:stretch;
            align-items:stretch;
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    -webkit-box-flex:1;
        -ms-flex:1;
            flex:1; }
  .bp3-panel-stack-header .bp3-heading{
    margin:0 5px; }

.bp3-button.bp3-panel-stack-header-back{
  margin-left:5px;
  padding-left:0;
  white-space:nowrap; }
  .bp3-button.bp3-panel-stack-header-back .bp3-icon{
    margin:0 2px; }

.bp3-panel-stack-view{
  bottom:0;
  left:0;
  position:absolute;
  right:0;
  top:0;
  background-color:#ffffff;
  border-right:1px solid rgba(16, 22, 26, 0.15);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  margin-right:-1px;
  overflow-y:auto;
  z-index:1; }
  .bp3-dark .bp3-panel-stack-view{
    background-color:#30404d; }
  .bp3-panel-stack-view:nth-last-child(n + 4){
    display:none; }

.bp3-panel-stack-push .bp3-panel-stack-enter, .bp3-panel-stack-push .bp3-panel-stack-appear{
  -webkit-transform:translateX(100%);
          transform:translateX(100%);
  opacity:0; }

.bp3-panel-stack-push .bp3-panel-stack-enter-active, .bp3-panel-stack-push .bp3-panel-stack-appear-active{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1;
  -webkit-transition-delay:0;
          transition-delay:0;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease; }

.bp3-panel-stack-push .bp3-panel-stack-exit{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1; }

.bp3-panel-stack-push .bp3-panel-stack-exit-active{
  -webkit-transform:translateX(-50%);
          transform:translateX(-50%);
  opacity:0;
  -webkit-transition-delay:0;
          transition-delay:0;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease; }

.bp3-panel-stack-pop .bp3-panel-stack-enter, .bp3-panel-stack-pop .bp3-panel-stack-appear{
  -webkit-transform:translateX(-50%);
          transform:translateX(-50%);
  opacity:0; }

.bp3-panel-stack-pop .bp3-panel-stack-enter-active, .bp3-panel-stack-pop .bp3-panel-stack-appear-active{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1;
  -webkit-transition-delay:0;
          transition-delay:0;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease; }

.bp3-panel-stack-pop .bp3-panel-stack-exit{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1; }

.bp3-panel-stack-pop .bp3-panel-stack-exit-active{
  -webkit-transform:translateX(100%);
          transform:translateX(100%);
  opacity:0;
  -webkit-transition-delay:0;
          transition-delay:0;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease; }
.bp3-popover{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
  -webkit-transform:scale(1);
          transform:scale(1);
  border-radius:3px;
  display:inline-block;
  z-index:20; }
  .bp3-popover .bp3-popover-arrow{
    height:30px;
    position:absolute;
    width:30px; }
    .bp3-popover .bp3-popover-arrow::before{
      height:20px;
      margin:5px;
      width:20px; }
  .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-popover{
    margin-bottom:17px;
    margin-top:-17px; }
    .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-popover > .bp3-popover-arrow{
      bottom:-11px; }
      .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-popover > .bp3-popover-arrow svg{
        -webkit-transform:rotate(-90deg);
                transform:rotate(-90deg); }
  .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-popover{
    margin-left:17px; }
    .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-popover > .bp3-popover-arrow{
      left:-11px; }
      .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-popover > .bp3-popover-arrow svg{
        -webkit-transform:rotate(0);
                transform:rotate(0); }
  .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-popover{
    margin-top:17px; }
    .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-popover > .bp3-popover-arrow{
      top:-11px; }
      .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-popover > .bp3-popover-arrow svg{
        -webkit-transform:rotate(90deg);
                transform:rotate(90deg); }
  .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-popover{
    margin-left:-17px;
    margin-right:17px; }
    .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-popover > .bp3-popover-arrow{
      right:-11px; }
      .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-popover > .bp3-popover-arrow svg{
        -webkit-transform:rotate(180deg);
                transform:rotate(180deg); }
  .bp3-tether-element-attached-middle > .bp3-popover > .bp3-popover-arrow{
    top:50%;
    -webkit-transform:translateY(-50%);
            transform:translateY(-50%); }
  .bp3-tether-element-attached-center > .bp3-popover > .bp3-popover-arrow{
    right:50%;
    -webkit-transform:translateX(50%);
            transform:translateX(50%); }
  .bp3-tether-element-attached-top.bp3-tether-target-attached-top > .bp3-popover > .bp3-popover-arrow{
    top:-0.3934px; }
  .bp3-tether-element-attached-right.bp3-tether-target-attached-right > .bp3-popover > .bp3-popover-arrow{
    right:-0.3934px; }
  .bp3-tether-element-attached-left.bp3-tether-target-attached-left > .bp3-popover > .bp3-popover-arrow{
    left:-0.3934px; }
  .bp3-tether-element-attached-bottom.bp3-tether-target-attached-bottom > .bp3-popover > .bp3-popover-arrow{
    bottom:-0.3934px; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-left > .bp3-popover{
    -webkit-transform-origin:top left;
            transform-origin:top left; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-center > .bp3-popover{
    -webkit-transform-origin:top center;
            transform-origin:top center; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-right > .bp3-popover{
    -webkit-transform-origin:top right;
            transform-origin:top right; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-left > .bp3-popover{
    -webkit-transform-origin:center left;
            transform-origin:center left; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-center > .bp3-popover{
    -webkit-transform-origin:center center;
            transform-origin:center center; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-right > .bp3-popover{
    -webkit-transform-origin:center right;
            transform-origin:center right; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-left > .bp3-popover{
    -webkit-transform-origin:bottom left;
            transform-origin:bottom left; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-center > .bp3-popover{
    -webkit-transform-origin:bottom center;
            transform-origin:bottom center; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-right > .bp3-popover{
    -webkit-transform-origin:bottom right;
            transform-origin:bottom right; }
  .bp3-popover .bp3-popover-content{
    background:#ffffff;
    color:inherit; }
  .bp3-popover .bp3-popover-arrow::before{
    -webkit-box-shadow:1px 1px 6px rgba(16, 22, 26, 0.2);
            box-shadow:1px 1px 6px rgba(16, 22, 26, 0.2); }
  .bp3-popover .bp3-popover-arrow-border{
    fill:#10161a;
    fill-opacity:0.1; }
  .bp3-popover .bp3-popover-arrow-fill{
    fill:#ffffff; }
  .bp3-popover-enter > .bp3-popover, .bp3-popover-appear > .bp3-popover{
    -webkit-transform:scale(0.3);
            transform:scale(0.3); }
  .bp3-popover-enter-active > .bp3-popover, .bp3-popover-appear-active > .bp3-popover{
    -webkit-transform:scale(1);
            transform:scale(1);
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11); }
  .bp3-popover-exit > .bp3-popover{
    -webkit-transform:scale(1);
            transform:scale(1); }
  .bp3-popover-exit-active > .bp3-popover{
    -webkit-transform:scale(0.3);
            transform:scale(0.3);
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11); }
  .bp3-popover .bp3-popover-content{
    border-radius:3px;
    position:relative; }
  .bp3-popover.bp3-popover-content-sizing .bp3-popover-content{
    max-width:350px;
    padding:20px; }
  .bp3-popover-target + .bp3-overlay .bp3-popover.bp3-popover-content-sizing{
    width:350px; }
  .bp3-popover.bp3-minimal{
    margin:0 !important; }
    .bp3-popover.bp3-minimal .bp3-popover-arrow{
      display:none; }
    .bp3-popover.bp3-minimal.bp3-popover{
      -webkit-transform:scale(1);
              transform:scale(1); }
      .bp3-popover-enter > .bp3-popover.bp3-minimal.bp3-popover, .bp3-popover-appear > .bp3-popover.bp3-minimal.bp3-popover{
        -webkit-transform:scale(1);
                transform:scale(1); }
      .bp3-popover-enter-active > .bp3-popover.bp3-minimal.bp3-popover, .bp3-popover-appear-active > .bp3-popover.bp3-minimal.bp3-popover{
        -webkit-transform:scale(1);
                transform:scale(1);
        -webkit-transition-delay:0;
                transition-delay:0;
        -webkit-transition-duration:100ms;
                transition-duration:100ms;
        -webkit-transition-property:-webkit-transform;
        transition-property:-webkit-transform;
        transition-property:transform;
        transition-property:transform, -webkit-transform;
        -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
                transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
      .bp3-popover-exit > .bp3-popover.bp3-minimal.bp3-popover{
        -webkit-transform:scale(1);
                transform:scale(1); }
      .bp3-popover-exit-active > .bp3-popover.bp3-minimal.bp3-popover{
        -webkit-transform:scale(1);
                transform:scale(1);
        -webkit-transition-delay:0;
                transition-delay:0;
        -webkit-transition-duration:100ms;
                transition-duration:100ms;
        -webkit-transition-property:-webkit-transform;
        transition-property:-webkit-transform;
        transition-property:transform;
        transition-property:transform, -webkit-transform;
        -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
                transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-popover.bp3-dark,
  .bp3-dark .bp3-popover{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }
    .bp3-popover.bp3-dark .bp3-popover-content,
    .bp3-dark .bp3-popover .bp3-popover-content{
      background:#30404d;
      color:inherit; }
    .bp3-popover.bp3-dark .bp3-popover-arrow::before,
    .bp3-dark .bp3-popover .bp3-popover-arrow::before{
      -webkit-box-shadow:1px 1px 6px rgba(16, 22, 26, 0.4);
              box-shadow:1px 1px 6px rgba(16, 22, 26, 0.4); }
    .bp3-popover.bp3-dark .bp3-popover-arrow-border,
    .bp3-dark .bp3-popover .bp3-popover-arrow-border{
      fill:#10161a;
      fill-opacity:0.2; }
    .bp3-popover.bp3-dark .bp3-popover-arrow-fill,
    .bp3-dark .bp3-popover .bp3-popover-arrow-fill{
      fill:#30404d; }

.bp3-popover-arrow::before{
  border-radius:2px;
  content:"";
  display:block;
  position:absolute;
  -webkit-transform:rotate(45deg);
          transform:rotate(45deg); }

.bp3-tether-pinned .bp3-popover-arrow{
  display:none; }

.bp3-popover-backdrop{
  background:rgba(255, 255, 255, 0); }

.bp3-transition-container{
  opacity:1;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  z-index:20; }
  .bp3-transition-container.bp3-popover-enter, .bp3-transition-container.bp3-popover-appear{
    opacity:0; }
  .bp3-transition-container.bp3-popover-enter-active, .bp3-transition-container.bp3-popover-appear-active{
    opacity:1;
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:100ms;
            transition-duration:100ms;
    -webkit-transition-property:opacity;
    transition-property:opacity;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-transition-container.bp3-popover-exit{
    opacity:1; }
  .bp3-transition-container.bp3-popover-exit-active{
    opacity:0;
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:100ms;
            transition-duration:100ms;
    -webkit-transition-property:opacity;
    transition-property:opacity;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-transition-container:focus{
    outline:none; }
  .bp3-transition-container.bp3-popover-leave .bp3-popover-content{
    pointer-events:none; }
  .bp3-transition-container[data-x-out-of-boundaries]{
    display:none; }

span.bp3-popover-target{
  display:inline-block; }

.bp3-popover-wrapper.bp3-fill{
  width:100%; }

.bp3-portal{
  left:0;
  position:absolute;
  right:0;
  top:0; }
@-webkit-keyframes linear-progress-bar-stripes{
  from{
    background-position:0 0; }
  to{
    background-position:30px 0; } }
@keyframes linear-progress-bar-stripes{
  from{
    background-position:0 0; }
  to{
    background-position:30px 0; } }

.bp3-progress-bar{
  background:rgba(92, 112, 128, 0.2);
  border-radius:40px;
  display:block;
  height:8px;
  overflow:hidden;
  position:relative;
  width:100%; }
  .bp3-progress-bar .bp3-progress-meter{
    background:linear-gradient(-45deg, rgba(255, 255, 255, 0.2) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.2) 50%, rgba(255, 255, 255, 0.2) 75%, transparent 75%);
    background-color:rgba(92, 112, 128, 0.8);
    background-size:30px 30px;
    border-radius:40px;
    height:100%;
    position:absolute;
    -webkit-transition:width 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:width 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    width:100%; }
  .bp3-progress-bar:not(.bp3-no-animation):not(.bp3-no-stripes) .bp3-progress-meter{
    animation:linear-progress-bar-stripes 300ms linear infinite reverse; }
  .bp3-progress-bar.bp3-no-stripes .bp3-progress-meter{
    background-image:none; }

.bp3-dark .bp3-progress-bar{
  background:rgba(16, 22, 26, 0.5); }
  .bp3-dark .bp3-progress-bar .bp3-progress-meter{
    background-color:#8a9ba8; }

.bp3-progress-bar.bp3-intent-primary .bp3-progress-meter{
  background-color:#137cbd; }

.bp3-progress-bar.bp3-intent-success .bp3-progress-meter{
  background-color:#0f9960; }

.bp3-progress-bar.bp3-intent-warning .bp3-progress-meter{
  background-color:#d9822b; }

.bp3-progress-bar.bp3-intent-danger .bp3-progress-meter{
  background-color:#db3737; }
@-webkit-keyframes skeleton-glow{
  from{
    background:rgba(206, 217, 224, 0.2);
    border-color:rgba(206, 217, 224, 0.2); }
  to{
    background:rgba(92, 112, 128, 0.2);
    border-color:rgba(92, 112, 128, 0.2); } }
@keyframes skeleton-glow{
  from{
    background:rgba(206, 217, 224, 0.2);
    border-color:rgba(206, 217, 224, 0.2); }
  to{
    background:rgba(92, 112, 128, 0.2);
    border-color:rgba(92, 112, 128, 0.2); } }
.bp3-skeleton{
  -webkit-animation:1000ms linear infinite alternate skeleton-glow;
          animation:1000ms linear infinite alternate skeleton-glow;
  background:rgba(206, 217, 224, 0.2);
  background-clip:padding-box !important;
  border-color:rgba(206, 217, 224, 0.2) !important;
  border-radius:2px;
  -webkit-box-shadow:none !important;
          box-shadow:none !important;
  color:transparent !important;
  cursor:default;
  pointer-events:none;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-skeleton::before, .bp3-skeleton::after,
  .bp3-skeleton *{
    visibility:hidden !important; }
.bp3-slider{
  height:40px;
  min-width:150px;
  width:100%;
  cursor:default;
  outline:none;
  position:relative;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-slider:hover{
    cursor:pointer; }
  .bp3-slider:active{
    cursor:-webkit-grabbing;
    cursor:grabbing; }
  .bp3-slider.bp3-disabled{
    cursor:not-allowed;
    opacity:0.5; }
  .bp3-slider.bp3-slider-unlabeled{
    height:16px; }

.bp3-slider-track,
.bp3-slider-progress{
  height:6px;
  left:0;
  right:0;
  top:5px;
  position:absolute; }

.bp3-slider-track{
  border-radius:3px;
  overflow:hidden; }

.bp3-slider-progress{
  background:rgba(92, 112, 128, 0.2); }
  .bp3-dark .bp3-slider-progress{
    background:rgba(16, 22, 26, 0.5); }
  .bp3-slider-progress.bp3-intent-primary{
    background-color:#137cbd; }
  .bp3-slider-progress.bp3-intent-success{
    background-color:#0f9960; }
  .bp3-slider-progress.bp3-intent-warning{
    background-color:#d9822b; }
  .bp3-slider-progress.bp3-intent-danger{
    background-color:#db3737; }

.bp3-slider-handle{
  background-color:#f5f8fa;
  background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.8)), to(rgba(255, 255, 255, 0)));
  background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
  -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
          box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
  color:#182026;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
  cursor:pointer;
  height:16px;
  left:0;
  position:absolute;
  top:0;
  width:16px; }
  .bp3-slider-handle:hover{
    background-clip:padding-box;
    background-color:#ebf1f5;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1); }
  .bp3-slider-handle:active, .bp3-slider-handle.bp3-active{
    background-color:#d8e1e8;
    background-image:none;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
  .bp3-slider-handle:disabled, .bp3-slider-handle.bp3-disabled{
    background-color:rgba(206, 217, 224, 0.5);
    background-image:none;
    -webkit-box-shadow:none;
            box-shadow:none;
    color:rgba(92, 112, 128, 0.6);
    cursor:not-allowed;
    outline:none; }
    .bp3-slider-handle:disabled.bp3-active, .bp3-slider-handle:disabled.bp3-active:hover, .bp3-slider-handle.bp3-disabled.bp3-active, .bp3-slider-handle.bp3-disabled.bp3-active:hover{
      background:rgba(206, 217, 224, 0.7); }
  .bp3-slider-handle:focus{
    z-index:1; }
  .bp3-slider-handle:hover{
    background-clip:padding-box;
    background-color:#ebf1f5;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
    cursor:-webkit-grab;
    cursor:grab;
    z-index:2; }
  .bp3-slider-handle.bp3-active{
    background-color:#d8e1e8;
    background-image:none;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 1px rgba(16, 22, 26, 0.1);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 1px rgba(16, 22, 26, 0.1);
    cursor:-webkit-grabbing;
    cursor:grabbing; }
  .bp3-disabled .bp3-slider-handle{
    background:#bfccd6;
    -webkit-box-shadow:none;
            box-shadow:none;
    pointer-events:none; }
  .bp3-dark .bp3-slider-handle{
    background-color:#394b59;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.05)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0));
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
    color:#f5f8fa; }
    .bp3-dark .bp3-slider-handle:hover, .bp3-dark .bp3-slider-handle:active, .bp3-dark .bp3-slider-handle.bp3-active{
      color:#f5f8fa; }
    .bp3-dark .bp3-slider-handle:hover{
      background-color:#30404d;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-slider-handle:active, .bp3-dark .bp3-slider-handle.bp3-active{
      background-color:#202b33;
      background-image:none;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-dark .bp3-slider-handle:disabled, .bp3-dark .bp3-slider-handle.bp3-disabled{
      background-color:rgba(57, 75, 89, 0.5);
      background-image:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(167, 182, 194, 0.6); }
      .bp3-dark .bp3-slider-handle:disabled.bp3-active, .bp3-dark .bp3-slider-handle.bp3-disabled.bp3-active{
        background:rgba(57, 75, 89, 0.7); }
    .bp3-dark .bp3-slider-handle .bp3-button-spinner .bp3-spinner-head{
      background:rgba(16, 22, 26, 0.5);
      stroke:#8a9ba8; }
    .bp3-dark .bp3-slider-handle, .bp3-dark .bp3-slider-handle:hover{
      background-color:#394b59; }
    .bp3-dark .bp3-slider-handle.bp3-active{
      background-color:#293742; }
  .bp3-dark .bp3-disabled .bp3-slider-handle{
    background:#5c7080;
    border-color:#5c7080;
    -webkit-box-shadow:none;
            box-shadow:none; }
  .bp3-slider-handle .bp3-slider-label{
    background:#394b59;
    border-radius:3px;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
    color:#f5f8fa;
    margin-left:8px; }
    .bp3-dark .bp3-slider-handle .bp3-slider-label{
      background:#e1e8ed;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
      color:#394b59; }
    .bp3-disabled .bp3-slider-handle .bp3-slider-label{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-slider-handle.bp3-start, .bp3-slider-handle.bp3-end{
    width:8px; }
  .bp3-slider-handle.bp3-start{
    border-bottom-right-radius:0;
    border-top-right-radius:0; }
  .bp3-slider-handle.bp3-end{
    border-bottom-left-radius:0;
    border-top-left-radius:0;
    margin-left:8px; }
    .bp3-slider-handle.bp3-end .bp3-slider-label{
      margin-left:0; }

.bp3-slider-label{
  -webkit-transform:translate(-50%, 20px);
          transform:translate(-50%, 20px);
  display:inline-block;
  font-size:12px;
  line-height:1;
  padding:2px 5px;
  position:absolute;
  vertical-align:top; }

.bp3-slider.bp3-vertical{
  height:150px;
  min-width:40px;
  width:40px; }
  .bp3-slider.bp3-vertical .bp3-slider-track,
  .bp3-slider.bp3-vertical .bp3-slider-progress{
    bottom:0;
    height:auto;
    left:5px;
    top:0;
    width:6px; }
  .bp3-slider.bp3-vertical .bp3-slider-progress{
    top:auto; }
  .bp3-slider.bp3-vertical .bp3-slider-label{
    -webkit-transform:translate(20px, 50%);
            transform:translate(20px, 50%); }
  .bp3-slider.bp3-vertical .bp3-slider-handle{
    top:auto; }
    .bp3-slider.bp3-vertical .bp3-slider-handle .bp3-slider-label{
      margin-left:0;
      margin-top:-8px; }
    .bp3-slider.bp3-vertical .bp3-slider-handle.bp3-end, .bp3-slider.bp3-vertical .bp3-slider-handle.bp3-start{
      height:8px;
      margin-left:0;
      width:16px; }
    .bp3-slider.bp3-vertical .bp3-slider-handle.bp3-start{
      border-bottom-right-radius:3px;
      border-top-left-radius:0; }
      .bp3-slider.bp3-vertical .bp3-slider-handle.bp3-start .bp3-slider-label{
        -webkit-transform:translate(20px);
                transform:translate(20px); }
    .bp3-slider.bp3-vertical .bp3-slider-handle.bp3-end{
      border-bottom-left-radius:0;
      border-bottom-right-radius:0;
      border-top-left-radius:3px;
      margin-bottom:8px; }

@-webkit-keyframes pt-spinner-animation{
  from{
    -webkit-transform:rotate(0deg);
            transform:rotate(0deg); }
  to{
    -webkit-transform:rotate(360deg);
            transform:rotate(360deg); } }

@keyframes pt-spinner-animation{
  from{
    -webkit-transform:rotate(0deg);
            transform:rotate(0deg); }
  to{
    -webkit-transform:rotate(360deg);
            transform:rotate(360deg); } }

.bp3-spinner{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  overflow:visible;
  vertical-align:middle; }
  .bp3-spinner svg{
    display:block; }
  .bp3-spinner path{
    fill-opacity:0; }
  .bp3-spinner .bp3-spinner-head{
    stroke:rgba(92, 112, 128, 0.8);
    stroke-linecap:round;
    -webkit-transform-origin:center;
            transform-origin:center;
    -webkit-transition:stroke-dashoffset 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:stroke-dashoffset 200ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-spinner .bp3-spinner-track{
    stroke:rgba(92, 112, 128, 0.2); }

.bp3-spinner-animation{
  -webkit-animation:pt-spinner-animation 500ms linear infinite;
          animation:pt-spinner-animation 500ms linear infinite; }
  .bp3-no-spin > .bp3-spinner-animation{
    -webkit-animation:none;
            animation:none; }

.bp3-dark .bp3-spinner .bp3-spinner-head{
  stroke:#8a9ba8; }

.bp3-dark .bp3-spinner .bp3-spinner-track{
  stroke:rgba(16, 22, 26, 0.5); }

.bp3-spinner.bp3-intent-primary .bp3-spinner-head{
  stroke:#137cbd; }

.bp3-spinner.bp3-intent-success .bp3-spinner-head{
  stroke:#0f9960; }

.bp3-spinner.bp3-intent-warning .bp3-spinner-head{
  stroke:#d9822b; }

.bp3-spinner.bp3-intent-danger .bp3-spinner-head{
  stroke:#db3737; }
.bp3-tabs.bp3-vertical{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex; }
  .bp3-tabs.bp3-vertical > .bp3-tab-list{
    -webkit-box-align:start;
        -ms-flex-align:start;
            align-items:flex-start;
    -webkit-box-orient:vertical;
    -webkit-box-direction:normal;
        -ms-flex-direction:column;
            flex-direction:column; }
    .bp3-tabs.bp3-vertical > .bp3-tab-list .bp3-tab{
      border-radius:3px;
      padding:0 10px;
      width:100%; }
      .bp3-tabs.bp3-vertical > .bp3-tab-list .bp3-tab[aria-selected="true"]{
        background-color:rgba(19, 124, 189, 0.2);
        -webkit-box-shadow:none;
                box-shadow:none; }
    .bp3-tabs.bp3-vertical > .bp3-tab-list .bp3-tab-indicator-wrapper .bp3-tab-indicator{
      background-color:rgba(19, 124, 189, 0.2);
      border-radius:3px;
      bottom:0;
      height:auto;
      left:0;
      right:0;
      top:0; }
  .bp3-tabs.bp3-vertical > .bp3-tab-panel{
    margin-top:0;
    padding-left:20px; }

.bp3-tab-list{
  -webkit-box-align:end;
      -ms-flex-align:end;
          align-items:flex-end;
  border:none;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  list-style:none;
  margin:0;
  padding:0;
  position:relative; }
  .bp3-tab-list > *:not(:last-child){
    margin-right:20px; }

.bp3-tab{
  overflow:hidden;
  text-overflow:ellipsis;
  white-space:nowrap;
  word-wrap:normal;
  color:#182026;
  cursor:pointer;
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  font-size:14px;
  line-height:30px;
  max-width:100%;
  position:relative;
  vertical-align:top; }
  .bp3-tab a{
    color:inherit;
    display:block;
    text-decoration:none; }
  .bp3-tab-indicator-wrapper ~ .bp3-tab{
    background-color:transparent !important;
    -webkit-box-shadow:none !important;
            box-shadow:none !important; }
  .bp3-tab[aria-disabled="true"]{
    color:rgba(92, 112, 128, 0.6);
    cursor:not-allowed; }
  .bp3-tab[aria-selected="true"]{
    border-radius:0;
    -webkit-box-shadow:inset 0 -3px 0 #106ba3;
            box-shadow:inset 0 -3px 0 #106ba3; }
  .bp3-tab[aria-selected="true"], .bp3-tab:not([aria-disabled="true"]):hover{
    color:#106ba3; }
  .bp3-tab:focus{
    -moz-outline-radius:0; }
  .bp3-large > .bp3-tab{
    font-size:16px;
    line-height:40px; }

.bp3-tab-panel{
  margin-top:20px; }
  .bp3-tab-panel[aria-hidden="true"]{
    display:none; }

.bp3-tab-indicator-wrapper{
  left:0;
  pointer-events:none;
  position:absolute;
  top:0;
  -webkit-transform:translateX(0), translateY(0);
          transform:translateX(0), translateY(0);
  -webkit-transition:height, width, -webkit-transform;
  transition:height, width, -webkit-transform;
  transition:height, transform, width;
  transition:height, transform, width, -webkit-transform;
  -webkit-transition-duration:200ms;
          transition-duration:200ms;
  -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
          transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-tab-indicator-wrapper .bp3-tab-indicator{
    background-color:#106ba3;
    bottom:0;
    height:3px;
    left:0;
    position:absolute;
    right:0; }
  .bp3-tab-indicator-wrapper.bp3-no-animation{
    -webkit-transition:none;
    transition:none; }

.bp3-dark .bp3-tab{
  color:#f5f8fa; }
  .bp3-dark .bp3-tab[aria-disabled="true"]{
    color:rgba(167, 182, 194, 0.6); }
  .bp3-dark .bp3-tab[aria-selected="true"]{
    -webkit-box-shadow:inset 0 -3px 0 #48aff0;
            box-shadow:inset 0 -3px 0 #48aff0; }
  .bp3-dark .bp3-tab[aria-selected="true"], .bp3-dark .bp3-tab:not([aria-disabled="true"]):hover{
    color:#48aff0; }

.bp3-dark .bp3-tab-indicator{
  background-color:#48aff0; }

.bp3-flex-expander{
  -webkit-box-flex:1;
      -ms-flex:1 1;
          flex:1 1; }
.bp3-tag{
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  background-color:#5c7080;
  border:none;
  border-radius:3px;
  -webkit-box-shadow:none;
          box-shadow:none;
  color:#f5f8fa;
  font-size:12px;
  line-height:16px;
  max-width:100%;
  min-height:20px;
  min-width:20px;
  padding:2px 6px;
  position:relative; }
  .bp3-tag.bp3-interactive{
    cursor:pointer; }
    .bp3-tag.bp3-interactive:hover{
      background-color:rgba(92, 112, 128, 0.85); }
    .bp3-tag.bp3-interactive.bp3-active, .bp3-tag.bp3-interactive:active{
      background-color:rgba(92, 112, 128, 0.7); }
  .bp3-tag > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-tag > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-tag::before,
  .bp3-tag > *{
    margin-right:4px; }
  .bp3-tag:empty::before,
  .bp3-tag > :last-child{
    margin-right:0; }
  .bp3-tag:focus{
    outline:rgba(19, 124, 189, 0.6) auto 2px;
    outline-offset:0;
    -moz-outline-radius:6px; }
  .bp3-tag.bp3-round{
    border-radius:30px;
    padding-left:8px;
    padding-right:8px; }
  .bp3-dark .bp3-tag{
    background-color:#bfccd6;
    color:#182026; }
    .bp3-dark .bp3-tag.bp3-interactive{
      cursor:pointer; }
      .bp3-dark .bp3-tag.bp3-interactive:hover{
        background-color:rgba(191, 204, 214, 0.85); }
      .bp3-dark .bp3-tag.bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-interactive:active{
        background-color:rgba(191, 204, 214, 0.7); }
    .bp3-dark .bp3-tag > .bp3-icon, .bp3-dark .bp3-tag .bp3-icon-standard, .bp3-dark .bp3-tag .bp3-icon-large{
      fill:currentColor; }
  .bp3-tag > .bp3-icon, .bp3-tag .bp3-icon-standard, .bp3-tag .bp3-icon-large{
    fill:#ffffff; }
  .bp3-tag.bp3-large,
  .bp3-large .bp3-tag{
    font-size:14px;
    line-height:20px;
    min-height:30px;
    min-width:30px;
    padding:5px 10px; }
    .bp3-tag.bp3-large::before,
    .bp3-tag.bp3-large > *,
    .bp3-large .bp3-tag::before,
    .bp3-large .bp3-tag > *{
      margin-right:7px; }
    .bp3-tag.bp3-large:empty::before,
    .bp3-tag.bp3-large > :last-child,
    .bp3-large .bp3-tag:empty::before,
    .bp3-large .bp3-tag > :last-child{
      margin-right:0; }
    .bp3-tag.bp3-large.bp3-round,
    .bp3-large .bp3-tag.bp3-round{
      padding-left:12px;
      padding-right:12px; }
  .bp3-tag.bp3-intent-primary{
    background:#137cbd;
    color:#ffffff; }
    .bp3-tag.bp3-intent-primary.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-intent-primary.bp3-interactive:hover{
        background-color:rgba(19, 124, 189, 0.85); }
      .bp3-tag.bp3-intent-primary.bp3-interactive.bp3-active, .bp3-tag.bp3-intent-primary.bp3-interactive:active{
        background-color:rgba(19, 124, 189, 0.7); }
  .bp3-tag.bp3-intent-success{
    background:#0f9960;
    color:#ffffff; }
    .bp3-tag.bp3-intent-success.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-intent-success.bp3-interactive:hover{
        background-color:rgba(15, 153, 96, 0.85); }
      .bp3-tag.bp3-intent-success.bp3-interactive.bp3-active, .bp3-tag.bp3-intent-success.bp3-interactive:active{
        background-color:rgba(15, 153, 96, 0.7); }
  .bp3-tag.bp3-intent-warning{
    background:#d9822b;
    color:#ffffff; }
    .bp3-tag.bp3-intent-warning.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-intent-warning.bp3-interactive:hover{
        background-color:rgba(217, 130, 43, 0.85); }
      .bp3-tag.bp3-intent-warning.bp3-interactive.bp3-active, .bp3-tag.bp3-intent-warning.bp3-interactive:active{
        background-color:rgba(217, 130, 43, 0.7); }
  .bp3-tag.bp3-intent-danger{
    background:#db3737;
    color:#ffffff; }
    .bp3-tag.bp3-intent-danger.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-intent-danger.bp3-interactive:hover{
        background-color:rgba(219, 55, 55, 0.85); }
      .bp3-tag.bp3-intent-danger.bp3-interactive.bp3-active, .bp3-tag.bp3-intent-danger.bp3-interactive:active{
        background-color:rgba(219, 55, 55, 0.7); }
  .bp3-tag.bp3-fill{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    width:100%; }
  .bp3-tag.bp3-minimal > .bp3-icon, .bp3-tag.bp3-minimal .bp3-icon-standard, .bp3-tag.bp3-minimal .bp3-icon-large{
    fill:#5c7080; }
  .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]){
    background-color:rgba(138, 155, 168, 0.2);
    color:#182026; }
    .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive:hover{
        background-color:rgba(92, 112, 128, 0.3); }
      .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive.bp3-active, .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive:active{
        background-color:rgba(92, 112, 128, 0.4); }
    .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]){
      color:#f5f8fa; }
      .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive{
        cursor:pointer; }
        .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive:hover{
          background-color:rgba(191, 204, 214, 0.3); }
        .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive:active{
          background-color:rgba(191, 204, 214, 0.4); }
      .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]) > .bp3-icon, .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]) .bp3-icon-standard, .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]) .bp3-icon-large{
        fill:#a7b6c2; }
  .bp3-tag.bp3-minimal.bp3-intent-primary{
    background-color:rgba(19, 124, 189, 0.15);
    color:#106ba3; }
    .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive:hover{
        background-color:rgba(19, 124, 189, 0.25); }
      .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive.bp3-active, .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive:active{
        background-color:rgba(19, 124, 189, 0.35); }
    .bp3-tag.bp3-minimal.bp3-intent-primary > .bp3-icon, .bp3-tag.bp3-minimal.bp3-intent-primary .bp3-icon-standard, .bp3-tag.bp3-minimal.bp3-intent-primary .bp3-icon-large{
      fill:#137cbd; }
    .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-primary{
      background-color:rgba(19, 124, 189, 0.25);
      color:#48aff0; }
      .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive{
        cursor:pointer; }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive:hover{
          background-color:rgba(19, 124, 189, 0.35); }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive:active{
          background-color:rgba(19, 124, 189, 0.45); }
  .bp3-tag.bp3-minimal.bp3-intent-success{
    background-color:rgba(15, 153, 96, 0.15);
    color:#0d8050; }
    .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive:hover{
        background-color:rgba(15, 153, 96, 0.25); }
      .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive.bp3-active, .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive:active{
        background-color:rgba(15, 153, 96, 0.35); }
    .bp3-tag.bp3-minimal.bp3-intent-success > .bp3-icon, .bp3-tag.bp3-minimal.bp3-intent-success .bp3-icon-standard, .bp3-tag.bp3-minimal.bp3-intent-success .bp3-icon-large{
      fill:#0f9960; }
    .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-success{
      background-color:rgba(15, 153, 96, 0.25);
      color:#3dcc91; }
      .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive{
        cursor:pointer; }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive:hover{
          background-color:rgba(15, 153, 96, 0.35); }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive:active{
          background-color:rgba(15, 153, 96, 0.45); }
  .bp3-tag.bp3-minimal.bp3-intent-warning{
    background-color:rgba(217, 130, 43, 0.15);
    color:#bf7326; }
    .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive:hover{
        background-color:rgba(217, 130, 43, 0.25); }
      .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive.bp3-active, .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive:active{
        background-color:rgba(217, 130, 43, 0.35); }
    .bp3-tag.bp3-minimal.bp3-intent-warning > .bp3-icon, .bp3-tag.bp3-minimal.bp3-intent-warning .bp3-icon-standard, .bp3-tag.bp3-minimal.bp3-intent-warning .bp3-icon-large{
      fill:#d9822b; }
    .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-warning{
      background-color:rgba(217, 130, 43, 0.25);
      color:#ffb366; }
      .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive{
        cursor:pointer; }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive:hover{
          background-color:rgba(217, 130, 43, 0.35); }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive:active{
          background-color:rgba(217, 130, 43, 0.45); }
  .bp3-tag.bp3-minimal.bp3-intent-danger{
    background-color:rgba(219, 55, 55, 0.15);
    color:#c23030; }
    .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive:hover{
        background-color:rgba(219, 55, 55, 0.25); }
      .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive.bp3-active, .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive:active{
        background-color:rgba(219, 55, 55, 0.35); }
    .bp3-tag.bp3-minimal.bp3-intent-danger > .bp3-icon, .bp3-tag.bp3-minimal.bp3-intent-danger .bp3-icon-standard, .bp3-tag.bp3-minimal.bp3-intent-danger .bp3-icon-large{
      fill:#db3737; }
    .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-danger{
      background-color:rgba(219, 55, 55, 0.25);
      color:#ff7373; }
      .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive{
        cursor:pointer; }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive:hover{
          background-color:rgba(219, 55, 55, 0.35); }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive:active{
          background-color:rgba(219, 55, 55, 0.45); }

.bp3-tag-remove{
  background:none;
  border:none;
  color:inherit;
  cursor:pointer;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  margin-bottom:-2px;
  margin-right:-6px !important;
  margin-top:-2px;
  opacity:0.5;
  padding:2px;
  padding-left:0; }
  .bp3-tag-remove:hover{
    background:none;
    opacity:0.8;
    text-decoration:none; }
  .bp3-tag-remove:active{
    opacity:1; }
  .bp3-tag-remove:empty::before{
    font-family:"Icons16", sans-serif;
    font-size:16px;
    font-style:normal;
    font-weight:400;
    line-height:1;
    -moz-osx-font-smoothing:grayscale;
    -webkit-font-smoothing:antialiased;
    content:""; }
  .bp3-large .bp3-tag-remove{
    margin-right:-10px !important;
    padding:0 5px 0 0; }
    .bp3-large .bp3-tag-remove:empty::before{
      font-family:"Icons20", sans-serif;
      font-size:20px;
      font-style:normal;
      font-weight:400;
      line-height:1; }
.bp3-tag-input{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:start;
      -ms-flex-align:start;
          align-items:flex-start;
  cursor:text;
  height:auto;
  line-height:inherit;
  min-height:30px;
  padding-left:5px;
  padding-right:0; }
  .bp3-tag-input > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-tag-input > .bp3-tag-input-values{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-tag-input .bp3-tag-input-icon{
    color:#5c7080;
    margin-left:2px;
    margin-right:7px;
    margin-top:7px; }
  .bp3-tag-input .bp3-tag-input-values{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    -webkit-box-orient:horizontal;
    -webkit-box-direction:normal;
        -ms-flex-direction:row;
            flex-direction:row;
    -webkit-box-align:center;
        -ms-flex-align:center;
            align-items:center;
    -ms-flex-item-align:stretch;
        align-self:stretch;
    -ms-flex-wrap:wrap;
        flex-wrap:wrap;
    margin-right:7px;
    margin-top:5px;
    min-width:0; }
    .bp3-tag-input .bp3-tag-input-values > *{
      -webkit-box-flex:0;
          -ms-flex-positive:0;
              flex-grow:0;
      -ms-flex-negative:0;
          flex-shrink:0; }
    .bp3-tag-input .bp3-tag-input-values > .bp3-fill{
      -webkit-box-flex:1;
          -ms-flex-positive:1;
              flex-grow:1;
      -ms-flex-negative:1;
          flex-shrink:1; }
    .bp3-tag-input .bp3-tag-input-values::before,
    .bp3-tag-input .bp3-tag-input-values > *{
      margin-right:5px; }
    .bp3-tag-input .bp3-tag-input-values:empty::before,
    .bp3-tag-input .bp3-tag-input-values > :last-child{
      margin-right:0; }
    .bp3-tag-input .bp3-tag-input-values:first-child .bp3-input-ghost:first-child{
      padding-left:5px; }
    .bp3-tag-input .bp3-tag-input-values > *{
      margin-bottom:5px; }
  .bp3-tag-input .bp3-tag{
    overflow-wrap:break-word; }
    .bp3-tag-input .bp3-tag.bp3-active{
      outline:rgba(19, 124, 189, 0.6) auto 2px;
      outline-offset:0;
      -moz-outline-radius:6px; }
  .bp3-tag-input .bp3-input-ghost{
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto;
    line-height:20px;
    width:80px; }
    .bp3-tag-input .bp3-input-ghost:disabled, .bp3-tag-input .bp3-input-ghost.bp3-disabled{
      cursor:not-allowed; }
  .bp3-tag-input .bp3-button,
  .bp3-tag-input .bp3-spinner{
    margin:3px;
    margin-left:0; }
  .bp3-tag-input .bp3-button{
    min-height:24px;
    min-width:24px;
    padding:0 7px; }
  .bp3-tag-input.bp3-large{
    height:auto;
    min-height:40px; }
    .bp3-tag-input.bp3-large::before,
    .bp3-tag-input.bp3-large > *{
      margin-right:10px; }
    .bp3-tag-input.bp3-large:empty::before,
    .bp3-tag-input.bp3-large > :last-child{
      margin-right:0; }
    .bp3-tag-input.bp3-large .bp3-tag-input-icon{
      margin-left:5px;
      margin-top:10px; }
    .bp3-tag-input.bp3-large .bp3-input-ghost{
      line-height:30px; }
    .bp3-tag-input.bp3-large .bp3-button{
      min-height:30px;
      min-width:30px;
      padding:5px 10px;
      margin:5px;
      margin-left:0; }
    .bp3-tag-input.bp3-large .bp3-spinner{
      margin:8px;
      margin-left:0; }
  .bp3-tag-input.bp3-active{
    background-color:#ffffff;
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-tag-input.bp3-active.bp3-intent-primary{
      -webkit-box-shadow:0 0 0 1px #106ba3, 0 0 0 3px rgba(16, 107, 163, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #106ba3, 0 0 0 3px rgba(16, 107, 163, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-tag-input.bp3-active.bp3-intent-success{
      -webkit-box-shadow:0 0 0 1px #0d8050, 0 0 0 3px rgba(13, 128, 80, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #0d8050, 0 0 0 3px rgba(13, 128, 80, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-tag-input.bp3-active.bp3-intent-warning{
      -webkit-box-shadow:0 0 0 1px #bf7326, 0 0 0 3px rgba(191, 115, 38, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #bf7326, 0 0 0 3px rgba(191, 115, 38, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-tag-input.bp3-active.bp3-intent-danger{
      -webkit-box-shadow:0 0 0 1px #c23030, 0 0 0 3px rgba(194, 48, 48, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #c23030, 0 0 0 3px rgba(194, 48, 48, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-dark .bp3-tag-input .bp3-tag-input-icon, .bp3-tag-input.bp3-dark .bp3-tag-input-icon{
    color:#a7b6c2; }
  .bp3-dark .bp3-tag-input .bp3-input-ghost, .bp3-tag-input.bp3-dark .bp3-input-ghost{
    color:#f5f8fa; }
    .bp3-dark .bp3-tag-input .bp3-input-ghost::-webkit-input-placeholder, .bp3-tag-input.bp3-dark .bp3-input-ghost::-webkit-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-tag-input .bp3-input-ghost::-moz-placeholder, .bp3-tag-input.bp3-dark .bp3-input-ghost::-moz-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-tag-input .bp3-input-ghost:-ms-input-placeholder, .bp3-tag-input.bp3-dark .bp3-input-ghost:-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-tag-input .bp3-input-ghost::-ms-input-placeholder, .bp3-tag-input.bp3-dark .bp3-input-ghost::-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-tag-input .bp3-input-ghost::placeholder, .bp3-tag-input.bp3-dark .bp3-input-ghost::placeholder{
      color:rgba(167, 182, 194, 0.6); }
  .bp3-dark .bp3-tag-input.bp3-active, .bp3-tag-input.bp3-dark.bp3-active{
    background-color:rgba(16, 22, 26, 0.3);
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-tag-input.bp3-active.bp3-intent-primary, .bp3-tag-input.bp3-dark.bp3-active.bp3-intent-primary{
      -webkit-box-shadow:0 0 0 1px #106ba3, 0 0 0 3px rgba(16, 107, 163, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #106ba3, 0 0 0 3px rgba(16, 107, 163, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-tag-input.bp3-active.bp3-intent-success, .bp3-tag-input.bp3-dark.bp3-active.bp3-intent-success{
      -webkit-box-shadow:0 0 0 1px #0d8050, 0 0 0 3px rgba(13, 128, 80, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #0d8050, 0 0 0 3px rgba(13, 128, 80, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-tag-input.bp3-active.bp3-intent-warning, .bp3-tag-input.bp3-dark.bp3-active.bp3-intent-warning{
      -webkit-box-shadow:0 0 0 1px #bf7326, 0 0 0 3px rgba(191, 115, 38, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #bf7326, 0 0 0 3px rgba(191, 115, 38, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-tag-input.bp3-active.bp3-intent-danger, .bp3-tag-input.bp3-dark.bp3-active.bp3-intent-danger{
      -webkit-box-shadow:0 0 0 1px #c23030, 0 0 0 3px rgba(194, 48, 48, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #c23030, 0 0 0 3px rgba(194, 48, 48, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }

.bp3-input-ghost{
  background:none;
  border:none;
  -webkit-box-shadow:none;
          box-shadow:none;
  padding:0; }
  .bp3-input-ghost::-webkit-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input-ghost::-moz-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input-ghost:-ms-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input-ghost::-ms-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input-ghost::placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input-ghost:focus{
    outline:none !important; }
.bp3-toast{
  -webkit-box-align:start;
      -ms-flex-align:start;
          align-items:flex-start;
  background-color:#ffffff;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  margin:20px 0 0;
  max-width:500px;
  min-width:300px;
  pointer-events:all;
  position:relative !important; }
  .bp3-toast.bp3-toast-enter, .bp3-toast.bp3-toast-appear{
    -webkit-transform:translateY(-40px);
            transform:translateY(-40px); }
  .bp3-toast.bp3-toast-enter-active, .bp3-toast.bp3-toast-appear-active{
    -webkit-transform:translateY(0);
            transform:translateY(0);
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11); }
  .bp3-toast.bp3-toast-enter ~ .bp3-toast, .bp3-toast.bp3-toast-appear ~ .bp3-toast{
    -webkit-transform:translateY(-40px);
            transform:translateY(-40px); }
  .bp3-toast.bp3-toast-enter-active ~ .bp3-toast, .bp3-toast.bp3-toast-appear-active ~ .bp3-toast{
    -webkit-transform:translateY(0);
            transform:translateY(0);
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11); }
  .bp3-toast.bp3-toast-exit{
    opacity:1;
    -webkit-filter:blur(0);
            filter:blur(0); }
  .bp3-toast.bp3-toast-exit-active{
    opacity:0;
    -webkit-filter:blur(10px);
            filter:blur(10px);
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-property:opacity, -webkit-filter;
    transition-property:opacity, -webkit-filter;
    transition-property:opacity, filter;
    transition-property:opacity, filter, -webkit-filter;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-toast.bp3-toast-exit ~ .bp3-toast{
    -webkit-transform:translateY(0);
            transform:translateY(0); }
  .bp3-toast.bp3-toast-exit-active ~ .bp3-toast{
    -webkit-transform:translateY(-40px);
            transform:translateY(-40px);
    -webkit-transition-delay:50ms;
            transition-delay:50ms;
    -webkit-transition-duration:100ms;
            transition-duration:100ms;
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-toast .bp3-button-group{
    -webkit-box-flex:0;
        -ms-flex:0 0 auto;
            flex:0 0 auto;
    padding:5px;
    padding-left:0; }
  .bp3-toast > .bp3-icon{
    color:#5c7080;
    margin:12px;
    margin-right:0; }
  .bp3-toast.bp3-dark,
  .bp3-dark .bp3-toast{
    background-color:#394b59;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }
    .bp3-toast.bp3-dark > .bp3-icon,
    .bp3-dark .bp3-toast > .bp3-icon{
      color:#a7b6c2; }
  .bp3-toast[class*="bp3-intent-"] a{
    color:rgba(255, 255, 255, 0.7); }
    .bp3-toast[class*="bp3-intent-"] a:hover{
      color:#ffffff; }
  .bp3-toast[class*="bp3-intent-"] > .bp3-icon{
    color:#ffffff; }
  .bp3-toast[class*="bp3-intent-"] .bp3-button, .bp3-toast[class*="bp3-intent-"] .bp3-button::before,
  .bp3-toast[class*="bp3-intent-"] .bp3-button .bp3-icon, .bp3-toast[class*="bp3-intent-"] .bp3-button:active{
    color:rgba(255, 255, 255, 0.7) !important; }
  .bp3-toast[class*="bp3-intent-"] .bp3-button:focus{
    outline-color:rgba(255, 255, 255, 0.5); }
  .bp3-toast[class*="bp3-intent-"] .bp3-button:hover{
    background-color:rgba(255, 255, 255, 0.15) !important;
    color:#ffffff !important; }
  .bp3-toast[class*="bp3-intent-"] .bp3-button:active{
    background-color:rgba(255, 255, 255, 0.3) !important;
    color:#ffffff !important; }
  .bp3-toast[class*="bp3-intent-"] .bp3-button::after{
    background:rgba(255, 255, 255, 0.3) !important; }
  .bp3-toast.bp3-intent-primary{
    background-color:#137cbd;
    color:#ffffff; }
  .bp3-toast.bp3-intent-success{
    background-color:#0f9960;
    color:#ffffff; }
  .bp3-toast.bp3-intent-warning{
    background-color:#d9822b;
    color:#ffffff; }
  .bp3-toast.bp3-intent-danger{
    background-color:#db3737;
    color:#ffffff; }

.bp3-toast-message{
  -webkit-box-flex:1;
      -ms-flex:1 1 auto;
          flex:1 1 auto;
  padding:11px;
  word-break:break-word; }

.bp3-toast-container{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  display:-webkit-box !important;
  display:-ms-flexbox !important;
  display:flex !important;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  left:0;
  overflow:hidden;
  padding:0 20px 20px;
  pointer-events:none;
  position:fixed;
  right:0;
  z-index:40; }
  .bp3-toast-container.bp3-toast-container-top{
    top:0; }
  .bp3-toast-container.bp3-toast-container-bottom{
    bottom:0;
    -webkit-box-orient:vertical;
    -webkit-box-direction:reverse;
        -ms-flex-direction:column-reverse;
            flex-direction:column-reverse;
    top:auto; }
  .bp3-toast-container.bp3-toast-container-left{
    -webkit-box-align:start;
        -ms-flex-align:start;
            align-items:flex-start; }
  .bp3-toast-container.bp3-toast-container-right{
    -webkit-box-align:end;
        -ms-flex-align:end;
            align-items:flex-end; }

.bp3-toast-container-bottom .bp3-toast.bp3-toast-enter:not(.bp3-toast-enter-active),
.bp3-toast-container-bottom .bp3-toast.bp3-toast-enter:not(.bp3-toast-enter-active) ~ .bp3-toast, .bp3-toast-container-bottom .bp3-toast.bp3-toast-appear:not(.bp3-toast-appear-active),
.bp3-toast-container-bottom .bp3-toast.bp3-toast-appear:not(.bp3-toast-appear-active) ~ .bp3-toast,
.bp3-toast-container-bottom .bp3-toast.bp3-toast-exit-active ~ .bp3-toast,
.bp3-toast-container-bottom .bp3-toast.bp3-toast-leave-active ~ .bp3-toast{
  -webkit-transform:translateY(60px);
          transform:translateY(60px); }
.bp3-tooltip{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
  -webkit-transform:scale(1);
          transform:scale(1); }
  .bp3-tooltip .bp3-popover-arrow{
    height:22px;
    position:absolute;
    width:22px; }
    .bp3-tooltip .bp3-popover-arrow::before{
      height:14px;
      margin:4px;
      width:14px; }
  .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-tooltip{
    margin-bottom:11px;
    margin-top:-11px; }
    .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-tooltip > .bp3-popover-arrow{
      bottom:-8px; }
      .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-tooltip > .bp3-popover-arrow svg{
        -webkit-transform:rotate(-90deg);
                transform:rotate(-90deg); }
  .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-tooltip{
    margin-left:11px; }
    .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-tooltip > .bp3-popover-arrow{
      left:-8px; }
      .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-tooltip > .bp3-popover-arrow svg{
        -webkit-transform:rotate(0);
                transform:rotate(0); }
  .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-tooltip{
    margin-top:11px; }
    .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-tooltip > .bp3-popover-arrow{
      top:-8px; }
      .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-tooltip > .bp3-popover-arrow svg{
        -webkit-transform:rotate(90deg);
                transform:rotate(90deg); }
  .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-tooltip{
    margin-left:-11px;
    margin-right:11px; }
    .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-tooltip > .bp3-popover-arrow{
      right:-8px; }
      .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-tooltip > .bp3-popover-arrow svg{
        -webkit-transform:rotate(180deg);
                transform:rotate(180deg); }
  .bp3-tether-element-attached-middle > .bp3-tooltip > .bp3-popover-arrow{
    top:50%;
    -webkit-transform:translateY(-50%);
            transform:translateY(-50%); }
  .bp3-tether-element-attached-center > .bp3-tooltip > .bp3-popover-arrow{
    right:50%;
    -webkit-transform:translateX(50%);
            transform:translateX(50%); }
  .bp3-tether-element-attached-top.bp3-tether-target-attached-top > .bp3-tooltip > .bp3-popover-arrow{
    top:-0.22183px; }
  .bp3-tether-element-attached-right.bp3-tether-target-attached-right > .bp3-tooltip > .bp3-popover-arrow{
    right:-0.22183px; }
  .bp3-tether-element-attached-left.bp3-tether-target-attached-left > .bp3-tooltip > .bp3-popover-arrow{
    left:-0.22183px; }
  .bp3-tether-element-attached-bottom.bp3-tether-target-attached-bottom > .bp3-tooltip > .bp3-popover-arrow{
    bottom:-0.22183px; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-left > .bp3-tooltip{
    -webkit-transform-origin:top left;
            transform-origin:top left; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-center > .bp3-tooltip{
    -webkit-transform-origin:top center;
            transform-origin:top center; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-right > .bp3-tooltip{
    -webkit-transform-origin:top right;
            transform-origin:top right; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-left > .bp3-tooltip{
    -webkit-transform-origin:center left;
            transform-origin:center left; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-center > .bp3-tooltip{
    -webkit-transform-origin:center center;
            transform-origin:center center; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-right > .bp3-tooltip{
    -webkit-transform-origin:center right;
            transform-origin:center right; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-left > .bp3-tooltip{
    -webkit-transform-origin:bottom left;
            transform-origin:bottom left; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-center > .bp3-tooltip{
    -webkit-transform-origin:bottom center;
            transform-origin:bottom center; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-right > .bp3-tooltip{
    -webkit-transform-origin:bottom right;
            transform-origin:bottom right; }
  .bp3-tooltip .bp3-popover-content{
    background:#394b59;
    color:#f5f8fa; }
  .bp3-tooltip .bp3-popover-arrow::before{
    -webkit-box-shadow:1px 1px 6px rgba(16, 22, 26, 0.2);
            box-shadow:1px 1px 6px rgba(16, 22, 26, 0.2); }
  .bp3-tooltip .bp3-popover-arrow-border{
    fill:#10161a;
    fill-opacity:0.1; }
  .bp3-tooltip .bp3-popover-arrow-fill{
    fill:#394b59; }
  .bp3-popover-enter > .bp3-tooltip, .bp3-popover-appear > .bp3-tooltip{
    -webkit-transform:scale(0.8);
            transform:scale(0.8); }
  .bp3-popover-enter-active > .bp3-tooltip, .bp3-popover-appear-active > .bp3-tooltip{
    -webkit-transform:scale(1);
            transform:scale(1);
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:100ms;
            transition-duration:100ms;
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-popover-exit > .bp3-tooltip{
    -webkit-transform:scale(1);
            transform:scale(1); }
  .bp3-popover-exit-active > .bp3-tooltip{
    -webkit-transform:scale(0.8);
            transform:scale(0.8);
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:100ms;
            transition-duration:100ms;
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-tooltip .bp3-popover-content{
    padding:10px 12px; }
  .bp3-tooltip.bp3-dark,
  .bp3-dark .bp3-tooltip{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }
    .bp3-tooltip.bp3-dark .bp3-popover-content,
    .bp3-dark .bp3-tooltip .bp3-popover-content{
      background:#e1e8ed;
      color:#394b59; }
    .bp3-tooltip.bp3-dark .bp3-popover-arrow::before,
    .bp3-dark .bp3-tooltip .bp3-popover-arrow::before{
      -webkit-box-shadow:1px 1px 6px rgba(16, 22, 26, 0.4);
              box-shadow:1px 1px 6px rgba(16, 22, 26, 0.4); }
    .bp3-tooltip.bp3-dark .bp3-popover-arrow-border,
    .bp3-dark .bp3-tooltip .bp3-popover-arrow-border{
      fill:#10161a;
      fill-opacity:0.2; }
    .bp3-tooltip.bp3-dark .bp3-popover-arrow-fill,
    .bp3-dark .bp3-tooltip .bp3-popover-arrow-fill{
      fill:#e1e8ed; }
  .bp3-tooltip.bp3-intent-primary .bp3-popover-content{
    background:#137cbd;
    color:#ffffff; }
  .bp3-tooltip.bp3-intent-primary .bp3-popover-arrow-fill{
    fill:#137cbd; }
  .bp3-tooltip.bp3-intent-success .bp3-popover-content{
    background:#0f9960;
    color:#ffffff; }
  .bp3-tooltip.bp3-intent-success .bp3-popover-arrow-fill{
    fill:#0f9960; }
  .bp3-tooltip.bp3-intent-warning .bp3-popover-content{
    background:#d9822b;
    color:#ffffff; }
  .bp3-tooltip.bp3-intent-warning .bp3-popover-arrow-fill{
    fill:#d9822b; }
  .bp3-tooltip.bp3-intent-danger .bp3-popover-content{
    background:#db3737;
    color:#ffffff; }
  .bp3-tooltip.bp3-intent-danger .bp3-popover-arrow-fill{
    fill:#db3737; }

.bp3-tooltip-indicator{
  border-bottom:dotted 1px;
  cursor:help; }
.bp3-tree .bp3-icon, .bp3-tree .bp3-icon-standard, .bp3-tree .bp3-icon-large{
  color:#5c7080; }
  .bp3-tree .bp3-icon.bp3-intent-primary, .bp3-tree .bp3-icon-standard.bp3-intent-primary, .bp3-tree .bp3-icon-large.bp3-intent-primary{
    color:#137cbd; }
  .bp3-tree .bp3-icon.bp3-intent-success, .bp3-tree .bp3-icon-standard.bp3-intent-success, .bp3-tree .bp3-icon-large.bp3-intent-success{
    color:#0f9960; }
  .bp3-tree .bp3-icon.bp3-intent-warning, .bp3-tree .bp3-icon-standard.bp3-intent-warning, .bp3-tree .bp3-icon-large.bp3-intent-warning{
    color:#d9822b; }
  .bp3-tree .bp3-icon.bp3-intent-danger, .bp3-tree .bp3-icon-standard.bp3-intent-danger, .bp3-tree .bp3-icon-large.bp3-intent-danger{
    color:#db3737; }

.bp3-tree-node-list{
  list-style:none;
  margin:0;
  padding-left:0; }

.bp3-tree-root{
  background-color:transparent;
  cursor:default;
  padding-left:0;
  position:relative; }

.bp3-tree-node-content-0{
  padding-left:0px; }

.bp3-tree-node-content-1{
  padding-left:23px; }

.bp3-tree-node-content-2{
  padding-left:46px; }

.bp3-tree-node-content-3{
  padding-left:69px; }

.bp3-tree-node-content-4{
  padding-left:92px; }

.bp3-tree-node-content-5{
  padding-left:115px; }

.bp3-tree-node-content-6{
  padding-left:138px; }

.bp3-tree-node-content-7{
  padding-left:161px; }

.bp3-tree-node-content-8{
  padding-left:184px; }

.bp3-tree-node-content-9{
  padding-left:207px; }

.bp3-tree-node-content-10{
  padding-left:230px; }

.bp3-tree-node-content-11{
  padding-left:253px; }

.bp3-tree-node-content-12{
  padding-left:276px; }

.bp3-tree-node-content-13{
  padding-left:299px; }

.bp3-tree-node-content-14{
  padding-left:322px; }

.bp3-tree-node-content-15{
  padding-left:345px; }

.bp3-tree-node-content-16{
  padding-left:368px; }

.bp3-tree-node-content-17{
  padding-left:391px; }

.bp3-tree-node-content-18{
  padding-left:414px; }

.bp3-tree-node-content-19{
  padding-left:437px; }

.bp3-tree-node-content-20{
  padding-left:460px; }

.bp3-tree-node-content{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  height:30px;
  padding-right:5px;
  width:100%; }
  .bp3-tree-node-content:hover{
    background-color:rgba(191, 204, 214, 0.4); }

.bp3-tree-node-caret,
.bp3-tree-node-caret-none{
  min-width:30px; }

.bp3-tree-node-caret{
  color:#5c7080;
  cursor:pointer;
  padding:7px;
  -webkit-transform:rotate(0deg);
          transform:rotate(0deg);
  -webkit-transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-tree-node-caret:hover{
    color:#182026; }
  .bp3-dark .bp3-tree-node-caret{
    color:#a7b6c2; }
    .bp3-dark .bp3-tree-node-caret:hover{
      color:#f5f8fa; }
  .bp3-tree-node-caret.bp3-tree-node-caret-open{
    -webkit-transform:rotate(90deg);
            transform:rotate(90deg); }
  .bp3-tree-node-caret.bp3-icon-standard::before{
    content:""; }

.bp3-tree-node-icon{
  margin-right:7px;
  position:relative; }

.bp3-tree-node-label{
  overflow:hidden;
  text-overflow:ellipsis;
  white-space:nowrap;
  word-wrap:normal;
  -webkit-box-flex:1;
      -ms-flex:1 1 auto;
          flex:1 1 auto;
  position:relative;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-tree-node-label span{
    display:inline; }

.bp3-tree-node-secondary-label{
  padding:0 5px;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-tree-node-secondary-label .bp3-popover-wrapper,
  .bp3-tree-node-secondary-label .bp3-popover-target{
    -webkit-box-align:center;
        -ms-flex-align:center;
            align-items:center;
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex; }

.bp3-tree-node.bp3-disabled .bp3-tree-node-content{
  background-color:inherit;
  color:rgba(92, 112, 128, 0.6);
  cursor:not-allowed; }

.bp3-tree-node.bp3-disabled .bp3-tree-node-caret,
.bp3-tree-node.bp3-disabled .bp3-tree-node-icon{
  color:rgba(92, 112, 128, 0.6);
  cursor:not-allowed; }

.bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content{
  background-color:#137cbd; }
  .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content,
  .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content .bp3-icon, .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content .bp3-icon-standard, .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content .bp3-icon-large{
    color:#ffffff; }
  .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content .bp3-tree-node-caret::before{
    color:rgba(255, 255, 255, 0.7); }
  .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content .bp3-tree-node-caret:hover::before{
    color:#ffffff; }

.bp3-dark .bp3-tree-node-content:hover{
  background-color:rgba(92, 112, 128, 0.3); }

.bp3-dark .bp3-tree .bp3-icon, .bp3-dark .bp3-tree .bp3-icon-standard, .bp3-dark .bp3-tree .bp3-icon-large{
  color:#a7b6c2; }
  .bp3-dark .bp3-tree .bp3-icon.bp3-intent-primary, .bp3-dark .bp3-tree .bp3-icon-standard.bp3-intent-primary, .bp3-dark .bp3-tree .bp3-icon-large.bp3-intent-primary{
    color:#137cbd; }
  .bp3-dark .bp3-tree .bp3-icon.bp3-intent-success, .bp3-dark .bp3-tree .bp3-icon-standard.bp3-intent-success, .bp3-dark .bp3-tree .bp3-icon-large.bp3-intent-success{
    color:#0f9960; }
  .bp3-dark .bp3-tree .bp3-icon.bp3-intent-warning, .bp3-dark .bp3-tree .bp3-icon-standard.bp3-intent-warning, .bp3-dark .bp3-tree .bp3-icon-large.bp3-intent-warning{
    color:#d9822b; }
  .bp3-dark .bp3-tree .bp3-icon.bp3-intent-danger, .bp3-dark .bp3-tree .bp3-icon-standard.bp3-intent-danger, .bp3-dark .bp3-tree .bp3-icon-large.bp3-intent-danger{
    color:#db3737; }

.bp3-dark .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content{
  background-color:#137cbd; }
.bp3-omnibar{
  -webkit-filter:blur(0);
          filter:blur(0);
  opacity:1;
  background-color:#ffffff;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
  left:calc(50% - 250px);
  top:20vh;
  width:500px;
  z-index:21; }
  .bp3-omnibar.bp3-overlay-enter, .bp3-omnibar.bp3-overlay-appear{
    -webkit-filter:blur(20px);
            filter:blur(20px);
    opacity:0.2; }
  .bp3-omnibar.bp3-overlay-enter-active, .bp3-omnibar.bp3-overlay-appear-active{
    -webkit-filter:blur(0);
            filter:blur(0);
    opacity:1;
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:200ms;
            transition-duration:200ms;
    -webkit-transition-property:opacity, -webkit-filter;
    transition-property:opacity, -webkit-filter;
    transition-property:filter, opacity;
    transition-property:filter, opacity, -webkit-filter;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-omnibar.bp3-overlay-exit{
    -webkit-filter:blur(0);
            filter:blur(0);
    opacity:1; }
  .bp3-omnibar.bp3-overlay-exit-active{
    -webkit-filter:blur(20px);
            filter:blur(20px);
    opacity:0.2;
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:200ms;
            transition-duration:200ms;
    -webkit-transition-property:opacity, -webkit-filter;
    transition-property:opacity, -webkit-filter;
    transition-property:filter, opacity;
    transition-property:filter, opacity, -webkit-filter;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-omnibar .bp3-input{
    background-color:transparent;
    border-radius:0; }
    .bp3-omnibar .bp3-input, .bp3-omnibar .bp3-input:focus{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-omnibar .bp3-menu{
    background-color:transparent;
    border-radius:0;
    -webkit-box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.15);
            box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.15);
    max-height:calc(60vh - 40px);
    overflow:auto; }
    .bp3-omnibar .bp3-menu:empty{
      display:none; }
  .bp3-dark .bp3-omnibar, .bp3-omnibar.bp3-dark{
    background-color:#30404d;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4); }

.bp3-omnibar-overlay .bp3-overlay-backdrop{
  background-color:rgba(16, 22, 26, 0.2); }

.bp3-select-popover .bp3-popover-content{
  padding:5px; }

.bp3-select-popover .bp3-input-group{
  margin-bottom:0; }

.bp3-select-popover .bp3-menu{
  max-height:300px;
  max-width:400px;
  overflow:auto;
  padding:0; }
  .bp3-select-popover .bp3-menu:not(:first-child){
    padding-top:5px; }

.bp3-multi-select{
  min-width:150px; }

.bp3-multi-select-popover .bp3-menu{
  max-height:300px;
  max-width:400px;
  overflow:auto; }

.bp3-select-popover .bp3-popover-content{
  padding:5px; }

.bp3-select-popover .bp3-input-group{
  margin-bottom:0; }

.bp3-select-popover .bp3-menu{
  max-height:300px;
  max-width:400px;
  overflow:auto;
  padding:0; }
  .bp3-select-popover .bp3-menu:not(:first-child){
    padding-top:5px; }
/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensureUiComponents() in @jupyterlab/buildutils */

/**
 * (DEPRECATED) Support for consuming icons as CSS background images
 */

/* Icons urls */

:root {
  --jp-icon-add: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE5IDEzaC02djZoLTJ2LTZINXYtMmg2VjVoMnY2aDZ2MnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-bug: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTIwIDhoLTIuODFjLS40NS0uNzgtMS4wNy0xLjQ1LTEuODItMS45NkwxNyA0LjQxIDE1LjU5IDNsLTIuMTcgMi4xN0MxMi45NiA1LjA2IDEyLjQ5IDUgMTIgNWMtLjQ5IDAtLjk2LjA2LTEuNDEuMTdMOC40MSAzIDcgNC40MWwxLjYyIDEuNjNDNy44OCA2LjU1IDcuMjYgNy4yMiA2LjgxIDhINHYyaDIuMDljLS4wNS4zMy0uMDkuNjYtLjA5IDF2MUg0djJoMnYxYzAgLjM0LjA0LjY3LjA5IDFINHYyaDIuODFjMS4wNCAxLjc5IDIuOTcgMyA1LjE5IDNzNC4xNS0xLjIxIDUuMTktM0gyMHYtMmgtMi4wOWMuMDUtLjMzLjA5LS42Ni4wOS0xdi0xaDJ2LTJoLTJ2LTFjMC0uMzQtLjA0LS42Ny0uMDktMUgyMFY4em0tNiA4aC00di0yaDR2MnptMC00aC00di0yaDR2MnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-build: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTYiIHZpZXdCb3g9IjAgMCAyNCAyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE0LjkgMTcuNDVDMTYuMjUgMTcuNDUgMTcuMzUgMTYuMzUgMTcuMzUgMTVDMTcuMzUgMTMuNjUgMTYuMjUgMTIuNTUgMTQuOSAxMi41NUMxMy41NCAxMi41NSAxMi40NSAxMy42NSAxMi40NSAxNUMxMi40NSAxNi4zNSAxMy41NCAxNy40NSAxNC45IDE3LjQ1Wk0yMC4xIDE1LjY4TDIxLjU4IDE2Ljg0QzIxLjcxIDE2Ljk1IDIxLjc1IDE3LjEzIDIxLjY2IDE3LjI5TDIwLjI2IDE5LjcxQzIwLjE3IDE5Ljg2IDIwIDE5LjkyIDE5LjgzIDE5Ljg2TDE4LjA5IDE5LjE2QzE3LjczIDE5LjQ0IDE3LjMzIDE5LjY3IDE2LjkxIDE5Ljg1TDE2LjY0IDIxLjdDMTYuNjIgMjEuODcgMTYuNDcgMjIgMTYuMyAyMkgxMy41QzEzLjMyIDIyIDEzLjE4IDIxLjg3IDEzLjE1IDIxLjdMMTIuODkgMTkuODVDMTIuNDYgMTkuNjcgMTIuMDcgMTkuNDQgMTEuNzEgMTkuMTZMOS45NjAwMiAxOS44NkM5LjgxMDAyIDE5LjkyIDkuNjIwMDIgMTkuODYgOS41NDAwMiAxOS43MUw4LjE0MDAyIDE3LjI5QzguMDUwMDIgMTcuMTMgOC4wOTAwMiAxNi45NSA4LjIyMDAyIDE2Ljg0TDkuNzAwMDIgMTUuNjhMOS42NTAwMSAxNUw5LjcwMDAyIDE0LjMxTDguMjIwMDIgMTMuMTZDOC4wOTAwMiAxMy4wNSA4LjA1MDAyIDEyLjg2IDguMTQwMDIgMTIuNzFMOS41NDAwMiAxMC4yOUM5LjYyMDAyIDEwLjEzIDkuODEwMDIgMTAuMDcgOS45NjAwMiAxMC4xM0wxMS43MSAxMC44NEMxMi4wNyAxMC41NiAxMi40NiAxMC4zMiAxMi44OSAxMC4xNUwxMy4xNSA4LjI4OTk4QzEzLjE4IDguMTI5OTggMTMuMzIgNy45OTk5OCAxMy41IDcuOTk5OThIMTYuM0MxNi40NyA3Ljk5OTk4IDE2LjYyIDguMTI5OTggMTYuNjQgOC4yODk5OEwxNi45MSAxMC4xNUMxNy4zMyAxMC4zMiAxNy43MyAxMC41NiAxOC4wOSAxMC44NEwxOS44MyAxMC4xM0MyMCAxMC4wNyAyMC4xNyAxMC4xMyAyMC4yNiAxMC4yOUwyMS42NiAxMi43MUMyMS43NSAxMi44NiAyMS43MSAxMy4wNSAyMS41OCAxMy4xNkwyMC4xIDE0LjMxTDIwLjE1IDE1TDIwLjEgMTUuNjhaIi8+CiAgICA8cGF0aCBkPSJNNy4zMjk2NiA3LjQ0NDU0QzguMDgzMSA3LjAwOTU0IDguMzM5MzIgNi4wNTMzMiA3LjkwNDMyIDUuMjk5ODhDNy40NjkzMiA0LjU0NjQzIDYuNTA4MSA0LjI4MTU2IDUuNzU0NjYgNC43MTY1NkM1LjM5MTc2IDQuOTI2MDggNS4xMjY5NSA1LjI3MTE4IDUuMDE4NDkgNS42NzU5NEM0LjkxMDA0IDYuMDgwNzEgNC45NjY4MiA2LjUxMTk4IDUuMTc2MzQgNi44NzQ4OEM1LjYxMTM0IDcuNjI4MzIgNi41NzYyMiA3Ljg3OTU0IDcuMzI5NjYgNy40NDQ1NFpNOS42NTcxOCA0Ljc5NTkzTDEwLjg2NzIgNC45NTE3OUMxMC45NjI4IDQuOTc3NDEgMTEuMDQwMiA1LjA3MTMzIDExLjAzODIgNS4xODc5M0wxMS4wMzg4IDYuOTg4OTNDMTEuMDQ1NSA3LjEwMDU0IDEwLjk2MTYgNy4xOTUxOCAxMC44NTUgNy4yMTA1NEw5LjY2MDAxIDcuMzgwODNMOS4yMzkxNSA4LjEzMTg4TDkuNjY5NjEgOS4yNTc0NUM5LjcwNzI5IDkuMzYyNzEgOS42NjkzNCA5LjQ3Njk5IDkuNTc0MDggOS41MzE5OUw4LjAxNTIzIDEwLjQzMkM3LjkxMTMxIDEwLjQ5MiA3Ljc5MzM3IDEwLjQ2NzcgNy43MjEwNSAxMC4zODI0TDYuOTg3NDggOS40MzE4OEw2LjEwOTMxIDkuNDMwODNMNS4zNDcwNCAxMC4zOTA1QzUuMjg5MDkgMTAuNDcwMiA1LjE3MzgzIDEwLjQ5MDUgNS4wNzE4NyAxMC40MzM5TDMuNTEyNDUgOS41MzI5M0MzLjQxMDQ5IDkuNDc2MzMgMy4zNzY0NyA5LjM1NzQxIDMuNDEwNzUgOS4yNTY3OUwzLjg2MzQ3IDguMTQwOTNMMy42MTc0OSA3Ljc3NDg4TDMuNDIzNDcgNy4zNzg4M0wyLjIzMDc1IDcuMjEyOTdDMi4xMjY0NyA3LjE5MjM1IDIuMDQwNDkgNy4xMDM0MiAyLjA0MjQ1IDYuOTg2ODJMMi4wNDE4NyA1LjE4NTgyQzIuMDQzODMgNS4wNjkyMiAyLjExOTA5IDQuOTc5NTggMi4yMTcwNCA0Ljk2OTIyTDMuNDIwNjUgNC43OTM5M0wzLjg2NzQ5IDQuMDI3ODhMMy40MTEwNSAyLjkxNzMxQzMuMzczMzcgMi44MTIwNCAzLjQxMTMxIDIuNjk3NzYgMy41MTUyMyAyLjYzNzc2TDUuMDc0MDggMS43Mzc3NkM1LjE2OTM0IDEuNjgyNzYgNS4yODcyOSAxLjcwNzA0IDUuMzU5NjEgMS43OTIzMUw2LjExOTE1IDIuNzI3ODhMNi45ODAwMSAyLjczODkzTDcuNzI0OTYgMS43ODkyMkM3Ljc5MTU2IDEuNzA0NTggNy45MTU0OCAxLjY3OTIyIDguMDA4NzkgMS43NDA4Mkw5LjU2ODIxIDIuNjQxODJDOS42NzAxNyAyLjY5ODQyIDkuNzEyODUgMi44MTIzNCA5LjY4NzIzIDIuOTA3OTdMOS4yMTcxOCA0LjAzMzgzTDkuNDYzMTYgNC4zOTk4OEw5LjY1NzE4IDQuNzk1OTNaIi8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-caret-down-empty-thin: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwb2x5Z29uIGNsYXNzPSJzdDEiIHBvaW50cz0iOS45LDEzLjYgMy42LDcuNCA0LjQsNi42IDkuOSwxMi4yIDE1LjQsNi43IDE2LjEsNy40ICIvPgoJPC9nPgo8L3N2Zz4K);
  --jp-icon-caret-down-empty: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiIHNoYXBlLXJlbmRlcmluZz0iZ2VvbWV0cmljUHJlY2lzaW9uIj4KICAgIDxwYXRoIGQ9Ik01LjIsNS45TDksOS43bDMuOC0zLjhsMS4yLDEuMmwtNC45LDVsLTQuOS01TDUuMiw1Ljl6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-caret-down: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiIHNoYXBlLXJlbmRlcmluZz0iZ2VvbWV0cmljUHJlY2lzaW9uIj4KICAgIDxwYXRoIGQ9Ik01LjIsNy41TDksMTEuMmwzLjgtMy44SDUuMnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-caret-left: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwYXRoIGQ9Ik0xMC44LDEyLjhMNy4xLDlsMy44LTMuOGwwLDcuNkgxMC44eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-caret-right: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiIHNoYXBlLXJlbmRlcmluZz0iZ2VvbWV0cmljUHJlY2lzaW9uIj4KICAgIDxwYXRoIGQ9Ik03LjIsNS4yTDEwLjksOWwtMy44LDMuOFY1LjJINy4yeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-caret-up-empty-thin: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwb2x5Z29uIGNsYXNzPSJzdDEiIHBvaW50cz0iMTUuNCwxMy4zIDkuOSw3LjcgNC40LDEzLjIgMy42LDEyLjUgOS45LDYuMyAxNi4xLDEyLjYgIi8+Cgk8L2c+Cjwvc3ZnPgo=);
  --jp-icon-caret-up: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwYXRoIGQ9Ik01LjIsMTAuNUw5LDYuOGwzLjgsMy44SDUuMnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-case-sensitive: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KICA8ZyBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiM0MTQxNDEiPgogICAgPHJlY3QgeD0iMiIgeT0iMiIgd2lkdGg9IjE2IiBoZWlnaHQ9IjE2Ii8+CiAgPC9nPgogIDxnIGNsYXNzPSJqcC1pY29uLWFjY2VudDIiIGZpbGw9IiNGRkYiPgogICAgPHBhdGggZD0iTTcuNiw4aDAuOWwzLjUsOGgtMS4xTDEwLDE0SDZsLTAuOSwySDRMNy42LDh6IE04LDkuMUw2LjQsMTNoMy4yTDgsOS4xeiIvPgogICAgPHBhdGggZD0iTTE2LjYsOS44Yy0wLjIsMC4xLTAuNCwwLjEtMC43LDAuMWMtMC4yLDAtMC40LTAuMS0wLjYtMC4yYy0wLjEtMC4xLTAuMi0wLjQtMC4yLTAuNyBjLTAuMywwLjMtMC42LDAuNS0wLjksMC43Yy0wLjMsMC4xLTAuNywwLjItMS4xLDAuMmMtMC4zLDAtMC41LDAtMC43LTAuMWMtMC4yLTAuMS0wLjQtMC4yLTAuNi0wLjNjLTAuMi0wLjEtMC4zLTAuMy0wLjQtMC41IGMtMC4xLTAuMi0wLjEtMC40LTAuMS0wLjdjMC0wLjMsMC4xLTAuNiwwLjItMC44YzAuMS0wLjIsMC4zLTAuNCwwLjQtMC41QzEyLDcsMTIuMiw2LjksMTIuNSw2LjhjMC4yLTAuMSwwLjUtMC4xLDAuNy0wLjIgYzAuMy0wLjEsMC41LTAuMSwwLjctMC4xYzAuMiwwLDAuNC0wLjEsMC42LTAuMWMwLjIsMCwwLjMtMC4xLDAuNC0wLjJjMC4xLTAuMSwwLjItMC4yLDAuMi0wLjRjMC0xLTEuMS0xLTEuMy0xIGMtMC40LDAtMS40LDAtMS40LDEuMmgtMC45YzAtMC40LDAuMS0wLjcsMC4yLTFjMC4xLTAuMiwwLjMtMC40LDAuNS0wLjZjMC4yLTAuMiwwLjUtMC4zLDAuOC0wLjNDMTMuMyw0LDEzLjYsNCwxMy45LDQgYzAuMywwLDAuNSwwLDAuOCwwLjFjMC4zLDAsMC41LDAuMSwwLjcsMC4yYzAuMiwwLjEsMC40LDAuMywwLjUsMC41QzE2LDUsMTYsNS4yLDE2LDUuNnYyLjljMCwwLjIsMCwwLjQsMCwwLjUgYzAsMC4xLDAuMSwwLjIsMC4zLDAuMmMwLjEsMCwwLjIsMCwwLjMsMFY5Ljh6IE0xNS4yLDYuOWMtMS4yLDAuNi0zLjEsMC4yLTMuMSwxLjRjMCwxLjQsMy4xLDEsMy4xLTAuNVY2Ljl6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-check: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTkgMTYuMTdMNC44MyAxMmwtMS40MiAxLjQxTDkgMTkgMjEgN2wtMS40MS0xLjQxeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-circle-empty: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyIDJDNi40NyAyIDIgNi40NyAyIDEyczQuNDcgMTAgMTAgMTAgMTAtNC40NyAxMC0xMFMxNy41MyAyIDEyIDJ6bTAgMThjLTQuNDEgMC04LTMuNTktOC04czMuNTktOCA4LTggOCAzLjU5IDggOC0zLjU5IDgtOCA4eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-circle: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMTggMTgiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPGNpcmNsZSBjeD0iOSIgY3k9IjkiIHI9IjgiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-clear: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8bWFzayBpZD0iZG9udXRIb2xlIj4KICAgIDxyZWN0IHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgZmlsbD0id2hpdGUiIC8+CiAgICA8Y2lyY2xlIGN4PSIxMiIgY3k9IjEyIiByPSI4IiBmaWxsPSJibGFjayIvPgogIDwvbWFzaz4KCiAgPGcgY2xhc3M9ImpwLWljb24zIiBmaWxsPSIjNjE2MTYxIj4KICAgIDxyZWN0IGhlaWdodD0iMTgiIHdpZHRoPSIyIiB4PSIxMSIgeT0iMyIgdHJhbnNmb3JtPSJyb3RhdGUoMzE1LCAxMiwgMTIpIi8+CiAgICA8Y2lyY2xlIGN4PSIxMiIgY3k9IjEyIiByPSIxMCIgbWFzaz0idXJsKCNkb251dEhvbGUpIi8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-close: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbi1ub25lIGpwLWljb24tc2VsZWN0YWJsZS1pbnZlcnNlIGpwLWljb24zLWhvdmVyIiBmaWxsPSJub25lIj4KICAgIDxjaXJjbGUgY3g9IjEyIiBjeT0iMTIiIHI9IjExIi8+CiAgPC9nPgoKICA8ZyBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIGpwLWljb24tYWNjZW50Mi1ob3ZlciIgZmlsbD0iIzYxNjE2MSI+CiAgICA8cGF0aCBkPSJNMTkgNi40MUwxNy41OSA1IDEyIDEwLjU5IDYuNDEgNSA1IDYuNDEgMTAuNTkgMTIgNSAxNy41OSA2LjQxIDE5IDEyIDEzLjQxIDE3LjU5IDE5IDE5IDE3LjU5IDEzLjQxIDEyeiIvPgogIDwvZz4KCiAgPGcgY2xhc3M9ImpwLWljb24tbm9uZSBqcC1pY29uLWJ1c3kiIGZpbGw9Im5vbmUiPgogICAgPGNpcmNsZSBjeD0iMTIiIGN5PSIxMiIgcj0iNyIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-code: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjIiIGhlaWdodD0iMjIiIHZpZXdCb3g9IjAgMCAyOCAyOCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CgkJPHBhdGggZD0iTTExLjQgMTguNkw2LjggMTRMMTEuNCA5LjRMMTAgOEw0IDE0TDEwIDIwTDExLjQgMTguNlpNMTYuNiAxOC42TDIxLjIgMTRMMTYuNiA5LjRMMTggOEwyNCAxNEwxOCAyMEwxNi42IDE4LjZWMTguNloiLz4KCTwvZz4KPC9zdmc+Cg==);
  --jp-icon-console: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwMCAyMDAiPgogIDxnIGNsYXNzPSJqcC1pY29uLWJyYW5kMSBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiMwMjg4RDEiPgogICAgPHBhdGggZD0iTTIwIDE5LjhoMTYwdjE1OS45SDIweiIvPgogIDwvZz4KICA8ZyBjbGFzcz0ianAtaWNvbi1zZWxlY3RhYmxlLWludmVyc2UiIGZpbGw9IiNmZmYiPgogICAgPHBhdGggZD0iTTEwNSAxMjcuM2g0MHYxMi44aC00MHpNNTEuMSA3N0w3NCA5OS45bC0yMy4zIDIzLjMgMTAuNSAxMC41IDIzLjMtMjMuM0w5NSA5OS45IDg0LjUgODkuNCA2MS42IDY2LjV6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-copy: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMTggMTgiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTExLjksMUgzLjJDMi40LDEsMS43LDEuNywxLjcsMi41djEwLjJoMS41VjIuNWg4LjdWMXogTTE0LjEsMy45aC04Yy0wLjgsMC0xLjUsMC43LTEuNSwxLjV2MTAuMmMwLDAuOCwwLjcsMS41LDEuNSwxLjVoOCBjMC44LDAsMS41LTAuNywxLjUtMS41VjUuNEMxNS41LDQuNiwxNC45LDMuOSwxNC4xLDMuOXogTTE0LjEsMTUuNWgtOFY1LjRoOFYxNS41eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-cut: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTkuNjQgNy42NGMuMjMtLjUuMzYtMS4wNS4zNi0xLjY0IDAtMi4yMS0xLjc5LTQtNC00UzIgMy43OSAyIDZzMS43OSA0IDQgNGMuNTkgMCAxLjE0LS4xMyAxLjY0LS4zNkwxMCAxMmwtMi4zNiAyLjM2QzcuMTQgMTQuMTMgNi41OSAxNCA2IDE0Yy0yLjIxIDAtNCAxLjc5LTQgNHMxLjc5IDQgNCA0IDQtMS43OSA0LTRjMC0uNTktLjEzLTEuMTQtLjM2LTEuNjRMMTIgMTRsNyA3aDN2LTFMOS42NCA3LjY0ek02IDhjLTEuMSAwLTItLjg5LTItMnMuOS0yIDItMiAyIC44OSAyIDItLjkgMi0yIDJ6bTAgMTJjLTEuMSAwLTItLjg5LTItMnMuOS0yIDItMiAyIC44OSAyIDItLjkgMi0yIDJ6bTYtNy41Yy0uMjggMC0uNS0uMjItLjUtLjVzLjIyLS41LjUtLjUuNS4yMi41LjUtLjIyLjUtLjUuNXpNMTkgM2wtNiA2IDIgMiA3LTdWM3oiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-download: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE5IDloLTRWM0g5djZINWw3IDcgNy03ek01IDE4djJoMTR2LTJINXoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-edit: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTMgMTcuMjVWMjFoMy43NUwxNy44MSA5Ljk0bC0zLjc1LTMuNzVMMyAxNy4yNXpNMjAuNzEgNy4wNGMuMzktLjM5LjM5LTEuMDIgMC0xLjQxbC0yLjM0LTIuMzRjLS4zOS0uMzktMS4wMi0uMzktMS40MSAwbC0xLjgzIDEuODMgMy43NSAzLjc1IDEuODMtMS44M3oiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-ellipses: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPGNpcmNsZSBjeD0iNSIgY3k9IjEyIiByPSIyIi8+CiAgICA8Y2lyY2xlIGN4PSIxMiIgY3k9IjEyIiByPSIyIi8+CiAgICA8Y2lyY2xlIGN4PSIxOSIgY3k9IjEyIiByPSIyIi8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-extension: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTIwLjUgMTFIMTlWN2MwLTEuMS0uOS0yLTItMmgtNFYzLjVDMTMgMi4xMiAxMS44OCAxIDEwLjUgMVM4IDIuMTIgOCAzLjVWNUg0Yy0xLjEgMC0xLjk5LjktMS45OSAydjMuOEgzLjVjMS40OSAwIDIuNyAxLjIxIDIuNyAyLjdzLTEuMjEgMi43LTIuNyAyLjdIMlYyMGMwIDEuMS45IDIgMiAyaDMuOHYtMS41YzAtMS40OSAxLjIxLTIuNyAyLjctMi43IDEuNDkgMCAyLjcgMS4yMSAyLjcgMi43VjIySDE3YzEuMSAwIDItLjkgMi0ydi00aDEuNWMxLjM4IDAgMi41LTEuMTIgMi41LTIuNVMyMS44OCAxMSAyMC41IDExeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-fast-forward: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTQgMThsOC41LTZMNCA2djEyem05LTEydjEybDguNS02TDEzIDZ6Ii8+CiAgICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-file-upload: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTkgMTZoNnYtNmg0bC03LTctNyA3aDR6bS00IDJoMTR2Mkg1eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-file: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTkuMyA4LjJsLTUuNS01LjVjLS4zLS4zLS43LS41LTEuMi0uNUgzLjljLS44LjEtMS42LjktMS42IDEuOHYxNC4xYzAgLjkuNyAxLjYgMS42IDEuNmgxNC4yYy45IDAgMS42LS43IDEuNi0xLjZWOS40Yy4xLS41LS4xLS45LS40LTEuMnptLTUuOC0zLjNsMy40IDMuNmgtMy40VjQuOXptMy45IDEyLjdINC43Yy0uMSAwLS4yIDAtLjItLjJWNC43YzAtLjIuMS0uMy4yLS4zaDcuMnY0LjRzMCAuOC4zIDEuMWMuMy4zIDEuMS4zIDEuMS4zaDQuM3Y3LjJzLS4xLjItLjIuMnoiLz4KPC9zdmc+Cg==);
  --jp-icon-filter-list: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEwIDE4aDR2LTJoLTR2MnpNMyA2djJoMThWNkgzem0zIDdoMTJ2LTJINnYyeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-folder: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTAgNEg0Yy0xLjEgMC0xLjk5LjktMS45OSAyTDIgMThjMCAxLjEuOSAyIDIgMmgxNmMxLjEgMCAyLS45IDItMlY4YzAtMS4xLS45LTItMi0yaC04bC0yLTJ6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-html5: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDUxMiA1MTIiPgogIDxwYXRoIGNsYXNzPSJqcC1pY29uMCBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiMwMDAiIGQ9Ik0xMDguNCAwaDIzdjIyLjhoMjEuMlYwaDIzdjY5aC0yM1Y0NmgtMjF2MjNoLTIzLjJNMjA2IDIzaC0yMC4zVjBoNjMuN3YyM0gyMjl2NDZoLTIzbTUzLjUtNjloMjQuMWwxNC44IDI0LjNMMzEzLjIgMGgyNC4xdjY5aC0yM1YzNC44bC0xNi4xIDI0LjgtMTYuMS0yNC44VjY5aC0yMi42bTg5LjItNjloMjN2NDYuMmgzMi42VjY5aC01NS42Ii8+CiAgPHBhdGggY2xhc3M9ImpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iI2U0NGQyNiIgZD0iTTEwNy42IDQ3MWwtMzMtMzcwLjRoMzYyLjhsLTMzIDM3MC4yTDI1NS43IDUxMiIvPgogIDxwYXRoIGNsYXNzPSJqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiNmMTY1MjkiIGQ9Ik0yNTYgNDgwLjVWMTMxaDE0OC4zTDM3NiA0NDciLz4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1zZWxlY3RhYmxlLWludmVyc2UiIGZpbGw9IiNlYmViZWIiIGQ9Ik0xNDIgMTc2LjNoMTE0djQ1LjRoLTY0LjJsNC4yIDQ2LjVoNjB2NDUuM0gxNTQuNG0yIDIyLjhIMjAybDMuMiAzNi4zIDUwLjggMTMuNnY0Ny40bC05My4yLTI2Ii8+CiAgPHBhdGggY2xhc3M9ImpwLWljb24tc2VsZWN0YWJsZS1pbnZlcnNlIiBmaWxsPSIjZmZmIiBkPSJNMzY5LjYgMTc2LjNIMjU1Ljh2NDUuNGgxMDkuNm0tNC4xIDQ2LjVIMjU1Ljh2NDUuNGg1NmwtNS4zIDU5LTUwLjcgMTMuNnY0Ny4ybDkzLTI1LjgiLz4KPC9zdmc+Cg==);
  --jp-icon-image: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1icmFuZDQganAtaWNvbi1zZWxlY3RhYmxlLWludmVyc2UiIGZpbGw9IiNGRkYiIGQ9Ik0yLjIgMi4yaDE3LjV2MTcuNUgyLjJ6Ii8+CiAgPHBhdGggY2xhc3M9ImpwLWljb24tYnJhbmQwIGpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iIzNGNTFCNSIgZD0iTTIuMiAyLjJ2MTcuNWgxNy41bC4xLTE3LjVIMi4yem0xMi4xIDIuMmMxLjIgMCAyLjIgMSAyLjIgMi4ycy0xIDIuMi0yLjIgMi4yLTIuMi0xLTIuMi0yLjIgMS0yLjIgMi4yLTIuMnpNNC40IDE3LjZsMy4zLTguOCAzLjMgNi42IDIuMi0zLjIgNC40IDUuNEg0LjR6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-inspector: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMjAgNEg0Yy0xLjEgMC0xLjk5LjktMS45OSAyTDIgMThjMCAxLjEuOSAyIDIgMmgxNmMxLjEgMCAyLS45IDItMlY2YzAtMS4xLS45LTItMi0yem0tNSAxNEg0di00aDExdjR6bTAtNUg0VjloMTF2NHptNSA1aC00VjloNHY5eiIvPgo8L3N2Zz4K);
  --jp-icon-json: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbi13YXJuMSBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiNGOUE4MjUiPgogICAgPHBhdGggZD0iTTIwLjIgMTEuOGMtMS42IDAtMS43LjUtMS43IDEgMCAuNC4xLjkuMSAxLjMuMS41LjEuOS4xIDEuMyAwIDEuNy0xLjQgMi4zLTMuNSAyLjNoLS45di0xLjloLjVjMS4xIDAgMS40IDAgMS40LS44IDAtLjMgMC0uNi0uMS0xIDAtLjQtLjEtLjgtLjEtMS4yIDAtMS4zIDAtMS44IDEuMy0yLTEuMy0uMi0xLjMtLjctMS4zLTIgMC0uNC4xLS44LjEtMS4yLjEtLjQuMS0uNy4xLTEgMC0uOC0uNC0uNy0xLjQtLjhoLS41VjQuMWguOWMyLjIgMCAzLjUuNyAzLjUgMi4zIDAgLjQtLjEuOS0uMSAxLjMtLjEuNS0uMS45LS4xIDEuMyAwIC41LjIgMSAxLjcgMXYxLjh6TTEuOCAxMC4xYzEuNiAwIDEuNy0uNSAxLjctMSAwLS40LS4xLS45LS4xLTEuMy0uMS0uNS0uMS0uOS0uMS0xLjMgMC0xLjYgMS40LTIuMyAzLjUtMi4zaC45djEuOWgtLjVjLTEgMC0xLjQgMC0xLjQuOCAwIC4zIDAgLjYuMSAxIDAgLjIuMS42LjEgMSAwIDEuMyAwIDEuOC0xLjMgMkM2IDExLjIgNiAxMS43IDYgMTNjMCAuNC0uMS44LS4xIDEuMi0uMS4zLS4xLjctLjEgMSAwIC44LjMuOCAxLjQuOGguNXYxLjloLS45Yy0yLjEgMC0zLjUtLjYtMy41LTIuMyAwLS40LjEtLjkuMS0xLjMuMS0uNS4xLS45LjEtMS4zIDAtLjUtLjItMS0xLjctMXYtMS45eiIvPgogICAgPGNpcmNsZSBjeD0iMTEiIGN5PSIxMy44IiByPSIyLjEiLz4KICAgIDxjaXJjbGUgY3g9IjExIiBjeT0iOC4yIiByPSIyLjEiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-jupyter-favicon: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTUyIiBoZWlnaHQ9IjE2NSIgdmlld0JveD0iMCAwIDE1MiAxNjUiIHZlcnNpb249IjEuMSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbi13YXJuMCIgZmlsbD0iI0YzNzcyNiI+CiAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgwLjA3ODk0NywgMTEwLjU4MjkyNykiIGQ9Ik03NS45NDIyODQyLDI5LjU4MDQ1NjEgQzQzLjMwMjM5NDcsMjkuNTgwNDU2MSAxNC43OTY3ODMyLDE3LjY1MzQ2MzQgMCwwIEM1LjUxMDgzMjExLDE1Ljg0MDY4MjkgMTUuNzgxNTM4OSwyOS41NjY3NzMyIDI5LjM5MDQ5NDcsMzkuMjc4NDE3MSBDNDIuOTk5Nyw0OC45ODk4NTM3IDU5LjI3MzcsNTQuMjA2NzgwNSA3NS45NjA1Nzg5LDU0LjIwNjc4MDUgQzkyLjY0NzQ1NzksNTQuMjA2NzgwNSAxMDguOTIxNDU4LDQ4Ljk4OTg1MzcgMTIyLjUzMDY2MywzOS4yNzg0MTcxIEMxMzYuMTM5NDUzLDI5LjU2Njc3MzIgMTQ2LjQxMDI4NCwxNS44NDA2ODI5IDE1MS45MjExNTgsMCBDMTM3LjA4Nzg2OCwxNy42NTM0NjM0IDEwOC41ODI1ODksMjkuNTgwNDU2MSA3NS45NDIyODQyLDI5LjU4MDQ1NjEgTDc1Ljk0MjI4NDIsMjkuNTgwNDU2MSBaIiAvPgogICAgPHBhdGggdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMC4wMzczNjgsIDAuNzA0ODc4KSIgZD0iTTc1Ljk3ODQ1NzksMjQuNjI2NDA3MyBDMTA4LjYxODc2MywyNC42MjY0MDczIDEzNy4xMjQ0NTgsMzYuNTUzNDQxNSAxNTEuOTIxMTU4LDU0LjIwNjc4MDUgQzE0Ni40MTAyODQsMzguMzY2MjIyIDEzNi4xMzk0NTMsMjQuNjQwMTMxNyAxMjIuNTMwNjYzLDE0LjkyODQ4NzggQzEwOC45MjE0NTgsNS4yMTY4NDM5IDkyLjY0NzQ1NzksMCA3NS45NjA1Nzg5LDAgQzU5LjI3MzcsMCA0Mi45OTk3LDUuMjE2ODQzOSAyOS4zOTA0OTQ3LDE0LjkyODQ4NzggQzE1Ljc4MTUzODksMjQuNjQwMTMxNyA1LjUxMDgzMjExLDM4LjM2NjIyMiAwLDU0LjIwNjc4MDUgQzE0LjgzMzA4MTYsMzYuNTg5OTI5MyA0My4zMzg1Njg0LDI0LjYyNjQwNzMgNzUuOTc4NDU3OSwyNC42MjY0MDczIEw3NS45Nzg0NTc5LDI0LjYyNjQwNzMgWiIgLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-jupyter: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMzkiIGhlaWdodD0iNTEiIHZpZXdCb3g9IjAgMCAzOSA1MSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgtMTYzOCAtMjI4MSkiPgogICAgPGcgY2xhc3M9ImpwLWljb24td2FybjAiIGZpbGw9IiNGMzc3MjYiPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjM5Ljc0IDIzMTEuOTgpIiBkPSJNIDE4LjI2NDYgNy4xMzQxMUMgMTAuNDE0NSA3LjEzNDExIDMuNTU4NzIgNC4yNTc2IDAgMEMgMS4zMjUzOSAzLjgyMDQgMy43OTU1NiA3LjEzMDgxIDcuMDY4NiA5LjQ3MzAzQyAxMC4zNDE3IDExLjgxNTIgMTQuMjU1NyAxMy4wNzM0IDE4LjI2OSAxMy4wNzM0QyAyMi4yODIzIDEzLjA3MzQgMjYuMTk2MyAxMS44MTUyIDI5LjQ2OTQgOS40NzMwM0MgMzIuNzQyNCA3LjEzMDgxIDM1LjIxMjYgMy44MjA0IDM2LjUzOCAwQyAzMi45NzA1IDQuMjU3NiAyNi4xMTQ4IDcuMTM0MTEgMTguMjY0NiA3LjEzNDExWiIvPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjM5LjczIDIyODUuNDgpIiBkPSJNIDE4LjI3MzMgNS45MzkzMUMgMjYuMTIzNSA1LjkzOTMxIDMyLjk3OTMgOC44MTU4MyAzNi41MzggMTMuMDczNEMgMzUuMjEyNiA5LjI1MzAzIDMyLjc0MjQgNS45NDI2MiAyOS40Njk0IDMuNjAwNEMgMjYuMTk2MyAxLjI1ODE4IDIyLjI4MjMgMCAxOC4yNjkgMEMgMTQuMjU1NyAwIDEwLjM0MTcgMS4yNTgxOCA3LjA2ODYgMy42MDA0QyAzLjc5NTU2IDUuOTQyNjIgMS4zMjUzOSA5LjI1MzAzIDAgMTMuMDczNEMgMy41Njc0NSA4LjgyNDYzIDEwLjQyMzIgNS45MzkzMSAxOC4yNzMzIDUuOTM5MzFaIi8+CiAgICA8L2c+CiAgICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjY5LjMgMjI4MS4zMSkiIGQ9Ik0gNS44OTM1MyAyLjg0NEMgNS45MTg4OSAzLjQzMTY1IDUuNzcwODUgNC4wMTM2NyA1LjQ2ODE1IDQuNTE2NDVDIDUuMTY1NDUgNS4wMTkyMiA0LjcyMTY4IDUuNDIwMTUgNC4xOTI5OSA1LjY2ODUxQyAzLjY2NDMgNS45MTY4OCAzLjA3NDQ0IDYuMDAxNTEgMi40OTgwNSA1LjkxMTcxQyAxLjkyMTY2IDUuODIxOSAxLjM4NDYzIDUuNTYxNyAwLjk1NDg5OCA1LjE2NDAxQyAwLjUyNTE3IDQuNzY2MzMgMC4yMjIwNTYgNC4yNDkwMyAwLjA4MzkwMzcgMy42Nzc1N0MgLTAuMDU0MjQ4MyAzLjEwNjExIC0wLjAyMTIzIDIuNTA2MTcgMC4xNzg3ODEgMS45NTM2NEMgMC4zNzg3OTMgMS40MDExIDAuNzM2ODA5IDAuOTIwODE3IDEuMjA3NTQgMC41NzM1MzhDIDEuNjc4MjYgMC4yMjYyNTkgMi4yNDA1NSAwLjAyNzU5MTkgMi44MjMyNiAwLjAwMjY3MjI5QyAzLjYwMzg5IC0wLjAzMDcxMTUgNC4zNjU3MyAwLjI0OTc4OSA0Ljk0MTQyIDAuNzgyNTUxQyA1LjUxNzExIDEuMzE1MzEgNS44NTk1NiAyLjA1Njc2IDUuODkzNTMgMi44NDRaIi8+CiAgICAgIDxwYXRoIHRyYW5zZm9ybT0idHJhbnNsYXRlKDE2MzkuOCAyMzIzLjgxKSIgZD0iTSA3LjQyNzg5IDMuNTgzMzhDIDcuNDYwMDggNC4zMjQzIDcuMjczNTUgNS4wNTgxOSA2Ljg5MTkzIDUuNjkyMTNDIDYuNTEwMzEgNi4zMjYwNyA1Ljk1MDc1IDYuODMxNTYgNS4yODQxMSA3LjE0NDZDIDQuNjE3NDcgNy40NTc2MyAzLjg3MzcxIDcuNTY0MTQgMy4xNDcwMiA3LjQ1MDYzQyAyLjQyMDMyIDcuMzM3MTIgMS43NDMzNiA3LjAwODcgMS4yMDE4NCA2LjUwNjk1QyAwLjY2MDMyOCA2LjAwNTIgMC4yNzg2MSA1LjM1MjY4IDAuMTA1MDE3IDQuNjMyMDJDIC0wLjA2ODU3NTcgMy45MTEzNSAtMC4wMjYyMzYxIDMuMTU0OTQgMC4yMjY2NzUgMi40NTg1NkMgMC40Nzk1ODcgMS43NjIxNyAwLjkzMTY5NyAxLjE1NzEzIDEuNTI1NzYgMC43MjAwMzNDIDIuMTE5ODMgMC4yODI5MzUgMi44MjkxNCAwLjAzMzQzOTUgMy41NjM4OSAwLjAwMzEzMzQ0QyA0LjU0NjY3IC0wLjAzNzQwMzMgNS41MDUyOSAwLjMxNjcwNiA2LjIyOTYxIDAuOTg3ODM1QyA2Ljk1MzkzIDEuNjU4OTYgNy4zODQ4NCAyLjU5MjM1IDcuNDI3ODkgMy41ODMzOEwgNy40Mjc4OSAzLjU4MzM4WiIvPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjM4LjM2IDIyODYuMDYpIiBkPSJNIDIuMjc0NzEgNC4zOTYyOUMgMS44NDM2MyA0LjQxNTA4IDEuNDE2NzEgNC4zMDQ0NSAxLjA0Nzk5IDQuMDc4NDNDIDAuNjc5MjY4IDMuODUyNCAwLjM4NTMyOCAzLjUyMTE0IDAuMjAzMzcxIDMuMTI2NTZDIDAuMDIxNDEzNiAyLjczMTk4IC0wLjA0MDM3OTggMi4yOTE4MyAwLjAyNTgxMTYgMS44NjE4MUMgMC4wOTIwMDMxIDEuNDMxOCAwLjI4MzIwNCAxLjAzMTI2IDAuNTc1MjEzIDAuNzEwODgzQyAwLjg2NzIyMiAwLjM5MDUxIDEuMjQ2OTEgMC4xNjQ3MDggMS42NjYyMiAwLjA2MjA1OTJDIDIuMDg1NTMgLTAuMDQwNTg5NyAyLjUyNTYxIC0wLjAxNTQ3MTQgMi45MzA3NiAwLjEzNDIzNUMgMy4zMzU5MSAwLjI4Mzk0MSAzLjY4NzkyIDAuNTUxNTA1IDMuOTQyMjIgMC45MDMwNkMgNC4xOTY1MiAxLjI1NDYyIDQuMzQxNjkgMS42NzQzNiA0LjM1OTM1IDIuMTA5MTZDIDQuMzgyOTkgMi42OTEwNyA0LjE3Njc4IDMuMjU4NjkgMy43ODU5NyAzLjY4NzQ2QyAzLjM5NTE2IDQuMTE2MjQgMi44NTE2NiA0LjM3MTE2IDIuMjc0NzEgNC4zOTYyOUwgMi4yNzQ3MSA0LjM5NjI5WiIvPgogICAgPC9nPgogIDwvZz4+Cjwvc3ZnPgo=);
  --jp-icon-jupyterlab-wordmark: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyMDAiIHZpZXdCb3g9IjAgMCAxODYwLjggNDc1Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiM0RTRFNEUiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDQ4MC4xMzY0MDEsIDY0LjI3MTQ5MykiPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMC4wMDAwMDAsIDU4Ljg3NTU2NikiPgogICAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgwLjA4NzYwMywgMC4xNDAyOTQpIj4KICAgICAgICA8cGF0aCBkPSJNLTQyNi45LDE2OS44YzAsNDguNy0zLjcsNjQuNy0xMy42LDc2LjRjLTEwLjgsMTAtMjUsMTUuNS0zOS43LDE1LjVsMy43LDI5IGMyMi44LDAuMyw0NC44LTcuOSw2MS45LTIzLjFjMTcuOC0xOC41LDI0LTQ0LjEsMjQtODMuM1YwSC00Mjd2MTcwLjFMLTQyNi45LDE2OS44TC00MjYuOSwxNjkuOHoiLz4KICAgICAgPC9nPgogICAgPC9nPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMTU1LjA0NTI5NiwgNTYuODM3MTA0KSI+CiAgICAgIDxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDEuNTYyNDUzLCAxLjc5OTg0MikiPgogICAgICAgIDxwYXRoIGQ9Ik0tMzEyLDE0OGMwLDIxLDAsMzkuNSwxLjcsNTUuNGgtMzEuOGwtMi4xLTMzLjNoLTAuOGMtNi43LDExLjYtMTYuNCwyMS4zLTI4LDI3LjkgYy0xMS42LDYuNi0yNC44LDEwLTM4LjIsOS44Yy0zMS40LDAtNjktMTcuNy02OS04OVYwaDM2LjR2MTEyLjdjMCwzOC43LDExLjYsNjQuNyw0NC42LDY0LjdjMTAuMy0wLjIsMjAuNC0zLjUsMjguOS05LjQgYzguNS01LjksMTUuMS0xNC4zLDE4LjktMjMuOWMyLjItNi4xLDMuMy0xMi41LDMuMy0xOC45VjAuMmgzNi40VjE0OEgtMzEyTC0zMTIsMTQ4eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgzOTAuMDEzMzIyLCA1My40Nzk2MzgpIj4KICAgICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMS43MDY0NTgsIDAuMjMxNDI1KSI+CiAgICAgICAgPHBhdGggZD0iTS00NzguNiw3MS40YzAtMjYtMC44LTQ3LTEuNy02Ni43aDMyLjdsMS43LDM0LjhoMC44YzcuMS0xMi41LDE3LjUtMjIuOCwzMC4xLTI5LjcgYzEyLjUtNywyNi43LTEwLjMsNDEtOS44YzQ4LjMsMCw4NC43LDQxLjcsODQuNywxMDMuM2MwLDczLjEtNDMuNywxMDkuMi05MSwxMDkuMmMtMTIuMSwwLjUtMjQuMi0yLjItMzUtNy44IGMtMTAuOC01LjYtMTkuOS0xMy45LTI2LjYtMjQuMmgtMC44VjI5MWgtMzZ2LTIyMEwtNDc4LjYsNzEuNEwtNDc4LjYsNzEuNHogTS00NDIuNiwxMjUuNmMwLjEsNS4xLDAuNiwxMC4xLDEuNywxNS4xIGMzLDEyLjMsOS45LDIzLjMsMTkuOCwzMS4xYzkuOSw3LjgsMjIuMSwxMi4xLDM0LjcsMTIuMWMzOC41LDAsNjAuNy0zMS45LDYwLjctNzguNWMwLTQwLjctMjEuMS03NS42LTU5LjUtNzUuNiBjLTEyLjksMC40LTI1LjMsNS4xLTM1LjMsMTMuNGMtOS45LDguMy0xNi45LDE5LjctMTkuNiwzMi40Yy0xLjUsNC45LTIuMywxMC0yLjUsMTUuMVYxMjUuNkwtNDQyLjYsMTI1LjZMLTQ0Mi42LDEyNS42eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSg2MDYuNzQwNzI2LCA1Ni44MzcxMDQpIj4KICAgICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMC43NTEyMjYsIDEuOTg5Mjk5KSI+CiAgICAgICAgPHBhdGggZD0iTS00NDAuOCwwbDQzLjcsMTIwLjFjNC41LDEzLjQsOS41LDI5LjQsMTIuOCw0MS43aDAuOGMzLjctMTIuMiw3LjktMjcuNywxMi44LTQyLjQgbDM5LjctMTE5LjJoMzguNUwtMzQ2LjksMTQ1Yy0yNiw2OS43LTQzLjcsMTA1LjQtNjguNiwxMjcuMmMtMTIuNSwxMS43LTI3LjksMjAtNDQuNiwyMy45bC05LjEtMzEuMSBjMTEuNy0zLjksMjIuNS0xMC4xLDMxLjgtMTguMWMxMy4yLTExLjEsMjMuNy0yNS4yLDMwLjYtNDEuMmMxLjUtMi44LDIuNS01LjcsMi45LTguOGMtMC4zLTMuMy0xLjItNi42LTIuNS05LjdMLTQ4MC4yLDAuMSBoMzkuN0wtNDQwLjgsMEwtNDQwLjgsMHoiLz4KICAgICAgPC9nPgogICAgPC9nPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoODIyLjc0ODEwNCwgMC4wMDAwMDApIj4KICAgICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMS40NjQwNTAsIDAuMzc4OTE0KSI+CiAgICAgICAgPHBhdGggZD0iTS00MTMuNywwdjU4LjNoNTJ2MjguMmgtNTJWMTk2YzAsMjUsNywzOS41LDI3LjMsMzkuNWM3LjEsMC4xLDE0LjItMC43LDIxLjEtMi41IGwxLjcsMjcuN2MtMTAuMywzLjctMjEuMyw1LjQtMzIuMiw1Yy03LjMsMC40LTE0LjYtMC43LTIxLjMtMy40Yy02LjgtMi43LTEyLjktNi44LTE3LjktMTIuMWMtMTAuMy0xMC45LTE0LjEtMjktMTQuMS01Mi45IFY4Ni41aC0zMVY1OC4zaDMxVjkuNkwtNDEzLjcsMEwtNDEzLjcsMHoiLz4KICAgICAgPC9nPgogICAgPC9nPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoOTc0LjQzMzI4NiwgNTMuNDc5NjM4KSI+CiAgICAgIDxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDAuOTkwMDM0LCAwLjYxMDMzOSkiPgogICAgICAgIDxwYXRoIGQ9Ik0tNDQ1LjgsMTEzYzAuOCw1MCwzMi4yLDcwLjYsNjguNiw3MC42YzE5LDAuNiwzNy45LTMsNTUuMy0xMC41bDYuMiwyNi40IGMtMjAuOSw4LjktNDMuNSwxMy4xLTY2LjIsMTIuNmMtNjEuNSwwLTk4LjMtNDEuMi05OC4zLTEwMi41Qy00ODAuMiw0OC4yLTQ0NC43LDAtMzg2LjUsMGM2NS4yLDAsODIuNyw1OC4zLDgyLjcsOTUuNyBjLTAuMSw1LjgtMC41LDExLjUtMS4yLDE3LjJoLTE0MC42SC00NDUuOEwtNDQ1LjgsMTEzeiBNLTMzOS4yLDg2LjZjMC40LTIzLjUtOS41LTYwLjEtNTAuNC02MC4xIGMtMzYuOCwwLTUyLjgsMzQuNC01NS43LDYwLjFILTMzOS4yTC0zMzkuMiw4Ni42TC0zMzkuMiw4Ni42eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxMjAxLjk2MTA1OCwgNTMuNDc5NjM4KSI+CiAgICAgIDxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDEuMTc5NjQwLCAwLjcwNTA2OCkiPgogICAgICAgIDxwYXRoIGQ9Ik0tNDc4LjYsNjhjMC0yMy45LTAuNC00NC41LTEuNy02My40aDMxLjhsMS4yLDM5LjloMS43YzkuMS0yNy4zLDMxLTQ0LjUsNTUuMy00NC41IGMzLjUtMC4xLDcsMC40LDEwLjMsMS4ydjM0LjhjLTQuMS0wLjktOC4yLTEuMy0xMi40LTEuMmMtMjUuNiwwLTQzLjcsMTkuNy00OC43LDQ3LjRjLTEsNS43LTEuNiwxMS41LTEuNywxNy4ydjEwOC4zaC0zNlY2OCBMLTQ3OC42LDY4eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgPC9nPgoKICA8ZyBjbGFzcz0ianAtaWNvbi13YXJuMCIgZmlsbD0iI0YzNzcyNiI+CiAgICA8cGF0aCBkPSJNMTM1Mi4zLDMyNi4yaDM3VjI4aC0zN1YzMjYuMnogTTE2MDQuOCwzMjYuMmMtMi41LTEzLjktMy40LTMxLjEtMy40LTQ4Ljd2LTc2IGMwLTQwLjctMTUuMS04My4xLTc3LjMtODMuMWMtMjUuNiwwLTUwLDcuMS02Ni44LDE4LjFsOC40LDI0LjRjMTQuMy05LjIsMzQtMTUuMSw1My0xNS4xYzQxLjYsMCw0Ni4yLDMwLjIsNDYuMiw0N3Y0LjIgYy03OC42LTAuNC0xMjIuMywyNi41LTEyMi4zLDc1LjZjMCwyOS40LDIxLDU4LjQsNjIuMiw1OC40YzI5LDAsNTAuOS0xNC4zLDYyLjItMzAuMmgxLjNsMi45LDI1LjZIMTYwNC44eiBNMTU2NS43LDI1Ny43IGMwLDMuOC0wLjgsOC0yLjEsMTEuOGMtNS45LDE3LjItMjIuNywzNC00OS4yLDM0Yy0xOC45LDAtMzQuOS0xMS4zLTM0LjktMzUuM2MwLTM5LjUsNDUuOC00Ni42LDg2LjItNDUuOFYyNTcuN3ogTTE2OTguNSwzMjYuMiBsMS43LTMzLjZoMS4zYzE1LjEsMjYuOSwzOC43LDM4LjIsNjguMSwzOC4yYzQ1LjQsMCw5MS4yLTM2LjEsOTEuMi0xMDguOGMwLjQtNjEuNy0zNS4zLTEwMy43LTg1LjctMTAzLjcgYy0zMi44LDAtNTYuMywxNC43LTY5LjMsMzcuNGgtMC44VjI4aC0zNi42djI0NS43YzAsMTguMS0wLjgsMzguNi0xLjcsNTIuNUgxNjk4LjV6IE0xNzA0LjgsMjA4LjJjMC01LjksMS4zLTEwLjksMi4xLTE1LjEgYzcuNi0yOC4xLDMxLjEtNDUuNCw1Ni4zLTQ1LjRjMzkuNSwwLDYwLjUsMzQuOSw2MC41LDc1LjZjMCw0Ni42LTIzLjEsNzguMS02MS44LDc4LjFjLTI2LjksMC00OC4zLTE3LjYtNTUuNS00My4zIGMtMC44LTQuMi0xLjctOC44LTEuNy0xMy40VjIwOC4yeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-kernel: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgZmlsbD0iIzYxNjE2MSIgZD0iTTE1IDlIOXY2aDZWOXptLTIgNGgtMnYtMmgydjJ6bTgtMlY5aC0yVjdjMC0xLjEtLjktMi0yLTJoLTJWM2gtMnYyaC0yVjNIOXYySDdjLTEuMSAwLTIgLjktMiAydjJIM3YyaDJ2MkgzdjJoMnYyYzAgMS4xLjkgMiAyIDJoMnYyaDJ2LTJoMnYyaDJ2LTJoMmMxLjEgMCAyLS45IDItMnYtMmgydi0yaC0ydi0yaDJ6bS00IDZIN1Y3aDEwdjEweiIvPgo8L3N2Zz4K);
  --jp-icon-keyboard: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMjAgNUg0Yy0xLjEgMC0xLjk5LjktMS45OSAyTDIgMTdjMCAxLjEuOSAyIDIgMmgxNmMxLjEgMCAyLS45IDItMlY3YzAtMS4xLS45LTItMi0yem0tOSAzaDJ2MmgtMlY4em0wIDNoMnYyaC0ydi0yek04IDhoMnYySDhWOHptMCAzaDJ2Mkg4di0yem0tMSAySDV2LTJoMnYyem0wLTNINVY4aDJ2MnptOSA3SDh2LTJoOHYyem0wLTRoLTJ2LTJoMnYyem0wLTNoLTJWOGgydjJ6bTMgM2gtMnYtMmgydjJ6bTAtM2gtMlY4aDJ2MnoiLz4KPC9zdmc+Cg==);
  --jp-icon-launcher: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTkgMTlINVY1aDdWM0g1YTIgMiAwIDAwLTIgMnYxNGEyIDIgMCAwMDIgMmgxNGMxLjEgMCAyLS45IDItMnYtN2gtMnY3ek0xNCAzdjJoMy41OWwtOS44MyA5LjgzIDEuNDEgMS40MUwxOSA2LjQxVjEwaDJWM2gtN3oiLz4KPC9zdmc+Cg==);
  --jp-icon-line-form: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxwYXRoIGZpbGw9IndoaXRlIiBkPSJNNS44OCA0LjEyTDEzLjc2IDEybC03Ljg4IDcuODhMOCAyMmwxMC0xMEw4IDJ6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-link: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTMuOSAxMmMwLTEuNzEgMS4zOS0zLjEgMy4xLTMuMWg0VjdIN2MtMi43NiAwLTUgMi4yNC01IDVzMi4yNCA1IDUgNWg0di0xLjlIN2MtMS43MSAwLTMuMS0xLjM5LTMuMS0zLjF6TTggMTNoOHYtMkg4djJ6bTktNmgtNHYxLjloNGMxLjcxIDAgMy4xIDEuMzkgMy4xIDMuMXMtMS4zOSAzLjEtMy4xIDMuMWgtNFYxN2g0YzIuNzYgMCA1LTIuMjQgNS01cy0yLjI0LTUtNS01eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-list: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiM2MTYxNjEiIGQ9Ik0xOSA1djE0SDVWNWgxNG0xLjEtMkgzLjljLS41IDAtLjkuNC0uOS45djE2LjJjMCAuNC40LjkuOS45aDE2LjJjLjQgMCAuOS0uNS45LS45VjMuOWMwLS41LS41LS45LS45LS45ek0xMSA3aDZ2MmgtNlY3em0wIDRoNnYyaC02di0yem0wIDRoNnYyaC02ek03IDdoMnYySDd6bTAgNGgydjJIN3ptMCA0aDJ2Mkg3eiIvPgo8L3N2Zz4=);
  --jp-icon-listings-info: url(data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iaXNvLTg4NTktMSI/Pg0KPHN2ZyB2ZXJzaW9uPSIxLjEiIGlkPSJDYXBhXzEiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIgeG1sbnM6eGxpbms9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkveGxpbmsiIHg9IjBweCIgeT0iMHB4Ig0KCSB2aWV3Qm94PSIwIDAgNTAuOTc4IDUwLjk3OCIgc3R5bGU9ImVuYWJsZS1iYWNrZ3JvdW5kOm5ldyAwIDAgNTAuOTc4IDUwLjk3ODsiIHhtbDpzcGFjZT0icHJlc2VydmUiPg0KPGc+DQoJPGc+DQoJCTxnPg0KCQkJPHBhdGggc3R5bGU9ImZpbGw6IzAxMDAwMjsiIGQ9Ik00My41Miw3LjQ1OEMzOC43MTEsMi42NDgsMzIuMzA3LDAsMjUuNDg5LDBDMTguNjcsMCwxMi4yNjYsMi42NDgsNy40NTgsNy40NTgNCgkJCQljLTkuOTQzLDkuOTQxLTkuOTQzLDI2LjExOSwwLDM2LjA2MmM0LjgwOSw0LjgwOSwxMS4yMTIsNy40NTYsMTguMDMxLDcuNDU4YzAsMCwwLjAwMSwwLDAuMDAyLDANCgkJCQljNi44MTYsMCwxMy4yMjEtMi42NDgsMTguMDI5LTcuNDU4YzQuODA5LTQuODA5LDcuNDU3LTExLjIxMiw3LjQ1Ny0xOC4wM0M1MC45NzcsMTguNjcsNDguMzI4LDEyLjI2Niw0My41Miw3LjQ1OHoNCgkJCQkgTTQyLjEwNiw0Mi4xMDVjLTQuNDMyLDQuNDMxLTEwLjMzMiw2Ljg3Mi0xNi42MTUsNi44NzJoLTAuMDAyYy02LjI4NS0wLjAwMS0xMi4xODctMi40NDEtMTYuNjE3LTYuODcyDQoJCQkJYy05LjE2Mi05LjE2My05LjE2Mi0yNC4wNzEsMC0zMy4yMzNDMTMuMzAzLDQuNDQsMTkuMjA0LDIsMjUuNDg5LDJjNi4yODQsMCwxMi4xODYsMi40NCwxNi42MTcsNi44NzINCgkJCQljNC40MzEsNC40MzEsNi44NzEsMTAuMzMyLDYuODcxLDE2LjYxN0M0OC45NzcsMzEuNzcyLDQ2LjUzNiwzNy42NzUsNDIuMTA2LDQyLjEwNXoiLz4NCgkJPC9nPg0KCQk8Zz4NCgkJCTxwYXRoIHN0eWxlPSJmaWxsOiMwMTAwMDI7IiBkPSJNMjMuNTc4LDMyLjIxOGMtMC4wMjMtMS43MzQsMC4xNDMtMy4wNTksMC40OTYtMy45NzJjMC4zNTMtMC45MTMsMS4xMS0xLjk5NywyLjI3Mi0zLjI1Mw0KCQkJCWMwLjQ2OC0wLjUzNiwwLjkyMy0xLjA2MiwxLjM2Ny0xLjU3NWMwLjYyNi0wLjc1MywxLjEwNC0xLjQ3OCwxLjQzNi0yLjE3NWMwLjMzMS0wLjcwNywwLjQ5NS0xLjU0MSwwLjQ5NS0yLjUNCgkJCQljMC0xLjA5Ni0wLjI2LTIuMDg4LTAuNzc5LTIuOTc5Yy0wLjU2NS0wLjg3OS0xLjUwMS0xLjMzNi0yLjgwNi0xLjM2OWMtMS44MDIsMC4wNTctMi45ODUsMC42NjctMy41NSwxLjgzMg0KCQkJCWMtMC4zMDEsMC41MzUtMC41MDMsMS4xNDEtMC42MDcsMS44MTRjLTAuMTM5LDAuNzA3LTAuMjA3LDEuNDMyLTAuMjA3LDIuMTc0aC0yLjkzN2MtMC4wOTEtMi4yMDgsMC40MDctNC4xMTQsMS40OTMtNS43MTkNCgkJCQljMS4wNjItMS42NCwyLjg1NS0yLjQ4MSw1LjM3OC0yLjUyN2MyLjE2LDAuMDIzLDMuODc0LDAuNjA4LDUuMTQxLDEuNzU4YzEuMjc4LDEuMTYsMS45MjksMi43NjQsMS45NSw0LjgxMQ0KCQkJCWMwLDEuMTQyLTAuMTM3LDIuMTExLTAuNDEsMi45MTFjLTAuMzA5LDAuODQ1LTAuNzMxLDEuNTkzLTEuMjY4LDIuMjQzYy0wLjQ5MiwwLjY1LTEuMDY4LDEuMzE4LTEuNzMsMi4wMDINCgkJCQljLTAuNjUsMC42OTctMS4zMTMsMS40NzktMS45ODcsMi4zNDZjLTAuMjM5LDAuMzc3LTAuNDI5LDAuNzc3LTAuNTY1LDEuMTk5Yy0wLjE2LDAuOTU5LTAuMjE3LDEuOTUxLTAuMTcxLDIuOTc5DQoJCQkJQzI2LjU4OSwzMi4yMTgsMjMuNTc4LDMyLjIxOCwyMy41NzgsMzIuMjE4eiBNMjMuNTc4LDM4LjIydi0zLjQ4NGgzLjA3NnYzLjQ4NEgyMy41Nzh6Ii8+DQoJCTwvZz4NCgk8L2c+DQo8L2c+DQo8Zz4NCjwvZz4NCjxnPg0KPC9nPg0KPGc+DQo8L2c+DQo8Zz4NCjwvZz4NCjxnPg0KPC9nPg0KPGc+DQo8L2c+DQo8Zz4NCjwvZz4NCjxnPg0KPC9nPg0KPGc+DQo8L2c+DQo8Zz4NCjwvZz4NCjxnPg0KPC9nPg0KPGc+DQo8L2c+DQo8Zz4NCjwvZz4NCjxnPg0KPC9nPg0KPGc+DQo8L2c+DQo8L3N2Zz4NCg==);
  --jp-icon-markdown: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1jb250cmFzdDAganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjN0IxRkEyIiBkPSJNNSAxNC45aDEybC02LjEgNnptOS40LTYuOGMwLTEuMy0uMS0yLjktLjEtNC41LS40IDEuNC0uOSAyLjktMS4zIDQuM2wtMS4zIDQuM2gtMkw4LjUgNy45Yy0uNC0xLjMtLjctMi45LTEtNC4zLS4xIDEuNi0uMSAzLjItLjIgNC42TDcgMTIuNEg0LjhsLjctMTFoMy4zTDEwIDVjLjQgMS4yLjcgMi43IDEgMy45LjMtMS4yLjctMi42IDEtMy45bDEuMi0zLjdoMy4zbC42IDExaC0yLjRsLS4zLTQuMnoiLz4KPC9zdmc+Cg==);
  --jp-icon-new-folder: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTIwIDZoLThsLTItMkg0Yy0xLjExIDAtMS45OS44OS0xLjk5IDJMMiAxOGMwIDEuMTEuODkgMiAyIDJoMTZjMS4xMSAwIDItLjg5IDItMlY4YzAtMS4xMS0uODktMi0yLTJ6bS0xIDhoLTN2M2gtMnYtM2gtM3YtMmgzVjloMnYzaDN2MnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-not-trusted: url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI1IDI1Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgc3Ryb2tlPSIjMzMzMzMzIiBzdHJva2Utd2lkdGg9IjIiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDMgMykiIGQ9Ik0xLjg2MDk0IDExLjQ0MDlDMC44MjY0NDggOC43NzAyNyAwLjg2Mzc3OSA2LjA1NzY0IDEuMjQ5MDcgNC4xOTkzMkMyLjQ4MjA2IDMuOTMzNDcgNC4wODA2OCAzLjQwMzQ3IDUuNjAxMDIgMi44NDQ5QzcuMjM1NDkgMi4yNDQ0IDguODU2NjYgMS41ODE1IDkuOTg3NiAxLjA5NTM5QzExLjA1OTcgMS41ODM0MSAxMi42MDk0IDIuMjQ0NCAxNC4yMTggMi44NDMzOUMxNS43NTAzIDMuNDEzOTQgMTcuMzk5NSAzLjk1MjU4IDE4Ljc1MzkgNC4yMTM4NUMxOS4xMzY0IDYuMDcxNzcgMTkuMTcwOSA4Ljc3NzIyIDE4LjEzOSAxMS40NDA5QzE3LjAzMDMgMTQuMzAzMiAxNC42NjY4IDE3LjE4NDQgOS45OTk5OSAxOC45MzU0QzUuMzMzMTkgMTcuMTg0NCAyLjk2OTY4IDE0LjMwMzIgMS44NjA5NCAxMS40NDA5WiIvPgogICAgPHBhdGggY2xhc3M9ImpwLWljb24yIiBzdHJva2U9IiMzMzMzMzMiIHN0cm9rZS13aWR0aD0iMiIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoOS4zMTU5MiA5LjMyMDMxKSIgZD0iTTcuMzY4NDIgMEwwIDcuMzY0NzkiLz4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgc3Ryb2tlPSIjMzMzMzMzIiBzdHJva2Utd2lkdGg9IjIiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDkuMzE1OTIgMTYuNjgzNikgc2NhbGUoMSAtMSkiIGQ9Ik03LjM2ODQyIDBMMCA3LjM2NDc5Ii8+Cjwvc3ZnPgo=);
  --jp-icon-notebook: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbi13YXJuMCBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiNFRjZDMDAiPgogICAgPHBhdGggZD0iTTE4LjcgMy4zdjE1LjRIMy4zVjMuM2gxNS40bTEuNS0xLjVIMS44djE4LjNoMTguM2wuMS0xOC4zeiIvPgogICAgPHBhdGggZD0iTTE2LjUgMTYuNWwtNS40LTQuMy01LjYgNC4zdi0xMWgxMXoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-numbering: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjIiIGhlaWdodD0iMjIiIHZpZXdCb3g9IjAgMCAyOCAyOCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CgkJPHBhdGggZD0iTTQgMTlINlYxOS41SDVWMjAuNUg2VjIxSDRWMjJIN1YxOEg0VjE5Wk01IDEwSDZWNkg0VjdINVYxMFpNNCAxM0g1LjhMNCAxNS4xVjE2SDdWMTVINS4yTDcgMTIuOVYxMkg0VjEzWk05IDdWOUgyM1Y3SDlaTTkgMjFIMjNWMTlIOVYyMVpNOSAxNUgyM1YxM0g5VjE1WiIvPgoJPC9nPgo8L3N2Zz4K);
  --jp-icon-offline-bolt: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCIgd2lkdGg9IjE2Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyIDIuMDJjLTUuNTEgMC05Ljk4IDQuNDctOS45OCA5Ljk4czQuNDcgOS45OCA5Ljk4IDkuOTggOS45OC00LjQ3IDkuOTgtOS45OFMxNy41MSAyLjAyIDEyIDIuMDJ6TTExLjQ4IDIwdi02LjI2SDhMMTMgNHY2LjI2aDMuMzVMMTEuNDggMjB6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-palette: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE4IDEzVjIwSDRWNkg5LjAyQzkuMDcgNS4yOSA5LjI0IDQuNjIgOS41IDRINEMyLjkgNCAyIDQuOSAyIDZWMjBDMiAyMS4xIDIuOSAyMiA0IDIySDE4QzE5LjEgMjIgMjAgMjEuMSAyMCAyMFYxNUwxOCAxM1pNMTkuMyA4Ljg5QzE5Ljc0IDguMTkgMjAgNy4zOCAyMCA2LjVDMjAgNC4wMSAxNy45OSAyIDE1LjUgMkMxMy4wMSAyIDExIDQuMDEgMTEgNi41QzExIDguOTkgMTMuMDEgMTEgMTUuNDkgMTFDMTYuMzcgMTEgMTcuMTkgMTAuNzQgMTcuODggMTAuM0wyMSAxMy40MkwyMi40MiAxMkwxOS4zIDguODlaTTE1LjUgOUMxNC4xMiA5IDEzIDcuODggMTMgNi41QzEzIDUuMTIgMTQuMTIgNCAxNS41IDRDMTYuODggNCAxOCA1LjEyIDE4IDYuNUMxOCA3Ljg4IDE2Ljg4IDkgMTUuNSA5WiIvPgogICAgPHBhdGggZmlsbC1ydWxlPSJldmVub2RkIiBjbGlwLXJ1bGU9ImV2ZW5vZGQiIGQ9Ik00IDZIOS4wMTg5NEM5LjAwNjM5IDYuMTY1MDIgOSA2LjMzMTc2IDkgNi41QzkgOC44MTU3NyAxMC4yMTEgMTAuODQ4NyAxMi4wMzQzIDEySDlWMTRIMTZWMTIuOTgxMUMxNi41NzAzIDEyLjkzNzcgMTcuMTIgMTIuODIwNyAxNy42Mzk2IDEyLjYzOTZMMTggMTNWMjBINFY2Wk04IDhINlYxMEg4VjhaTTYgMTJIOFYxNEg2VjEyWk04IDE2SDZWMThIOFYxNlpNOSAxNkgxNlYxOEg5VjE2WiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-paste: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTE5IDJoLTQuMThDMTQuNC44NCAxMy4zIDAgMTIgMGMtMS4zIDAtMi40Ljg0LTIuODIgMkg1Yy0xLjEgMC0yIC45LTIgMnYxNmMwIDEuMS45IDIgMiAyaDE0YzEuMSAwIDItLjkgMi0yVjRjMC0xLjEtLjktMi0yLTJ6bS03IDBjLjU1IDAgMSAuNDUgMSAxcy0uNDUgMS0xIDEtMS0uNDUtMS0xIC40NS0xIDEtMXptNyAxOEg1VjRoMnYzaDEwVjRoMnYxNnoiLz4KICAgIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-pdf: url(data:image/svg+xml;base64,PHN2ZwogICB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyMiAyMiIgd2lkdGg9IjE2Ij4KICAgIDxwYXRoIHRyYW5zZm9ybT0icm90YXRlKDQ1KSIgY2xhc3M9ImpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iI0ZGMkEyQSIKICAgICAgIGQ9Im0gMjIuMzQ0MzY5LC0zLjAxNjM2NDIgaCA1LjYzODYwNCB2IDEuNTc5MjQzMyBoIC0zLjU0OTIyNyB2IDEuNTA4NjkyOTkgaCAzLjMzNzU3NiBWIDEuNjUwODE1NCBoIC0zLjMzNzU3NiB2IDMuNDM1MjYxMyBoIC0yLjA4OTM3NyB6IG0gLTcuMTM2NDQ0LDEuNTc5MjQzMyB2IDQuOTQzOTU0MyBoIDAuNzQ4OTIgcSAxLjI4MDc2MSwwIDEuOTUzNzAzLC0wLjYzNDk1MzUgMC42NzgzNjksLTAuNjM0OTUzNSAwLjY3ODM2OSwtMS44NDUxNjQxIDAsLTEuMjA0NzgzNTUgLTAuNjcyOTQyLC0xLjgzNDMxMDExIC0wLjY3Mjk0MiwtMC42Mjk1MjY1OSAtMS45NTkxMywtMC42Mjk1MjY1OSB6IG0gLTIuMDg5Mzc3LC0xLjU3OTI0MzMgaCAyLjIwMzM0MyBxIDEuODQ1MTY0LDAgMi43NDYwMzksMC4yNjU5MjA3IDAuOTA2MzAxLDAuMjYwNDkzNyAxLjU1MjEwOCwwLjg5MDAyMDMgMC41Njk4MywwLjU0ODEyMjMgMC44NDY2MDUsMS4yNjQ0ODAwNiAwLjI3Njc3NCwwLjcxNjM1NzgxIDAuMjc2Nzc0LDEuNjIyNjU4OTQgMCwwLjkxNzE1NTEgLTAuMjc2Nzc0LDEuNjM4OTM5OSAtMC4yNzY3NzUsMC43MTYzNTc4IC0wLjg0NjYwNSwxLjI2NDQ4IC0wLjY1MTIzNCwwLjYyOTUyNjYgLTEuNTYyOTYyLDAuODk1NDQ3MyAtMC45MTE3MjgsMC4yNjA0OTM3IC0yLjczNTE4NSwwLjI2MDQ5MzcgaCAtMi4yMDMzNDMgeiBtIC04LjE0NTg1NjUsMCBoIDMuNDY3ODIzIHEgMS41NDY2ODE2LDAgMi4zNzE1Nzg1LDAuNjg5MjIzIDAuODMwMzI0LDAuNjgzNzk2MSAwLjgzMDMyNCwxLjk1MzcwMzE0IDAsMS4yNzUzMzM5NyAtMC44MzAzMjQsMS45NjQ1NTcwNiBRIDkuOTg3MTk2MSwyLjI3NDkxNSA4LjQ0MDUxNDUsMi4yNzQ5MTUgSCA3LjA2MjA2ODQgViA1LjA4NjA3NjcgSCA0Ljk3MjY5MTUgWiBtIDIuMDg5Mzc2OSwxLjUxNDExOTkgdiAyLjI2MzAzOTQzIGggMS4xNTU5NDEgcSAwLjYwNzgxODgsMCAwLjkzODg2MjksLTAuMjkzMDU1NDcgMC4zMzEwNDQxLC0wLjI5ODQ4MjQxIDAuMzMxMDQ0MSwtMC44NDExNzc3MiAwLC0wLjU0MjY5NTMxIC0wLjMzMTA0NDEsLTAuODM1NzUwNzQgLTAuMzMxMDQ0MSwtMC4yOTMwNTU1IC0wLjkzODg2MjksLTAuMjkzMDU1NSB6IgovPgo8L3N2Zz4K);
  --jp-icon-python: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbi1icmFuZDAganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjMEQ0N0ExIj4KICAgIDxwYXRoIGQ9Ik0xMS4xIDYuOVY1LjhINi45YzAtLjUgMC0xLjMuMi0xLjYuNC0uNy44LTEuMSAxLjctMS40IDEuNy0uMyAyLjUtLjMgMy45LS4xIDEgLjEgMS45LjkgMS45IDEuOXY0LjJjMCAuNS0uOSAxLjYtMiAxLjZIOC44Yy0xLjUgMC0yLjQgMS40LTIuNCAyLjh2Mi4ySDQuN0MzLjUgMTUuMSAzIDE0IDMgMTMuMVY5Yy0uMS0xIC42LTIgMS44LTIgMS41LS4xIDYuMy0uMSA2LjMtLjF6Ii8+CiAgICA8cGF0aCBkPSJNMTAuOSAxNS4xdjEuMWg0LjJjMCAuNSAwIDEuMy0uMiAxLjYtLjQuNy0uOCAxLjEtMS43IDEuNC0xLjcuMy0yLjUuMy0zLjkuMS0xLS4xLTEuOS0uOS0xLjktMS45di00LjJjMC0uNS45LTEuNiAyLTEuNmgzLjhjMS41IDAgMi40LTEuNCAyLjQtMi44VjYuNmgxLjdDMTguNSA2LjkgMTkgOCAxOSA4LjlWMTNjMCAxLS43IDIuMS0xLjkgMi4xaC02LjJ6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-r-kernel: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1jb250cmFzdDMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjMjE5NkYzIiBkPSJNNC40IDIuNWMxLjItLjEgMi45LS4zIDQuOS0uMyAyLjUgMCA0LjEuNCA1LjIgMS4zIDEgLjcgMS41IDEuOSAxLjUgMy41IDAgMi0xLjQgMy41LTIuOSA0LjEgMS4yLjQgMS43IDEuNiAyLjIgMyAuNiAxLjkgMSAzLjkgMS4zIDQuNmgtMy44Yy0uMy0uNC0uOC0xLjctMS4yLTMuN3MtMS4yLTIuNi0yLjYtMi42aC0uOXY2LjRINC40VjIuNXptMy43IDYuOWgxLjRjMS45IDAgMi45LS45IDIuOS0yLjNzLTEtMi4zLTIuOC0yLjNjLS43IDAtMS4zIDAtMS42LjJ2NC41aC4xdi0uMXoiLz4KPC9zdmc+Cg==);
  --jp-icon-react: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMTUwIDE1MCA1NDEuOSAyOTUuMyI+CiAgPGcgY2xhc3M9ImpwLWljb24tYnJhbmQyIGpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iIzYxREFGQiI+CiAgICA8cGF0aCBkPSJNNjY2LjMgMjk2LjVjMC0zMi41LTQwLjctNjMuMy0xMDMuMS04Mi40IDE0LjQtNjMuNiA4LTExNC4yLTIwLjItMTMwLjQtNi41LTMuOC0xNC4xLTUuNi0yMi40LTUuNnYyMi4zYzQuNiAwIDguMy45IDExLjQgMi42IDEzLjYgNy44IDE5LjUgMzcuNSAxNC45IDc1LjctMS4xIDkuNC0yLjkgMTkuMy01LjEgMjkuNC0xOS42LTQuOC00MS04LjUtNjMuNS0xMC45LTEzLjUtMTguNS0yNy41LTM1LjMtNDEuNi01MCAzMi42LTMwLjMgNjMuMi00Ni45IDg0LTQ2LjlWNzhjLTI3LjUgMC02My41IDE5LjYtOTkuOSA1My42LTM2LjQtMzMuOC03Mi40LTUzLjItOTkuOS01My4ydjIyLjNjMjAuNyAwIDUxLjQgMTYuNSA4NCA0Ni42LTE0IDE0LjctMjggMzEuNC00MS4zIDQ5LjktMjIuNiAyLjQtNDQgNi4xLTYzLjYgMTEtMi4zLTEwLTQtMTkuNy01LjItMjktNC43LTM4LjIgMS4xLTY3LjkgMTQuNi03NS44IDMtMS44IDYuOS0yLjYgMTEuNS0yLjZWNzguNWMtOC40IDAtMTYgMS44LTIyLjYgNS42LTI4LjEgMTYuMi0zNC40IDY2LjctMTkuOSAxMzAuMS02Mi4yIDE5LjItMTAyLjcgNDkuOS0xMDIuNyA4Mi4zIDAgMzIuNSA0MC43IDYzLjMgMTAzLjEgODIuNC0xNC40IDYzLjYtOCAxMTQuMiAyMC4yIDEzMC40IDYuNSAzLjggMTQuMSA1LjYgMjIuNSA1LjYgMjcuNSAwIDYzLjUtMTkuNiA5OS45LTUzLjYgMzYuNCAzMy44IDcyLjQgNTMuMiA5OS45IDUzLjIgOC40IDAgMTYtMS44IDIyLjYtNS42IDI4LjEtMTYuMiAzNC40LTY2LjcgMTkuOS0xMzAuMSA2Mi0xOS4xIDEwMi41LTQ5LjkgMTAyLjUtODIuM3ptLTEzMC4yLTY2LjdjLTMuNyAxMi45LTguMyAyNi4yLTEzLjUgMzkuNS00LjEtOC04LjQtMTYtMTMuMS0yNC00LjYtOC05LjUtMTUuOC0xNC40LTIzLjQgMTQuMiAyLjEgMjcuOSA0LjcgNDEgNy45em0tNDUuOCAxMDYuNWMtNy44IDEzLjUtMTUuOCAyNi4zLTI0LjEgMzguMi0xNC45IDEuMy0zMCAyLTQ1LjIgMi0xNS4xIDAtMzAuMi0uNy00NS0xLjktOC4zLTExLjktMTYuNC0yNC42LTI0LjItMzgtNy42LTEzLjEtMTQuNS0yNi40LTIwLjgtMzkuOCA2LjItMTMuNCAxMy4yLTI2LjggMjAuNy0zOS45IDcuOC0xMy41IDE1LjgtMjYuMyAyNC4xLTM4LjIgMTQuOS0xLjMgMzAtMiA0NS4yLTIgMTUuMSAwIDMwLjIuNyA0NSAxLjkgOC4zIDExLjkgMTYuNCAyNC42IDI0LjIgMzggNy42IDEzLjEgMTQuNSAyNi40IDIwLjggMzkuOC02LjMgMTMuNC0xMy4yIDI2LjgtMjAuNyAzOS45em0zMi4zLTEzYzUuNCAxMy40IDEwIDI2LjggMTMuOCAzOS44LTEzLjEgMy4yLTI2LjkgNS45LTQxLjIgOCA0LjktNy43IDkuOC0xNS42IDE0LjQtMjMuNyA0LjYtOCA4LjktMTYuMSAxMy0yNC4xek00MjEuMiA0MzBjLTkuMy05LjYtMTguNi0yMC4zLTI3LjgtMzIgOSAuNCAxOC4yLjcgMjcuNS43IDkuNCAwIDE4LjctLjIgMjcuOC0uNy05IDExLjctMTguMyAyMi40LTI3LjUgMzJ6bS03NC40LTU4LjljLTE0LjItMi4xLTI3LjktNC43LTQxLTcuOSAzLjctMTIuOSA4LjMtMjYuMiAxMy41LTM5LjUgNC4xIDggOC40IDE2IDEzLjEgMjQgNC43IDggOS41IDE1LjggMTQuNCAyMy40ek00MjAuNyAxNjNjOS4zIDkuNiAxOC42IDIwLjMgMjcuOCAzMi05LS40LTE4LjItLjctMjcuNS0uNy05LjQgMC0xOC43LjItMjcuOC43IDktMTEuNyAxOC4zLTIyLjQgMjcuNS0zMnptLTc0IDU4LjljLTQuOSA3LjctOS44IDE1LjYtMTQuNCAyMy43LTQuNiA4LTguOSAxNi0xMyAyNC01LjQtMTMuNC0xMC0yNi44LTEzLjgtMzkuOCAxMy4xLTMuMSAyNi45LTUuOCA0MS4yLTcuOXptLTkwLjUgMTI1LjJjLTM1LjQtMTUuMS01OC4zLTM0LjktNTguMy01MC42IDAtMTUuNyAyMi45LTM1LjYgNTguMy01MC42IDguNi0zLjcgMTgtNyAyNy43LTEwLjEgNS43IDE5LjYgMTMuMiA0MCAyMi41IDYwLjktOS4yIDIwLjgtMTYuNiA0MS4xLTIyLjIgNjAuNi05LjktMy4xLTE5LjMtNi41LTI4LTEwLjJ6TTMxMCA0OTBjLTEzLjYtNy44LTE5LjUtMzcuNS0xNC45LTc1LjcgMS4xLTkuNCAyLjktMTkuMyA1LjEtMjkuNCAxOS42IDQuOCA0MSA4LjUgNjMuNSAxMC45IDEzLjUgMTguNSAyNy41IDM1LjMgNDEuNiA1MC0zMi42IDMwLjMtNjMuMiA0Ni45LTg0IDQ2LjktNC41LS4xLTguMy0xLTExLjMtMi43em0yMzcuMi03Ni4yYzQuNyAzOC4yLTEuMSA2Ny45LTE0LjYgNzUuOC0zIDEuOC02LjkgMi42LTExLjUgMi42LTIwLjcgMC01MS40LTE2LjUtODQtNDYuNiAxNC0xNC43IDI4LTMxLjQgNDEuMy00OS45IDIyLjYtMi40IDQ0LTYuMSA2My42LTExIDIuMyAxMC4xIDQuMSAxOS44IDUuMiAyOS4xem0zOC41LTY2LjdjLTguNiAzLjctMTggNy0yNy43IDEwLjEtNS43LTE5LjYtMTMuMi00MC0yMi41LTYwLjkgOS4yLTIwLjggMTYuNi00MS4xIDIyLjItNjAuNiA5LjkgMy4xIDE5LjMgNi41IDI4LjEgMTAuMiAzNS40IDE1LjEgNTguMyAzNC45IDU4LjMgNTAuNi0uMSAxNS43LTIzIDM1LjYtNTguNCA1MC42ek0zMjAuOCA3OC40eiIvPgogICAgPGNpcmNsZSBjeD0iNDIwLjkiIGN5PSIyOTYuNSIgcj0iNDUuNyIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-redo: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIGhlaWdodD0iMjQiIHZpZXdCb3g9IjAgMCAyNCAyNCIgd2lkdGg9IjE2Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgICA8cGF0aCBkPSJNMCAwaDI0djI0SDB6IiBmaWxsPSJub25lIi8+PHBhdGggZD0iTTE4LjQgMTAuNkMxNi41NSA4Ljk5IDE0LjE1IDggMTEuNSA4Yy00LjY1IDAtOC41OCAzLjAzLTkuOTYgNy4yMkwzLjkgMTZjMS4wNS0zLjE5IDQuMDUtNS41IDcuNi01LjUgMS45NSAwIDMuNzMuNzIgNS4xMiAxLjg4TDEzIDE2aDlWN2wtMy42IDMuNnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-refresh: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTkgMTMuNWMtMi40OSAwLTQuNS0yLjAxLTQuNS00LjVTNi41MSA0LjUgOSA0LjVjMS4yNCAwIDIuMzYuNTIgMy4xNyAxLjMzTDEwIDhoNVYzbC0xLjc2IDEuNzZDMTIuMTUgMy42OCAxMC42NiAzIDkgMyA1LjY5IDMgMy4wMSA1LjY5IDMuMDEgOVM1LjY5IDE1IDkgMTVjMi45NyAwIDUuNDMtMi4xNiA1LjktNWgtMS41MmMtLjQ2IDItMi4yNCAzLjUtNC4zOCAzLjV6Ii8+CiAgICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-regex: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KICA8ZyBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiM0MTQxNDEiPgogICAgPHJlY3QgeD0iMiIgeT0iMiIgd2lkdGg9IjE2IiBoZWlnaHQ9IjE2Ii8+CiAgPC9nPgoKICA8ZyBjbGFzcz0ianAtaWNvbi1hY2NlbnQyIiBmaWxsPSIjRkZGIj4KICAgIDxjaXJjbGUgY2xhc3M9InN0MiIgY3g9IjUuNSIgY3k9IjE0LjUiIHI9IjEuNSIvPgogICAgPHJlY3QgeD0iMTIiIHk9IjQiIGNsYXNzPSJzdDIiIHdpZHRoPSIxIiBoZWlnaHQ9IjgiLz4KICAgIDxyZWN0IHg9IjguNSIgeT0iNy41IiB0cmFuc2Zvcm09Im1hdHJpeCgwLjg2NiAtMC41IDAuNSAwLjg2NiAtMi4zMjU1IDcuMzIxOSkiIGNsYXNzPSJzdDIiIHdpZHRoPSI4IiBoZWlnaHQ9IjEiLz4KICAgIDxyZWN0IHg9IjEyIiB5PSI0IiB0cmFuc2Zvcm09Im1hdHJpeCgwLjUgLTAuODY2IDAuODY2IDAuNSAtMC42Nzc5IDE0LjgyNTIpIiBjbGFzcz0ic3QyIiB3aWR0aD0iMSIgaGVpZ2h0PSI4Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-run: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTggNXYxNGwxMS03eiIvPgogICAgPC9nPgo8L3N2Zz4K);
  --jp-icon-running: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDUxMiA1MTIiPgogIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICA8cGF0aCBkPSJNMjU2IDhDMTE5IDggOCAxMTkgOCAyNTZzMTExIDI0OCAyNDggMjQ4IDI0OC0xMTEgMjQ4LTI0OFMzOTMgOCAyNTYgOHptOTYgMzI4YzAgOC44LTcuMiAxNi0xNiAxNkgxNzZjLTguOCAwLTE2LTcuMi0xNi0xNlYxNzZjMC04LjggNy4yLTE2IDE2LTE2aDE2MGM4LjggMCAxNiA3LjIgMTYgMTZ2MTYweiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-save: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTE3IDNINWMtMS4xMSAwLTIgLjktMiAydjE0YzAgMS4xLjg5IDIgMiAyaDE0YzEuMSAwIDItLjkgMi0yVjdsLTQtNHptLTUgMTZjLTEuNjYgMC0zLTEuMzQtMy0zczEuMzQtMyAzLTMgMyAxLjM0IDMgMy0xLjM0IDMtMyAzem0zLTEwSDVWNWgxMHY0eiIvPgogICAgPC9nPgo8L3N2Zz4K);
  --jp-icon-search: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMTggMTgiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyLjEsMTAuOWgtMC43bC0wLjItMC4yYzAuOC0wLjksMS4zLTIuMiwxLjMtMy41YzAtMy0yLjQtNS40LTUuNC01LjRTMS44LDQuMiwxLjgsNy4xczIuNCw1LjQsNS40LDUuNCBjMS4zLDAsMi41LTAuNSwzLjUtMS4zbDAuMiwwLjJ2MC43bDQuMSw0LjFsMS4yLTEuMkwxMi4xLDEwLjl6IE03LjEsMTAuOWMtMi4xLDAtMy43LTEuNy0zLjctMy43czEuNy0zLjcsMy43LTMuN3MzLjcsMS43LDMuNywzLjcgUzkuMiwxMC45LDcuMSwxMC45eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-settings: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTkuNDMgMTIuOThjLjA0LS4zMi4wNy0uNjQuMDctLjk4cy0uMDMtLjY2LS4wNy0uOThsMi4xMS0xLjY1Yy4xOS0uMTUuMjQtLjQyLjEyLS42NGwtMi0zLjQ2Yy0uMTItLjIyLS4zOS0uMy0uNjEtLjIybC0yLjQ5IDFjLS41Mi0uNC0xLjA4LS43My0xLjY5LS45OGwtLjM4LTIuNjVBLjQ4OC40ODggMCAwMDE0IDJoLTRjLS4yNSAwLS40Ni4xOC0uNDkuNDJsLS4zOCAyLjY1Yy0uNjEuMjUtMS4xNy41OS0xLjY5Ljk4bC0yLjQ5LTFjLS4yMy0uMDktLjQ5IDAtLjYxLjIybC0yIDMuNDZjLS4xMy4yMi0uMDcuNDkuMTIuNjRsMi4xMSAxLjY1Yy0uMDQuMzItLjA3LjY1LS4wNy45OHMuMDMuNjYuMDcuOThsLTIuMTEgMS42NWMtLjE5LjE1LS4yNC40Mi0uMTIuNjRsMiAzLjQ2Yy4xMi4yMi4zOS4zLjYxLjIybDIuNDktMWMuNTIuNCAxLjA4LjczIDEuNjkuOThsLjM4IDIuNjVjLjAzLjI0LjI0LjQyLjQ5LjQyaDRjLjI1IDAgLjQ2LS4xOC40OS0uNDJsLjM4LTIuNjVjLjYxLS4yNSAxLjE3LS41OSAxLjY5LS45OGwyLjQ5IDFjLjIzLjA5LjQ5IDAgLjYxLS4yMmwyLTMuNDZjLjEyLS4yMi4wNy0uNDktLjEyLS42NGwtMi4xMS0xLjY1ek0xMiAxNS41Yy0xLjkzIDAtMy41LTEuNTctMy41LTMuNXMxLjU3LTMuNSAzLjUtMy41IDMuNSAxLjU3IDMuNSAzLjUtMS41NyAzLjUtMy41IDMuNXoiLz4KPC9zdmc+Cg==);
  --jp-icon-spreadsheet: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1jb250cmFzdDEganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNENBRjUwIiBkPSJNMi4yIDIuMnYxNy42aDE3LjZWMi4ySDIuMnptMTUuNCA3LjdoLTUuNVY0LjRoNS41djUuNXpNOS45IDQuNHY1LjVINC40VjQuNGg1LjV6bS01LjUgNy43aDUuNXY1LjVINC40di01LjV6bTcuNyA1LjV2LTUuNWg1LjV2NS41aC01LjV6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-stop: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIvPgogICAgICAgIDxwYXRoIGQ9Ik02IDZoMTJ2MTJINnoiLz4KICAgIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-tab: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTIxIDNIM2MtMS4xIDAtMiAuOS0yIDJ2MTRjMCAxLjEuOSAyIDIgMmgxOGMxLjEgMCAyLS45IDItMlY1YzAtMS4xLS45LTItMi0yem0wIDE2SDNWNWgxMHY0aDh2MTB6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-table-rows: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIvPgogICAgICAgIDxwYXRoIGQ9Ik0yMSw4SDNWNGgxOFY4eiBNMjEsMTBIM3Y0aDE4VjEweiBNMjEsMTZIM3Y0aDE4VjE2eiIvPgogICAgPC9nPgo8L3N2Zz4=);
  --jp-icon-tag: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjgiIGhlaWdodD0iMjgiIHZpZXdCb3g9IjAgMCA0MyAyOCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CgkJPHBhdGggZD0iTTI4LjgzMzIgMTIuMzM0TDMyLjk5OTggMTYuNTAwN0wzNy4xNjY1IDEyLjMzNEgyOC44MzMyWiIvPgoJCTxwYXRoIGQ9Ik0xNi4yMDk1IDIxLjYxMDRDMTUuNjg3MyAyMi4xMjk5IDE0Ljg0NDMgMjIuMTI5OSAxNC4zMjQ4IDIxLjYxMDRMNi45ODI5IDE0LjcyNDVDNi41NzI0IDE0LjMzOTQgNi4wODMxMyAxMy42MDk4IDYuMDQ3ODYgMTMuMDQ4MkM1Ljk1MzQ3IDExLjUyODggNi4wMjAwMiA4LjYxOTQ0IDYuMDY2MjEgNy4wNzY5NUM2LjA4MjgxIDYuNTE0NzcgNi41NTU0OCA2LjA0MzQ3IDcuMTE4MDQgNi4wMzA1NUM5LjA4ODYzIDUuOTg0NzMgMTMuMjYzOCA1LjkzNTc5IDEzLjY1MTggNi4zMjQyNUwyMS43MzY5IDEzLjYzOUMyMi4yNTYgMTQuMTU4NSAyMS43ODUxIDE1LjQ3MjQgMjEuMjYyIDE1Ljk5NDZMMTYuMjA5NSAyMS42MTA0Wk05Ljc3NTg1IDguMjY1QzkuMzM1NTEgNy44MjU2NiA4LjYyMzUxIDcuODI1NjYgOC4xODI4IDguMjY1QzcuNzQzNDYgOC43MDU3MSA3Ljc0MzQ2IDkuNDE3MzMgOC4xODI4IDkuODU2NjdDOC42MjM4MiAxMC4yOTY0IDkuMzM1ODIgMTAuMjk2NCA5Ljc3NTg1IDkuODU2NjdDMTAuMjE1NiA5LjQxNzMzIDEwLjIxNTYgOC43MDUzMyA5Ljc3NTg1IDguMjY1WiIvPgoJPC9nPgo8L3N2Zz4K);
  --jp-icon-terminal: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0IiA+CiAgICA8cmVjdCBjbGFzcz0ianAtaWNvbjIganAtaWNvbi1zZWxlY3RhYmxlIiB3aWR0aD0iMjAiIGhlaWdodD0iMjAiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDIgMikiIGZpbGw9IiMzMzMzMzMiLz4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uLWFjY2VudDIganAtaWNvbi1zZWxlY3RhYmxlLWludmVyc2UiIGQ9Ik01LjA1NjY0IDguNzYxNzJDNS4wNTY2NCA4LjU5NzY2IDUuMDMxMjUgOC40NTMxMiA0Ljk4MDQ3IDguMzI4MTJDNC45MzM1OSA4LjE5OTIyIDQuODU1NDcgOC4wODIwMyA0Ljc0NjA5IDcuOTc2NTZDNC42NDA2MiA3Ljg3MTA5IDQuNSA3Ljc3NTM5IDQuMzI0MjIgNy42ODk0NUM0LjE1MjM0IDcuNTk5NjEgMy45NDMzNiA3LjUxMTcyIDMuNjk3MjcgNy40MjU3OEMzLjMwMjczIDcuMjg1MTYgMi45NDMzNiA3LjEzNjcyIDIuNjE5MTQgNi45ODA0N0MyLjI5NDkyIDYuODI0MjIgMi4wMTc1OCA2LjY0MjU4IDEuNzg3MTEgNi40MzU1NUMxLjU2MDU1IDYuMjI4NTIgMS4zODQ3NyA1Ljk4ODI4IDEuMjU5NzcgNS43MTQ4NEMxLjEzNDc3IDUuNDM3NSAxLjA3MjI3IDUuMTA5MzggMS4wNzIyNyA0LjczMDQ3QzEuMDcyMjcgNC4zOTg0NCAxLjEyODkxIDQuMDk1NyAxLjI0MjE5IDMuODIyMjdDMS4zNTU0NyAzLjU0NDkyIDEuNTE1NjIgMy4zMDQ2OSAxLjcyMjY2IDMuMTAxNTZDMS45Mjk2OSAyLjg5ODQ0IDIuMTc5NjkgMi43MzQzNyAyLjQ3MjY2IDIuNjA5MzhDMi43NjU2MiAyLjQ4NDM4IDMuMDkxOCAyLjQwNDMgMy40NTExNyAyLjM2OTE0VjEuMTA5MzhINC4zODg2N1YyLjM4MDg2QzQuNzQwMjMgMi40Mjc3MyA1LjA1NjY0IDIuNTIzNDQgNS4zMzc4OSAyLjY2Nzk3QzUuNjE5MTQgMi44MTI1IDUuODU3NDIgMy4wMDE5NSA2LjA1MjczIDMuMjM2MzNDNi4yNTE5NSAzLjQ2NjggNi40MDQzIDMuNzQwMjMgNi41MDk3NyA0LjA1NjY0QzYuNjE5MTQgNC4zNjkxNCA2LjY3MzgzIDQuNzIwNyA2LjY3MzgzIDUuMTExMzNINS4wNDQ5MkM1LjA0NDkyIDQuNjM4NjcgNC45Mzc1IDQuMjgxMjUgNC43MjI2NiA0LjAzOTA2QzQuNTA3ODEgMy43OTI5NyA0LjIxNjggMy42Njk5MiAzLjg0OTYxIDMuNjY5OTJDMy42NTAzOSAzLjY2OTkyIDMuNDc2NTYgMy42OTcyNyAzLjMyODEyIDMuNzUxOTVDMy4xODM1OSAzLjgwMjczIDMuMDY0NDUgMy44NzY5NSAyLjk3MDcgMy45NzQ2MUMyLjg3Njk1IDQuMDY4MzYgMi44MDY2NCA0LjE3OTY5IDIuNzU5NzcgNC4zMDg1OUMyLjcxNjggNC40Mzc1IDIuNjk1MzEgNC41NzgxMiAyLjY5NTMxIDQuNzMwNDdDMi42OTUzMSA0Ljg4MjgxIDIuNzE2OCA1LjAxOTUzIDIuNzU5NzcgNS4xNDA2MkMyLjgwNjY0IDUuMjU3ODEgMi44ODI4MSA1LjM2NzE5IDIuOTg4MjggNS40Njg3NUMzLjA5NzY2IDUuNTcwMzEgMy4yNDAyMyA1LjY2Nzk3IDMuNDE2MDIgNS43NjE3MkMzLjU5MTggNS44NTE1NiAzLjgxMDU1IDUuOTQzMzYgNC4wNzIyNyA2LjAzNzExQzQuNDY2OCA2LjE4NTU1IDQuODI0MjIgNi4zMzk4NCA1LjE0NDUzIDYuNUM1LjQ2NDg0IDYuNjU2MjUgNS43MzgyOCA2LjgzOTg0IDUuOTY0ODQgNy4wNTA3OEM2LjE5NTMxIDcuMjU3ODEgNi4zNzEwOSA3LjUgNi40OTIxOSA3Ljc3NzM0QzYuNjE3MTkgOC4wNTA3OCA2LjY3OTY5IDguMzc1IDYuNjc5NjkgOC43NUM2LjY3OTY5IDkuMDkzNzUgNi42MjMwNSA5LjQwNDMgNi41MDk3NyA5LjY4MTY0QzYuMzk2NDggOS45NTUwOCA2LjIzNDM4IDEwLjE5MTQgNi4wMjM0NCAxMC4zOTA2QzUuODEyNSAxMC41ODk4IDUuNTU4NTkgMTAuNzUgNS4yNjE3MiAxMC44NzExQzQuOTY0ODQgMTAuOTg4MyA0LjYzMjgxIDExLjA2NDUgNC4yNjU2MiAxMS4wOTk2VjEyLjI0OEgzLjMzMzk4VjExLjA5OTZDMy4wMDE5NSAxMS4wNjg0IDIuNjc5NjkgMTAuOTk2MSAyLjM2NzE5IDEwLjg4MjhDMi4wNTQ2OSAxMC43NjU2IDEuNzc3MzQgMTAuNTk3NyAxLjUzNTE2IDEwLjM3ODlDMS4yOTY4OCAxMC4xNjAyIDEuMTA1NDcgOS44ODQ3NyAwLjk2MDkzOCA5LjU1MjczQzAuODE2NDA2IDkuMjE2OCAwLjc0NDE0MSA4LjgxNDQ1IDAuNzQ0MTQxIDguMzQ1N0gyLjM3ODkxQzIuMzc4OTEgOC42MjY5NSAyLjQxOTkyIDguODYzMjggMi41MDE5NSA5LjA1NDY5QzIuNTgzOTggOS4yNDIxOSAyLjY4OTQ1IDkuMzkyNTggMi44MTgzNiA5LjUwNTg2QzIuOTUxMTcgOS42MTUyMyAzLjEwMTU2IDkuNjkzMzYgMy4yNjk1MyA5Ljc0MDIzQzMuNDM3NSA5Ljc4NzExIDMuNjA5MzggOS44MTA1NSAzLjc4NTE2IDkuODEwNTVDNC4yMDMxMiA5LjgxMDU1IDQuNTE5NTMgOS43MTI4OSA0LjczNDM4IDkuNTE3NThDNC45NDkyMiA5LjMyMjI3IDUuMDU2NjQgOS4wNzAzMSA1LjA1NjY0IDguNzYxNzJaTTEzLjQxOCAxMi4yNzE1SDguMDc0MjJWMTFIMTMuNDE4VjEyLjI3MTVaIiB0cmFuc2Zvcm09InRyYW5zbGF0ZSgzLjk1MjY0IDYpIiBmaWxsPSJ3aGl0ZSIvPgo8L3N2Zz4K);
  --jp-icon-text-editor: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTUgMTVIM3YyaDEydi0yem0wLThIM3YyaDEyVjd6TTMgMTNoMTh2LTJIM3Yyem0wIDhoMTh2LTJIM3Yyek0zIDN2MmgxOFYzSDN6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-toc: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHhtbG5zOnhsaW5rPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5L3hsaW5rIiB2ZXJzaW9uPSIxLjEiIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0IiBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgoJPHBhdGggZD0iTTcsNUgyMVY3SDdWNU03LDEzVjExSDIxVjEzSDdNNCw0LjVBMS41LDEuNSAwIDAsMSA1LjUsNkExLjUsMS41IDAgMCwxIDQsNy41QTEuNSwxLjUgMCAwLDEgMi41LDZBMS41LDEuNSAwIDAsMSA0LDQuNU00LDEwLjVBMS41LDEuNSAwIDAsMSA1LjUsMTJBMS41LDEuNSAwIDAsMSA0LDEzLjVBMS41LDEuNSAwIDAsMSAyLjUsMTJBMS41LDEuNSAwIDAsMSA0LDEwLjVNNywxOVYxN0gyMVYxOUg3TTQsMTYuNUExLjUsMS41IDAgMCwxIDUuNSwxOEExLjUsMS41IDAgMCwxIDQsMTkuNUExLjUsMS41IDAgMCwxIDIuNSwxOEExLjUsMS41IDAgMCwxIDQsMTYuNVoiIC8+Cjwvc3ZnPgo=);
  --jp-icon-tree-view: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIvPgogICAgICAgIDxwYXRoIGQ9Ik0yMiAxMVYzaC03djNIOVYzSDJ2OGg3VjhoMnYxMGg0djNoN3YtOGgtN3YzaC0yVjhoMnYzeiIvPgogICAgPC9nPgo8L3N2Zz4=);
  --jp-icon-trusted: url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI1Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgc3Ryb2tlPSIjMzMzMzMzIiBzdHJva2Utd2lkdGg9IjIiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDIgMykiIGQ9Ik0xLjg2MDk0IDExLjQ0MDlDMC44MjY0NDggOC43NzAyNyAwLjg2Mzc3OSA2LjA1NzY0IDEuMjQ5MDcgNC4xOTkzMkMyLjQ4MjA2IDMuOTMzNDcgNC4wODA2OCAzLjQwMzQ3IDUuNjAxMDIgMi44NDQ5QzcuMjM1NDkgMi4yNDQ0IDguODU2NjYgMS41ODE1IDkuOTg3NiAxLjA5NTM5QzExLjA1OTcgMS41ODM0MSAxMi42MDk0IDIuMjQ0NCAxNC4yMTggMi44NDMzOUMxNS43NTAzIDMuNDEzOTQgMTcuMzk5NSAzLjk1MjU4IDE4Ljc1MzkgNC4yMTM4NUMxOS4xMzY0IDYuMDcxNzcgMTkuMTcwOSA4Ljc3NzIyIDE4LjEzOSAxMS40NDA5QzE3LjAzMDMgMTQuMzAzMiAxNC42NjY4IDE3LjE4NDQgOS45OTk5OSAxOC45MzU0QzUuMzMzMiAxNy4xODQ0IDIuOTY5NjggMTQuMzAzMiAxLjg2MDk0IDExLjQ0MDlaIi8+CiAgICA8cGF0aCBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiMzMzMzMzMiIHN0cm9rZT0iIzMzMzMzMyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoOCA5Ljg2NzE5KSIgZD0iTTIuODYwMTUgNC44NjUzNUwwLjcyNjU0OSAyLjk5OTU5TDAgMy42MzA0NUwyLjg2MDE1IDYuMTMxNTdMOCAwLjYzMDg3Mkw3LjI3ODU3IDBMMi44NjAxNSA0Ljg2NTM1WiIvPgo8L3N2Zz4K);
  --jp-icon-undo: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyLjUgOGMtMi42NSAwLTUuMDUuOTktNi45IDIuNkwyIDd2OWg5bC0zLjYyLTMuNjJjMS4zOS0xLjE2IDMuMTYtMS44OCA1LjEyLTEuODggMy41NCAwIDYuNTUgMi4zMSA3LjYgNS41bDIuMzctLjc4QzIxLjA4IDExLjAzIDE3LjE1IDggMTIuNSA4eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-vega: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbjEganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjMjEyMTIxIj4KICAgIDxwYXRoIGQ9Ik0xMC42IDUuNGwyLjItMy4ySDIuMnY3LjNsNC02LjZ6Ii8+CiAgICA8cGF0aCBkPSJNMTUuOCAyLjJsLTQuNCA2LjZMNyA2LjNsLTQuOCA4djUuNWgxNy42VjIuMmgtNHptLTcgMTUuNEg1LjV2LTQuNGgzLjN2NC40em00LjQgMEg5LjhWOS44aDMuNHY3Ljh6bTQuNCAwaC0zLjRWNi41aDMuNHYxMS4xeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-yaml: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbi1jb250cmFzdDIganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjRDgxQjYwIj4KICAgIDxwYXRoIGQ9Ik03LjIgMTguNnYtNS40TDMgNS42aDMuM2wxLjQgMy4xYy4zLjkuNiAxLjYgMSAyLjUuMy0uOC42LTEuNiAxLTIuNWwxLjQtMy4xaDMuNGwtNC40IDcuNnY1LjVsLTIuOS0uMXoiLz4KICAgIDxjaXJjbGUgY2xhc3M9InN0MCIgY3g9IjE3LjYiIGN5PSIxNi41IiByPSIyLjEiLz4KICAgIDxjaXJjbGUgY2xhc3M9InN0MCIgY3g9IjE3LjYiIGN5PSIxMSIgcj0iMi4xIi8+CiAgPC9nPgo8L3N2Zz4K);
}

/* Icon CSS class declarations */

.jp-AddIcon {
  background-image: var(--jp-icon-add);
}
.jp-BugIcon {
  background-image: var(--jp-icon-bug);
}
.jp-BuildIcon {
  background-image: var(--jp-icon-build);
}
.jp-CaretDownEmptyIcon {
  background-image: var(--jp-icon-caret-down-empty);
}
.jp-CaretDownEmptyThinIcon {
  background-image: var(--jp-icon-caret-down-empty-thin);
}
.jp-CaretDownIcon {
  background-image: var(--jp-icon-caret-down);
}
.jp-CaretLeftIcon {
  background-image: var(--jp-icon-caret-left);
}
.jp-CaretRightIcon {
  background-image: var(--jp-icon-caret-right);
}
.jp-CaretUpEmptyThinIcon {
  background-image: var(--jp-icon-caret-up-empty-thin);
}
.jp-CaretUpIcon {
  background-image: var(--jp-icon-caret-up);
}
.jp-CaseSensitiveIcon {
  background-image: var(--jp-icon-case-sensitive);
}
.jp-CheckIcon {
  background-image: var(--jp-icon-check);
}
.jp-CircleEmptyIcon {
  background-image: var(--jp-icon-circle-empty);
}
.jp-CircleIcon {
  background-image: var(--jp-icon-circle);
}
.jp-ClearIcon {
  background-image: var(--jp-icon-clear);
}
.jp-CloseIcon {
  background-image: var(--jp-icon-close);
}
.jp-CodeIcon {
  background-image: var(--jp-icon-code);
}
.jp-ConsoleIcon {
  background-image: var(--jp-icon-console);
}
.jp-CopyIcon {
  background-image: var(--jp-icon-copy);
}
.jp-CutIcon {
  background-image: var(--jp-icon-cut);
}
.jp-DownloadIcon {
  background-image: var(--jp-icon-download);
}
.jp-EditIcon {
  background-image: var(--jp-icon-edit);
}
.jp-EllipsesIcon {
  background-image: var(--jp-icon-ellipses);
}
.jp-ExtensionIcon {
  background-image: var(--jp-icon-extension);
}
.jp-FastForwardIcon {
  background-image: var(--jp-icon-fast-forward);
}
.jp-FileIcon {
  background-image: var(--jp-icon-file);
}
.jp-FileUploadIcon {
  background-image: var(--jp-icon-file-upload);
}
.jp-FilterListIcon {
  background-image: var(--jp-icon-filter-list);
}
.jp-FolderIcon {
  background-image: var(--jp-icon-folder);
}
.jp-Html5Icon {
  background-image: var(--jp-icon-html5);
}
.jp-ImageIcon {
  background-image: var(--jp-icon-image);
}
.jp-InspectorIcon {
  background-image: var(--jp-icon-inspector);
}
.jp-JsonIcon {
  background-image: var(--jp-icon-json);
}
.jp-JupyterFaviconIcon {
  background-image: var(--jp-icon-jupyter-favicon);
}
.jp-JupyterIcon {
  background-image: var(--jp-icon-jupyter);
}
.jp-JupyterlabWordmarkIcon {
  background-image: var(--jp-icon-jupyterlab-wordmark);
}
.jp-KernelIcon {
  background-image: var(--jp-icon-kernel);
}
.jp-KeyboardIcon {
  background-image: var(--jp-icon-keyboard);
}
.jp-LauncherIcon {
  background-image: var(--jp-icon-launcher);
}
.jp-LineFormIcon {
  background-image: var(--jp-icon-line-form);
}
.jp-LinkIcon {
  background-image: var(--jp-icon-link);
}
.jp-ListIcon {
  background-image: var(--jp-icon-list);
}
.jp-ListingsInfoIcon {
  background-image: var(--jp-icon-listings-info);
}
.jp-MarkdownIcon {
  background-image: var(--jp-icon-markdown);
}
.jp-NewFolderIcon {
  background-image: var(--jp-icon-new-folder);
}
.jp-NotTrustedIcon {
  background-image: var(--jp-icon-not-trusted);
}
.jp-NotebookIcon {
  background-image: var(--jp-icon-notebook);
}
.jp-NumberingIcon {
  background-image: var(--jp-icon-numbering);
}
.jp-OfflineBoltIcon {
  background-image: var(--jp-icon-offline-bolt);
}
.jp-PaletteIcon {
  background-image: var(--jp-icon-palette);
}
.jp-PasteIcon {
  background-image: var(--jp-icon-paste);
}
.jp-PdfIcon {
  background-image: var(--jp-icon-pdf);
}
.jp-PythonIcon {
  background-image: var(--jp-icon-python);
}
.jp-RKernelIcon {
  background-image: var(--jp-icon-r-kernel);
}
.jp-ReactIcon {
  background-image: var(--jp-icon-react);
}
.jp-RedoIcon {
  background-image: var(--jp-icon-redo);
}
.jp-RefreshIcon {
  background-image: var(--jp-icon-refresh);
}
.jp-RegexIcon {
  background-image: var(--jp-icon-regex);
}
.jp-RunIcon {
  background-image: var(--jp-icon-run);
}
.jp-RunningIcon {
  background-image: var(--jp-icon-running);
}
.jp-SaveIcon {
  background-image: var(--jp-icon-save);
}
.jp-SearchIcon {
  background-image: var(--jp-icon-search);
}
.jp-SettingsIcon {
  background-image: var(--jp-icon-settings);
}
.jp-SpreadsheetIcon {
  background-image: var(--jp-icon-spreadsheet);
}
.jp-StopIcon {
  background-image: var(--jp-icon-stop);
}
.jp-TabIcon {
  background-image: var(--jp-icon-tab);
}
.jp-TableRowsIcon {
  background-image: var(--jp-icon-table-rows);
}
.jp-TagIcon {
  background-image: var(--jp-icon-tag);
}
.jp-TerminalIcon {
  background-image: var(--jp-icon-terminal);
}
.jp-TextEditorIcon {
  background-image: var(--jp-icon-text-editor);
}
.jp-TocIcon {
  background-image: var(--jp-icon-toc);
}
.jp-TreeViewIcon {
  background-image: var(--jp-icon-tree-view);
}
.jp-TrustedIcon {
  background-image: var(--jp-icon-trusted);
}
.jp-UndoIcon {
  background-image: var(--jp-icon-undo);
}
.jp-VegaIcon {
  background-image: var(--jp-icon-vega);
}
.jp-YamlIcon {
  background-image: var(--jp-icon-yaml);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/**
 * (DEPRECATED) Support for consuming icons as CSS background images
 */

:root {
  --jp-icon-search-white: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMTggMTgiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyLjEsMTAuOWgtMC43bC0wLjItMC4yYzAuOC0wLjksMS4zLTIuMiwxLjMtMy41YzAtMy0yLjQtNS40LTUuNC01LjRTMS44LDQuMiwxLjgsNy4xczIuNCw1LjQsNS40LDUuNCBjMS4zLDAsMi41LTAuNSwzLjUtMS4zbDAuMiwwLjJ2MC43bDQuMSw0LjFsMS4yLTEuMkwxMi4xLDEwLjl6IE03LjEsMTAuOWMtMi4xLDAtMy43LTEuNy0zLjctMy43czEuNy0zLjcsMy43LTMuN3MzLjcsMS43LDMuNywzLjcgUzkuMiwxMC45LDcuMSwxMC45eiIvPgogIDwvZz4KPC9zdmc+Cg==);
}

.jp-Icon,
.jp-MaterialIcon {
  background-position: center;
  background-repeat: no-repeat;
  background-size: 16px;
  min-width: 16px;
  min-height: 16px;
}

.jp-Icon-cover {
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}

/**
 * (DEPRECATED) Support for specific CSS icon sizes
 */

.jp-Icon-16 {
  background-size: 16px;
  min-width: 16px;
  min-height: 16px;
}

.jp-Icon-18 {
  background-size: 18px;
  min-width: 18px;
  min-height: 18px;
}

.jp-Icon-20 {
  background-size: 20px;
  min-width: 20px;
  min-height: 20px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/**
 * Support for icons as inline SVG HTMLElements
 */

/* recolor the primary elements of an icon */
.jp-icon0[fill] {
  fill: var(--jp-inverse-layout-color0);
}
.jp-icon1[fill] {
  fill: var(--jp-inverse-layout-color1);
}
.jp-icon2[fill] {
  fill: var(--jp-inverse-layout-color2);
}
.jp-icon3[fill] {
  fill: var(--jp-inverse-layout-color3);
}
.jp-icon4[fill] {
  fill: var(--jp-inverse-layout-color4);
}

.jp-icon0[stroke] {
  stroke: var(--jp-inverse-layout-color0);
}
.jp-icon1[stroke] {
  stroke: var(--jp-inverse-layout-color1);
}
.jp-icon2[stroke] {
  stroke: var(--jp-inverse-layout-color2);
}
.jp-icon3[stroke] {
  stroke: var(--jp-inverse-layout-color3);
}
.jp-icon4[stroke] {
  stroke: var(--jp-inverse-layout-color4);
}
/* recolor the accent elements of an icon */
.jp-icon-accent0[fill] {
  fill: var(--jp-layout-color0);
}
.jp-icon-accent1[fill] {
  fill: var(--jp-layout-color1);
}
.jp-icon-accent2[fill] {
  fill: var(--jp-layout-color2);
}
.jp-icon-accent3[fill] {
  fill: var(--jp-layout-color3);
}
.jp-icon-accent4[fill] {
  fill: var(--jp-layout-color4);
}

.jp-icon-accent0[stroke] {
  stroke: var(--jp-layout-color0);
}
.jp-icon-accent1[stroke] {
  stroke: var(--jp-layout-color1);
}
.jp-icon-accent2[stroke] {
  stroke: var(--jp-layout-color2);
}
.jp-icon-accent3[stroke] {
  stroke: var(--jp-layout-color3);
}
.jp-icon-accent4[stroke] {
  stroke: var(--jp-layout-color4);
}
/* set the color of an icon to transparent */
.jp-icon-none[fill] {
  fill: none;
}

.jp-icon-none[stroke] {
  stroke: none;
}
/* brand icon colors. Same for light and dark */
.jp-icon-brand0[fill] {
  fill: var(--jp-brand-color0);
}
.jp-icon-brand1[fill] {
  fill: var(--jp-brand-color1);
}
.jp-icon-brand2[fill] {
  fill: var(--jp-brand-color2);
}
.jp-icon-brand3[fill] {
  fill: var(--jp-brand-color3);
}
.jp-icon-brand4[fill] {
  fill: var(--jp-brand-color4);
}

.jp-icon-brand0[stroke] {
  stroke: var(--jp-brand-color0);
}
.jp-icon-brand1[stroke] {
  stroke: var(--jp-brand-color1);
}
.jp-icon-brand2[stroke] {
  stroke: var(--jp-brand-color2);
}
.jp-icon-brand3[stroke] {
  stroke: var(--jp-brand-color3);
}
.jp-icon-brand4[stroke] {
  stroke: var(--jp-brand-color4);
}
/* warn icon colors. Same for light and dark */
.jp-icon-warn0[fill] {
  fill: var(--jp-warn-color0);
}
.jp-icon-warn1[fill] {
  fill: var(--jp-warn-color1);
}
.jp-icon-warn2[fill] {
  fill: var(--jp-warn-color2);
}
.jp-icon-warn3[fill] {
  fill: var(--jp-warn-color3);
}

.jp-icon-warn0[stroke] {
  stroke: var(--jp-warn-color0);
}
.jp-icon-warn1[stroke] {
  stroke: var(--jp-warn-color1);
}
.jp-icon-warn2[stroke] {
  stroke: var(--jp-warn-color2);
}
.jp-icon-warn3[stroke] {
  stroke: var(--jp-warn-color3);
}
/* icon colors that contrast well with each other and most backgrounds */
.jp-icon-contrast0[fill] {
  fill: var(--jp-icon-contrast-color0);
}
.jp-icon-contrast1[fill] {
  fill: var(--jp-icon-contrast-color1);
}
.jp-icon-contrast2[fill] {
  fill: var(--jp-icon-contrast-color2);
}
.jp-icon-contrast3[fill] {
  fill: var(--jp-icon-contrast-color3);
}

.jp-icon-contrast0[stroke] {
  stroke: var(--jp-icon-contrast-color0);
}
.jp-icon-contrast1[stroke] {
  stroke: var(--jp-icon-contrast-color1);
}
.jp-icon-contrast2[stroke] {
  stroke: var(--jp-icon-contrast-color2);
}
.jp-icon-contrast3[stroke] {
  stroke: var(--jp-icon-contrast-color3);
}

/* CSS for icons in selected items in the settings editor */
#setting-editor .jp-PluginList .jp-mod-selected .jp-icon-selectable[fill] {
  fill: #fff;
}
#setting-editor
  .jp-PluginList
  .jp-mod-selected
  .jp-icon-selectable-inverse[fill] {
  fill: var(--jp-brand-color1);
}

/* CSS for icons in selected filebrowser listing items */
.jp-DirListing-item.jp-mod-selected .jp-icon-selectable[fill] {
  fill: #fff;
}
.jp-DirListing-item.jp-mod-selected .jp-icon-selectable-inverse[fill] {
  fill: var(--jp-brand-color1);
}

/* CSS for icons in selected tabs in the sidebar tab manager */
#tab-manager .lm-TabBar-tab.jp-mod-active .jp-icon-selectable[fill] {
  fill: #fff;
}

#tab-manager .lm-TabBar-tab.jp-mod-active .jp-icon-selectable-inverse[fill] {
  fill: var(--jp-brand-color1);
}
#tab-manager
  .lm-TabBar-tab.jp-mod-active
  .jp-icon-hover
  :hover
  .jp-icon-selectable[fill] {
  fill: var(--jp-brand-color1);
}

#tab-manager
  .lm-TabBar-tab.jp-mod-active
  .jp-icon-hover
  :hover
  .jp-icon-selectable-inverse[fill] {
  fill: #fff;
}

/**
 * TODO: come up with non css-hack solution for showing the busy icon on top
 *  of the close icon
 * CSS for complex behavior of close icon of tabs in the sidebar tab manager
 */
#tab-manager
  .lm-TabBar-tab.jp-mod-dirty
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon3[fill] {
  fill: none;
}
#tab-manager
  .lm-TabBar-tab.jp-mod-dirty
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon-busy[fill] {
  fill: var(--jp-inverse-layout-color3);
}

#tab-manager
  .lm-TabBar-tab.jp-mod-dirty.jp-mod-active
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon-busy[fill] {
  fill: #fff;
}

/**
* TODO: come up with non css-hack solution for showing the busy icon on top
*  of the close icon
* CSS for complex behavior of close icon of tabs in the main area tabbar
*/
.lm-DockPanel-tabBar
  .lm-TabBar-tab.lm-mod-closable.jp-mod-dirty
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon3[fill] {
  fill: none;
}
.lm-DockPanel-tabBar
  .lm-TabBar-tab.lm-mod-closable.jp-mod-dirty
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon-busy[fill] {
  fill: var(--jp-inverse-layout-color3);
}

/* CSS for icons in status bar */
#jp-main-statusbar .jp-mod-selected .jp-icon-selectable[fill] {
  fill: #fff;
}

#jp-main-statusbar .jp-mod-selected .jp-icon-selectable-inverse[fill] {
  fill: var(--jp-brand-color1);
}
/* special handling for splash icon CSS. While the theme CSS reloads during
   splash, the splash icon can loose theming. To prevent that, we set a
   default for its color variable */
:root {
  --jp-warn-color0: var(--md-orange-700);
}

/* not sure what to do with this one, used in filebrowser listing */
.jp-DragIcon {
  margin-right: 4px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/**
 * Support for alt colors for icons as inline SVG HTMLElements
 */

/* alt recolor the primary elements of an icon */
.jp-icon-alt .jp-icon0[fill] {
  fill: var(--jp-layout-color0);
}
.jp-icon-alt .jp-icon1[fill] {
  fill: var(--jp-layout-color1);
}
.jp-icon-alt .jp-icon2[fill] {
  fill: var(--jp-layout-color2);
}
.jp-icon-alt .jp-icon3[fill] {
  fill: var(--jp-layout-color3);
}
.jp-icon-alt .jp-icon4[fill] {
  fill: var(--jp-layout-color4);
}

.jp-icon-alt .jp-icon0[stroke] {
  stroke: var(--jp-layout-color0);
}
.jp-icon-alt .jp-icon1[stroke] {
  stroke: var(--jp-layout-color1);
}
.jp-icon-alt .jp-icon2[stroke] {
  stroke: var(--jp-layout-color2);
}
.jp-icon-alt .jp-icon3[stroke] {
  stroke: var(--jp-layout-color3);
}
.jp-icon-alt .jp-icon4[stroke] {
  stroke: var(--jp-layout-color4);
}

/* alt recolor the accent elements of an icon */
.jp-icon-alt .jp-icon-accent0[fill] {
  fill: var(--jp-inverse-layout-color0);
}
.jp-icon-alt .jp-icon-accent1[fill] {
  fill: var(--jp-inverse-layout-color1);
}
.jp-icon-alt .jp-icon-accent2[fill] {
  fill: var(--jp-inverse-layout-color2);
}
.jp-icon-alt .jp-icon-accent3[fill] {
  fill: var(--jp-inverse-layout-color3);
}
.jp-icon-alt .jp-icon-accent4[fill] {
  fill: var(--jp-inverse-layout-color4);
}

.jp-icon-alt .jp-icon-accent0[stroke] {
  stroke: var(--jp-inverse-layout-color0);
}
.jp-icon-alt .jp-icon-accent1[stroke] {
  stroke: var(--jp-inverse-layout-color1);
}
.jp-icon-alt .jp-icon-accent2[stroke] {
  stroke: var(--jp-inverse-layout-color2);
}
.jp-icon-alt .jp-icon-accent3[stroke] {
  stroke: var(--jp-inverse-layout-color3);
}
.jp-icon-alt .jp-icon-accent4[stroke] {
  stroke: var(--jp-inverse-layout-color4);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-icon-hoverShow:not(:hover) svg {
  display: none !important;
}

/**
 * Support for hover colors for icons as inline SVG HTMLElements
 */

/**
 * regular colors
 */

/* recolor the primary elements of an icon */
.jp-icon-hover :hover .jp-icon0-hover[fill] {
  fill: var(--jp-inverse-layout-color0);
}
.jp-icon-hover :hover .jp-icon1-hover[fill] {
  fill: var(--jp-inverse-layout-color1);
}
.jp-icon-hover :hover .jp-icon2-hover[fill] {
  fill: var(--jp-inverse-layout-color2);
}
.jp-icon-hover :hover .jp-icon3-hover[fill] {
  fill: var(--jp-inverse-layout-color3);
}
.jp-icon-hover :hover .jp-icon4-hover[fill] {
  fill: var(--jp-inverse-layout-color4);
}

.jp-icon-hover :hover .jp-icon0-hover[stroke] {
  stroke: var(--jp-inverse-layout-color0);
}
.jp-icon-hover :hover .jp-icon1-hover[stroke] {
  stroke: var(--jp-inverse-layout-color1);
}
.jp-icon-hover :hover .jp-icon2-hover[stroke] {
  stroke: var(--jp-inverse-layout-color2);
}
.jp-icon-hover :hover .jp-icon3-hover[stroke] {
  stroke: var(--jp-inverse-layout-color3);
}
.jp-icon-hover :hover .jp-icon4-hover[stroke] {
  stroke: var(--jp-inverse-layout-color4);
}

/* recolor the accent elements of an icon */
.jp-icon-hover :hover .jp-icon-accent0-hover[fill] {
  fill: var(--jp-layout-color0);
}
.jp-icon-hover :hover .jp-icon-accent1-hover[fill] {
  fill: var(--jp-layout-color1);
}
.jp-icon-hover :hover .jp-icon-accent2-hover[fill] {
  fill: var(--jp-layout-color2);
}
.jp-icon-hover :hover .jp-icon-accent3-hover[fill] {
  fill: var(--jp-layout-color3);
}
.jp-icon-hover :hover .jp-icon-accent4-hover[fill] {
  fill: var(--jp-layout-color4);
}

.jp-icon-hover :hover .jp-icon-accent0-hover[stroke] {
  stroke: var(--jp-layout-color0);
}
.jp-icon-hover :hover .jp-icon-accent1-hover[stroke] {
  stroke: var(--jp-layout-color1);
}
.jp-icon-hover :hover .jp-icon-accent2-hover[stroke] {
  stroke: var(--jp-layout-color2);
}
.jp-icon-hover :hover .jp-icon-accent3-hover[stroke] {
  stroke: var(--jp-layout-color3);
}
.jp-icon-hover :hover .jp-icon-accent4-hover[stroke] {
  stroke: var(--jp-layout-color4);
}

/* set the color of an icon to transparent */
.jp-icon-hover :hover .jp-icon-none-hover[fill] {
  fill: none;
}

.jp-icon-hover :hover .jp-icon-none-hover[stroke] {
  stroke: none;
}

/**
 * inverse colors
 */

/* inverse recolor the primary elements of an icon */
.jp-icon-hover.jp-icon-alt :hover .jp-icon0-hover[fill] {
  fill: var(--jp-layout-color0);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon1-hover[fill] {
  fill: var(--jp-layout-color1);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon2-hover[fill] {
  fill: var(--jp-layout-color2);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon3-hover[fill] {
  fill: var(--jp-layout-color3);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon4-hover[fill] {
  fill: var(--jp-layout-color4);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon0-hover[stroke] {
  stroke: var(--jp-layout-color0);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon1-hover[stroke] {
  stroke: var(--jp-layout-color1);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon2-hover[stroke] {
  stroke: var(--jp-layout-color2);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon3-hover[stroke] {
  stroke: var(--jp-layout-color3);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon4-hover[stroke] {
  stroke: var(--jp-layout-color4);
}

/* inverse recolor the accent elements of an icon */
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent0-hover[fill] {
  fill: var(--jp-inverse-layout-color0);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent1-hover[fill] {
  fill: var(--jp-inverse-layout-color1);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent2-hover[fill] {
  fill: var(--jp-inverse-layout-color2);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent3-hover[fill] {
  fill: var(--jp-inverse-layout-color3);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent4-hover[fill] {
  fill: var(--jp-inverse-layout-color4);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent0-hover[stroke] {
  stroke: var(--jp-inverse-layout-color0);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent1-hover[stroke] {
  stroke: var(--jp-inverse-layout-color1);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent2-hover[stroke] {
  stroke: var(--jp-inverse-layout-color2);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent3-hover[stroke] {
  stroke: var(--jp-inverse-layout-color3);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent4-hover[stroke] {
  stroke: var(--jp-inverse-layout-color4);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-switch {
  display: flex;
  align-items: center;
  padding-left: 4px;
  padding-right: 4px;
  font-size: var(--jp-ui-font-size1);
  background-color: transparent;
  color: var(--jp-ui-font-color1);
  border: none;
  height: 20px;
}

.jp-switch:hover {
  background-color: var(--jp-layout-color2);
}

.jp-switch-label {
  margin-right: 5px;
}

.jp-switch-track {
  cursor: pointer;
  background-color: var(--jp-border-color1);
  -webkit-transition: 0.4s;
  transition: 0.4s;
  border-radius: 34px;
  height: 16px;
  width: 35px;
  position: relative;
}

.jp-switch-track::before {
  content: '';
  position: absolute;
  height: 10px;
  width: 10px;
  margin: 3px;
  left: 0px;
  background-color: var(--jp-ui-inverse-font-color1);
  -webkit-transition: 0.4s;
  transition: 0.4s;
  border-radius: 50%;
}

.jp-switch[aria-checked='true'] .jp-switch-track {
  background-color: var(--jp-warn-color0);
}

.jp-switch[aria-checked='true'] .jp-switch-track::before {
  /* track width (35) - margins (3 + 3) - thumb width (10) */
  left: 19px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* Sibling imports */

/* Override Blueprint's _reset.scss styles */
html {
  box-sizing: unset;
}

*,
*::before,
*::after {
  box-sizing: unset;
}

body {
  color: unset;
  font-family: var(--jp-ui-font-family);
}

p {
  margin-top: unset;
  margin-bottom: unset;
}

small {
  font-size: unset;
}

strong {
  font-weight: unset;
}

/* Override Blueprint's _typography.scss styles */
a {
  text-decoration: unset;
  color: unset;
}
a:hover {
  text-decoration: unset;
  color: unset;
}

/* Override Blueprint's _accessibility.scss styles */
:focus {
  outline: unset;
  outline-offset: unset;
  -moz-outline-radius: unset;
}

/* Styles for ui-components */
.jp-Button {
  border-radius: var(--jp-border-radius);
  padding: 0px 12px;
  font-size: var(--jp-ui-font-size1);
}

/* Use our own theme for hover styles */
button.jp-Button.bp3-button.bp3-minimal:hover {
  background-color: var(--jp-layout-color2);
}
.jp-Button.minimal {
  color: unset !important;
}

.jp-Button.jp-ToolbarButtonComponent {
  text-transform: none;
}

.jp-InputGroup input {
  box-sizing: border-box;
  border-radius: 0;
  background-color: transparent;
  color: var(--jp-ui-font-color0);
  box-shadow: inset 0 0 0 var(--jp-border-width) var(--jp-input-border-color);
}

.jp-InputGroup input:focus {
  box-shadow: inset 0 0 0 var(--jp-border-width)
      var(--jp-input-active-box-shadow-color),
    inset 0 0 0 3px var(--jp-input-active-box-shadow-color);
}

.jp-InputGroup input::placeholder,
input::placeholder {
  color: var(--jp-ui-font-color3);
}

.jp-BPIcon {
  display: inline-block;
  vertical-align: middle;
  margin: auto;
}

/* Stop blueprint futzing with our icon fills */
.bp3-icon.jp-BPIcon > svg:not([fill]) {
  fill: var(--jp-inverse-layout-color3);
}

.jp-InputGroupAction {
  padding: 6px;
}

.jp-HTMLSelect.jp-DefaultStyle select {
  background-color: initial;
  border: none;
  border-radius: 0;
  box-shadow: none;
  color: var(--jp-ui-font-color0);
  display: block;
  font-size: var(--jp-ui-font-size1);
  height: 24px;
  line-height: 14px;
  padding: 0 25px 0 10px;
  text-align: left;
  -moz-appearance: none;
  -webkit-appearance: none;
}

/* Use our own theme for hover and option styles */
.jp-HTMLSelect.jp-DefaultStyle select:hover,
.jp-HTMLSelect.jp-DefaultStyle select > option {
  background-color: var(--jp-layout-color2);
  color: var(--jp-ui-font-color0);
}
select {
  box-sizing: border-box;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Collapse {
  display: flex;
  flex-direction: column;
  align-items: stretch;
  border-top: 1px solid var(--jp-border-color2);
  border-bottom: 1px solid var(--jp-border-color2);
}

.jp-Collapse-header {
  padding: 1px 12px;
  color: var(--jp-ui-font-color1);
  background-color: var(--jp-layout-color1);
  font-size: var(--jp-ui-font-size2);
}

.jp-Collapse-header:hover {
  background-color: var(--jp-layout-color2);
}

.jp-Collapse-contents {
  padding: 0px 12px 0px 12px;
  background-color: var(--jp-layout-color1);
  color: var(--jp-ui-font-color1);
  overflow: auto;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Variables
|----------------------------------------------------------------------------*/

:root {
  --jp-private-commandpalette-search-height: 28px;
}

/*-----------------------------------------------------------------------------
| Overall styles
|----------------------------------------------------------------------------*/

.lm-CommandPalette {
  padding-bottom: 0px;
  color: var(--jp-ui-font-color1);
  background: var(--jp-layout-color1);
  /* This is needed so that all font sizing of children done in ems is
   * relative to this base size */
  font-size: var(--jp-ui-font-size1);
}

/*-----------------------------------------------------------------------------
| Modal variant
|----------------------------------------------------------------------------*/

.jp-ModalCommandPalette {
  position: absolute;
  z-index: 10000;
  top: 38px;
  left: 30%;
  margin: 0;
  padding: 4px;
  width: 40%;
  box-shadow: var(--jp-elevation-z4);
  border-radius: 4px;
  background: var(--jp-layout-color0);
}

.jp-ModalCommandPalette .lm-CommandPalette {
  max-height: 40vh;
}

.jp-ModalCommandPalette .lm-CommandPalette .lm-close-icon::after {
  display: none;
}

.jp-ModalCommandPalette .lm-CommandPalette .lm-CommandPalette-header {
  display: none;
}

.jp-ModalCommandPalette .lm-CommandPalette .lm-CommandPalette-item {
  margin-left: 4px;
  margin-right: 4px;
}

.jp-ModalCommandPalette
  .lm-CommandPalette
  .lm-CommandPalette-item.lm-mod-disabled {
  display: none;
}

/*-----------------------------------------------------------------------------
| Search
|----------------------------------------------------------------------------*/

.lm-CommandPalette-search {
  padding: 4px;
  background-color: var(--jp-layout-color1);
  z-index: 2;
}

.lm-CommandPalette-wrapper {
  overflow: overlay;
  padding: 0px 9px;
  background-color: var(--jp-input-active-background);
  height: 30px;
  box-shadow: inset 0 0 0 var(--jp-border-width) var(--jp-input-border-color);
}

.lm-CommandPalette.lm-mod-focused .lm-CommandPalette-wrapper {
  box-shadow: inset 0 0 0 1px var(--jp-input-active-box-shadow-color),
    inset 0 0 0 3px var(--jp-input-active-box-shadow-color);
}

.lm-CommandPalette-wrapper::after {
  content: ' ';
  color: white;
  background-color: var(--jp-brand-color1);
  position: absolute;
  top: 4px;
  right: 4px;
  height: 30px;
  width: 10px;
  padding: 0px 10px;
  background-image: var(--jp-icon-search-white);
  background-size: 20px;
  background-repeat: no-repeat;
  background-position: center;
}

.lm-CommandPalette-input {
  background: transparent;
  width: calc(100% - 18px);
  float: left;
  border: none;
  outline: none;
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color0);
  line-height: var(--jp-private-commandpalette-search-height);
}

.lm-CommandPalette-input::-webkit-input-placeholder,
.lm-CommandPalette-input::-moz-placeholder,
.lm-CommandPalette-input:-ms-input-placeholder {
  color: var(--jp-ui-font-color3);
  font-size: var(--jp-ui-font-size1);
}

/*-----------------------------------------------------------------------------
| Results
|----------------------------------------------------------------------------*/

.lm-CommandPalette-header:first-child {
  margin-top: 0px;
}

.lm-CommandPalette-header {
  border-bottom: solid var(--jp-border-width) var(--jp-border-color2);
  color: var(--jp-ui-font-color1);
  cursor: pointer;
  display: flex;
  font-size: var(--jp-ui-font-size0);
  font-weight: 600;
  letter-spacing: 1px;
  margin-top: 8px;
  padding: 8px 0 8px 12px;
  text-transform: uppercase;
}

.lm-CommandPalette-header.lm-mod-active {
  background: var(--jp-layout-color2);
}

.lm-CommandPalette-header > mark {
  background-color: transparent;
  font-weight: bold;
  color: var(--jp-ui-font-color1);
}

.lm-CommandPalette-item {
  padding: 4px 12px 4px 4px;
  color: var(--jp-ui-font-color1);
  font-size: var(--jp-ui-font-size1);
  font-weight: 400;
  display: flex;
}

.lm-CommandPalette-item.lm-mod-disabled {
  color: var(--jp-ui-font-color3);
}

.lm-CommandPalette-item.lm-mod-active {
  background: var(--jp-layout-color3);
}

.lm-CommandPalette-item.lm-mod-active:hover:not(.lm-mod-disabled) {
  background: var(--jp-layout-color4);
}

.lm-CommandPalette-item:hover:not(.lm-mod-active):not(.lm-mod-disabled) {
  background: var(--jp-layout-color2);
}

.lm-CommandPalette-itemContent {
  overflow: hidden;
}

.lm-CommandPalette-itemLabel > mark {
  color: var(--jp-ui-font-color0);
  background-color: transparent;
  font-weight: bold;
}

.lm-CommandPalette-item.lm-mod-disabled mark {
  color: var(--jp-ui-font-color3);
}

.lm-CommandPalette-item .lm-CommandPalette-itemIcon {
  margin: 0 4px 0 0;
  position: relative;
  width: 16px;
  top: 2px;
  flex: 0 0 auto;
}

.lm-CommandPalette-item.lm-mod-disabled .lm-CommandPalette-itemIcon {
  opacity: 0.4;
}

.lm-CommandPalette-item .lm-CommandPalette-itemShortcut {
  flex: 0 0 auto;
}

.lm-CommandPalette-itemCaption {
  display: none;
}

.lm-CommandPalette-content {
  background-color: var(--jp-layout-color1);
}

.lm-CommandPalette-content:empty:after {
  content: 'No results';
  margin: auto;
  margin-top: 20px;
  width: 100px;
  display: block;
  font-size: var(--jp-ui-font-size2);
  font-family: var(--jp-ui-font-family);
  font-weight: lighter;
}

.lm-CommandPalette-emptyMessage {
  text-align: center;
  margin-top: 24px;
  line-height: 1.32;
  padding: 0px 8px;
  color: var(--jp-content-font-color3);
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2017, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Dialog {
  position: absolute;
  z-index: 10000;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  top: 0px;
  left: 0px;
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100%;
  background: var(--jp-dialog-background);
}

.jp-Dialog-content {
  display: flex;
  flex-direction: column;
  margin-left: auto;
  margin-right: auto;
  background: var(--jp-layout-color1);
  padding: 24px;
  padding-bottom: 12px;
  min-width: 300px;
  min-height: 150px;
  max-width: 1000px;
  max-height: 500px;
  box-sizing: border-box;
  box-shadow: var(--jp-elevation-z20);
  word-wrap: break-word;
  border-radius: var(--jp-border-radius);
  /* This is needed so that all font sizing of children done in ems is
   * relative to this base size */
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color1);
  resize: both;
}

.jp-Dialog-button {
  overflow: visible;
}

button.jp-Dialog-button:focus {
  outline: 1px solid var(--jp-brand-color1);
  outline-offset: 4px;
  -moz-outline-radius: 0px;
}

button.jp-Dialog-button:focus::-moz-focus-inner {
  border: 0;
}

button.jp-Dialog-close-button {
  padding: 0;
  height: 100%;
  min-width: unset;
  min-height: unset;
}

.jp-Dialog-header {
  display: flex;
  justify-content: space-between;
  flex: 0 0 auto;
  padding-bottom: 12px;
  font-size: var(--jp-ui-font-size3);
  font-weight: 400;
  color: var(--jp-ui-font-color0);
}

.jp-Dialog-body {
  display: flex;
  flex-direction: column;
  flex: 1 1 auto;
  font-size: var(--jp-ui-font-size1);
  background: var(--jp-layout-color1);
  overflow: auto;
}

.jp-Dialog-footer {
  display: flex;
  flex-direction: row;
  justify-content: flex-end;
  flex: 0 0 auto;
  margin-left: -12px;
  margin-right: -12px;
  padding: 12px;
}

.jp-Dialog-title {
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}

.jp-Dialog-body > .jp-select-wrapper {
  width: 100%;
}

.jp-Dialog-body > button {
  padding: 0px 16px;
}

.jp-Dialog-body > label {
  line-height: 1.4;
  color: var(--jp-ui-font-color0);
}

.jp-Dialog-button.jp-mod-styled:not(:last-child) {
  margin-right: 12px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2016, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-HoverBox {
  position: fixed;
}

.jp-HoverBox.jp-mod-outofview {
  display: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-IFrame {
  width: 100%;
  height: 100%;
}

.jp-IFrame > iframe {
  border: none;
}

/*
When drag events occur, `p-mod-override-cursor` is added to the body.
Because iframes steal all cursor events, the following two rules are necessary
to suppress pointer events while resize drags are occurring. There may be a
better solution to this problem.
*/
body.lm-mod-override-cursor .jp-IFrame {
  position: relative;
}

body.lm-mod-override-cursor .jp-IFrame:before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: transparent;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2016, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-MainAreaWidget > :focus {
  outline: none;
}

/**
 * google-material-color v1.2.6
 * https://github.com/danlevan/google-material-color
 */
:root {
  --md-red-50: #ffebee;
  --md-red-100: #ffcdd2;
  --md-red-200: #ef9a9a;
  --md-red-300: #e57373;
  --md-red-400: #ef5350;
  --md-red-500: #f44336;
  --md-red-600: #e53935;
  --md-red-700: #d32f2f;
  --md-red-800: #c62828;
  --md-red-900: #b71c1c;
  --md-red-A100: #ff8a80;
  --md-red-A200: #ff5252;
  --md-red-A400: #ff1744;
  --md-red-A700: #d50000;

  --md-pink-50: #fce4ec;
  --md-pink-100: #f8bbd0;
  --md-pink-200: #f48fb1;
  --md-pink-300: #f06292;
  --md-pink-400: #ec407a;
  --md-pink-500: #e91e63;
  --md-pink-600: #d81b60;
  --md-pink-700: #c2185b;
  --md-pink-800: #ad1457;
  --md-pink-900: #880e4f;
  --md-pink-A100: #ff80ab;
  --md-pink-A200: #ff4081;
  --md-pink-A400: #f50057;
  --md-pink-A700: #c51162;

  --md-purple-50: #f3e5f5;
  --md-purple-100: #e1bee7;
  --md-purple-200: #ce93d8;
  --md-purple-300: #ba68c8;
  --md-purple-400: #ab47bc;
  --md-purple-500: #9c27b0;
  --md-purple-600: #8e24aa;
  --md-purple-700: #7b1fa2;
  --md-purple-800: #6a1b9a;
  --md-purple-900: #4a148c;
  --md-purple-A100: #ea80fc;
  --md-purple-A200: #e040fb;
  --md-purple-A400: #d500f9;
  --md-purple-A700: #aa00ff;

  --md-deep-purple-50: #ede7f6;
  --md-deep-purple-100: #d1c4e9;
  --md-deep-purple-200: #b39ddb;
  --md-deep-purple-300: #9575cd;
  --md-deep-purple-400: #7e57c2;
  --md-deep-purple-500: #673ab7;
  --md-deep-purple-600: #5e35b1;
  --md-deep-purple-700: #512da8;
  --md-deep-purple-800: #4527a0;
  --md-deep-purple-900: #311b92;
  --md-deep-purple-A100: #b388ff;
  --md-deep-purple-A200: #7c4dff;
  --md-deep-purple-A400: #651fff;
  --md-deep-purple-A700: #6200ea;

  --md-indigo-50: #e8eaf6;
  --md-indigo-100: #c5cae9;
  --md-indigo-200: #9fa8da;
  --md-indigo-300: #7986cb;
  --md-indigo-400: #5c6bc0;
  --md-indigo-500: #3f51b5;
  --md-indigo-600: #3949ab;
  --md-indigo-700: #303f9f;
  --md-indigo-800: #283593;
  --md-indigo-900: #1a237e;
  --md-indigo-A100: #8c9eff;
  --md-indigo-A200: #536dfe;
  --md-indigo-A400: #3d5afe;
  --md-indigo-A700: #304ffe;

  --md-blue-50: #e3f2fd;
  --md-blue-100: #bbdefb;
  --md-blue-200: #90caf9;
  --md-blue-300: #64b5f6;
  --md-blue-400: #42a5f5;
  --md-blue-500: #2196f3;
  --md-blue-600: #1e88e5;
  --md-blue-700: #1976d2;
  --md-blue-800: #1565c0;
  --md-blue-900: #0d47a1;
  --md-blue-A100: #82b1ff;
  --md-blue-A200: #448aff;
  --md-blue-A400: #2979ff;
  --md-blue-A700: #2962ff;

  --md-light-blue-50: #e1f5fe;
  --md-light-blue-100: #b3e5fc;
  --md-light-blue-200: #81d4fa;
  --md-light-blue-300: #4fc3f7;
  --md-light-blue-400: #29b6f6;
  --md-light-blue-500: #03a9f4;
  --md-light-blue-600: #039be5;
  --md-light-blue-700: #0288d1;
  --md-light-blue-800: #0277bd;
  --md-light-blue-900: #01579b;
  --md-light-blue-A100: #80d8ff;
  --md-light-blue-A200: #40c4ff;
  --md-light-blue-A400: #00b0ff;
  --md-light-blue-A700: #0091ea;

  --md-cyan-50: #e0f7fa;
  --md-cyan-100: #b2ebf2;
  --md-cyan-200: #80deea;
  --md-cyan-300: #4dd0e1;
  --md-cyan-400: #26c6da;
  --md-cyan-500: #00bcd4;
  --md-cyan-600: #00acc1;
  --md-cyan-700: #0097a7;
  --md-cyan-800: #00838f;
  --md-cyan-900: #006064;
  --md-cyan-A100: #84ffff;
  --md-cyan-A200: #18ffff;
  --md-cyan-A400: #00e5ff;
  --md-cyan-A700: #00b8d4;

  --md-teal-50: #e0f2f1;
  --md-teal-100: #b2dfdb;
  --md-teal-200: #80cbc4;
  --md-teal-300: #4db6ac;
  --md-teal-400: #26a69a;
  --md-teal-500: #009688;
  --md-teal-600: #00897b;
  --md-teal-700: #00796b;
  --md-teal-800: #00695c;
  --md-teal-900: #004d40;
  --md-teal-A100: #a7ffeb;
  --md-teal-A200: #64ffda;
  --md-teal-A400: #1de9b6;
  --md-teal-A700: #00bfa5;

  --md-green-50: #e8f5e9;
  --md-green-100: #c8e6c9;
  --md-green-200: #a5d6a7;
  --md-green-300: #81c784;
  --md-green-400: #66bb6a;
  --md-green-500: #4caf50;
  --md-green-600: #43a047;
  --md-green-700: #388e3c;
  --md-green-800: #2e7d32;
  --md-green-900: #1b5e20;
  --md-green-A100: #b9f6ca;
  --md-green-A200: #69f0ae;
  --md-green-A400: #00e676;
  --md-green-A700: #00c853;

  --md-light-green-50: #f1f8e9;
  --md-light-green-100: #dcedc8;
  --md-light-green-200: #c5e1a5;
  --md-light-green-300: #aed581;
  --md-light-green-400: #9ccc65;
  --md-light-green-500: #8bc34a;
  --md-light-green-600: #7cb342;
  --md-light-green-700: #689f38;
  --md-light-green-800: #558b2f;
  --md-light-green-900: #33691e;
  --md-light-green-A100: #ccff90;
  --md-light-green-A200: #b2ff59;
  --md-light-green-A400: #76ff03;
  --md-light-green-A700: #64dd17;

  --md-lime-50: #f9fbe7;
  --md-lime-100: #f0f4c3;
  --md-lime-200: #e6ee9c;
  --md-lime-300: #dce775;
  --md-lime-400: #d4e157;
  --md-lime-500: #cddc39;
  --md-lime-600: #c0ca33;
  --md-lime-700: #afb42b;
  --md-lime-800: #9e9d24;
  --md-lime-900: #827717;
  --md-lime-A100: #f4ff81;
  --md-lime-A200: #eeff41;
  --md-lime-A400: #c6ff00;
  --md-lime-A700: #aeea00;

  --md-yellow-50: #fffde7;
  --md-yellow-100: #fff9c4;
  --md-yellow-200: #fff59d;
  --md-yellow-300: #fff176;
  --md-yellow-400: #ffee58;
  --md-yellow-500: #ffeb3b;
  --md-yellow-600: #fdd835;
  --md-yellow-700: #fbc02d;
  --md-yellow-800: #f9a825;
  --md-yellow-900: #f57f17;
  --md-yellow-A100: #ffff8d;
  --md-yellow-A200: #ffff00;
  --md-yellow-A400: #ffea00;
  --md-yellow-A700: #ffd600;

  --md-amber-50: #fff8e1;
  --md-amber-100: #ffecb3;
  --md-amber-200: #ffe082;
  --md-amber-300: #ffd54f;
  --md-amber-400: #ffca28;
  --md-amber-500: #ffc107;
  --md-amber-600: #ffb300;
  --md-amber-700: #ffa000;
  --md-amber-800: #ff8f00;
  --md-amber-900: #ff6f00;
  --md-amber-A100: #ffe57f;
  --md-amber-A200: #ffd740;
  --md-amber-A400: #ffc400;
  --md-amber-A700: #ffab00;

  --md-orange-50: #fff3e0;
  --md-orange-100: #ffe0b2;
  --md-orange-200: #ffcc80;
  --md-orange-300: #ffb74d;
  --md-orange-400: #ffa726;
  --md-orange-500: #ff9800;
  --md-orange-600: #fb8c00;
  --md-orange-700: #f57c00;
  --md-orange-800: #ef6c00;
  --md-orange-900: #e65100;
  --md-orange-A100: #ffd180;
  --md-orange-A200: #ffab40;
  --md-orange-A400: #ff9100;
  --md-orange-A700: #ff6d00;

  --md-deep-orange-50: #fbe9e7;
  --md-deep-orange-100: #ffccbc;
  --md-deep-orange-200: #ffab91;
  --md-deep-orange-300: #ff8a65;
  --md-deep-orange-400: #ff7043;
  --md-deep-orange-500: #ff5722;
  --md-deep-orange-600: #f4511e;
  --md-deep-orange-700: #e64a19;
  --md-deep-orange-800: #d84315;
  --md-deep-orange-900: #bf360c;
  --md-deep-orange-A100: #ff9e80;
  --md-deep-orange-A200: #ff6e40;
  --md-deep-orange-A400: #ff3d00;
  --md-deep-orange-A700: #dd2c00;

  --md-brown-50: #efebe9;
  --md-brown-100: #d7ccc8;
  --md-brown-200: #bcaaa4;
  --md-brown-300: #a1887f;
  --md-brown-400: #8d6e63;
  --md-brown-500: #795548;
  --md-brown-600: #6d4c41;
  --md-brown-700: #5d4037;
  --md-brown-800: #4e342e;
  --md-brown-900: #3e2723;

  --md-grey-50: #fafafa;
  --md-grey-100: #f5f5f5;
  --md-grey-200: #eeeeee;
  --md-grey-300: #e0e0e0;
  --md-grey-400: #bdbdbd;
  --md-grey-500: #9e9e9e;
  --md-grey-600: #757575;
  --md-grey-700: #616161;
  --md-grey-800: #424242;
  --md-grey-900: #212121;

  --md-blue-grey-50: #eceff1;
  --md-blue-grey-100: #cfd8dc;
  --md-blue-grey-200: #b0bec5;
  --md-blue-grey-300: #90a4ae;
  --md-blue-grey-400: #78909c;
  --md-blue-grey-500: #607d8b;
  --md-blue-grey-600: #546e7a;
  --md-blue-grey-700: #455a64;
  --md-blue-grey-800: #37474f;
  --md-blue-grey-900: #263238;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2017, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Spinner {
  position: absolute;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 10;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background: var(--jp-layout-color0);
  outline: none;
}

.jp-SpinnerContent {
  font-size: 10px;
  margin: 50px auto;
  text-indent: -9999em;
  width: 3em;
  height: 3em;
  border-radius: 50%;
  background: var(--jp-brand-color3);
  background: linear-gradient(
    to right,
    #f37626 10%,
    rgba(255, 255, 255, 0) 42%
  );
  position: relative;
  animation: load3 1s infinite linear, fadeIn 1s;
}

.jp-SpinnerContent:before {
  width: 50%;
  height: 50%;
  background: #f37626;
  border-radius: 100% 0 0 0;
  position: absolute;
  top: 0;
  left: 0;
  content: '';
}

.jp-SpinnerContent:after {
  background: var(--jp-layout-color0);
  width: 75%;
  height: 75%;
  border-radius: 50%;
  content: '';
  margin: auto;
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
}

@keyframes fadeIn {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}

@keyframes load3 {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2017, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

button.jp-mod-styled {
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color0);
  border: none;
  box-sizing: border-box;
  text-align: center;
  line-height: 32px;
  height: 32px;
  padding: 0px 12px;
  letter-spacing: 0.8px;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
}

input.jp-mod-styled {
  background: var(--jp-input-background);
  height: 28px;
  box-sizing: border-box;
  border: var(--jp-border-width) solid var(--jp-border-color1);
  padding-left: 7px;
  padding-right: 7px;
  font-size: var(--jp-ui-font-size2);
  color: var(--jp-ui-font-color0);
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
}

input.jp-mod-styled:focus {
  border: var(--jp-border-width) solid var(--md-blue-500);
  box-shadow: inset 0 0 4px var(--md-blue-300);
}

.jp-select-wrapper {
  display: flex;
  position: relative;
  flex-direction: column;
  padding: 1px;
  background-color: var(--jp-layout-color1);
  height: 28px;
  box-sizing: border-box;
  margin-bottom: 12px;
}

.jp-select-wrapper.jp-mod-focused select.jp-mod-styled {
  border: var(--jp-border-width) solid var(--jp-input-active-border-color);
  box-shadow: var(--jp-input-box-shadow);
  background-color: var(--jp-input-active-background);
}

select.jp-mod-styled:hover {
  background-color: var(--jp-layout-color1);
  cursor: pointer;
  color: var(--jp-ui-font-color0);
  background-color: var(--jp-input-hover-background);
  box-shadow: inset 0 0px 1px rgba(0, 0, 0, 0.5);
}

select.jp-mod-styled {
  flex: 1 1 auto;
  height: 32px;
  width: 100%;
  font-size: var(--jp-ui-font-size2);
  background: var(--jp-input-background);
  color: var(--jp-ui-font-color0);
  padding: 0 25px 0 8px;
  border: var(--jp-border-width) solid var(--jp-input-border-color);
  border-radius: 0px;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2016, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

:root {
  --jp-private-toolbar-height: calc(
    28px + var(--jp-border-width)
  ); /* leave 28px for content */
}

.jp-Toolbar {
  color: var(--jp-ui-font-color1);
  flex: 0 0 auto;
  display: flex;
  flex-direction: row;
  border-bottom: var(--jp-border-width) solid var(--jp-toolbar-border-color);
  box-shadow: var(--jp-toolbar-box-shadow);
  background: var(--jp-toolbar-background);
  min-height: var(--jp-toolbar-micro-height);
  padding: 2px;
  z-index: 1;
  overflow-x: hidden;
}

.jp-Toolbar:hover {
  overflow-x: auto;
}

/* Toolbar items */

.jp-Toolbar > .jp-Toolbar-item.jp-Toolbar-spacer {
  flex-grow: 1;
  flex-shrink: 1;
}

.jp-Toolbar-item.jp-Toolbar-kernelStatus {
  display: inline-block;
  width: 32px;
  background-repeat: no-repeat;
  background-position: center;
  background-size: 16px;
}

.jp-Toolbar > .jp-Toolbar-item {
  flex: 0 0 auto;
  display: flex;
  padding-left: 1px;
  padding-right: 1px;
  font-size: var(--jp-ui-font-size1);
  line-height: var(--jp-private-toolbar-height);
  height: 100%;
}

/* Toolbar buttons */

/* This is the div we use to wrap the react component into a Widget */
div.jp-ToolbarButton {
  color: transparent;
  border: none;
  box-sizing: border-box;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
  padding: 0px;
  margin: 0px;
}

button.jp-ToolbarButtonComponent {
  background: var(--jp-layout-color1);
  border: none;
  box-sizing: border-box;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
  padding: 0px 6px;
  margin: 0px;
  height: 24px;
  border-radius: var(--jp-border-radius);
  display: flex;
  align-items: center;
  text-align: center;
  font-size: 14px;
  min-width: unset;
  min-height: unset;
}

button.jp-ToolbarButtonComponent:disabled {
  opacity: 0.4;
}

button.jp-ToolbarButtonComponent span {
  padding: 0px;
  flex: 0 0 auto;
}

button.jp-ToolbarButtonComponent .jp-ToolbarButtonComponent-label {
  font-size: var(--jp-ui-font-size1);
  line-height: 100%;
  padding-left: 2px;
  color: var(--jp-ui-font-color1);
}

#jp-main-dock-panel[data-mode='single-document']
  .jp-MainAreaWidget
  > .jp-Toolbar.jp-Toolbar-micro {
  padding: 0;
  min-height: 0;
}

#jp-main-dock-panel[data-mode='single-document']
  .jp-MainAreaWidget
  > .jp-Toolbar {
  border: none;
  box-shadow: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2017, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ body.p-mod-override-cursor *, /* </DEPRECATED> */
body.lm-mod-override-cursor * {
  cursor: inherit !important;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2016, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-JSONEditor {
  display: flex;
  flex-direction: column;
  width: 100%;
}

.jp-JSONEditor-host {
  flex: 1 1 auto;
  border: var(--jp-border-width) solid var(--jp-input-border-color);
  border-radius: 0px;
  background: var(--jp-layout-color0);
  min-height: 50px;
  padding: 1px;
}

.jp-JSONEditor.jp-mod-error .jp-JSONEditor-host {
  border-color: red;
  outline-color: red;
}

.jp-JSONEditor-header {
  display: flex;
  flex: 1 0 auto;
  padding: 0 0 0 12px;
}

.jp-JSONEditor-header label {
  flex: 0 0 auto;
}

.jp-JSONEditor-commitButton {
  height: 16px;
  width: 16px;
  background-size: 18px;
  background-repeat: no-repeat;
  background-position: center;
}

.jp-JSONEditor-host.jp-mod-focused {
  background-color: var(--jp-input-active-background);
  border: 1px solid var(--jp-input-active-border-color);
  box-shadow: var(--jp-input-box-shadow);
}

.jp-Editor.jp-mod-dropTarget {
  border: var(--jp-border-width) solid var(--jp-input-active-border-color);
  box-shadow: var(--jp-input-box-shadow);
}

/* BASICS */

.CodeMirror {
  /* Set height, width, borders, and global font properties here */
  font-family: monospace;
  height: 300px;
  color: black;
  direction: ltr;
}

/* PADDING */

.CodeMirror-lines {
  padding: 4px 0; /* Vertical padding around content */
}
.CodeMirror pre.CodeMirror-line,
.CodeMirror pre.CodeMirror-line-like {
  padding: 0 4px; /* Horizontal padding of content */
}

.CodeMirror-scrollbar-filler, .CodeMirror-gutter-filler {
  background-color: white; /* The little square between H and V scrollbars */
}

/* GUTTER */

.CodeMirror-gutters {
  border-right: 1px solid #ddd;
  background-color: #f7f7f7;
  white-space: nowrap;
}
.CodeMirror-linenumbers {}
.CodeMirror-linenumber {
  padding: 0 3px 0 5px;
  min-width: 20px;
  text-align: right;
  color: #999;
  white-space: nowrap;
}

.CodeMirror-guttermarker { color: black; }
.CodeMirror-guttermarker-subtle { color: #999; }

/* CURSOR */

.CodeMirror-cursor {
  border-left: 1px solid black;
  border-right: none;
  width: 0;
}
/* Shown when moving in bi-directional text */
.CodeMirror div.CodeMirror-secondarycursor {
  border-left: 1px solid silver;
}
.cm-fat-cursor .CodeMirror-cursor {
  width: auto;
  border: 0 !important;
  background: #7e7;
}
.cm-fat-cursor div.CodeMirror-cursors {
  z-index: 1;
}
.cm-fat-cursor-mark {
  background-color: rgba(20, 255, 20, 0.5);
  -webkit-animation: blink 1.06s steps(1) infinite;
  -moz-animation: blink 1.06s steps(1) infinite;
  animation: blink 1.06s steps(1) infinite;
}
.cm-animate-fat-cursor {
  width: auto;
  border: 0;
  -webkit-animation: blink 1.06s steps(1) infinite;
  -moz-animation: blink 1.06s steps(1) infinite;
  animation: blink 1.06s steps(1) infinite;
  background-color: #7e7;
}
@-moz-keyframes blink {
  0% {}
  50% { background-color: transparent; }
  100% {}
}
@-webkit-keyframes blink {
  0% {}
  50% { background-color: transparent; }
  100% {}
}
@keyframes blink {
  0% {}
  50% { background-color: transparent; }
  100% {}
}

/* Can style cursor different in overwrite (non-insert) mode */
.CodeMirror-overwrite .CodeMirror-cursor {}

.cm-tab { display: inline-block; text-decoration: inherit; }

.CodeMirror-rulers {
  position: absolute;
  left: 0; right: 0; top: -50px; bottom: 0;
  overflow: hidden;
}
.CodeMirror-ruler {
  border-left: 1px solid #ccc;
  top: 0; bottom: 0;
  position: absolute;
}

/* DEFAULT THEME */

.cm-s-default .cm-header {color: blue;}
.cm-s-default .cm-quote {color: #090;}
.cm-negative {color: #d44;}
.cm-positive {color: #292;}
.cm-header, .cm-strong {font-weight: bold;}
.cm-em {font-style: italic;}
.cm-link {text-decoration: underline;}
.cm-strikethrough {text-decoration: line-through;}

.cm-s-default .cm-keyword {color: #708;}
.cm-s-default .cm-atom {color: #219;}
.cm-s-default .cm-number {color: #164;}
.cm-s-default .cm-def {color: #00f;}
.cm-s-default .cm-variable,
.cm-s-default .cm-punctuation,
.cm-s-default .cm-property,
.cm-s-default .cm-operator {}
.cm-s-default .cm-variable-2 {color: #05a;}
.cm-s-default .cm-variable-3, .cm-s-default .cm-type {color: #085;}
.cm-s-default .cm-comment {color: #a50;}
.cm-s-default .cm-string {color: #a11;}
.cm-s-default .cm-string-2 {color: #f50;}
.cm-s-default .cm-meta {color: #555;}
.cm-s-default .cm-qualifier {color: #555;}
.cm-s-default .cm-builtin {color: #30a;}
.cm-s-default .cm-bracket {color: #997;}
.cm-s-default .cm-tag {color: #170;}
.cm-s-default .cm-attribute {color: #00c;}
.cm-s-default .cm-hr {color: #999;}
.cm-s-default .cm-link {color: #00c;}

.cm-s-default .cm-error {color: #f00;}
.cm-invalidchar {color: #f00;}

.CodeMirror-composing { border-bottom: 2px solid; }

/* Default styles for common addons */

div.CodeMirror span.CodeMirror-matchingbracket {color: #0b0;}
div.CodeMirror span.CodeMirror-nonmatchingbracket {color: #a22;}
.CodeMirror-matchingtag { background: rgba(255, 150, 0, .3); }
.CodeMirror-activeline-background {background: #e8f2ff;}

/* STOP */

/* The rest of this file contains styles related to the mechanics of
   the editor. You probably shouldn't touch them. */

.CodeMirror {
  position: relative;
  overflow: hidden;
  background: white;
}

.CodeMirror-scroll {
  overflow: scroll !important; /* Things will break if this is overridden */
  /* 50px is the magic margin used to hide the element's real scrollbars */
  /* See overflow: hidden in .CodeMirror */
  margin-bottom: -50px; margin-right: -50px;
  padding-bottom: 50px;
  height: 100%;
  outline: none; /* Prevent dragging from highlighting the element */
  position: relative;
}
.CodeMirror-sizer {
  position: relative;
  border-right: 50px solid transparent;
}

/* The fake, visible scrollbars. Used to force redraw during scrolling
   before actual scrolling happens, thus preventing shaking and
   flickering artifacts. */
.CodeMirror-vscrollbar, .CodeMirror-hscrollbar, .CodeMirror-scrollbar-filler, .CodeMirror-gutter-filler {
  position: absolute;
  z-index: 6;
  display: none;
}
.CodeMirror-vscrollbar {
  right: 0; top: 0;
  overflow-x: hidden;
  overflow-y: scroll;
}
.CodeMirror-hscrollbar {
  bottom: 0; left: 0;
  overflow-y: hidden;
  overflow-x: scroll;
}
.CodeMirror-scrollbar-filler {
  right: 0; bottom: 0;
}
.CodeMirror-gutter-filler {
  left: 0; bottom: 0;
}

.CodeMirror-gutters {
  position: absolute; left: 0; top: 0;
  min-height: 100%;
  z-index: 3;
}
.CodeMirror-gutter {
  white-space: normal;
  height: 100%;
  display: inline-block;
  vertical-align: top;
  margin-bottom: -50px;
}
.CodeMirror-gutter-wrapper {
  position: absolute;
  z-index: 4;
  background: none !important;
  border: none !important;
}
.CodeMirror-gutter-background {
  position: absolute;
  top: 0; bottom: 0;
  z-index: 4;
}
.CodeMirror-gutter-elt {
  position: absolute;
  cursor: default;
  z-index: 4;
}
.CodeMirror-gutter-wrapper ::selection { background-color: transparent }
.CodeMirror-gutter-wrapper ::-moz-selection { background-color: transparent }

.CodeMirror-lines {
  cursor: text;
  min-height: 1px; /* prevents collapsing before first draw */
}
.CodeMirror pre.CodeMirror-line,
.CodeMirror pre.CodeMirror-line-like {
  /* Reset some styles that the rest of the page might have set */
  -moz-border-radius: 0; -webkit-border-radius: 0; border-radius: 0;
  border-width: 0;
  background: transparent;
  font-family: inherit;
  font-size: inherit;
  margin: 0;
  white-space: pre;
  word-wrap: normal;
  line-height: inherit;
  color: inherit;
  z-index: 2;
  position: relative;
  overflow: visible;
  -webkit-tap-highlight-color: transparent;
  -webkit-font-variant-ligatures: contextual;
  font-variant-ligatures: contextual;
}
.CodeMirror-wrap pre.CodeMirror-line,
.CodeMirror-wrap pre.CodeMirror-line-like {
  word-wrap: break-word;
  white-space: pre-wrap;
  word-break: normal;
}

.CodeMirror-linebackground {
  position: absolute;
  left: 0; right: 0; top: 0; bottom: 0;
  z-index: 0;
}

.CodeMirror-linewidget {
  position: relative;
  z-index: 2;
  padding: 0.1px; /* Force widget margins to stay inside of the container */
}

.CodeMirror-widget {}

.CodeMirror-rtl pre { direction: rtl; }

.CodeMirror-code {
  outline: none;
}

/* Force content-box sizing for the elements where we expect it */
.CodeMirror-scroll,
.CodeMirror-sizer,
.CodeMirror-gutter,
.CodeMirror-gutters,
.CodeMirror-linenumber {
  -moz-box-sizing: content-box;
  box-sizing: content-box;
}

.CodeMirror-measure {
  position: absolute;
  width: 100%;
  height: 0;
  overflow: hidden;
  visibility: hidden;
}

.CodeMirror-cursor {
  position: absolute;
  pointer-events: none;
}
.CodeMirror-measure pre { position: static; }

div.CodeMirror-cursors {
  visibility: hidden;
  position: relative;
  z-index: 3;
}
div.CodeMirror-dragcursors {
  visibility: visible;
}

.CodeMirror-focused div.CodeMirror-cursors {
  visibility: visible;
}

.CodeMirror-selected { background: #d9d9d9; }
.CodeMirror-focused .CodeMirror-selected { background: #d7d4f0; }
.CodeMirror-crosshair { cursor: crosshair; }
.CodeMirror-line::selection, .CodeMirror-line > span::selection, .CodeMirror-line > span > span::selection { background: #d7d4f0; }
.CodeMirror-line::-moz-selection, .CodeMirror-line > span::-moz-selection, .CodeMirror-line > span > span::-moz-selection { background: #d7d4f0; }

.cm-searching {
  background-color: #ffa;
  background-color: rgba(255, 255, 0, .4);
}

/* Used to force a border model for a node */
.cm-force-border { padding-right: .1px; }

@media print {
  /* Hide the cursor when printing */
  .CodeMirror div.CodeMirror-cursors {
    visibility: hidden;
  }
}

/* See issue #2901 */
.cm-tab-wrap-hack:after { content: ''; }

/* Help users use markselection to safely style text background */
span.CodeMirror-selectedtext { background: none; }

.CodeMirror-dialog {
  position: absolute;
  left: 0; right: 0;
  background: inherit;
  z-index: 15;
  padding: .1em .8em;
  overflow: hidden;
  color: inherit;
}

.CodeMirror-dialog-top {
  border-bottom: 1px solid #eee;
  top: 0;
}

.CodeMirror-dialog-bottom {
  border-top: 1px solid #eee;
  bottom: 0;
}

.CodeMirror-dialog input {
  border: none;
  outline: none;
  background: transparent;
  width: 20em;
  color: inherit;
  font-family: monospace;
}

.CodeMirror-dialog button {
  font-size: 70%;
}

.CodeMirror-foldmarker {
  color: blue;
  text-shadow: #b9f 1px 1px 2px, #b9f -1px -1px 2px, #b9f 1px -1px 2px, #b9f -1px 1px 2px;
  font-family: arial;
  line-height: .3;
  cursor: pointer;
}
.CodeMirror-foldgutter {
  width: .7em;
}
.CodeMirror-foldgutter-open,
.CodeMirror-foldgutter-folded {
  cursor: pointer;
}
.CodeMirror-foldgutter-open:after {
  content: "\25BE";
}
.CodeMirror-foldgutter-folded:after {
  content: "\25B8";
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.CodeMirror {
  line-height: var(--jp-code-line-height);
  font-size: var(--jp-code-font-size);
  font-family: var(--jp-code-font-family);
  border: 0;
  border-radius: 0;
  height: auto;
  /* Changed to auto to autogrow */
}

.CodeMirror pre {
  padding: 0 var(--jp-code-padding);
}

.jp-CodeMirrorEditor[data-type='inline'] .CodeMirror-dialog {
  background-color: var(--jp-layout-color0);
  color: var(--jp-content-font-color1);
}

/* This causes https://github.com/jupyter/jupyterlab/issues/522 */
/* May not cause it not because we changed it! */
.CodeMirror-lines {
  padding: var(--jp-code-padding) 0;
}

.CodeMirror-linenumber {
  padding: 0 8px;
}

.jp-CodeMirrorEditor {
  cursor: text;
}

.jp-CodeMirrorEditor[data-type='inline'] .CodeMirror-cursor {
  border-left: var(--jp-code-cursor-width0) solid var(--jp-editor-cursor-color);
}

/* When zoomed out 67% and 33% on a screen of 1440 width x 900 height */
@media screen and (min-width: 2138px) and (max-width: 4319px) {
  .jp-CodeMirrorEditor[data-type='inline'] .CodeMirror-cursor {
    border-left: var(--jp-code-cursor-width1) solid
      var(--jp-editor-cursor-color);
  }
}

/* When zoomed out less than 33% */
@media screen and (min-width: 4320px) {
  .jp-CodeMirrorEditor[data-type='inline'] .CodeMirror-cursor {
    border-left: var(--jp-code-cursor-width2) solid
      var(--jp-editor-cursor-color);
  }
}

.CodeMirror.jp-mod-readOnly .CodeMirror-cursor {
  display: none;
}

.CodeMirror-gutters {
  border-right: 1px solid var(--jp-border-color2);
  background-color: var(--jp-layout-color0);
}

.jp-CollaboratorCursor {
  border-left: 5px solid transparent;
  border-right: 5px solid transparent;
  border-top: none;
  border-bottom: 3px solid;
  background-clip: content-box;
  margin-left: -5px;
  margin-right: -5px;
}

.CodeMirror-selectedtext.cm-searching {
  background-color: var(--jp-search-selected-match-background-color) !important;
  color: var(--jp-search-selected-match-color) !important;
}

.cm-searching {
  background-color: var(
    --jp-search-unselected-match-background-color
  ) !important;
  color: var(--jp-search-unselected-match-color) !important;
}

.CodeMirror-focused .CodeMirror-selected {
  background-color: var(--jp-editor-selected-focused-background);
}

.CodeMirror-selected {
  background-color: var(--jp-editor-selected-background);
}

.jp-CollaboratorCursor-hover {
  position: absolute;
  z-index: 1;
  transform: translateX(-50%);
  color: white;
  border-radius: 3px;
  padding-left: 4px;
  padding-right: 4px;
  padding-top: 1px;
  padding-bottom: 1px;
  text-align: center;
  font-size: var(--jp-ui-font-size1);
  white-space: nowrap;
}

.jp-CodeMirror-ruler {
  border-left: 1px dashed var(--jp-border-color2);
}

/**
 * Here is our jupyter theme for CodeMirror syntax highlighting
 * This is used in our marked.js syntax highlighting and CodeMirror itself
 * The string "jupyter" is set in ../codemirror/widget.DEFAULT_CODEMIRROR_THEME
 * This came from the classic notebook, which came form highlight.js/GitHub
 */

/**
 * CodeMirror themes are handling the background/color in this way. This works
 * fine for CodeMirror editors outside the notebook, but the notebook styles
 * these things differently.
 */
.CodeMirror.cm-s-jupyter {
  background: var(--jp-layout-color0);
  color: var(--jp-content-font-color1);
}

/* In the notebook, we want this styling to be handled by its container */
.jp-CodeConsole .CodeMirror.cm-s-jupyter,
.jp-Notebook .CodeMirror.cm-s-jupyter {
  background: transparent;
}

.cm-s-jupyter .CodeMirror-cursor {
  border-left: var(--jp-code-cursor-width0) solid var(--jp-editor-cursor-color);
}
.cm-s-jupyter span.cm-keyword {
  color: var(--jp-mirror-editor-keyword-color);
  font-weight: bold;
}
.cm-s-jupyter span.cm-atom {
  color: var(--jp-mirror-editor-atom-color);
}
.cm-s-jupyter span.cm-number {
  color: var(--jp-mirror-editor-number-color);
}
.cm-s-jupyter span.cm-def {
  color: var(--jp-mirror-editor-def-color);
}
.cm-s-jupyter span.cm-variable {
  color: var(--jp-mirror-editor-variable-color);
}
.cm-s-jupyter span.cm-variable-2 {
  color: var(--jp-mirror-editor-variable-2-color);
}
.cm-s-jupyter span.cm-variable-3 {
  color: var(--jp-mirror-editor-variable-3-color);
}
.cm-s-jupyter span.cm-punctuation {
  color: var(--jp-mirror-editor-punctuation-color);
}
.cm-s-jupyter span.cm-property {
  color: var(--jp-mirror-editor-property-color);
}
.cm-s-jupyter span.cm-operator {
  color: var(--jp-mirror-editor-operator-color);
  font-weight: bold;
}
.cm-s-jupyter span.cm-comment {
  color: var(--jp-mirror-editor-comment-color);
  font-style: italic;
}
.cm-s-jupyter span.cm-string {
  color: var(--jp-mirror-editor-string-color);
}
.cm-s-jupyter span.cm-string-2 {
  color: var(--jp-mirror-editor-string-2-color);
}
.cm-s-jupyter span.cm-meta {
  color: var(--jp-mirror-editor-meta-color);
}
.cm-s-jupyter span.cm-qualifier {
  color: var(--jp-mirror-editor-qualifier-color);
}
.cm-s-jupyter span.cm-builtin {
  color: var(--jp-mirror-editor-builtin-color);
}
.cm-s-jupyter span.cm-bracket {
  color: var(--jp-mirror-editor-bracket-color);
}
.cm-s-jupyter span.cm-tag {
  color: var(--jp-mirror-editor-tag-color);
}
.cm-s-jupyter span.cm-attribute {
  color: var(--jp-mirror-editor-attribute-color);
}
.cm-s-jupyter span.cm-header {
  color: var(--jp-mirror-editor-header-color);
}
.cm-s-jupyter span.cm-quote {
  color: var(--jp-mirror-editor-quote-color);
}
.cm-s-jupyter span.cm-link {
  color: var(--jp-mirror-editor-link-color);
}
.cm-s-jupyter span.cm-error {
  color: var(--jp-mirror-editor-error-color);
}
.cm-s-jupyter span.cm-hr {
  color: #999;
}

.cm-s-jupyter span.cm-tab {
  background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAMCAYAAAAkuj5RAAAAAXNSR0IArs4c6QAAAGFJREFUSMft1LsRQFAQheHPowAKoACx3IgEKtaEHujDjORSgWTH/ZOdnZOcM/sgk/kFFWY0qV8foQwS4MKBCS3qR6ixBJvElOobYAtivseIE120FaowJPN75GMu8j/LfMwNjh4HUpwg4LUAAAAASUVORK5CYII=);
  background-position: right;
  background-repeat: no-repeat;
}

.cm-s-jupyter .CodeMirror-activeline-background,
.cm-s-jupyter .CodeMirror-gutter {
  background-color: var(--jp-layout-color2);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| RenderedText
|----------------------------------------------------------------------------*/

:root {
  /* This is the padding value to fill the gaps between lines containing spans with background color. */
  --jp-private-code-span-padding: calc(
    (var(--jp-code-line-height) - 1) * var(--jp-code-font-size) / 2
  );
}

.jp-RenderedText {
  text-align: left;
  padding-left: var(--jp-code-padding);
  line-height: var(--jp-code-line-height);
  font-family: var(--jp-code-font-family);
}

.jp-RenderedText pre,
.jp-RenderedJavaScript pre,
.jp-RenderedHTMLCommon pre {
  color: var(--jp-content-font-color1);
  font-size: var(--jp-code-font-size);
  border: none;
  margin: 0px;
  padding: 0px;
}

.jp-RenderedText pre a:link {
  text-decoration: none;
  color: var(--jp-content-link-color);
}
.jp-RenderedText pre a:hover {
  text-decoration: underline;
  color: var(--jp-content-link-color);
}
.jp-RenderedText pre a:visited {
  text-decoration: none;
  color: var(--jp-content-link-color);
}

/* console foregrounds and backgrounds */
.jp-RenderedText pre .ansi-black-fg {
  color: #3e424d;
}
.jp-RenderedText pre .ansi-red-fg {
  color: #e75c58;
}
.jp-RenderedText pre .ansi-green-fg {
  color: #00a250;
}
.jp-RenderedText pre .ansi-yellow-fg {
  color: #ddb62b;
}
.jp-RenderedText pre .ansi-blue-fg {
  color: #208ffb;
}
.jp-RenderedText pre .ansi-magenta-fg {
  color: #d160c4;
}
.jp-RenderedText pre .ansi-cyan-fg {
  color: #60c6c8;
}
.jp-RenderedText pre .ansi-white-fg {
  color: #c5c1b4;
}

.jp-RenderedText pre .ansi-black-bg {
  background-color: #3e424d;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-red-bg {
  background-color: #e75c58;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-green-bg {
  background-color: #00a250;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-yellow-bg {
  background-color: #ddb62b;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-blue-bg {
  background-color: #208ffb;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-magenta-bg {
  background-color: #d160c4;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-cyan-bg {
  background-color: #60c6c8;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-white-bg {
  background-color: #c5c1b4;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-black-intense-fg {
  color: #282c36;
}
.jp-RenderedText pre .ansi-red-intense-fg {
  color: #b22b31;
}
.jp-RenderedText pre .ansi-green-intense-fg {
  color: #007427;
}
.jp-RenderedText pre .ansi-yellow-intense-fg {
  color: #b27d12;
}
.jp-RenderedText pre .ansi-blue-intense-fg {
  color: #0065ca;
}
.jp-RenderedText pre .ansi-magenta-intense-fg {
  color: #a03196;
}
.jp-RenderedText pre .ansi-cyan-intense-fg {
  color: #258f8f;
}
.jp-RenderedText pre .ansi-white-intense-fg {
  color: #a1a6b2;
}

.jp-RenderedText pre .ansi-black-intense-bg {
  background-color: #282c36;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-red-intense-bg {
  background-color: #b22b31;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-green-intense-bg {
  background-color: #007427;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-yellow-intense-bg {
  background-color: #b27d12;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-blue-intense-bg {
  background-color: #0065ca;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-magenta-intense-bg {
  background-color: #a03196;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-cyan-intense-bg {
  background-color: #258f8f;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-white-intense-bg {
  background-color: #a1a6b2;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-default-inverse-fg {
  color: var(--jp-ui-inverse-font-color0);
}
.jp-RenderedText pre .ansi-default-inverse-bg {
  background-color: var(--jp-inverse-layout-color0);
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-bold {
  font-weight: bold;
}
.jp-RenderedText pre .ansi-underline {
  text-decoration: underline;
}

.jp-RenderedText[data-mime-type='application/vnd.jupyter.stderr'] {
  background: var(--jp-rendermime-error-background);
  padding-top: var(--jp-code-padding);
}

/*-----------------------------------------------------------------------------
| RenderedLatex
|----------------------------------------------------------------------------*/

.jp-RenderedLatex {
  color: var(--jp-content-font-color1);
  font-size: var(--jp-content-font-size1);
  line-height: var(--jp-content-line-height);
}

/* Left-justify outputs.*/
.jp-OutputArea-output.jp-RenderedLatex {
  padding: var(--jp-code-padding);
  text-align: left;
}

/*-----------------------------------------------------------------------------
| RenderedHTML
|----------------------------------------------------------------------------*/

.jp-RenderedHTMLCommon {
  color: var(--jp-content-font-color1);
  font-family: var(--jp-content-font-family);
  font-size: var(--jp-content-font-size1);
  line-height: var(--jp-content-line-height);
  /* Give a bit more R padding on Markdown text to keep line lengths reasonable */
  padding-right: 20px;
}

.jp-RenderedHTMLCommon em {
  font-style: italic;
}

.jp-RenderedHTMLCommon strong {
  font-weight: bold;
}

.jp-RenderedHTMLCommon u {
  text-decoration: underline;
}

.jp-RenderedHTMLCommon a:link {
  text-decoration: none;
  color: var(--jp-content-link-color);
}

.jp-RenderedHTMLCommon a:hover {
  text-decoration: underline;
  color: var(--jp-content-link-color);
}

.jp-RenderedHTMLCommon a:visited {
  text-decoration: none;
  color: var(--jp-content-link-color);
}

/* Headings */

.jp-RenderedHTMLCommon h1,
.jp-RenderedHTMLCommon h2,
.jp-RenderedHTMLCommon h3,
.jp-RenderedHTMLCommon h4,
.jp-RenderedHTMLCommon h5,
.jp-RenderedHTMLCommon h6 {
  line-height: var(--jp-content-heading-line-height);
  font-weight: var(--jp-content-heading-font-weight);
  font-style: normal;
  margin: var(--jp-content-heading-margin-top) 0
    var(--jp-content-heading-margin-bottom) 0;
}

.jp-RenderedHTMLCommon h1:first-child,
.jp-RenderedHTMLCommon h2:first-child,
.jp-RenderedHTMLCommon h3:first-child,
.jp-RenderedHTMLCommon h4:first-child,
.jp-RenderedHTMLCommon h5:first-child,
.jp-RenderedHTMLCommon h6:first-child {
  margin-top: calc(0.5 * var(--jp-content-heading-margin-top));
}

.jp-RenderedHTMLCommon h1:last-child,
.jp-RenderedHTMLCommon h2:last-child,
.jp-RenderedHTMLCommon h3:last-child,
.jp-RenderedHTMLCommon h4:last-child,
.jp-RenderedHTMLCommon h5:last-child,
.jp-RenderedHTMLCommon h6:last-child {
  margin-bottom: calc(0.5 * var(--jp-content-heading-margin-bottom));
}

.jp-RenderedHTMLCommon h1 {
  font-size: var(--jp-content-font-size5);
}

.jp-RenderedHTMLCommon h2 {
  font-size: var(--jp-content-font-size4);
}

.jp-RenderedHTMLCommon h3 {
  font-size: var(--jp-content-font-size3);
}

.jp-RenderedHTMLCommon h4 {
  font-size: var(--jp-content-font-size2);
}

.jp-RenderedHTMLCommon h5 {
  font-size: var(--jp-content-font-size1);
}

.jp-RenderedHTMLCommon h6 {
  font-size: var(--jp-content-font-size0);
}

/* Lists */

.jp-RenderedHTMLCommon ul:not(.list-inline),
.jp-RenderedHTMLCommon ol:not(.list-inline) {
  padding-left: 2em;
}

.jp-RenderedHTMLCommon ul {
  list-style: disc;
}

.jp-RenderedHTMLCommon ul ul {
  list-style: square;
}

.jp-RenderedHTMLCommon ul ul ul {
  list-style: circle;
}

.jp-RenderedHTMLCommon ol {
  list-style: decimal;
}

.jp-RenderedHTMLCommon ol ol {
  list-style: upper-alpha;
}

.jp-RenderedHTMLCommon ol ol ol {
  list-style: lower-alpha;
}

.jp-RenderedHTMLCommon ol ol ol ol {
  list-style: lower-roman;
}

.jp-RenderedHTMLCommon ol ol ol ol ol {
  list-style: decimal;
}

.jp-RenderedHTMLCommon ol,
.jp-RenderedHTMLCommon ul {
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon ul ul,
.jp-RenderedHTMLCommon ul ol,
.jp-RenderedHTMLCommon ol ul,
.jp-RenderedHTMLCommon ol ol {
  margin-bottom: 0em;
}

.jp-RenderedHTMLCommon hr {
  color: var(--jp-border-color2);
  background-color: var(--jp-border-color1);
  margin-top: 1em;
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon > pre {
  margin: 1.5em 2em;
}

.jp-RenderedHTMLCommon pre,
.jp-RenderedHTMLCommon code {
  border: 0;
  background-color: var(--jp-layout-color0);
  color: var(--jp-content-font-color1);
  font-family: var(--jp-code-font-family);
  font-size: inherit;
  line-height: var(--jp-code-line-height);
  padding: 0;
  white-space: pre-wrap;
}

.jp-RenderedHTMLCommon :not(pre) > code {
  background-color: var(--jp-layout-color2);
  padding: 1px 5px;
}

/* Tables */

.jp-RenderedHTMLCommon table {
  border-collapse: collapse;
  border-spacing: 0;
  border: none;
  color: var(--jp-ui-font-color1);
  font-size: 12px;
  table-layout: fixed;
  margin-left: auto;
  margin-right: auto;
}

.jp-RenderedHTMLCommon thead {
  border-bottom: var(--jp-border-width) solid var(--jp-border-color1);
  vertical-align: bottom;
}

.jp-RenderedHTMLCommon td,
.jp-RenderedHTMLCommon th,
.jp-RenderedHTMLCommon tr {
  vertical-align: middle;
  padding: 0.5em 0.5em;
  line-height: normal;
  white-space: normal;
  max-width: none;
  border: none;
}

.jp-RenderedMarkdown.jp-RenderedHTMLCommon td,
.jp-RenderedMarkdown.jp-RenderedHTMLCommon th {
  max-width: none;
}

:not(.jp-RenderedMarkdown).jp-RenderedHTMLCommon td,
:not(.jp-RenderedMarkdown).jp-RenderedHTMLCommon th,
:not(.jp-RenderedMarkdown).jp-RenderedHTMLCommon tr {
  text-align: right;
}

.jp-RenderedHTMLCommon th {
  font-weight: bold;
}

.jp-RenderedHTMLCommon tbody tr:nth-child(odd) {
  background: var(--jp-layout-color0);
}

.jp-RenderedHTMLCommon tbody tr:nth-child(even) {
  background: var(--jp-rendermime-table-row-background);
}

.jp-RenderedHTMLCommon tbody tr:hover {
  background: var(--jp-rendermime-table-row-hover-background);
}

.jp-RenderedHTMLCommon table {
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon p {
  text-align: left;
  margin: 0px;
}

.jp-RenderedHTMLCommon p {
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon img {
  -moz-force-broken-image-icon: 1;
}

/* Restrict to direct children as other images could be nested in other content. */
.jp-RenderedHTMLCommon > img {
  display: block;
  margin-left: 0;
  margin-right: 0;
  margin-bottom: 1em;
}

/* Change color behind transparent images if they need it... */
[data-jp-theme-light='false'] .jp-RenderedImage img.jp-needs-light-background {
  background-color: var(--jp-inverse-layout-color1);
}
[data-jp-theme-light='true'] .jp-RenderedImage img.jp-needs-dark-background {
  background-color: var(--jp-inverse-layout-color1);
}
/* ...or leave it untouched if they don't */
[data-jp-theme-light='false'] .jp-RenderedImage img.jp-needs-dark-background {
}
[data-jp-theme-light='true'] .jp-RenderedImage img.jp-needs-light-background {
}

.jp-RenderedHTMLCommon img,
.jp-RenderedImage img,
.jp-RenderedHTMLCommon svg,
.jp-RenderedSVG svg {
  max-width: 100%;
  height: auto;
}

.jp-RenderedHTMLCommon img.jp-mod-unconfined,
.jp-RenderedImage img.jp-mod-unconfined,
.jp-RenderedHTMLCommon svg.jp-mod-unconfined,
.jp-RenderedSVG svg.jp-mod-unconfined {
  max-width: none;
}

.jp-RenderedHTMLCommon .alert {
  padding: var(--jp-notebook-padding);
  border: var(--jp-border-width) solid transparent;
  border-radius: var(--jp-border-radius);
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon .alert-info {
  color: var(--jp-info-color0);
  background-color: var(--jp-info-color3);
  border-color: var(--jp-info-color2);
}
.jp-RenderedHTMLCommon .alert-info hr {
  border-color: var(--jp-info-color3);
}
.jp-RenderedHTMLCommon .alert-info > p:last-child,
.jp-RenderedHTMLCommon .alert-info > ul:last-child {
  margin-bottom: 0;
}

.jp-RenderedHTMLCommon .alert-warning {
  color: var(--jp-warn-color0);
  background-color: var(--jp-warn-color3);
  border-color: var(--jp-warn-color2);
}
.jp-RenderedHTMLCommon .alert-warning hr {
  border-color: var(--jp-warn-color3);
}
.jp-RenderedHTMLCommon .alert-warning > p:last-child,
.jp-RenderedHTMLCommon .alert-warning > ul:last-child {
  margin-bottom: 0;
}

.jp-RenderedHTMLCommon .alert-success {
  color: var(--jp-success-color0);
  background-color: var(--jp-success-color3);
  border-color: var(--jp-success-color2);
}
.jp-RenderedHTMLCommon .alert-success hr {
  border-color: var(--jp-success-color3);
}
.jp-RenderedHTMLCommon .alert-success > p:last-child,
.jp-RenderedHTMLCommon .alert-success > ul:last-child {
  margin-bottom: 0;
}

.jp-RenderedHTMLCommon .alert-danger {
  color: var(--jp-error-color0);
  background-color: var(--jp-error-color3);
  border-color: var(--jp-error-color2);
}
.jp-RenderedHTMLCommon .alert-danger hr {
  border-color: var(--jp-error-color3);
}
.jp-RenderedHTMLCommon .alert-danger > p:last-child,
.jp-RenderedHTMLCommon .alert-danger > ul:last-child {
  margin-bottom: 0;
}

.jp-RenderedHTMLCommon blockquote {
  margin: 1em 2em;
  padding: 0 1em;
  border-left: 5px solid var(--jp-border-color2);
}

a.jp-InternalAnchorLink {
  visibility: hidden;
  margin-left: 8px;
  color: var(--md-blue-800);
}

h1:hover .jp-InternalAnchorLink,
h2:hover .jp-InternalAnchorLink,
h3:hover .jp-InternalAnchorLink,
h4:hover .jp-InternalAnchorLink,
h5:hover .jp-InternalAnchorLink,
h6:hover .jp-InternalAnchorLink {
  visibility: visible;
}

.jp-RenderedHTMLCommon kbd {
  background-color: var(--jp-rendermime-table-row-background);
  border: 1px solid var(--jp-border-color0);
  border-bottom-color: var(--jp-border-color2);
  border-radius: 3px;
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.25);
  display: inline-block;
  font-size: 0.8em;
  line-height: 1em;
  padding: 0.2em 0.5em;
}

/* Most direct children of .jp-RenderedHTMLCommon have a margin-bottom of 1.0.
 * At the bottom of cells this is a bit too much as there is also spacing
 * between cells. Going all the way to 0 gets too tight between markdown and
 * code cells.
 */
.jp-RenderedHTMLCommon > *:last-child {
  margin-bottom: 0.5em;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-MimeDocument {
  outline: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Variables
|----------------------------------------------------------------------------*/

:root {
  --jp-private-filebrowser-button-height: 28px;
  --jp-private-filebrowser-button-width: 48px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-FileBrowser {
  display: flex;
  flex-direction: column;
  color: var(--jp-ui-font-color1);
  background: var(--jp-layout-color1);
  /* This is needed so that all font sizing of children done in ems is
   * relative to this base size */
  font-size: var(--jp-ui-font-size1);
}

.jp-FileBrowser-toolbar.jp-Toolbar {
  border-bottom: none;
  height: auto;
  margin: var(--jp-toolbar-header-margin);
  box-shadow: none;
}

.jp-BreadCrumbs {
  flex: 0 0 auto;
  margin: 8px 12px 8px 12px;
}

.jp-BreadCrumbs-item {
  margin: 0px 2px;
  padding: 0px 2px;
  border-radius: var(--jp-border-radius);
  cursor: pointer;
}

.jp-BreadCrumbs-item:hover {
  background-color: var(--jp-layout-color2);
}

.jp-BreadCrumbs-item:first-child {
  margin-left: 0px;
}

.jp-BreadCrumbs-item.jp-mod-dropTarget {
  background-color: var(--jp-brand-color2);
  opacity: 0.7;
}

/*-----------------------------------------------------------------------------
| Buttons
|----------------------------------------------------------------------------*/

.jp-FileBrowser-toolbar.jp-Toolbar {
  padding: 0px;
  margin: 8px 12px 0px 12px;
}

.jp-FileBrowser-toolbar.jp-Toolbar {
  justify-content: flex-start;
}

.jp-FileBrowser-toolbar.jp-Toolbar .jp-Toolbar-item {
  flex: 0 0 auto;
  padding-left: 0px;
  padding-right: 2px;
}

.jp-FileBrowser-toolbar.jp-Toolbar .jp-ToolbarButtonComponent {
  width: 40px;
}

.jp-FileBrowser-toolbar.jp-Toolbar
  .jp-Toolbar-item:first-child
  .jp-ToolbarButtonComponent {
  width: 72px;
  background: var(--jp-brand-color1);
}

.jp-FileBrowser-toolbar.jp-Toolbar
  .jp-Toolbar-item:first-child
  .jp-ToolbarButtonComponent
  .jp-icon3 {
  fill: white;
}

/*-----------------------------------------------------------------------------
| Other styles
|----------------------------------------------------------------------------*/

.jp-FileDialog.jp-mod-conflict input {
  color: red;
}

.jp-FileDialog .jp-new-name-title {
  margin-top: 12px;
}

.jp-LastModified-hidden {
  display: none;
}

.jp-FileBrowser-filterBox {
  padding: 0px;
  flex: 0 0 auto;
  margin: 8px 12px 0px 12px;
}

/*-----------------------------------------------------------------------------
| DirListing
|----------------------------------------------------------------------------*/

.jp-DirListing {
  flex: 1 1 auto;
  display: flex;
  flex-direction: column;
  outline: 0;
}

.jp-DirListing-header {
  flex: 0 0 auto;
  display: flex;
  flex-direction: row;
  overflow: hidden;
  border-top: var(--jp-border-width) solid var(--jp-border-color2);
  border-bottom: var(--jp-border-width) solid var(--jp-border-color1);
  box-shadow: var(--jp-toolbar-box-shadow);
  z-index: 2;
}

.jp-DirListing-headerItem {
  padding: 4px 12px 2px 12px;
  font-weight: 500;
}

.jp-DirListing-headerItem:hover {
  background: var(--jp-layout-color2);
}

.jp-DirListing-headerItem.jp-id-name {
  flex: 1 0 84px;
}

.jp-DirListing-headerItem.jp-id-modified {
  flex: 0 0 112px;
  border-left: var(--jp-border-width) solid var(--jp-border-color2);
  text-align: right;
}

.jp-id-narrow {
  display: none;
  flex: 0 0 5px;
  padding: 4px 4px;
  border-left: var(--jp-border-width) solid var(--jp-border-color2);
  text-align: right;
  color: var(--jp-border-color2);
}

.jp-DirListing-narrow .jp-id-narrow {
  display: block;
}

.jp-DirListing-narrow .jp-id-modified,
.jp-DirListing-narrow .jp-DirListing-itemModified {
  display: none;
}

.jp-DirListing-headerItem.jp-mod-selected {
  font-weight: 600;
}

/* increase specificity to override bundled default */
.jp-DirListing-content {
  flex: 1 1 auto;
  margin: 0;
  padding: 0;
  list-style-type: none;
  overflow: auto;
  background-color: var(--jp-layout-color1);
}

.jp-DirListing-content mark {
  color: var(--jp-ui-font-color0);
  background-color: transparent;
  font-weight: bold;
}

/* Style the directory listing content when a user drops a file to upload */
.jp-DirListing.jp-mod-native-drop .jp-DirListing-content {
  outline: 5px dashed rgba(128, 128, 128, 0.5);
  outline-offset: -10px;
  cursor: copy;
}

.jp-DirListing-item {
  display: flex;
  flex-direction: row;
  padding: 4px 12px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.jp-DirListing-item[data-is-dot] {
  opacity: 75%;
}

.jp-DirListing-item.jp-mod-selected {
  color: white;
  background: var(--jp-brand-color1);
}

.jp-DirListing-item.jp-mod-dropTarget {
  background: var(--jp-brand-color3);
}

.jp-DirListing-item:hover:not(.jp-mod-selected) {
  background: var(--jp-layout-color2);
}

.jp-DirListing-itemIcon {
  flex: 0 0 20px;
  margin-right: 4px;
}

.jp-DirListing-itemText {
  flex: 1 0 64px;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  user-select: none;
}

.jp-DirListing-itemModified {
  flex: 0 0 125px;
  text-align: right;
}

.jp-DirListing-editor {
  flex: 1 0 64px;
  outline: none;
  border: none;
}

.jp-DirListing-item.jp-mod-running .jp-DirListing-itemIcon:before {
  color: limegreen;
  content: '\25CF';
  font-size: 8px;
  position: absolute;
  left: -8px;
}

.jp-DirListing-item.lm-mod-drag-image,
.jp-DirListing-item.jp-mod-selected.lm-mod-drag-image {
  font-size: var(--jp-ui-font-size1);
  padding-left: 4px;
  margin-left: 4px;
  width: 160px;
  background-color: var(--jp-ui-inverse-font-color2);
  box-shadow: var(--jp-elevation-z2);
  border-radius: 0px;
  color: var(--jp-ui-font-color1);
  transform: translateX(-40%) translateY(-58%);
}

.jp-DirListing-deadSpace {
  flex: 1 1 auto;
  margin: 0;
  padding: 0;
  list-style-type: none;
  overflow: auto;
  background-color: var(--jp-layout-color1);
}

.jp-Document {
  min-width: 120px;
  min-height: 120px;
  outline: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Private CSS variables
|----------------------------------------------------------------------------*/

:root {
}

/*-----------------------------------------------------------------------------
| Main OutputArea
| OutputArea has a list of Outputs
|----------------------------------------------------------------------------*/

.jp-OutputArea {
  overflow-y: auto;
}

.jp-OutputArea-child {
  display: flex;
  flex-direction: row;
}

.jp-OutputPrompt {
  flex: 0 0 var(--jp-cell-prompt-width);
  color: var(--jp-cell-outprompt-font-color);
  font-family: var(--jp-cell-prompt-font-family);
  padding: var(--jp-code-padding);
  letter-spacing: var(--jp-cell-prompt-letter-spacing);
  line-height: var(--jp-code-line-height);
  font-size: var(--jp-code-font-size);
  border: var(--jp-border-width) solid transparent;
  opacity: var(--jp-cell-prompt-opacity);
  /* Right align prompt text, don't wrap to handle large prompt numbers */
  text-align: right;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  /* Disable text selection */
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.jp-OutputArea-output {
  height: auto;
  overflow: auto;
  user-select: text;
  -moz-user-select: text;
  -webkit-user-select: text;
  -ms-user-select: text;
}

.jp-OutputArea-child .jp-OutputArea-output {
  flex-grow: 1;
  flex-shrink: 1;
}

/**
 * Isolated output.
 */
.jp-OutputArea-output.jp-mod-isolated {
  width: 100%;
  display: block;
}

/*
When drag events occur, `p-mod-override-cursor` is added to the body.
Because iframes steal all cursor events, the following two rules are necessary
to suppress pointer events while resize drags are occurring. There may be a
better solution to this problem.
*/
body.lm-mod-override-cursor .jp-OutputArea-output.jp-mod-isolated {
  position: relative;
}

body.lm-mod-override-cursor .jp-OutputArea-output.jp-mod-isolated:before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: transparent;
}

/* pre */

.jp-OutputArea-output pre {
  border: none;
  margin: 0px;
  padding: 0px;
  overflow-x: auto;
  overflow-y: auto;
  word-break: break-all;
  word-wrap: break-word;
  white-space: pre-wrap;
}

/* tables */

.jp-OutputArea-output.jp-RenderedHTMLCommon table {
  margin-left: 0;
  margin-right: 0;
}

/* description lists */

.jp-OutputArea-output dl,
.jp-OutputArea-output dt,
.jp-OutputArea-output dd {
  display: block;
}

.jp-OutputArea-output dl {
  width: 100%;
  overflow: hidden;
  padding: 0;
  margin: 0;
}

.jp-OutputArea-output dt {
  font-weight: bold;
  float: left;
  width: 20%;
  padding: 0;
  margin: 0;
}

.jp-OutputArea-output dd {
  float: left;
  width: 80%;
  padding: 0;
  margin: 0;
}

/* Hide the gutter in case of
 *  - nested output areas (e.g. in the case of output widgets)
 *  - mirrored output areas
 */
.jp-OutputArea .jp-OutputArea .jp-OutputArea-prompt {
  display: none;
}

/*-----------------------------------------------------------------------------
| executeResult is added to any Output-result for the display of the object
| returned by a cell
|----------------------------------------------------------------------------*/

.jp-OutputArea-output.jp-OutputArea-executeResult {
  margin-left: 0px;
  flex: 1 1 auto;
}

/* Text output with the Out[] prompt needs a top padding to match the
 * alignment of the Out[] prompt itself.
 */
.jp-OutputArea-executeResult .jp-RenderedText.jp-OutputArea-output {
  padding-top: var(--jp-code-padding);
  border-top: var(--jp-border-width) solid transparent;
}

/*-----------------------------------------------------------------------------
| The Stdin output
|----------------------------------------------------------------------------*/

.jp-OutputArea-stdin {
  line-height: var(--jp-code-line-height);
  padding-top: var(--jp-code-padding);
  display: flex;
}

.jp-Stdin-prompt {
  color: var(--jp-content-font-color0);
  padding-right: var(--jp-code-padding);
  vertical-align: baseline;
  flex: 0 0 auto;
}

.jp-Stdin-input {
  font-family: var(--jp-code-font-family);
  font-size: inherit;
  color: inherit;
  background-color: inherit;
  width: 42%;
  min-width: 200px;
  /* make sure input baseline aligns with prompt */
  vertical-align: baseline;
  /* padding + margin = 0.5em between prompt and cursor */
  padding: 0em 0.25em;
  margin: 0em 0.25em;
  flex: 0 0 70%;
}

.jp-Stdin-input:focus {
  box-shadow: none;
}

/*-----------------------------------------------------------------------------
| Output Area View
|----------------------------------------------------------------------------*/

.jp-LinkedOutputView .jp-OutputArea {
  height: 100%;
  display: block;
}

.jp-LinkedOutputView .jp-OutputArea-output:only-child {
  height: 100%;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Collapser {
  flex: 0 0 var(--jp-cell-collapser-width);
  padding: 0px;
  margin: 0px;
  border: none;
  outline: none;
  background: transparent;
  border-radius: var(--jp-border-radius);
  opacity: 1;
}

.jp-Collapser-child {
  display: block;
  width: 100%;
  box-sizing: border-box;
  /* height: 100% doesn't work because the height of its parent is computed from content */
  position: absolute;
  top: 0px;
  bottom: 0px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Header/Footer
|----------------------------------------------------------------------------*/

/* Hidden by zero height by default */
.jp-CellHeader,
.jp-CellFooter {
  height: 0px;
  width: 100%;
  padding: 0px;
  margin: 0px;
  border: none;
  outline: none;
  background: transparent;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Input
|----------------------------------------------------------------------------*/

/* All input areas */
.jp-InputArea {
  display: flex;
  flex-direction: row;
  overflow: hidden;
}

.jp-InputArea-editor {
  flex: 1 1 auto;
  overflow: hidden;
}

.jp-InputArea-editor {
  /* This is the non-active, default styling */
  border: var(--jp-border-width) solid var(--jp-cell-editor-border-color);
  border-radius: 0px;
  background: var(--jp-cell-editor-background);
}

.jp-InputPrompt {
  flex: 0 0 var(--jp-cell-prompt-width);
  color: var(--jp-cell-inprompt-font-color);
  font-family: var(--jp-cell-prompt-font-family);
  padding: var(--jp-code-padding);
  letter-spacing: var(--jp-cell-prompt-letter-spacing);
  opacity: var(--jp-cell-prompt-opacity);
  line-height: var(--jp-code-line-height);
  font-size: var(--jp-code-font-size);
  border: var(--jp-border-width) solid transparent;
  opacity: var(--jp-cell-prompt-opacity);
  /* Right align prompt text, don't wrap to handle large prompt numbers */
  text-align: right;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  /* Disable text selection */
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Placeholder
|----------------------------------------------------------------------------*/

.jp-Placeholder {
  display: flex;
  flex-direction: row;
  flex: 1 1 auto;
}

.jp-Placeholder-prompt {
  box-sizing: border-box;
}

.jp-Placeholder-content {
  flex: 1 1 auto;
  border: none;
  background: transparent;
  height: 20px;
  box-sizing: border-box;
}

.jp-Placeholder-content .jp-MoreHorizIcon {
  width: 32px;
  height: 16px;
  border: 1px solid transparent;
  border-radius: var(--jp-border-radius);
}

.jp-Placeholder-content .jp-MoreHorizIcon:hover {
  border: 1px solid var(--jp-border-color1);
  box-shadow: 0px 0px 2px 0px rgba(0, 0, 0, 0.25);
  background-color: var(--jp-layout-color0);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Private CSS variables
|----------------------------------------------------------------------------*/

:root {
  --jp-private-cell-scrolling-output-offset: 5px;
}

/*-----------------------------------------------------------------------------
| Cell
|----------------------------------------------------------------------------*/

.jp-Cell {
  padding: var(--jp-cell-padding);
  margin: 0px;
  border: none;
  outline: none;
  background: transparent;
}

/*-----------------------------------------------------------------------------
| Common input/output
|----------------------------------------------------------------------------*/

.jp-Cell-inputWrapper,
.jp-Cell-outputWrapper {
  display: flex;
  flex-direction: row;
  padding: 0px;
  margin: 0px;
  /* Added to reveal the box-shadow on the input and output collapsers. */
  overflow: visible;
}

/* Only input/output areas inside cells */
.jp-Cell-inputArea,
.jp-Cell-outputArea {
  flex: 1 1 auto;
}

/*-----------------------------------------------------------------------------
| Collapser
|----------------------------------------------------------------------------*/

/* Make the output collapser disappear when there is not output, but do so
 * in a manner that leaves it in the layout and preserves its width.
 */
.jp-Cell.jp-mod-noOutputs .jp-Cell-outputCollapser {
  border: none !important;
  background: transparent !important;
}

.jp-Cell:not(.jp-mod-noOutputs) .jp-Cell-outputCollapser {
  min-height: var(--jp-cell-collapser-min-height);
}

/*-----------------------------------------------------------------------------
| Output
|----------------------------------------------------------------------------*/

/* Put a space between input and output when there IS output */
.jp-Cell:not(.jp-mod-noOutputs) .jp-Cell-outputWrapper {
  margin-top: 5px;
}

.jp-CodeCell.jp-mod-outputsScrolled .jp-Cell-outputArea {
  overflow-y: auto;
  max-height: 200px;
  box-shadow: inset 0 0 6px 2px rgba(0, 0, 0, 0.3);
  margin-left: var(--jp-private-cell-scrolling-output-offset);
}

.jp-CodeCell.jp-mod-outputsScrolled .jp-OutputArea-prompt {
  flex: 0 0
    calc(
      var(--jp-cell-prompt-width) -
        var(--jp-private-cell-scrolling-output-offset)
    );
}

/*-----------------------------------------------------------------------------
| CodeCell
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| MarkdownCell
|----------------------------------------------------------------------------*/

.jp-MarkdownOutput {
  flex: 1 1 auto;
  margin-top: 0;
  margin-bottom: 0;
  padding-left: var(--jp-code-padding);
}

.jp-MarkdownOutput.jp-RenderedHTMLCommon {
  overflow: auto;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Variables
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------

/*-----------------------------------------------------------------------------
| Styles
|----------------------------------------------------------------------------*/

.jp-NotebookPanel-toolbar {
  padding: 2px;
}

.jp-Toolbar-item.jp-Notebook-toolbarCellType .jp-select-wrapper.jp-mod-focused {
  border: none;
  box-shadow: none;
}

.jp-Notebook-toolbarCellTypeDropdown select {
  height: 24px;
  font-size: var(--jp-ui-font-size1);
  line-height: 14px;
  border-radius: 0;
  display: block;
}

.jp-Notebook-toolbarCellTypeDropdown span {
  top: 5px !important;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Private CSS variables
|----------------------------------------------------------------------------*/

:root {
  --jp-private-notebook-dragImage-width: 304px;
  --jp-private-notebook-dragImage-height: 36px;
  --jp-private-notebook-selected-color: var(--md-blue-400);
  --jp-private-notebook-active-color: var(--md-green-400);
}

/*-----------------------------------------------------------------------------
| Imports
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Notebook
|----------------------------------------------------------------------------*/

.jp-NotebookPanel {
  display: block;
  height: 100%;
}

.jp-NotebookPanel.jp-Document {
  min-width: 240px;
  min-height: 120px;
}

.jp-Notebook {
  padding: var(--jp-notebook-padding);
  outline: none;
  overflow: auto;
  background: var(--jp-layout-color0);
}

.jp-Notebook.jp-mod-scrollPastEnd::after {
  display: block;
  content: '';
  min-height: var(--jp-notebook-scroll-padding);
}

.jp-Notebook .jp-Cell {
  overflow: visible;
}

.jp-Notebook .jp-Cell .jp-InputPrompt {
  cursor: move;
}

/*-----------------------------------------------------------------------------
| Notebook state related styling
|
| The notebook and cells each have states, here are the possibilities:
|
| - Notebook
|   - Command
|   - Edit
| - Cell
|   - None
|   - Active (only one can be active)
|   - Selected (the cells actions are applied to)
|   - Multiselected (when multiple selected, the cursor)
|   - No outputs
|----------------------------------------------------------------------------*/

/* Command or edit modes */

.jp-Notebook .jp-Cell:not(.jp-mod-active) .jp-InputPrompt {
  opacity: var(--jp-cell-prompt-not-active-opacity);
  color: var(--jp-cell-prompt-not-active-font-color);
}

.jp-Notebook .jp-Cell:not(.jp-mod-active) .jp-OutputPrompt {
  opacity: var(--jp-cell-prompt-not-active-opacity);
  color: var(--jp-cell-prompt-not-active-font-color);
}

/* cell is active */
.jp-Notebook .jp-Cell.jp-mod-active .jp-Collapser {
  background: var(--jp-brand-color1);
}

/* collapser is hovered */
.jp-Notebook .jp-Cell .jp-Collapser:hover {
  box-shadow: var(--jp-elevation-z2);
  background: var(--jp-brand-color1);
  opacity: var(--jp-cell-collapser-not-active-hover-opacity);
}

/* cell is active and collapser is hovered */
.jp-Notebook .jp-Cell.jp-mod-active .jp-Collapser:hover {
  background: var(--jp-brand-color0);
  opacity: 1;
}

/* Command mode */

.jp-Notebook.jp-mod-commandMode .jp-Cell.jp-mod-selected {
  background: var(--jp-notebook-multiselected-color);
}

.jp-Notebook.jp-mod-commandMode
  .jp-Cell.jp-mod-active.jp-mod-selected:not(.jp-mod-multiSelected) {
  background: transparent;
}

/* Edit mode */

.jp-Notebook.jp-mod-editMode .jp-Cell.jp-mod-active .jp-InputArea-editor {
  border: var(--jp-border-width) solid var(--jp-cell-editor-active-border-color);
  box-shadow: var(--jp-input-box-shadow);
  background-color: var(--jp-cell-editor-active-background);
}

/*-----------------------------------------------------------------------------
| Notebook drag and drop
|----------------------------------------------------------------------------*/

.jp-Notebook-cell.jp-mod-dropSource {
  opacity: 0.5;
}

.jp-Notebook-cell.jp-mod-dropTarget,
.jp-Notebook.jp-mod-commandMode
  .jp-Notebook-cell.jp-mod-active.jp-mod-selected.jp-mod-dropTarget {
  border-top-color: var(--jp-private-notebook-selected-color);
  border-top-style: solid;
  border-top-width: 2px;
}

.jp-dragImage {
  display: flex;
  flex-direction: row;
  width: var(--jp-private-notebook-dragImage-width);
  height: var(--jp-private-notebook-dragImage-height);
  border: var(--jp-border-width) solid var(--jp-cell-editor-border-color);
  background: var(--jp-cell-editor-background);
  overflow: visible;
}

.jp-dragImage-singlePrompt {
  box-shadow: 2px 2px 4px 0px rgba(0, 0, 0, 0.12);
}

.jp-dragImage .jp-dragImage-content {
  flex: 1 1 auto;
  z-index: 2;
  font-size: var(--jp-code-font-size);
  font-family: var(--jp-code-font-family);
  line-height: var(--jp-code-line-height);
  padding: var(--jp-code-padding);
  border: var(--jp-border-width) solid var(--jp-cell-editor-border-color);
  background: var(--jp-cell-editor-background-color);
  color: var(--jp-content-font-color3);
  text-align: left;
  margin: 4px 4px 4px 0px;
}

.jp-dragImage .jp-dragImage-prompt {
  flex: 0 0 auto;
  min-width: 36px;
  color: var(--jp-cell-inprompt-font-color);
  padding: var(--jp-code-padding);
  padding-left: 12px;
  font-family: var(--jp-cell-prompt-font-family);
  letter-spacing: var(--jp-cell-prompt-letter-spacing);
  line-height: 1.9;
  font-size: var(--jp-code-font-size);
  border: var(--jp-border-width) solid transparent;
}

.jp-dragImage-multipleBack {
  z-index: -1;
  position: absolute;
  height: 32px;
  width: 300px;
  top: 8px;
  left: 8px;
  background: var(--jp-layout-color2);
  border: var(--jp-border-width) solid var(--jp-input-border-color);
  box-shadow: 2px 2px 4px 0px rgba(0, 0, 0, 0.12);
}

/*-----------------------------------------------------------------------------
| Cell toolbar
|----------------------------------------------------------------------------*/

.jp-NotebookTools {
  display: block;
  min-width: var(--jp-sidebar-min-width);
  color: var(--jp-ui-font-color1);
  background: var(--jp-layout-color1);
  /* This is needed so that all font sizing of children done in ems is
    * relative to this base size */
  font-size: var(--jp-ui-font-size1);
  overflow: auto;
}

.jp-NotebookTools-tool {
  padding: 0px 12px 0 12px;
}

.jp-ActiveCellTool {
  padding: 12px;
  background-color: var(--jp-layout-color1);
  border-top: none !important;
}

.jp-ActiveCellTool .jp-InputArea-prompt {
  flex: 0 0 auto;
  padding-left: 0px;
}

.jp-ActiveCellTool .jp-InputArea-editor {
  flex: 1 1 auto;
  background: var(--jp-cell-editor-background);
  border-color: var(--jp-cell-editor-border-color);
}

.jp-ActiveCellTool .jp-InputArea-editor .CodeMirror {
  background: transparent;
}

.jp-MetadataEditorTool {
  flex-direction: column;
  padding: 12px 0px 12px 0px;
}

.jp-RankedPanel > :not(:first-child) {
  margin-top: 12px;
}

.jp-KeySelector select.jp-mod-styled {
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color0);
  border: var(--jp-border-width) solid var(--jp-border-color1);
}

.jp-KeySelector label,
.jp-MetadataEditorTool label {
  line-height: 1.4;
}

.jp-NotebookTools .jp-select-wrapper {
  margin-top: 4px;
  margin-bottom: 0px;
}

.jp-NotebookTools .jp-Collapse {
  margin-top: 16px;
}

/*-----------------------------------------------------------------------------
| Presentation Mode (.jp-mod-presentationMode)
|----------------------------------------------------------------------------*/

.jp-mod-presentationMode .jp-Notebook {
  --jp-content-font-size1: var(--jp-content-presentation-font-size1);
  --jp-code-font-size: var(--jp-code-presentation-font-size);
}

.jp-mod-presentationMode .jp-Notebook .jp-Cell .jp-InputPrompt,
.jp-mod-presentationMode .jp-Notebook .jp-Cell .jp-OutputPrompt {
  flex: 0 0 110px;
}

</style>

    <style type="text/css">
/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*
The following CSS variables define the main, public API for styling JupyterLab.
These variables should be used by all plugins wherever possible. In other
words, plugins should not define custom colors, sizes, etc unless absolutely
necessary. This enables users to change the visual theme of JupyterLab
by changing these variables.

Many variables appear in an ordered sequence (0,1,2,3). These sequences
are designed to work well together, so for example, `--jp-border-color1` should
be used with `--jp-layout-color1`. The numbers have the following meanings:

* 0: super-primary, reserved for special emphasis
* 1: primary, most important under normal situations
* 2: secondary, next most important under normal situations
* 3: tertiary, next most important under normal situations

Throughout JupyterLab, we are mostly following principles from Google's
Material Design when selecting colors. We are not, however, following
all of MD as it is not optimized for dense, information rich UIs.
*/

:root {
  /* Elevation
   *
   * We style box-shadows using Material Design's idea of elevation. These particular numbers are taken from here:
   *
   * https://github.com/material-components/material-components-web
   * https://material-components-web.appspot.com/elevation.html
   */

  --jp-shadow-base-lightness: 0;
  --jp-shadow-umbra-color: rgba(
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    0.2
  );
  --jp-shadow-penumbra-color: rgba(
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    0.14
  );
  --jp-shadow-ambient-color: rgba(
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    0.12
  );
  --jp-elevation-z0: none;
  --jp-elevation-z1: 0px 2px 1px -1px var(--jp-shadow-umbra-color),
    0px 1px 1px 0px var(--jp-shadow-penumbra-color),
    0px 1px 3px 0px var(--jp-shadow-ambient-color);
  --jp-elevation-z2: 0px 3px 1px -2px var(--jp-shadow-umbra-color),
    0px 2px 2px 0px var(--jp-shadow-penumbra-color),
    0px 1px 5px 0px var(--jp-shadow-ambient-color);
  --jp-elevation-z4: 0px 2px 4px -1px var(--jp-shadow-umbra-color),
    0px 4px 5px 0px var(--jp-shadow-penumbra-color),
    0px 1px 10px 0px var(--jp-shadow-ambient-color);
  --jp-elevation-z6: 0px 3px 5px -1px var(--jp-shadow-umbra-color),
    0px 6px 10px 0px var(--jp-shadow-penumbra-color),
    0px 1px 18px 0px var(--jp-shadow-ambient-color);
  --jp-elevation-z8: 0px 5px 5px -3px var(--jp-shadow-umbra-color),
    0px 8px 10px 1px var(--jp-shadow-penumbra-color),
    0px 3px 14px 2px var(--jp-shadow-ambient-color);
  --jp-elevation-z12: 0px 7px 8px -4px var(--jp-shadow-umbra-color),
    0px 12px 17px 2px var(--jp-shadow-penumbra-color),
    0px 5px 22px 4px var(--jp-shadow-ambient-color);
  --jp-elevation-z16: 0px 8px 10px -5px var(--jp-shadow-umbra-color),
    0px 16px 24px 2px var(--jp-shadow-penumbra-color),
    0px 6px 30px 5px var(--jp-shadow-ambient-color);
  --jp-elevation-z20: 0px 10px 13px -6px var(--jp-shadow-umbra-color),
    0px 20px 31px 3px var(--jp-shadow-penumbra-color),
    0px 8px 38px 7px var(--jp-shadow-ambient-color);
  --jp-elevation-z24: 0px 11px 15px -7px var(--jp-shadow-umbra-color),
    0px 24px 38px 3px var(--jp-shadow-penumbra-color),
    0px 9px 46px 8px var(--jp-shadow-ambient-color);

  /* Borders
   *
   * The following variables, specify the visual styling of borders in JupyterLab.
   */

  --jp-border-width: 1px;
  --jp-border-color0: var(--md-grey-400);
  --jp-border-color1: var(--md-grey-400);
  --jp-border-color2: var(--md-grey-300);
  --jp-border-color3: var(--md-grey-200);
  --jp-border-radius: 2px;

  /* UI Fonts
   *
   * The UI font CSS variables are used for the typography all of the JupyterLab
   * user interface elements that are not directly user generated content.
   *
   * The font sizing here is done assuming that the body font size of --jp-ui-font-size1
   * is applied to a parent element. When children elements, such as headings, are sized
   * in em all things will be computed relative to that body size.
   */

  --jp-ui-font-scale-factor: 1.2;
  --jp-ui-font-size0: 0.83333em;
  --jp-ui-font-size1: 13px; /* Base font size */
  --jp-ui-font-size2: 1.2em;
  --jp-ui-font-size3: 1.44em;

  --jp-ui-font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica,
    Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol';

  /*
   * Use these font colors against the corresponding main layout colors.
   * In a light theme, these go from dark to light.
   */

  /* Defaults use Material Design specification */
  --jp-ui-font-color0: rgba(0, 0, 0, 1);
  --jp-ui-font-color1: rgba(0, 0, 0, 0.87);
  --jp-ui-font-color2: rgba(0, 0, 0, 0.54);
  --jp-ui-font-color3: rgba(0, 0, 0, 0.38);

  /*
   * Use these against the brand/accent/warn/error colors.
   * These will typically go from light to darker, in both a dark and light theme.
   */

  --jp-ui-inverse-font-color0: rgba(255, 255, 255, 1);
  --jp-ui-inverse-font-color1: rgba(255, 255, 255, 1);
  --jp-ui-inverse-font-color2: rgba(255, 255, 255, 0.7);
  --jp-ui-inverse-font-color3: rgba(255, 255, 255, 0.5);

  /* Content Fonts
   *
   * Content font variables are used for typography of user generated content.
   *
   * The font sizing here is done assuming that the body font size of --jp-content-font-size1
   * is applied to a parent element. When children elements, such as headings, are sized
   * in em all things will be computed relative to that body size.
   */

  --jp-content-line-height: 1.6;
  --jp-content-font-scale-factor: 1.2;
  --jp-content-font-size0: 0.83333em;
  --jp-content-font-size1: 14px; /* Base font size */
  --jp-content-font-size2: 1.2em;
  --jp-content-font-size3: 1.44em;
  --jp-content-font-size4: 1.728em;
  --jp-content-font-size5: 2.0736em;

  /* This gives a magnification of about 125% in presentation mode over normal. */
  --jp-content-presentation-font-size1: 17px;

  --jp-content-heading-line-height: 1;
  --jp-content-heading-margin-top: 1.2em;
  --jp-content-heading-margin-bottom: 0.8em;
  --jp-content-heading-font-weight: 500;

  /* Defaults use Material Design specification */
  --jp-content-font-color0: rgba(0, 0, 0, 1);
  --jp-content-font-color1: rgba(0, 0, 0, 0.87);
  --jp-content-font-color2: rgba(0, 0, 0, 0.54);
  --jp-content-font-color3: rgba(0, 0, 0, 0.38);

  --jp-content-link-color: var(--md-blue-700);

  --jp-content-font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji',
    'Segoe UI Symbol';

  /*
   * Code Fonts
   *
   * Code font variables are used for typography of code and other monospaces content.
   */

  --jp-code-font-size: 13px;
  --jp-code-line-height: 1.3077; /* 17px for 13px base */
  --jp-code-padding: 5px; /* 5px for 13px base, codemirror highlighting needs integer px value */
  --jp-code-font-family-default: Menlo, Consolas, 'DejaVu Sans Mono', monospace;
  --jp-code-font-family: var(--jp-code-font-family-default);

  /* This gives a magnification of about 125% in presentation mode over normal. */
  --jp-code-presentation-font-size: 16px;

  /* may need to tweak cursor width if you change font size */
  --jp-code-cursor-width0: 1.4px;
  --jp-code-cursor-width1: 2px;
  --jp-code-cursor-width2: 4px;

  /* Layout
   *
   * The following are the main layout colors use in JupyterLab. In a light
   * theme these would go from light to dark.
   */

  --jp-layout-color0: white;
  --jp-layout-color1: white;
  --jp-layout-color2: var(--md-grey-200);
  --jp-layout-color3: var(--md-grey-400);
  --jp-layout-color4: var(--md-grey-600);

  /* Inverse Layout
   *
   * The following are the inverse layout colors use in JupyterLab. In a light
   * theme these would go from dark to light.
   */

  --jp-inverse-layout-color0: #111111;
  --jp-inverse-layout-color1: var(--md-grey-900);
  --jp-inverse-layout-color2: var(--md-grey-800);
  --jp-inverse-layout-color3: var(--md-grey-700);
  --jp-inverse-layout-color4: var(--md-grey-600);

  /* Brand/accent */

  --jp-brand-color0: var(--md-blue-700);
  --jp-brand-color1: var(--md-blue-500);
  --jp-brand-color2: var(--md-blue-300);
  --jp-brand-color3: var(--md-blue-100);
  --jp-brand-color4: var(--md-blue-50);

  --jp-accent-color0: var(--md-green-700);
  --jp-accent-color1: var(--md-green-500);
  --jp-accent-color2: var(--md-green-300);
  --jp-accent-color3: var(--md-green-100);

  /* State colors (warn, error, success, info) */

  --jp-warn-color0: var(--md-orange-700);
  --jp-warn-color1: var(--md-orange-500);
  --jp-warn-color2: var(--md-orange-300);
  --jp-warn-color3: var(--md-orange-100);

  --jp-error-color0: var(--md-red-700);
  --jp-error-color1: var(--md-red-500);
  --jp-error-color2: var(--md-red-300);
  --jp-error-color3: var(--md-red-100);

  --jp-success-color0: var(--md-green-700);
  --jp-success-color1: var(--md-green-500);
  --jp-success-color2: var(--md-green-300);
  --jp-success-color3: var(--md-green-100);

  --jp-info-color0: var(--md-cyan-700);
  --jp-info-color1: var(--md-cyan-500);
  --jp-info-color2: var(--md-cyan-300);
  --jp-info-color3: var(--md-cyan-100);

  /* Cell specific styles */

  --jp-cell-padding: 5px;

  --jp-cell-collapser-width: 8px;
  --jp-cell-collapser-min-height: 20px;
  --jp-cell-collapser-not-active-hover-opacity: 0.6;

  --jp-cell-editor-background: var(--md-grey-100);
  --jp-cell-editor-border-color: var(--md-grey-300);
  --jp-cell-editor-box-shadow: inset 0 0 2px var(--md-blue-300);
  --jp-cell-editor-active-background: var(--jp-layout-color0);
  --jp-cell-editor-active-border-color: var(--jp-brand-color1);

  --jp-cell-prompt-width: 64px;
  --jp-cell-prompt-font-family: var(--jp-code-font-family-default);
  --jp-cell-prompt-letter-spacing: 0px;
  --jp-cell-prompt-opacity: 1;
  --jp-cell-prompt-not-active-opacity: 0.5;
  --jp-cell-prompt-not-active-font-color: var(--md-grey-700);
  /* A custom blend of MD grey and blue 600
   * See https://meyerweb.com/eric/tools/color-blend/#546E7A:1E88E5:5:hex */
  --jp-cell-inprompt-font-color: #307fc1;
  /* A custom blend of MD grey and orange 600
   * https://meyerweb.com/eric/tools/color-blend/#546E7A:F4511E:5:hex */
  --jp-cell-outprompt-font-color: #bf5b3d;

  /* Notebook specific styles */

  --jp-notebook-padding: 10px;
  --jp-notebook-select-background: var(--jp-layout-color1);
  --jp-notebook-multiselected-color: var(--md-blue-50);

  /* The scroll padding is calculated to fill enough space at the bottom of the
  notebook to show one single-line cell (with appropriate padding) at the top
  when the notebook is scrolled all the way to the bottom. We also subtract one
  pixel so that no scrollbar appears if we have just one single-line cell in the
  notebook. This padding is to enable a 'scroll past end' feature in a notebook.
  */
  --jp-notebook-scroll-padding: calc(
    100% - var(--jp-code-font-size) * var(--jp-code-line-height) -
      var(--jp-code-padding) - var(--jp-cell-padding) - 1px
  );

  /* Rendermime styles */

  --jp-rendermime-error-background: #fdd;
  --jp-rendermime-table-row-background: var(--md-grey-100);
  --jp-rendermime-table-row-hover-background: var(--md-light-blue-50);

  /* Dialog specific styles */

  --jp-dialog-background: rgba(0, 0, 0, 0.25);

  /* Console specific styles */

  --jp-console-padding: 10px;

  /* Toolbar specific styles */

  --jp-toolbar-border-color: var(--jp-border-color1);
  --jp-toolbar-micro-height: 8px;
  --jp-toolbar-background: var(--jp-layout-color1);
  --jp-toolbar-box-shadow: 0px 0px 2px 0px rgba(0, 0, 0, 0.24);
  --jp-toolbar-header-margin: 4px 4px 0px 4px;
  --jp-toolbar-active-background: var(--md-grey-300);

  /* Input field styles */

  --jp-input-box-shadow: inset 0 0 2px var(--md-blue-300);
  --jp-input-active-background: var(--jp-layout-color1);
  --jp-input-hover-background: var(--jp-layout-color1);
  --jp-input-background: var(--md-grey-100);
  --jp-input-border-color: var(--jp-border-color1);
  --jp-input-active-border-color: var(--jp-brand-color1);
  --jp-input-active-box-shadow-color: rgba(19, 124, 189, 0.3);

  /* General editor styles */

  --jp-editor-selected-background: #d9d9d9;
  --jp-editor-selected-focused-background: #d7d4f0;
  --jp-editor-cursor-color: var(--jp-ui-font-color0);

  /* Code mirror specific styles */

  --jp-mirror-editor-keyword-color: #008000;
  --jp-mirror-editor-atom-color: #88f;
  --jp-mirror-editor-number-color: #080;
  --jp-mirror-editor-def-color: #00f;
  --jp-mirror-editor-variable-color: var(--md-grey-900);
  --jp-mirror-editor-variable-2-color: #05a;
  --jp-mirror-editor-variable-3-color: #085;
  --jp-mirror-editor-punctuation-color: #05a;
  --jp-mirror-editor-property-color: #05a;
  --jp-mirror-editor-operator-color: #aa22ff;
  --jp-mirror-editor-comment-color: #408080;
  --jp-mirror-editor-string-color: #ba2121;
  --jp-mirror-editor-string-2-color: #708;
  --jp-mirror-editor-meta-color: #aa22ff;
  --jp-mirror-editor-qualifier-color: #555;
  --jp-mirror-editor-builtin-color: #008000;
  --jp-mirror-editor-bracket-color: #997;
  --jp-mirror-editor-tag-color: #170;
  --jp-mirror-editor-attribute-color: #00c;
  --jp-mirror-editor-header-color: blue;
  --jp-mirror-editor-quote-color: #090;
  --jp-mirror-editor-link-color: #00c;
  --jp-mirror-editor-error-color: #f00;
  --jp-mirror-editor-hr-color: #999;

  /* Vega extension styles */

  --jp-vega-background: white;

  /* Sidebar-related styles */

  --jp-sidebar-min-width: 250px;

  /* Search-related styles */

  --jp-search-toggle-off-opacity: 0.5;
  --jp-search-toggle-hover-opacity: 0.8;
  --jp-search-toggle-on-opacity: 1;
  --jp-search-selected-match-background-color: rgb(245, 200, 0);
  --jp-search-selected-match-color: black;
  --jp-search-unselected-match-background-color: var(
    --jp-inverse-layout-color0
  );
  --jp-search-unselected-match-color: var(--jp-ui-inverse-font-color0);

  /* Icon colors that work well with light or dark backgrounds */
  --jp-icon-contrast-color0: var(--md-purple-600);
  --jp-icon-contrast-color1: var(--md-green-600);
  --jp-icon-contrast-color2: var(--md-pink-600);
  --jp-icon-contrast-color3: var(--md-blue-600);
}
</style>

<style type="text/css">
a.anchor-link {
   display: none;
}
.highlight  {
    margin: 0.4em;
}

/* Input area styling */
.jp-InputArea {
    overflow: hidden;
}

.jp-InputArea-editor {
    overflow: hidden;
}

@media print {
  body {
    margin: 0;
  }
}
</style>

<!-- Load mathjax -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.7/latest.js?config=TeX-MML-AM_CHTML-full,Safe"> </script>
    <!-- MathJax configuration -->
    <script type="text/x-mathjax-config">
    init_mathjax = function() {
        if (window.MathJax) {
        // MathJax loaded
            MathJax.Hub.Config({
                TeX: {
                    equationNumbers: {
                    autoNumber: "AMS",
                    useLabelIds: true
                    }
                },
                tex2jax: {
                    inlineMath: [ ['$','$'], ["\\(","\\)"] ],
                    displayMath: [ ['$$','$$'], ["\\[","\\]"] ],
                    processEscapes: true,
                    processEnvironments: true
                },
                displayAlign: 'center',
                CommonHTML: {
                    linebreaks: { 
                    automatic: true 
                    }
                },
                "HTML-CSS": {
                    linebreaks: { 
                    automatic: true 
                    }
                }
            });
        
            MathJax.Hub.Queue(["Typeset", MathJax.Hub]);
        }
    }
    init_mathjax();
    </script>
    <!-- End of mathjax configuration --></head>
<body class="jp-Notebook" data-jp-theme-light="true" data-jp-theme-name="JupyterLab Light">
<div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs  ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[15]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="kn">from</span> <span class="nn">scipy.signal</span> <span class="kn">import</span> <span class="n">savgol_filter</span>
<span class="kn">import</span> <span class="nn">csv</span>
<span class="kn">from</span> <span class="nn">sklearn.decomposition</span> <span class="kn">import</span> <span class="n">PCA</span>
<span class="kn">from</span> <span class="nn">math</span> <span class="kn">import</span> <span class="n">sqrt</span>
<span class="kn">from</span> <span class="nn">sklearn</span> <span class="kn">import</span> <span class="n">metrics</span>
<span class="kn">from</span> <span class="nn">sklearn.model_selection</span> <span class="kn">import</span> <span class="n">train_test_split</span>
<span class="kn">from</span> <span class="nn">sklearn</span> <span class="kn">import</span> <span class="n">svm</span>
<span class="kn">import</span> <span class="nn">seaborn</span> <span class="k">as</span> <span class="nn">sns</span>
<span class="kn">from</span> <span class="nn">matplotlib.colors</span> <span class="kn">import</span> <span class="n">ListedColormap</span>
<span class="kn">import</span> <span class="nn">warnings</span>
<span class="n">warnings</span><span class="o">.</span><span class="n">filterwarnings</span><span class="p">(</span><span class="s2">&quot;ignore&quot;</span><span class="p">,</span> <span class="n">category</span><span class="o">=</span><span class="ne">DeprecationWarning</span><span class="p">)</span> 
</pre></div>

     </div>
</div>
</div>
</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs  ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[12]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Performs Standard Normal Variate on Spectra</span>
<span class="k">def</span> <span class="nf">snv</span><span class="p">(</span><span class="n">y</span><span class="p">):</span>
    <span class="n">average</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">mean</span><span class="p">(</span><span class="n">y</span><span class="p">)</span>
    <span class="n">standardDev</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">std</span><span class="p">(</span><span class="n">y</span><span class="p">)</span>
    <span class="k">for</span> <span class="n">count</span><span class="p">,</span> <span class="n">element</span> <span class="ow">in</span> <span class="nb">enumerate</span><span class="p">(</span><span class="n">y</span><span class="p">):</span>
        <span class="n">y</span><span class="p">[</span><span class="n">count</span><span class="p">]</span> <span class="o">=</span> <span class="p">(</span><span class="n">element</span> <span class="o">-</span> <span class="n">average</span><span class="p">)</span> <span class="o">/</span> <span class="n">standardDev</span>

    <span class="k">return</span> <span class="n">y</span>
</pre></div>

     </div>
</div>
</div>
</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs  ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[13]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># encodes text array containing unique categorical labels into numeric labels</span>

<span class="k">def</span> <span class="nf">encode</span><span class="p">(</span><span class="n">x</span><span class="p">):</span>
    <span class="n">uniqueClasses</span> <span class="o">=</span> <span class="nb">set</span><span class="p">(</span><span class="n">x</span><span class="p">)</span>

    <span class="n">encodedArray</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">array</span><span class="p">(</span><span class="n">x</span><span class="p">)</span>
    <span class="k">for</span> <span class="n">count</span><span class="p">,</span> <span class="n">word</span> <span class="ow">in</span> <span class="nb">enumerate</span><span class="p">(</span><span class="n">uniqueClasses</span><span class="p">):</span>
        <span class="n">indices</span> <span class="o">=</span> <span class="p">[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span><span class="p">,</span> <span class="n">y</span> <span class="ow">in</span> <span class="nb">enumerate</span><span class="p">(</span><span class="n">x</span><span class="p">)</span> <span class="k">if</span> <span class="n">y</span> <span class="o">==</span> <span class="n">word</span><span class="p">]</span>
        <span class="n">encodedArray</span><span class="p">[</span><span class="n">indices</span><span class="p">]</span> <span class="o">=</span> <span class="n">count</span>
    
    <span class="k">return</span> <span class="n">encodedArray</span>
</pre></div>

     </div>
</div>
</div>
</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs  ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[16]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">vector</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">vectorize</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">float</span><span class="p">)</span>
<span class="n">trainSetFile</span> <span class="o">=</span> <span class="sa">r</span><span class="s2">&quot;covid_and_healthy_spectra.csv&quot;</span>
<span class="n">labels</span> <span class="o">=</span> <span class="sa">r</span><span class="s2">&quot;covid_and_healthy_spectra.csv&quot;</span>
</pre></div>

     </div>
</div>
</div>
</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs  ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[18]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">with</span> <span class="nb">open</span><span class="p">(</span><span class="n">labels</span><span class="p">,</span> <span class="n">newline</span><span class="o">=</span><span class="s1">&#39;&#39;</span><span class="p">)</span> <span class="k">as</span> <span class="n">labelcsvfile</span><span class="p">:</span>
    <span class="n">labelcsvfile</span> <span class="o">=</span> <span class="n">csv</span><span class="o">.</span><span class="n">reader</span><span class="p">(</span><span class="n">labelcsvfile</span><span class="p">,</span> <span class="n">delimiter</span><span class="o">=</span><span class="s1">&#39;,&#39;</span><span class="p">,</span> <span class="n">quotechar</span><span class="o">=</span><span class="s1">&#39;|&#39;</span><span class="p">)</span>
    <span class="n">labelHeader</span> <span class="o">=</span> <span class="nb">next</span><span class="p">(</span><span class="n">labelcsvfile</span><span class="p">)</span>
    <span class="n">classData</span> <span class="o">=</span> <span class="p">[</span><span class="mi">0</span><span class="p">]</span>
    <span class="k">for</span> <span class="n">row</span> <span class="ow">in</span> <span class="n">labelcsvfile</span><span class="p">:</span>
        <span class="n">classData</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">row</span><span class="p">[</span><span class="o">-</span><span class="mi">1</span><span class="p">])</span>
<span class="n">classData</span><span class="o">.</span><span class="n">pop</span><span class="p">(</span><span class="mi">0</span><span class="p">)</span>
<span class="n">encodeClassdata</span> <span class="o">=</span> <span class="n">encode</span><span class="p">(</span><span class="n">classData</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[19]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">with</span> <span class="nb">open</span><span class="p">(</span><span class="n">trainSetFile</span><span class="p">,</span> <span class="n">newline</span><span class="o">=</span><span class="s1">&#39;&#39;</span><span class="p">)</span> <span class="k">as</span> <span class="n">csvfile</span><span class="p">:</span>
    <span class="n">csvfile</span> <span class="o">=</span> <span class="n">csv</span><span class="o">.</span><span class="n">reader</span><span class="p">(</span><span class="n">csvfile</span><span class="p">,</span> <span class="n">delimiter</span><span class="o">=</span><span class="s1">&#39;,&#39;</span><span class="p">,</span> <span class="n">quotechar</span><span class="o">=</span><span class="s1">&#39;|&#39;</span><span class="p">)</span>
    <span class="n">header</span> <span class="o">=</span> <span class="nb">next</span><span class="p">(</span><span class="n">csvfile</span><span class="p">)</span>
    <span class="k">for</span> <span class="n">count</span><span class="p">,</span> <span class="n">element</span> <span class="ow">in</span> <span class="nb">enumerate</span><span class="p">(</span><span class="n">header</span><span class="p">[</span><span class="mi">1</span><span class="p">:]):</span>
        <span class="n">header</span><span class="p">[</span><span class="n">count</span><span class="p">]</span> <span class="o">=</span> <span class="n">header</span><span class="p">[</span><span class="n">count</span><span class="p">]</span><span class="o">.</span><span class="n">split</span><span class="p">(</span><span class="s2">&quot;cm-1&quot;</span><span class="p">)[</span><span class="mi">0</span><span class="p">]</span>

    <span class="n">xvals</span> <span class="o">=</span> <span class="n">vector</span><span class="p">(</span><span class="n">header</span><span class="p">[</span><span class="mi">1</span><span class="p">:</span><span class="o">-</span><span class="mi">1</span><span class="p">])</span>
    <span class="n">idx1</span> <span class="o">=</span> <span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">abs</span><span class="p">(</span><span class="n">xvals</span> <span class="o">-</span> <span class="mi">400</span><span class="p">))</span><span class="o">.</span><span class="n">argmin</span><span class="p">()</span>
    <span class="n">idx2</span> <span class="o">=</span> <span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">abs</span><span class="p">(</span><span class="n">xvals</span> <span class="o">-</span> <span class="mi">1750</span><span class="p">))</span><span class="o">.</span><span class="n">argmin</span><span class="p">()</span>
    <span class="n">xvals</span> <span class="o">=</span> <span class="n">xvals</span><span class="p">[</span><span class="n">idx1</span><span class="p">:</span><span class="n">idx2</span><span class="p">]</span>
    <span class="n">dataMatrix</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">zeros</span><span class="p">(</span><span class="nb">len</span><span class="p">(</span><span class="n">xvals</span><span class="p">))</span>
    <span class="n">plot1</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>


    <span class="k">for</span> <span class="n">count</span><span class="p">,</span> <span class="n">row</span> <span class="ow">in</span> <span class="nb">enumerate</span><span class="p">(</span><span class="n">csvfile</span><span class="p">):</span>
        <span class="n">spectrum</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">asarray</span><span class="p">(</span><span class="n">row</span><span class="p">[</span><span class="n">idx1</span><span class="p">:</span><span class="n">idx2</span><span class="p">])</span>
        <span class="n">spectrum</span> <span class="o">=</span> <span class="n">vector</span><span class="p">(</span><span class="n">spectrum</span><span class="p">)</span>
        <span class="c1"># Savitzky-golay smoothing, 15 point</span>
        <span class="n">spectrum</span> <span class="o">=</span> <span class="n">savgol_filter</span><span class="p">(</span><span class="n">spectrum</span><span class="p">,</span> <span class="mi">15</span><span class="p">,</span> <span class="mi">3</span><span class="p">,</span> <span class="n">deriv</span><span class="o">=</span><span class="mi">0</span><span class="p">)</span>

        <span class="c1"># Standard Normal Variate</span>
        <span class="n">spectrum</span> <span class="o">=</span> <span class="n">snv</span><span class="p">(</span><span class="n">spectrum</span><span class="p">)</span>
        <span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">xvals</span><span class="p">,</span> <span class="n">spectrum</span><span class="p">)</span>
        <span class="n">dataMatrix</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">vstack</span><span class="p">((</span><span class="n">dataMatrix</span><span class="p">,</span> <span class="n">spectrum</span><span class="p">))</span>

        <span class="k">if</span> <span class="n">row</span><span class="p">[</span><span class="o">-</span><span class="mi">1</span><span class="p">]</span> <span class="o">==</span> <span class="s2">&quot;Healthy&quot;</span><span class="p">:</span>
            <span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">xvals</span><span class="p">,</span> <span class="n">spectrum</span><span class="p">,</span> <span class="n">color</span><span class="o">=</span><span class="s1">&#39;blue&#39;</span><span class="p">,</span> <span class="n">label</span><span class="o">=</span><span class="s1">&#39;Healthy&#39;</span><span class="p">)</span>

        <span class="k">elif</span> <span class="n">row</span><span class="p">[</span><span class="o">-</span><span class="mi">1</span><span class="p">]</span> <span class="o">==</span> <span class="s2">&quot;SARS-CoV-2&quot;</span><span class="p">:</span>
            <span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">xvals</span><span class="p">,</span> <span class="n">spectrum</span><span class="p">,</span> <span class="n">color</span><span class="o">=</span><span class="s1">&#39;red&#39;</span><span class="p">,</span><span class="n">label</span><span class="o">=</span><span class="s1">&#39;SARS-CoV-2&#39;</span><span class="p">)</span>


<span class="n">dataMatrix</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">delete</span><span class="p">(</span><span class="n">dataMatrix</span><span class="p">,</span> <span class="p">(</span><span class="mi">0</span><span class="p">),</span> <span class="n">axis</span><span class="o">=</span><span class="mi">0</span><span class="p">)</span>

<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s2">&quot;Raman Shifts ($cm^{-1}$)&quot;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s2">&quot;Spectra of healthy and infected subjects&quot;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s2">&quot;Counts&quot;</span><span class="p">)</span>
<span class="c1"># Below gets unique series names to reduce size of the legend</span>
<span class="n">handles</span><span class="p">,</span> <span class="n">labels</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">gca</span><span class="p">()</span><span class="o">.</span><span class="n">get_legend_handles_labels</span><span class="p">()</span>
<span class="n">by_label</span> <span class="o">=</span> <span class="nb">dict</span><span class="p">(</span><span class="nb">zip</span><span class="p">(</span><span class="n">labels</span><span class="p">,</span> <span class="n">handles</span><span class="p">))</span>
<span class="n">plt</span><span class="o">.</span><span class="n">legend</span><span class="p">(</span><span class="n">by_label</span><span class="o">.</span><span class="n">values</span><span class="p">(),</span> <span class="n">by_label</span><span class="o">.</span><span class="n">keys</span><span class="p">())</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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olMUaZKqRSEiG4F2IALCI5lDczgcxxYmDAnaYgXhd9mUpTm+GQlTT29RVRfS4HA49sEzFhPG70356Am6ORZxU08Oh2NEYuhdZCeRUxRpkraiUOB3IrJCRD59oBNE5NMislxEljc2Ng6zeIPn61//OnPnzmXevHnMnz+fZ555BoAwDGloaODmm2/e5/zLLruMU089lbPOOovzzjtvnxQgd9xxB2eeeSbz5s3jjDPO2CfhX1927tzJhz/8YWbPns2cOXN4xzvewauvvtqvjDNnznxd8sHPfvazfPOb39zns4cffphzzjmHM888k3POOYdHH330kNrC4agEnsbmhPVBnIsiXVQ1tRcwOfk7AXgeePNA559zzjm6P6tWrXrdZ8PN4sWL9YILLtBCoaCqqo2Njbpt2zZVVX3wwQf1oosu0lmzZqm1tueaSy+9VJctW6aqqnfccYdeccUVqqq6ZcsWnTVrlra0tKiqant7u65fv/51dVpr9YILLtB///d/7/nsueee04ULF/Yr55e//GW95ZZbev6PokinTJmiGzdu3Oe8Z599tkf+F198USdPnnzA8kZC2zuOXV5942xV0OJoT0t1Jm1xjmqA5XoEfXWqFoWqbk/+7gYWAOenKc/hsmPHDhoaGnryMDU0NDB58mQA7r77bm666SZOPPFEnn766QNef+GFF7Jt2zYAdu/eTV1dXc9mSLW1tQfcl/qxxx4jCAJuuOGGns/mz5/Pm970JlSVL37xi5xxxhmceeaZ3HvvvQBce+213HPPPT3nL1y4kBkzZjB9+vR9yj777LN75J87dy6FQoFi0aVQcAwvhtiiCKsNEilRyeV7SovUnNkiUgMYVW1P3l8JfOWICk0pz/iVV17JV77yFU455RSuuOIKrrnmGi699FLy+Ty///3v+f73v09LSwt33303F1544euuf+ihh3jf+94HwFlnncXEiROZOXMmb33rW3n/+9/Pu9/97tdd89JLL3HOOeccUJ4HHniAlStX8vzzz7Nnzx7OO+883vzmNzNv3jyMMTz//POcddZZ3HPPPVx77bUD3tv999/P2WefvU8yQodjODCSKIoqQ7YJOjauZ/Qpp6Us1fFJmhbFRGCRiDwPLAUeVNWHUpTnsKmtrWXFihX84Ac/YPz48VxzzTXceeed/OY3v+Etb3kL1dXVXH311SxYsGCfvE4f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
"
>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[20]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Mean center data</span>
<span class="n">dataMatrixTrans</span> <span class="o">=</span> <span class="n">dataMatrix</span><span class="o">.</span><span class="n">T</span>

<span class="k">for</span> <span class="n">col</span> <span class="ow">in</span> <span class="n">dataMatrixTrans</span><span class="p">:</span>
    <span class="n">meanVal</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">mean</span><span class="p">(</span><span class="n">col</span><span class="p">)</span>

    <span class="k">for</span> <span class="n">count</span><span class="p">,</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">enumerate</span><span class="p">(</span><span class="n">col</span><span class="p">):</span>
        <span class="n">col</span><span class="p">[</span><span class="n">count</span><span class="p">]</span> <span class="o">=</span> <span class="n">col</span><span class="p">[</span><span class="n">count</span><span class="p">]</span> <span class="o">-</span> <span class="n">meanVal</span>

<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">dataMatrixTrans</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s2">&quot;Raman Shifts ($cm^{-1}$)&quot;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s2">&quot;Mean centered spectra&quot;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s2">&quot;Mean centered counts&quot;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[21]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># PCA dimensionality reduction and Training and Test Split</span>
<span class="n">PCAmat</span> <span class="o">=</span> <span class="n">dataMatrixTrans</span><span class="o">.</span><span class="n">T</span>
<span class="n">X_train</span><span class="p">,</span> <span class="n">X_test</span><span class="p">,</span> <span class="n">y_train</span><span class="p">,</span> <span class="n">y_test</span> <span class="o">=</span> <span class="n">train_test_split</span><span class="p">(</span><span class="n">PCAmat</span><span class="p">,</span> <span class="n">encodeClassdata</span><span class="p">,</span> <span class="n">test_size</span><span class="o">=</span><span class="mf">0.33</span><span class="p">,</span> <span class="n">random_state</span><span class="o">=</span><span class="mi">42</span><span class="p">)</span>
<span class="n">pca</span> <span class="o">=</span> <span class="n">PCA</span><span class="p">(</span><span class="n">n_components</span><span class="o">=</span><span class="mi">5</span><span class="p">)</span>
<span class="n">pca</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">X_train</span><span class="p">)</span>
<span class="n">PCAmat</span> <span class="o">=</span> <span class="n">pca</span><span class="o">.</span><span class="n">transform</span><span class="p">(</span><span class="n">X_train</span><span class="p">)</span>

<span class="c1"># Plot % explained variance by # of components</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">arange</span><span class="p">(</span><span class="mi">1</span><span class="p">,</span> <span class="nb">len</span><span class="p">(</span><span class="n">pca</span><span class="o">.</span><span class="n">explained_variance_ratio_</span><span class="p">)</span><span class="o">+</span><span class="mi">1</span><span class="p">,</span> <span class="mi">1</span><span class="p">),</span> <span class="n">np</span><span class="o">.</span><span class="n">cumsum</span><span class="p">(</span><span class="n">pca</span><span class="o">.</span><span class="n">explained_variance_ratio_</span><span class="p">),</span> <span class="s1">&#39;ro-&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s2">&quot;Component #&quot;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s2">&quot;% Variance Explained&quot;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">grid</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[22]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Plot component loadings</span>
<span class="k">for</span> <span class="n">count</span><span class="p">,</span> <span class="n">row</span> <span class="ow">in</span> <span class="nb">enumerate</span><span class="p">(</span><span class="n">pca</span><span class="o">.</span><span class="n">components_</span><span class="p">):</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">xvals</span><span class="p">,</span> <span class="n">np</span><span class="o">.</span><span class="n">transpose</span><span class="p">(</span><span class="n">pca</span><span class="o">.</span><span class="n">components_</span><span class="p">[</span><span class="n">count</span><span class="p">]),</span> <span class="n">label</span><span class="o">=</span><span class="s2">&quot;PC &quot;</span> <span class="o">+</span> <span class="nb">str</span><span class="p">(</span><span class="n">count</span><span class="o">+</span><span class="mi">1</span><span class="p">))</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s2">&quot;Loadings&quot;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s2">&quot;Counts&quot;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s2">&quot;Raman Shifts ($cm^{-1}$)&quot;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">legend</span><span class="p">()</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[30]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Plot scores of component 4 vs component 5 against each other in 2D plot</span>
<span class="k">for</span> <span class="n">count</span><span class="p">,</span> <span class="n">column</span> <span class="ow">in</span> <span class="nb">enumerate</span><span class="p">(</span><span class="n">X_train</span><span class="p">):</span>

    <span class="k">if</span> <span class="n">y_train</span><span class="p">[</span><span class="n">count</span><span class="p">]</span> <span class="o">==</span> <span class="s2">&quot;0&quot;</span><span class="p">:</span>
        <span class="n">plt</span><span class="o">.</span><span class="n">scatter</span><span class="p">(</span><span class="n">PCAmat</span><span class="p">[</span><span class="n">count</span><span class="p">,</span> <span class="mi">3</span><span class="p">],</span> <span class="n">PCAmat</span><span class="p">[</span><span class="n">count</span><span class="p">,</span> <span class="mi">4</span><span class="p">],</span> <span class="n">label</span><span class="o">=</span><span class="s2">&quot;Healthy&quot;</span><span class="p">,</span> <span class="n">color</span><span class="o">=</span><span class="s2">&quot;blue&quot;</span><span class="p">)</span>
    <span class="k">elif</span> <span class="n">y_train</span><span class="p">[</span><span class="n">count</span><span class="p">]</span> <span class="o">==</span> <span class="s2">&quot;1&quot;</span><span class="p">:</span>
        <span class="n">plt</span><span class="o">.</span><span class="n">scatter</span><span class="p">(</span><span class="n">PCAmat</span><span class="p">[</span><span class="n">count</span><span class="p">,</span> <span class="mi">3</span><span class="p">],</span> <span class="n">PCAmat</span><span class="p">[</span><span class="n">count</span><span class="p">,</span> <span class="mi">4</span><span class="p">],</span> <span class="n">label</span><span class="o">=</span><span class="s2">&quot;SARS-CoV-2&quot;</span><span class="p">,</span> <span class="n">color</span><span class="o">=</span><span class="s2">&quot;red&quot;</span><span class="p">)</span>

<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s2">&quot;PC 4&quot;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s2">&quot;PC 5&quot;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s2">&quot;Scatterplot Healthy vs Sick&quot;</span><span class="p">)</span>
<span class="n">handles</span><span class="p">,</span> <span class="n">labels</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">gca</span><span class="p">()</span><span class="o">.</span><span class="n">get_legend_handles_labels</span><span class="p">()</span>
<span class="n">by_label</span> <span class="o">=</span> <span class="nb">dict</span><span class="p">(</span><span class="nb">zip</span><span class="p">(</span><span class="n">labels</span><span class="p">,</span> <span class="n">handles</span><span class="p">))</span>
<span class="n">plt</span><span class="o">.</span><span class="n">legend</span><span class="p">(</span><span class="n">by_label</span><span class="o">.</span><span class="n">values</span><span class="p">(),</span> <span class="n">by_label</span><span class="o">.</span><span class="n">keys</span><span class="p">())</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[31]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># SVM classifier, we will start with using only components 4 and 5</span>

<span class="n">SVMdataMatrix</span> <span class="o">=</span> <span class="n">PCAmat</span><span class="p">[:,</span> <span class="mi">3</span><span class="p">:</span><span class="mi">5</span><span class="p">]</span>
<span class="c1"># SVMdataMatrix = PCAmat[:, :]</span>
<span class="n">SVMmodel</span> <span class="o">=</span> <span class="n">svm</span><span class="o">.</span><span class="n">SVC</span><span class="p">(</span><span class="n">kernel</span><span class="o">=</span><span class="s1">&#39;poly&#39;</span><span class="p">,</span> <span class="n">degree</span><span class="o">=</span><span class="mi">3</span><span class="p">)</span><span class="c1">#, C=1, gamma=1)</span>
<span class="n">SVMmodel</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">SVMdataMatrix</span><span class="p">,</span> <span class="n">y_train</span><span class="p">)</span>

<span class="c1"># Use gridsearch to tune hyper-parameters</span>
<span class="kn">from</span> <span class="nn">sklearn.model_selection</span> <span class="kn">import</span> <span class="n">GridSearchCV</span>

<span class="c1"># defining parameter range</span>
<span class="n">param_grid</span> <span class="o">=</span> <span class="p">{</span><span class="s1">&#39;C&#39;</span><span class="p">:</span> <span class="p">[</span><span class="mf">0.1</span><span class="p">,</span> <span class="mi">1</span><span class="p">,</span> <span class="mi">10</span><span class="p">,</span> <span class="mi">100</span><span class="p">,</span> <span class="mi">1000</span><span class="p">],</span>
              <span class="s1">&#39;gamma&#39;</span><span class="p">:</span> <span class="p">[</span><span class="mi">1</span><span class="p">,</span> <span class="mf">0.1</span><span class="p">,</span> <span class="mf">0.01</span><span class="p">,</span> <span class="mf">0.001</span><span class="p">,</span> <span class="mf">0.0001</span><span class="p">],</span>
              <span class="s1">&#39;kernel&#39;</span><span class="p">:</span> <span class="p">[</span><span class="s1">&#39;poly&#39;</span><span class="p">],</span>
              <span class="s1">&#39;degree&#39;</span><span class="p">:[</span><span class="mi">0</span><span class="p">,</span> <span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">3</span><span class="p">,</span> <span class="mi">4</span><span class="p">]}</span>

<span class="n">grid</span> <span class="o">=</span> <span class="n">GridSearchCV</span><span class="p">(</span><span class="n">svm</span><span class="o">.</span><span class="n">SVC</span><span class="p">(),</span> <span class="n">param_grid</span><span class="p">,</span> <span class="n">refit</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span><span class="c1">#, verbose=3)</span>

<span class="c1"># fitting the model for grid search</span>
<span class="n">grid</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">SVMdataMatrix</span><span class="p">,</span> <span class="n">y_train</span><span class="p">)</span>
<span class="c1"># print best parameter after tuning</span>
<span class="nb">print</span><span class="p">(</span><span class="n">grid</span><span class="o">.</span><span class="n">best_params_</span><span class="p">)</span>

<span class="c1"># print how our model looks after hyper-parameter tuning</span>
<span class="nb">print</span><span class="p">(</span><span class="n">grid</span><span class="o">.</span><span class="n">best_estimator_</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>{&#39;C&#39;: 0.1, &#39;degree&#39;: 1, &#39;gamma&#39;: 1, &#39;kernel&#39;: &#39;poly&#39;}
SVC(C=0.1, degree=1, gamma=1, kernel=&#39;poly&#39;)
</pre>
</div>
</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[43]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Use model to predict disease state on split testing Set</span>
<span class="n">test_PCAmat</span> <span class="o">=</span> <span class="n">pca</span><span class="o">.</span><span class="n">transform</span><span class="p">(</span><span class="n">X_test</span><span class="p">)</span>
<span class="n">test_SVMdataMatrix</span> <span class="o">=</span> <span class="n">test_PCAmat</span><span class="p">[:,</span> <span class="mi">3</span><span class="p">:</span><span class="mi">5</span><span class="p">]</span>
<span class="c1"># test_SVMdataMatrix = test_PCAmat[:, :]</span>
<span class="n">test_preds</span> <span class="o">=</span> <span class="n">grid</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">test_SVMdataMatrix</span><span class="p">)</span>
<span class="n">nocode_y_test</span> <span class="o">=</span> <span class="p">[</span><span class="n">item</span><span class="o">.</span><span class="n">replace</span><span class="p">(</span><span class="s2">&quot;0&quot;</span><span class="p">,</span> <span class="s2">&quot;Covid (-)&quot;</span><span class="p">)</span> <span class="k">for</span> <span class="n">item</span> <span class="ow">in</span> <span class="n">y_test</span><span class="o">.</span><span class="n">tolist</span><span class="p">()]</span>
<span class="n">nocode_y_test</span> <span class="o">=</span> <span class="p">[</span><span class="n">item</span><span class="o">.</span><span class="n">replace</span><span class="p">(</span><span class="s2">&quot;1&quot;</span><span class="p">,</span> <span class="s2">&quot;Covid (+)&quot;</span><span class="p">)</span> <span class="k">for</span> <span class="n">item</span> <span class="ow">in</span> <span class="n">nocode_y_test</span><span class="p">]</span>

<span class="c1"># Build and plot confusion matrix</span>
<span class="n">cfMat</span> <span class="o">=</span> <span class="n">metrics</span><span class="o">.</span><span class="n">confusion_matrix</span><span class="p">(</span><span class="n">y_test</span><span class="p">,</span> <span class="n">test_preds</span><span class="p">)</span>
<span class="n">disp</span> <span class="o">=</span> <span class="n">metrics</span><span class="o">.</span><span class="n">plot_confusion_matrix</span><span class="p">(</span><span class="n">grid</span><span class="p">,</span> <span class="n">test_SVMdataMatrix</span><span class="p">,</span> <span class="n">y_test</span><span class="p">,</span>  <span class="n">cmap</span><span class="o">=</span><span class="n">plt</span><span class="o">.</span><span class="n">cm</span><span class="o">.</span><span class="n">Blues</span><span class="p">,</span> <span class="n">normalize</span><span class="o">=</span><span class="s1">&#39;true&#39;</span><span class="p">,</span> <span class="n">display_labels</span><span class="o">=</span><span class="n">nocode_y_test</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAV4AAAEKCAYAAABaND37AAAABHNCSVQICAgIfAhkiAAAAAlwSFlzAAALEgAACxIB0t1+/AAAADh0RVh0U29mdHdhcmUAbWF0cGxvdGxpYiB2ZXJzaW9uMy4yLjIsIGh0dHA6Ly9tYXRwbG90bGliLm9yZy+WH4yJAAAeqklEQVR4nO3deZwdVZ338c+3OyEQ9mwQsiBLgmyyJSBGIIBAEhmRRUHRGRgRUJBHH0VxGRfUmXmIzCgYjAkyiCgBBCRABFQMARHNQghJME7YQpNAEgKEVejk9/xR1XD7pu/te5PbdW9Xf9+86kVX1alTv5tL/zg5dc4pRQRmZpadpnoHYGbW0zjxmpllzInXzCxjTrxmZhlz4jUzy5gTr5lZxpx4zczKkHSVpJWSFpY4L0mXSVoqaYGkAzur04nXzKy8q4FxZc6PB0ak29nATzqr0InXzKyMiJgFrClT5ATgmkg8CGwnaXC5OnvVMsC8U5+tQ3371zsMq8LeO/erdwhWpYUPP7Q6IgZuSh3N2+wc0fp6RWXj9VWLgDcKDk2JiClV3G4I8HTBfkt6bEWpC5x4q6C+/ekz9uv1DsOqcOuUT9Q7BKvSboP6PrWpdUTr6/TZ46MVlX1j/qQ3ImLUJtxOHYVQ7gInXjPLIYEy60ltAYYV7A8Flpe7wH28ZpY/ApqaK9s23XTgn9PRDe8FXoqIkt0M4BavmeWVOuoB2JhqdB0wFhggqQX4FtAbICImAzOACcBS4DXgzM7qdOI1sxyqXVdDRHysk/MBnFdNnU68ZpZPNWrxdgUnXjPLH5Hlw7WqOfGaWQ7JLV4zs8zVZsRCl3DiNbMcynQcb9WceM0sf4S7GszMMucWr5lZltzVYGaWLQHNfrhmZpYt9/GamWXJXQ1mZtlzi9fMLGNu8ZqZZUieMmxmlj1PGTYzy5IfrpmZZc9dDWZmGfJ6vGZmWXNXg5lZ9vxwzcwsY+7jNTPLkNzVYGaWPbd4zcyyJSdeM7PsJG/+ceI1M8uOhJqceM3MMuUWr5lZxpx4zcwy5sRrZpYlpVuDcuI1s9wRcovXzCxrTU2euWZmlim3eM3MsuQ+XjOz7DVyi7dxO0HMzDZS28O1SrZO65LGSVoiaamkizo4v62k2yQ9LGmRpDM7q9MtXjPLpVpMGZbUDEwCjgFagNmSpkfE4oJi5wGLI+KfJA0Elkj6ZUS8Wapet3jNLH9ErVq8BwNLI+LxNJFOA04oKhPA1koq2wpYA7SWq9QtXjPLpSr6eAdImlOwPyUipqQ/DwGeLjjXAhxSdP2PgenAcmBr4NSIWF/uhk68ZpZLVSTe1RExqlQ1HRyLov3jgPnAUcBuwO8k3RcRa0vd0F0NZpY7NXy41gIMK9gfStKyLXQmcHMklgJPAO8uV6kTr5nlkyrcypsNjJC0i6TNgNNIuhUKLQOOBpC0A7AH8Hi5St3VYGb5o9pMGY6IVknnA3cBzcBVEbFI0rnp+cnAd4GrJT2S3JmvRMTqcvU68ZpZLtVqAkVEzABmFB2bXPDzcuDYaup04jWzfGrciWtOvHl39P5D+Y8zD6W5SfziD0v44W8ebnd+m769+ennjmTogK1obm7ix9MX8KuZfwfgMx/ch08e/W6IYPGyNZx3xSz+8da6enyMHuW+2X/jP38ynXXr13PyuIP59GlHtTv/+LKVfOPS61m89Bn+zxnjOPMjYwFYsfJFvjpxGs+veRk1iY9MOIRPnnhYHT5BY/CU4ZSkHSVNk/SYpMWSZkgauRH1jJJ0WYlzT0oa0MFxSbpH0jYdnDte0neqjaPRNTWJiZ8aw0e+fyfv/cKvOXnMbuwxdLt2Zc46bm+WtLzIYRfezD99+3a+9y+H0LtXE4P79eWcCftw1EW38L4v3kRTUxMnjdm1Tp+k51i3bj3f//EtTP7+p5g+9UvMmDmfpU89167Mtlv35auf/TBnnnJEu+O9mpv48tnHc9vPLuS6H53PddMf2ODanqLSEQ31Ss6ZJd50VsctwMyI2C0i9gK+BuxQbV0RMSciLqjysgnAwyXG1t0BfEhS32pjaWQH7T6Qx59dy1MrX+at1vXc/KfHmDBq53ZlIoKttugNwJab9+aFV/5B67pk7HevJrH5Zr1obhJ9+/Ti2TWvZf4ZeppHlixj2E4DGDa4P5v17sWEI/bnjw8salem//Zbse8ew+jV3Nzu+MD+27DXiKEAbNl3c3YdPoiVq1/KLPZG48SbOBJ4q6hTen5E3Je2RidKWijpEUmnAki6XtKEtvKSrpZ0sqSxkm5Pj/WXdLekhyT9lNI9O6cDt3Z0IiICmAkcX5NP2iAG99uSZ55/5e395WteZXD/LduVmXrnYkYO2Y5Hp5zOny49ma/+z5+JgBVrXuPy2xbwyE8+xt+mns7a197kjwueyfoj9DjPrV7L4IHv/K1kh4Hb8tzz1SfPZ55dw6NLl/Oedw+vZXjdippU0VYPWSbefYC5Jc6dBOwP7Ad8AJgoaTDJvOi2JLwZyVi5GUXXfgu4PyIOIBlfV+q/tDFl7g8wB9igQ0zS2ZLmSJoT/3i5zOWNp8MpN0Vzbo7afyiPPPk8e579Sw6/8GYu+dQYtt6iN9tuuRkTRr+L/c+bxp5n/5K+fXrx0cN2zyTunq14UlT1fZWvvv4PPn/xNVz0mQ+x1Zab1yqwbsct3s69H7guItZFxHPAvcBo4LfAUZL6AOOBWRHxetG1hwPXAkTEHcALJe7RLyLKZc6VwE7FByNiSkSMiohR6rN1VR+q3paveZUh/bd6e3+nflvy7JpX25U5/ciR3P6XJwF4Iu2WGDFkO8buO4SnVr7M82vfoHVdcNtfnuTgParuFbIq7TBgW1asevHt/edWvcSgfhs8lijprdZ1fP7ia/jgUQdwzPv37YoQu4faLZLTJbJMvIuAg0qc6/DTR8QbJF0Ax5G0fKeVuH7DZsKGWiU1AUg6T9L8dGtLtpsDxUm9W5u3dBW7Dd6G4YO2pnevJk4asxu/nbOsXZmW1a9w+L7JH8HAbbdg95225cnn1tKy+hVGjRjEFpsl/YhH7LsTS1pe3OAeVlv77DGMZc+spmXFGt58q5UZ987nyEP3qujaiOCb/3UDuw4fxBlFD956GgFSZVs9ZDmc7B7g3yV9OiKmAkgaDfQFZgHnSPo50I+kFXthet004CxgFHBGB/XOIum//Z6k8cD2Je6/BNiVZIm3SSRrbBYaCSzcuI/WmNatD778swe46evjaW4Sv/zjEv7W8gJnHrMnAP/zu0eZ+OuHmHTeEfzp0pMR8J1r/8qal//BmpdXMf3Bx5l5yUmsW7eeBU8+z89//2h9P1AP0Ku5ma+f/2HO/tpU1q9fz4nHHczu79qR62//MwCnHn8oq9as5dTzL+OV196gSeIXt9zP9KlfYskTK5j++3mM3GVHTjr3vwD4/L+O5/CD96znR6qTxn7LsKK4068rb5a0Ln9I0vJ9A3gS+DywFLiEpDshgO9FxPXpNb2BZ4HpEXFmemws8KWIOF5Sf+A6YABJF8VJwEHFU/Yk/RuwIiKuLBHb7cBXI+KRUvE3bf+u6DP26xv34a0uFk35RL1DsCrtNqjv3DKrhVVk8x1Hxs7/cnlFZf9+ybhNvl+1Mp1AkU6t+2iJ0xfyTiu38Jq3gP5Fx2aSdEEQEc/TfrreF0rUfyVwTfrvdtKFLbYol3TNrBupYzdCJXrMzLWIWCFpqqRtOhjLOxz4Yj3iMrPaE8kEokbVYxIvQETcUOL47KxjMbOu5RavmVnGGvnhmhOvmeWP+3jNzLIlVJOF0LuKE6+Z5ZJbvGZmGXMfr5lZltzHa2aWrWSthsbNvE68ZpZLDZx3nXjNLJ88c83MLEtyV4OZWaba1uNtVE68ZpZDjb0erxOvmeVSA+ddJ14zyyH54ZqZWaY8jtfMrA6ceM3MMtbAedeJ18zyyS1eM7MseZEcM7NsJQuhN27mdeI1s1xqauAmb+O+G8PMbBNIlW2d16NxkpZIWirpohJlxkqaL2mRpHs7q9MtXjPLHdVokRxJzcAk4BigBZgtaXpELC4osx1wBTAuIpZJGtRZvW7xmlkuNamyrRMHA0sj4vGIeBOYBpxQVObjwM0RsQwgIlZ2VmnJFq+ky4EodT4iLug0ZDOzOqni4doASXMK9qdExJT05yHA0wXnWoBDiq4fCfSWNBPYGvhRRFxT7obluhrmlDlnZtawRDKyoUKrI2JUmaqKFTdIewEHAUcDWwB/lvRgRPy91A1LJt6I+Hm7u0tbRsSrpcqbmTWSGo0mawGGFewPBZZ3UGZ1mh9flTQL2A8omXg77eOVdKikxcCj6f5+kq6oMngzs+woWY+3kq0Ts4ERknaRtBlwGjC9qMytwGGSeknqS9IV8Wi5SisZ1fBD4Li2m0XEw5IOr+A6M7O6qcUw3oholXQ+cBfQDFwVEYsknZuenxwRj0q6E1gArAeujIiF5eqtaDhZRDxd9H+GdRvzIczMsiBqN4EiImYAM4qOTS7anwhMrLTOShLv05LeB0Ta1L6ATprRZmb11shThisZx3sucB7JsIpngP3TfTOzhlTprLV6zSrutMUbEauB0zOIxcysZrr1Wg2SdpV0m6RVklZKulXSrlkEZ2a2sVThVg+VdDX8CrgBGAzsBNwIXNeVQZmZbaoaDSfrEpUkXkXELyKiNd2upcxUYjOzektGNdRkrYYuUW6thn7pj39Ml0KbRpJwTwXuyCA2M7ONo+67EPpckkTbFv05BecC+G5XBWVmtqm65TvXImKXLAMxM6uVtq6GRlXRzDVJ+wB7AZu3Hets2TMzs3rqli3eNpK+BYwlSbwzgPHA/YATr5k1rMZNu5WNajiFZJ3JZyPiTJLlzvp0aVRmZptAguYmVbTVQyVdDa9HxHpJrZK2AVYCnkBhZg2tW3c1AHPSl7lNJRnp8Arw1y6NysxsEzVw3q1orYbPpj9OTtec3CYiFnRtWGZmG0+ooddqKDeB4sBy5yJiXteEZGa2ieq48lglyrV4Ly1zLoCjahxLwztg1wH86cZP1zsMq8L2o8+vdwhWJ92yjzcijswyEDOzWhHQ3B0Tr5lZd9btZ66ZmXU3TrxmZhlKXuvTuJm3kjdQSNInJH0z3R8u6eCuD83MbOM18nq8lUwZvgI4FPhYuv8yMKnLIjIzq4Fu/bJL4JCIOFDSQwAR8UL6mnczs4YkoFcDdzVUknjfktRM+rofSQOB9V0alZnZJmrgvFtR4r0MuAUYJOn7JKuVfaNLozIz2wRSN50y3CYifilpLsnSkAI+HBGPdnlkZmaboIHzbkULoQ8HXgNuKzwWEcu6MjAzs03R3cfx3sE7L73cHNgFWALs3YVxmZltNEHdFjmvRCVdDfsW7qerlp1ToriZWf3VcYxuJaqeuRYR8ySN7opgzMxqRQ381rVK+nj/b8FuE3AgsKrLIjIz20R5eL371gU/t5L0+d7UNeGYmdVGt0286cSJrSLiwoziMTOriUZeJKfcq396RURruVcAmZk1ouT17vWOorRyobW9SXi+pOmSPinppLYti+DMzDZWUzp7rbOtM5LGSVoiaamki8qUGy1pnaRTOquzkj7efsDzJO9YaxvPG8DNFVxrZpa5Wj1cS7tbJwHHAC3AbEnTI2JxB+X+H3BXJfWWS7yD0hENC3kn4baJKmI3M8tcjbp4DwaWRsTjSZ2aBpwALC4q9zmSQQcVDbUtl3ibga2gw8FwTrxm1sBEU+XjeAdImlOwPyUipqQ/DwGeLjjXAhzS7k7SEOBEkl6BTU68KyLi4koqMTNrJKKqFu/qiBhVpqpixQ3PHwJfiYh1lY6kKJd4G3cshplZOYJetRnI2wIMK9gfCiwvKjMKmJYm3QHABEmtEfGbUpWWS7xHb2SgZmZ1VWWLt5zZwAhJuwDPAKcBHy8sEBG7vH1f6Wrg9nJJF8ok3ohYsynRmpnVUy0WQk/nMpxPMlqhGbgqIhZJOjc9P3lj6vXr3c0sl2o1cS0iZgAzio51mHAj4oxK6nTiNbPcEZW9Qr1enHjNLH9Um66GruLEa2a5k8xcc+I1M8tU46ZdJ14zy6kGbvA68ZpZHql7rsdrZtZdeVSDmVkd+OGamVmW1E1f/WNm1l25q8HMrA7c4jUzy1jjpl0nXjPLIQHNbvGamWWrgfOuE6+Z5ZFQA3c2OPGaWS65xWtmlqFkOFnjZl4nXjPLH7nFa2aWOU8ZNjPLULIQer2jKM2J18xyyaMazMwy1sA9DQ29joRl4PcPLGb0yRdz4Inf5r+vvrve4VgnLv+30/n7Xf/BA9O+Vu9QGp4q/KcenHh7sHXr1nPhJTdw448+y4M3fIOb7p7L3x5fUe+wrIzrbn+QUy6YVO8wGl5bH28lWz10WeKVtKOkaZIek7RY0gxJIzeinlGSLitx7klJAzo4Lkn3SNqmwnv8QNJR1cbW3c1d9CS7DhvAu4YOYLPevTjpmAOZce+CeodlZTzw0GO8sPa1eofR+CSaKtzqoUsSr5L12G4BZkbEbhGxF/A1YIdq64qIORFxQZWXTQAejoi1RXGNlXR1B+UvBy6qNrbubsWqlxiyw/Zv7++0w/asWPVSHSMyqx1VuNVDV7V4jwTeiojJbQciYn5E3Je2RidKWijpEUmnAki6XtKEtvKSrpZ0cposb0+P9Zd0t6SHJP2U0n9upwO3VhpsRDwF9Je0Y/E5SWdLmiNpzqrVqyqtsluIiA2ONfIDCbNKJV0NPazFC+wDzC1x7iRgf2A/4APAREmDgWlAWxLeDDgamFF07beA+yPiAGA6MLzEPcaUuX8p89Lr2omIKRExKiJGDRwwsMoqG9tOg7bjmedeeHt/+XMvsOOAbesYkVnt9MQWbznvB66LiHUR8RxwLzAa+C1wlKQ+wHhgVkS8XnTt4cC1ABFxB/ACHesXES+37Uj6i6T5wJXAhyTNT7fjCq5ZCexUg8/XbRy41848tmwVTz2zmjffauXm381j/OHvqXdYZrXRwJm3q8bxLgJOKXGuw48aEW9ImgkcR9Lyva7E9Rv+/XhDrZKaImJ9WvchkPTxAmdExBkdXLM5UJzoc61Xr2Yu+fJHOfmCSaxbF5z+ofey526D6x2WlXHl985gzEEj6L/dViy8/bv855QZXDv9z/UOqyH1xCnD9wD/LunTETEVQNJooC8wCzhH0s+BfiSt2AvT66YBZwGjgDM6qHcWSf/t9ySNB7bvoAzAEmBXYGkVMY8EbqyifC4cO2Zvjh2zd73DsAqd9Y2r6x1Ct9G4abeLuhoieWpzInBMOpxsEfBtYDnJaIcFwMMkCfrLEfFseundJIn49xHxZgdVfwc4XNI84FhgWYkQ7gDGVhqvpN7A7sCcSq8xswbXA7saiIjlwEdLnL6Qd1q5hde8BfQvOjYTmJn+/DxJwm3zhRL1Xwlck/67w7qKHA/8OiJaS9RnZt1IklMbt82by5lrEbECmFrpBAqS/wFd2oUhmVmW0vV4K9nqIZeJFyAibiieQFGm7I0R8WJXx2Rm2alVT4OkcZKWSFoqaYOJVpJOl7Qg3R6QtF9ndXp1MjPLIaEaNGclNQOTgGOAFmC2pOkRsbig2BPAERHxQvrQfwpwSLl6nXjNLJdq1I1wMLA0Ih5P6tQ04ATg7cQbEQ8UlH8QGNpZpbntajCznqvSboY0Nw9oWxYg3c4uqGoI8HTBfkt6rJRPkUwGK8stXjPLp8pbvKsjYlQVtXQ4iUvSkSSJ9/2d3dCJ18xyqUbDyVqAYQX7Q0nmI7S/l/QekuGr49Nhr2W5q8HMcqlGw8lmAyMk7ZIu3nUayQJdBffRcOBm4JMR8fdKYnOL18zyp0ZjdCOiVdL5wF1AM3BVRCySdG56fjLwTZKJX1ekIylay3RdAE68ZpZTtZq5FhEzKFqitmit8bNI1pipmBOvmeWOaOxF/Z14zSyXGjjvOvGaWU41cOZ14jWzXOqJC6GbmdVV46ZdJ14zy6sGzrxOvGaWO42+ELoTr5nlTx0XOa+EE6+Z5VID510nXjPLo9oshN5VnHjNLJcaOO868ZpZ/tTxze0VceI1s3xq4MzrxGtmueThZGZmGXMfr5lZlgRNTrxmZllr3MzrxGtmueOF0M3M6qCB864Tr5nlk1u8ZmYZ85RhM7OMNW7adeI1sxySl4U0M8ueZ66ZmWWtcfOuE6+Z5VMD510nXjPLI/n17mZmWWr0mWtN9Q7AzKyncYvXzHKpkVu8TrxmlkseTmZmliVPoDAzy1ajP1xz4jWzXHJXg5lZxhq5xevhZGaWS6pw67QeaZykJZKWSrqog/OSdFl6foGkAzur04nXzPKpBplXUjMwCRgP7AV8TNJeRcXGAyPS7WzgJ52F5sRrZrkjoEmqaOvEwcDSiHg8It4EpgEnFJU5AbgmEg8C20kaXK5S9/FWYd68uau36K2n6h1HFxkArK53EFaVvH5nO29qBfPmzb1ri94aUGHxzSXNKdifEhFT0p+HAE8XnGsBDim6vqMyQ4AVpW7oxFuFiBhY7xi6iqQ5ETGq3nFY5fydlRYR42pUVUdN4tiIMu24q8HMrLQWYFjB/lBg+UaUaceJ18ystNnACEm7SNoMOA2YXlRmOvDP6eiG9wIvRUTJbgZwV4O9Y0rnRazB+DvrYhHRKul84C6gGbgqIhZJOjc9PxmYAUwAlgKvAWd2Vq8iynZFmJlZjbmrwcwsY068ZmYZc+LtpiTtKGmapMckLZY0Q9LIjahnlKTLSpx7UtpwLGT6EOEeSdt0cO54Sd+pNo68atTvqUQ9P5B0VLWxWfWceLshSQJuAWZGxG4RsRfwNWCHauuKiDkRcUGVl00AHo6ItR2cuwP4kKS+1caSN436PUkaK+nqDspfDmywFoHVnhNv93Qk8Fb6RBWAiJgfEfelrZyJkhZKekTSqQCSrpc0oa28pKslnZz+Et6eHusv6W5JD0n6KaVnsp8O3NrRiUie1s4Ejq/JJ+3eGvZ76khEPAX0l7TjRnxWq4ITb/e0DzC3xLmTgP2B/YAPABPTeePTgLZf7s2Ao0mGwRT6FnB/RBxAMjZxeIl7jClzf4A5wGGdf4zca/TvqSPz0uusC3kcb/68H7guItYBz0m6FxgN/Ba4TFIfYBwwKyJeV/tFQg4nSQhExB2SXihxj34R8XKZGFYCO23i58i7zL8nSX8B+gBbAf0kzU9PfSUi7kp/9neXAbd4u6dFwEElznX4186IeIOkC+A4khbVtBLXVzKwu1VSE4Ck8yTNT7e2X9jNgdcrqCfvGuZ7Sus+JCL2B84CpkfE/ul2V8E1/u4y4MTbPd0D9JH06bYDkkZLOgKYBZwqqVnSQJLW0V/TYtNIZtUcRjITp9gskn5BJI0Hti9x/yXArgARMangF7htfvpIYOGmfMCcaJjvqQr+7jLgxNsNpQ+wTgSOSYcpLQK+TbIwxy3AAuBhkl/8L0fEs+mld5P8gv8+XVu02HeAwyXNA44FlpUI4Q5gbJkQj0zL9Gjd4HtqR1JvYHeSPnrrQp4ybFVLHwJdExHHdHBuB+BXEXF09pFZoXLfU4nyJwIHRsS/dW1k5havVS1deWlqiYH5w4EvZhySdaCT76kjvYBLuzAkS7nFa2aWMbd4zcwy5sRrZpYxJ14zs4w58VpNSVqXTqZYKOnGTVksJ12n4JT05ysl7VWm7FhJ79uIe5Ra2avD40VlXqnyXt+W9KVqY7T8ceK1Wns9nUyxD/AmcG7hSUnNG1NpRJwVEYvLFBkLVJ14zerBide60n3A7mlr9I+SfgU8ks7WmihptqQFks6Bt9eP/bGSdWvvAAa1VSRppqRR6c/jJM2T9LCkP0h6F0mC/0La2j5M0kBJN6X3mC1pTHptpSt7vU3SbyTNlbRI0tlF5y5NY/lDOgMNSbtJujO95j5J767FH6blhxfJsS4hqRcwHrgzPXQwsE9EPJEmr5ciYnS6GMyfJN0NHADsAexLsmbtYuCqonoHAlOBw9O6+kXEGkmTgVci4gdpuV8B/x0R90saTjL1dk/eWdnrYkkfBNol0hL+Nb3HFsBsSTdFxPPAlsC8iPiipG+mdZ9P8hLKcyPifyUdAlwBeIFxe5sTr9XaFgWrXt0H/IykC+CvEfFEevxY4D1t/bfAtsAIkmmybSt2LZd0Twf1v5dkxa4nACJiTYk4PgDsVbCq1zaStqbylb0KXZDO6gIYlsb6PLAeuD49fi1ws6St0s97Y8G9+1RwD+tBnHit1l5PV8B6W5qAXi08BHyuaFUslCwA3tmMHlVQBpJutEMjot1KW2ksFc8akjSWJIkfGhGvSZpJsoJXRyK974vFfwZmhdzHa/VwF/CZdFEWJI2UtCXJqlunpX3Ag0kW2yn2Z+AISbuk1/ZLj78MbF1Q7m6Sv/aTlmtLhJWu7NVmW+CFNOm+m6TF3aYJaGu1f5ykC2Mt8ISkj6T3kKT9OrmH9TBOvFYPV5L0386TtBD4Kcnfvm4B/hd4BPgJcG/xhRGxiqRf9mZJD/POX/VvA05se7gGXACMSh/eLead0RWVruzV5k6gl6QFwHeBBwvOvQrsLWkuSR/uxenx04FPpfEtAk6o4M/EehCv1WBmljG3eM3MMubEa2aWMSdeM7OMOfGamWXMidfMLGNOvGZmGXPiNTPL2P8HS3+lJ3qwi+wAAAAASUVORK5CYII=
"
>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[42]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Create color maps</span>
<span class="n">cmap_light</span> <span class="o">=</span> <span class="n">ListedColormap</span><span class="p">([</span><span class="s1">&#39;orange&#39;</span><span class="p">,</span> <span class="s1">&#39;cyan&#39;</span><span class="p">])</span>
<span class="n">cmap_bold</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;darkorange&#39;</span><span class="p">,</span> <span class="s1">&#39;darkblue&#39;</span><span class="p">]</span>

<span class="c1"># Plotting the decision boundary</span>
<span class="n">x_min</span><span class="p">,</span> <span class="n">x_max</span> <span class="o">=</span> <span class="n">test_SVMdataMatrix</span><span class="p">[:,</span> <span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">min</span><span class="p">()</span> <span class="o">-</span> <span class="mi">1</span><span class="p">,</span> <span class="n">test_SVMdataMatrix</span><span class="p">[:,</span> <span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">max</span><span class="p">()</span> <span class="o">+</span> <span class="mi">1</span>
<span class="n">y_min</span><span class="p">,</span> <span class="n">y_max</span> <span class="o">=</span> <span class="n">test_SVMdataMatrix</span><span class="p">[:,</span> <span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">min</span><span class="p">()</span> <span class="o">-</span> <span class="mi">1</span><span class="p">,</span> <span class="n">test_SVMdataMatrix</span><span class="p">[:,</span> <span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">max</span><span class="p">()</span> <span class="o">+</span> <span class="mi">1</span>

<span class="n">h</span> <span class="o">=</span> <span class="mf">0.02</span>
<span class="n">xx</span><span class="p">,</span> <span class="n">yy</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">meshgrid</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">arange</span><span class="p">(</span><span class="n">x_min</span><span class="p">,</span> <span class="n">x_max</span><span class="p">,</span> <span class="n">h</span><span class="p">),</span> <span class="n">np</span><span class="o">.</span><span class="n">arange</span><span class="p">(</span><span class="n">y_min</span><span class="p">,</span> <span class="n">y_max</span><span class="p">,</span> <span class="n">h</span><span class="p">))</span>

<span class="n">zMat</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">c_</span><span class="p">[</span><span class="n">xx</span><span class="o">.</span><span class="n">flatten</span><span class="p">(),</span> <span class="n">yy</span><span class="o">.</span><span class="n">flatten</span><span class="p">()]</span>

<span class="n">Z</span> <span class="o">=</span> <span class="n">grid</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">zMat</span><span class="p">[:,</span> <span class="mi">0</span><span class="p">:</span><span class="mi">2</span><span class="p">])</span>

<span class="c1"># Put the result into a color plot</span>
<span class="n">Z</span> <span class="o">=</span> <span class="n">Z</span><span class="o">.</span><span class="n">reshape</span><span class="p">(</span><span class="n">xx</span><span class="o">.</span><span class="n">shape</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">contourf</span><span class="p">(</span><span class="n">xx</span><span class="p">,</span> <span class="n">yy</span><span class="p">,</span> <span class="n">Z</span><span class="p">,</span> <span class="n">cmap</span><span class="o">=</span><span class="n">cmap_light</span><span class="p">,</span> <span class="n">alpha</span><span class="o">=</span><span class="mf">0.8</span><span class="p">)</span>

<span class="n">sns</span><span class="o">.</span><span class="n">scatterplot</span><span class="p">(</span><span class="n">test_SVMdataMatrix</span><span class="p">[:,</span> <span class="mi">0</span><span class="p">],</span> <span class="n">test_SVMdataMatrix</span><span class="p">[:,</span> <span class="mi">1</span><span class="p">],</span> <span class="n">hue</span><span class="o">=</span><span class="n">nocode_y_test</span><span class="p">,</span>
                    <span class="n">palette</span><span class="o">=</span><span class="n">cmap_bold</span><span class="p">,</span> <span class="n">alpha</span><span class="o">=</span><span class="mf">1.0</span><span class="p">,</span> <span class="n">edgecolor</span><span class="o">=</span><span class="s2">&quot;black&quot;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s1">&#39;PC 4&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s1">&#39;PC 5&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs  ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[&nbsp;]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

     </div>
</div>
</div>
</div>

</div>
</body>







</html>

