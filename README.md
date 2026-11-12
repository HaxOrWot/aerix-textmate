# aerix-textmate

Official **TextMate grammar** (`source.aerix`) for the **[Aerix Programming Language](https://github.com/HaxOrWot/AerixLang)** (`.arx`), packaged cleanly under the MIT License for **GitHub Linguist** submodule integration and TextMate-compatible editors.

## Contents
- `syntaxes/aerix.tmLanguage.json` — TextMate grammar (`scopeName: source.aerix`, `fileTypes: ["arx"]`)
- `language-configuration.json` — Comment, bracket, and auto-closing pairs configuration
- `package.json` — Standard grammar contribution manifest (`contributes.languages` & `contributes.grammars`)
- `samples/showcase.arx` — Representative `.arx` sample for grammar highlighting validation
- `LICENSE` — MIT License

## Submitting to `github-linguist/linguist` (When Ecosystem Criteria Are Met)

Per [`github-linguist/linguist` CONTRIBUTING.md](https://github.com/github-linguist/linguist/blob/main/CONTRIBUTING.md), new source extensions (`.arx`) require at least **2,000 indexed `.arx` files** across unique public non-fork GitHub repositories within the last year before opening a Linguist PR.

Once `.arx` meets that adoption threshold:

1. Fork & clone `github-linguist/linguist`.
2. Register this repository as a grammar submodule:
   ```bash
   script/add-grammar https://github.com/HaxOrWot/aerix-textmate.git
   ```
3. Add `Aerix` to `lib/linguist/languages.yml`:
   ```yaml
   Aerix:
     type: programming
     color: "#00DCFF"
     extensions:
       - .arx
     tm_scope: source.aerix
     ace_mode: text
   ```
4. Add a sample `.arx` file under `samples/Aerix/` in Linguist, run `bundle exec rake test`, and submit the PR with the GitHub Code Search query proving adoption.
