# Working on this Backbone snapshot

`backbone.js` is the library, `test/` contains browser/CoffeeScript tests,
`examples/` demonstrates integrations, and `docs/` contains generated/reference
pages. This is version 0.5.3; preserve its API and legacy JavaScript conventions.

`npm install` resolves the declared Underscore dependency. There are no npm
scripts. Open `test/test.html` for the browser suite. `rake test` invokes CoffeeScript
integration tests and requires `coffee`; it is not the complete browser suite.
`rake lint` invokes the external `jsl` tool with `docs/jsl.conf`.

`rake build` needs Ruby and closure-compiler and writes `backbone-min.js`;
`rake doc` requires Docco and rewrites docs. Rake tasks use shell calls and may
not reliably propagate a failed tool exit, so inspect actual output and run the
underlying command directly when establishing a pass. No typecheck task exists.

## Completing changes

Follow existing patterns and carry authorized work through the relevant checks,
repairing failures caused by the change. Choose routine implementation details
directly; ask only when missing information materially changes scope or outcome.
For documentation-only edits, check the diff, referenced paths, and command
accuracy rather than starting application runtimes. If a prerequisite blocks a
check, report the exact blocker and continue independent authorized work. Close
with changed paths, checks actually run and results, and remaining unverified
behavior; distinguish commands inspected from commands executed.
