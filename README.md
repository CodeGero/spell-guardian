# Spell Guardian

Check spelling in code comments, documentation, and markdown before they merge.

## What it does
Runs [codespell](https://github.com/codespell-project/codespell) over the target path and reports typos. Fails the workflow when `fail-on-error` is true and misspellings are found.

## Usage
```yaml
- uses: CodeGero/spell-guardian@v1
  with:
    path: '.'
    fail-on-error: 'false'
    ignore-words: 'crate,ser,ba,fo,te,ot'
```

## Inputs
| Input | Required | Default | Description |
|---|---|---|---|
| `path` | no | `.` | Directory or file to check. |
| `fail-on-error` | no | `false` | Fail the workflow on spelling errors. |
| `ignore-words` | no | `''` | Comma-separated words to skip. |

## Custom dictionary
Maintain a project wordlist and pass it via `ignore-words`, or commit a `.codespellrc`/wordlist file in the repo.

## License
MIT — free to use. Premium support via [Gumroad](https://kryptorious.gumroad.com/l/jbvet).
