Return to [README](../README.md) \
Return to [skill tree](skill_tree.md)

# Advanced Git Exercise

## Configure git locally

Set gits "core" editor to your editor of choice. I have chosen Vim below.
`git config --global core.editor "vim"`

### If you are using Vim you can add the below lines to your .vimrc file to 
enforce the commit conventions discussed in a later section.
```
" Force the cursor onto a new line after 80 characters
set textwidth=80
" However, in Git commit messages, let’s make it 72 characters
autocmd FileType gitcommit set textwidth=72
" Colour the 81st (or 73rd) column so that we don’t type over our limit
set colorcolumn=+1
" In Git commit messages, also colour the 51st column (for titles)
autocmd FileType gitcommit set colorcolumn+=51
```

## Branching strategy

We use a parallel 'develop' branch for staging changes and annotated tags for 
[semantic versioning](https://semver.org/spec/v2.0.0.html)

`git tag -a v1.0.1 <commit>`

Follow the commit message conventions outlined below to annotate your tags.

## Commit Messages

An excellent source of insight into what commit messages are for and why commit
conventions matter. https://cbea.ms/git-commit/

We follow a simplified commit convention based off the popular Angular commit 
[convention](https://github.com/angular/angular/blob/main/CONTRIBUTING.md#commit)
https://www.conventionalcommits.org/en/v1.0.0/

From the root of this repository run the following command to configure this
projects commit template.
`git config --global commit.template ${PWD}/.git-commit-template`

Here is a lengthy example of a properly formatted commit message

```
feat(docs): Add 50 char subject in imperative mood

More detailed explanatory text, if necessary. Wrap it to about 72
characters or so. In some contexts, the first line is treated as the
subject of the commit and the rest of the text as the body. The
blank line separating the summary from the body is critical (unless
you omit the body entirely); various tools like `log`, `shortlog`
and `rebase` can get confused if you run the two together.

Explain the problem that this commit is solving. Focus on why you
are making this change as opposed to how (the code explains that).
Are there side effects or other unintuitive consequences of this
change? Here's the place to explain them.

Further paragraphs come after blank lines.

 - Bullet points are okay, too

 - Typically a hyphen or asterisk is used for the bullet, preceded
   by a single space, with blank lines in between, but conventions
   vary here

If you use an issue tracker, put references to them at the bottom,
like this:

Resolves: #123
See also: #456, #789
```

Configure [commitlint](https://commitlint.js.org/) locally or as a commit hook.

https://github.com/semantic-release/semantic-release
