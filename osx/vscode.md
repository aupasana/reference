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

## Other

A zsh function to open a workspace, and navigate to a file in the workspace

```zsh
function vscode-notes {
    code ~/vscode/notes.code-workspace ~/notes/home.md
}

alias notes=vscode-notes
```
