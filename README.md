# Standard Commit Format

**Standard Commit Format** is a git commit message format that I utilize when commiting to repositories of my own and others, unless otherwise stated in the projects Contributing guide. Since I commonly re-use this, I've decided to make a dedicated location for its existance and simply link to this document as a reference.

## Message Format

Each commit message consists of a **header**, a **body** and a **footer**.  The header has a special
format that includes a **type**, a **scope** and a **subject**:

```
<type>(<scope>): <subject>
<BLANK LINE>
<body>
<BLANK LINE>
<footer>
```

The **header** is mandatory and the **scope** of the header is optional.

Any line of the commit message **cannot** be longer **100 characters**! This allows the message to be easier
to read on GitHub as well as in various git tools.

### Reverts

If the commit reverts a previous commit, it should begin with `revert: `, followed by the header of the reverted commit. In the body it should say: `This reverts commit <hash>.`, where the `hash` is the SHA of the commit being reverted.

### Message Header

#### Type
Must be one of the following:

* **feat**: A new feature
* **fix**: A bug fix
* **docs**: Documentation only changes
* **style**: Changes that do not affect the meaning of the code (white-space, formatting, missing
  semi-colons, etc)
* **refactor**: A code change that neither fixes a bug nor adds a feature
* **perf**: A code change that improves performance
* **test**: Adding missing tests
* **revert**: Reverting to previous commit, see [Reverts](#reverts)
* **misc**: Anything that falls outside of the other types.

##### When not to use a type:

- Version Bumps (Avoiding version bumps within release logs)
- Merges

#### Scope

Area inside repository of which the commit modifies or is related to.

#### Subject

The subject contains succinct description<sup>[1][1]</sup> of the change:

* use the imperative, present tense: "change" not "changed" nor "changes"
* don't capitalize first letter
* no dot (.) at the end

### Message Body

Just as in the **subject**, use the imperative, present tense: "change" not "changed" nor "changes".
The body should include the motivation for the change and contrast this with previous behavior.

### Message Footer

The footer should contain any information about **Breaking Changes** and **Referencing issues**.


#### Referencing issues

Issues should be listed on a separate line in the footer prefixed with `Closes` or `See` keyword like this:

```
Closes #234
```

or in case of multiple issues:

```
See #123, #245, #992
```

#### Breaking Changes

All breaking changes have to be mentioned as a breaking change block in the footer, which should start with the word `BREAKING CHANGE:` with a space or two newlines. The rest of the commit message is then the description of the change, justification and migration notes.

##### Example

```
BREAKING CHANGE: Api columns now return two new values

- Value1
- Value2
```
