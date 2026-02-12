Hi
i am shiva

## GitHub Actions automation

- `CI Pipeline` runs pytest on every push or pull request against `main`.
- When tests pass on `main`, the deploy job copies `shiva.html` into `site/` and publishes only that folder to the `gh-pages` branch via `peaceiris/actions-gh-pages`.
- Manual rollbacks are available through the same workflow: use the **Run workflow** button, set `rollback_steps` (defaults to `1` for the previous deploy), and the job will force-push the earlier commit back to `gh-pages`.

Follow the Actions tab to see deployments or to initiate a rollback without touching the command line.
