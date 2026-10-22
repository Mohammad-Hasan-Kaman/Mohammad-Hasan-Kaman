# Contributing

This repository holds the GitHub profile README for
[github.com/Mohammad-Hasan-Kaman](https://github.com/Mohammad-Hasan-Kaman).

## What belongs here

- The profile README — the page GitHub renders on the profile itself.
- A `CHANGELOG.md` recording what changed in the profile, so the history of the
  published page is reviewable.

## Development setup

```bash
git clone https://github.com/Mohammad-Hasan-Kaman/Mohammad-Hasan-Kaman.git
cd Mohammad-Hasan-Kaman
```

The repository is Markdown only — there is nothing to build or install.

## Making a change

1. Create a branch from `main`:

   ```bash
   git checkout -b feature/short-description
   ```

2. Edit the README, then commit with a clear message:

   ```bash
   git add -A
   git commit -m "docs: describe the change in one line"
   ```

3. Push and open a pull request:

   ```bash
   git push -u origin feature/short-description
   ```

## Commit message format

Use the conventional prefixes, in the past tense:

| Prefix | Use it for |
| --- | --- |
| `feat:` | A new feature. |
| `fix:` | A bug fix. |
| `docs:` | Documentation only. |
| `refactor:` | A change that neither fixes a bug nor adds a feature. |
| `chore:` | Build, dependency or housekeeping changes. |
| `test:` | Adding or correcting tests. |

## Pull request checklist

- [ ] Every claim in the README is verifiable — check it against the source
      repository or the live API, not against a draft.
- [ ] Every repository link, badge and download URL resolves.
- [ ] No credentials, tokens, `.env` files or local machine paths are committed.
- [ ] The diff contains only the files this pull request is meant to change.

## Keeping the profile accurate

The profile lists public repositories, so it goes stale on its own. Before a
change lands, re-check:

- the live repository list, star counts and the flagship ordering;
- the language byte totals behind the language badge;
- every release asset that is linked.

## License

By contributing you agree that your contribution is licensed under the
[MIT License](LICENSE) of this repository.
