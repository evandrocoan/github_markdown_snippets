# GitHub Markdown Snippets
Helpful Sublime Text snippets to get you started with GitHub flavored Markdown by letting you type the plain old HTML tags.


## Installation

### By Package Control

1. Download & Install **`Sublime Text 3`** (https://www.sublimetext.com/3)
1. Go to the menu **`Tools -> Install Package Control`**, then,
   wait few seconds until the installation finishes up
1. Now,
   Go to the menu **`Preferences -> Package Control`**
1. Type **`Add Channel`** on the opened quick panel and press <kbd>Enter</kbd>
1. Then,
   input the following address and press <kbd>Enter</kbd>
   ```
   https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json
   ```
1. Go to the menu **`Tools -> Command Palette...
   (Ctrl+Shift+P)`**
1. Type **`Preferences:
   Package Control Settings – User`** on the opened quick panel and press <kbd>Enter</kbd>
1. Then,
   find the following setting on your **`Package Control.sublime-settings`** file:
   ```js
       "channels":
       [
           "https://packagecontrol.io/channel_v3.json",
           "https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json",
       ],
   ```
1. And,
   change it to the following, i.e.,
   put the **`https://raw.githubusercontent...`** line as first:
   ```js
       "channels":
       [
           "https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json",
           "https://packagecontrol.io/channel_v3.json",
       ],
   ```
   * The **`https://raw.githubusercontent...`** line must to be added before the **`https://packagecontrol.io...`** one, otherwise,
     you will not install this forked version of the package,
     but the original available on the Package Control default channel **`https://packagecontrol.io...`**
1. Now,
   go to the menu **`Preferences -> Package Control`**
1. Type **`Install Package`** on the opened quick panel and press <kbd>Enter</kbd>
1. Then,
search for **`GitHubMarkdownSnippets`** and press <kbd>Enter</kbd>

See also:
1. [ITE - Integrated Toolset Environment](https://github.com/evandrocoan/ITE)
1. [Package control docs](https://packagecontrol.io/docs/usage) for details.


### Using with Emmet
If you have Emmet installed, tab triggers may not function as expected due to [this](https://github.com/sergeche/emmet-sublime#tab-key-handler).

To get around the problem, go to
```
Preferences > Package Settings > Emmet > User Settings
```
and add the following in your settings file.

```
{
    "disable_tab_abbreviations_for_scopes": "text.html.markdown"
}
```

This should let markdown snippets take precedence over emmet's tab to expand abbreviations feature and provide correct snippets.

Note that any tab trigger not set by this plugin will be converted to HTML tags which is convenient for people
who want to use HTML tags inside Markdown files.

## Usage
A consolidated guide is available [here](http://praveenpuglia.github.io/github_markdown_snippets).

Type a tag name and hit tab. That's it! :relaxed:

:snowflake: Long tags like `blockquote` are shortened for power use.

## List of Tab Triggers

```
h1     // Heading 1
h2     // Heading 2
h3     // Heading 3
h4     // Heading 4
h5     // Heading 5
h6     // Heading 6
```
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6
```
b         // Bold
i         // Italic
bq        // Blockquote
strike    // Strikeout
hr        // Horizontal Rule, Divider
```
**Bold Text**

*Italic Text*

> Put a nice, beautiful
> quote here...

~~Strike Through~~

---

```
code    // Inline Code
pre     // Code Block with language based highlighting.
```
`Inline Code Snippet`

```javascript
var message = "Code Block";
alert( message );
```

```
a      // Anchor
img    // Image
```
[Link Title](Link)

![Puppies are cute](https://c1.staticflickr.com/5/4112/5170590074_714d36db83_b.jpg)

```
ol       // Ordered List
ul       // Unordered List
table    // Table
```

1. First Item
2. Second Item
3. Third Item


- I
- Love
- Markdown

| Column 1 | Column 2 |
| ------------- | ------------- |
| Cell 1-1 | Cell 1-2 |
| Cell 2-1 | Cell 2-2 |









