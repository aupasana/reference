# visual studio code

### Markdown Extensions

#### Markdown All in One

- Id: yzhang.markdown-all-in-one
- Description: All you need to write Markdown (keyboard shortcuts, table of contents, auto preview and more)
- VS Marketplace Link: https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one

#### Paste Image
- Id: mushan.vscode-paste-image
- Description: paste image from clipboard directly
- VS Marketplace Link: https://marketplace.visualstudio.com/items?itemName=mushan.vscode-paste-image

#### markdown-link-expander
- Id: skn0tt.markdown-link-expander
- Description: Easily create pretty Markdown links using its HTML title.
- VS Marketplace Link: https://marketplace.visualstudio.com/items?itemName=skn0tt.markdown-link-expander

#### Foam

- Id: foam.foam-vscode
- Description: VS Code + Markdown + Wikilinks for your note taking and knowledge base
- VS Marketplace Link: https://marketplace.visualstudio.com/items?itemName=foam.foam-vscode

### Markdown diagram extensions

#### Mermaid Markdown Syntax Highlighting

- Id: bpruitt-goddard.mermaid-markdown-syntax-highlighting
- Description: Markdown syntax support for the Mermaid charting language
- VS Marketplace Link: https://marketplace.visualstudio.com/items?itemName=bpruitt-goddard.mermaid-markdown-syntax-highlighting

#### Markdown Preview Mermaid Support

- Id: bierner.markdown-mermaid
- Description: Adds Mermaid diagram and flowchart support to VS Code's builtin markdown preview
- VS Marketplace Link: https://marketplace.visualstudio.com/items?itemName=bierner.markdown-mermaid

#### Draw.io Integration

- Id: hediet.vscode-drawio
- Description: This unofficial extension integrates Draw.io into VS Code.
- VS Marketplace Link: https://marketplace.visualstudio.com/items?itemName=hediet.vscode-drawio

## Preferences

From the command palette, select `Preferences: Open User Settings (JSON)` and insert this snippet

```json
    "pasteImage.showFilePathConfirmInputBox": true,
    "markdown.styles": [
        "https://use.fontawesome.com/releases/v6.1.2/css/all.css"
    ]
```

## Snippets

From the command palette, select `Snippets: Configure User Snippets` --> `markdown.json`

```json
	"Meeting Notes": {
		"prefix": "Meeting Notes",
		"body" : [
			"## Meeting - $CURRENT_DAY_NAME_SHORT $CURRENT_MONTH_NAME_SHORT $CURRENT_DATE @ $CURRENT_HOUR:$CURRENT_MINUTE ",
			"",
			"$1",
			"",
			"### Notes",
			" - ",
			"",
			"### Action Items",
			" - [ ]",
			"",
			"-----",
			""
		]
	}
```

## ZSH

A zsh function to open a workspace, and navigate to a file in the workspace

```zsh
function vscode-notes {
    code ~/vscode/notes.code-workspace ~/notes/home.md
}

alias notes=vscode-notes
```
