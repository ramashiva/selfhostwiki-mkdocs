# The Git repo for the [Self-host Wiki](https://escargot.tech/selfhost/) (formerly selfhostwiki.neocities.org)

This wiki is written in MultiMarkdown and converted to HTML using Pandoc.

Example usage:

```bash
# Convert a single file:
pandoc -c ./style.css -B ./navbar.html -f markdown_mmd -t html ./index.md -o ./selfhostwiki_html/index.html
```
OR

Convert the entire folder using the [conversion script](convert_pandoc.sh):
```bash
./convert_pandoc.sh
```
