# Contributing

Thanks for helping. Keep changes small and proven.

## Before you open a pull request

1. Run the tests and the checks — all three must be clean:

   ```sh
   cd commandcode
   go test ./...
   go vet ./...
   gofmt -l .
   ```

2. Add or update a test for anything you change. The tests replay real `cmd`
   recordings, so a fix usually means adding a line to a fixture and asserting
   the event it should produce.

3. Keep it in scope. The harness is the only thing that should change here. The
   Docker Agent side is a five-line wiring patch and stays that way.

## Sign your commits (DCO)

Every commit needs a sign-off line. It is not a contract — it just states that
you wrote the change (or have the right to send it) and you are contributing it
under this project's license (MIT).

Add it automatically:

```sh
git commit -s -m "your message"
```

That appends a line like:

```
Signed-off-by: Your Name <you@example.com>
```

If you forget, `git commit --amend -s` on the last commit fixes it.

## Style

- Match the surrounding code — the other harness packages are the reference.
- Comments only where the code is not self-evident.
- Plain commit messages, one logical change each.

## Conduct

By participating you agree to [`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md).
