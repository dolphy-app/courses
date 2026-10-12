# Contributing a course

Each top-level directory is a course in the KnowledgeBase format (`course_manifest.json`, `<lesson>.lesson/` directories). New courses and fixes to existing ones are welcome as pull requests; CI validates every change.

## Validate

With the monorepo of Dolphy checked out:

```sh
pnpm -F @dolphy-app/engine engine-cli validate <path-to-this-repo> --run-checks --extensions <dolphy>/apps/desktop/extensions
```

CI (`.github/workflows/validate.yml`) does the same on every push and pull request to `main`: it builds `engine-cli` and
the exercise-type extensions from [dolphy-app/dolphy](https://github.com/dolphy-app/dolphy), validates every course and
runs every reference solution. Any error, any warning (for example an exercise type that no extension provides) or a
failing reference solution fails the check; problems are annotated on the offending file and line. The workflow can be
started by hand with a different `dolphy-ref` (tag, branch or commit).

## Exercise format

`dolphy.js` exercises keep the tests and the reference solution inside the exercise front matter, so a course works
wherever the repository is mounted:

```yaml
---
engine:
  exercise:
    type: dolphy.js
    spec:
      starter: |
        function sum(a, b) {}
      tests: |
        test('adds numbers', () => assert.equal(sum(1, 2), 3));
      reference: |
        function sum(a, b) { return a + b; }
---
Write `sum(a, b)`.
```

Available in `tests`: `test(name, fn)`, `assert` (`node:assert/strict`), `logs` (the learner's `console.log` lines),
`sleep(ms)`. Learner code and tests run in a fresh Node.js `vm` context with a timeout.
