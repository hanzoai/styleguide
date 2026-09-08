# Whitespace

*What every language in the estate is indented with, and who decides it*

A file that arrives with the wrong width shows up as whole-file noise in a diff, burying
the change that was actually made. That is the whole reason this page exists: not taste,
but that a reviewer should be able to see what changed.

## Table of Contents

  1. [The widths](#the-widths)
  1. [The formatter decides where there is one](#the-formatter-decides)
  1. [An existing file wins](#an-existing-file-wins)
  1. [Endings and trailing space](#endings)

## The widths

  <a name="the-widths"></a><a name="1.1"></a>
  - [1.1](#the-widths) **Indentation width**, by language. These are what the estate is
    already written in — counted across the tree, not chosen here:

    | Language | Indent | Decided by |
    |---|---|---|
    | Go | tab | `gofmt` |
    | TypeScript, JavaScript, JSX, TSX | 2 spaces | this guide |
    | Python | 4 spaces | PEP 8 |
    | Shell | 2 spaces | this guide |
    | YAML, JSON | 2 spaces | this guide |
    | Rust | 4 spaces | `rustfmt` |
    | Makefile | tab | make requires it |

    ```typescript
    const routes = {
      users: '/v1/users',
      orgs: '/v1/orgs',
    }
    ```

    ```python
    def routes():
        return {
            "users": "/v1/users",
        }
    ```

  <a name="the-widths--why-two"></a><a name="1.2"></a>
  - [1.2](#the-widths--why-two) **Why two and not four** for the curly-brace languages:
    they nest deeply — a component inside a provider inside a router — and four spaces
    spends the line on the left margin. Python does not nest that way and reads better
    with four, which is also what every Python tool assumes.

## The formatter decides where there is one

  <a name="the-formatter-decides"></a><a name="2.1"></a>
  - [2.1](#the-formatter-decides) **Where a language has a canonical formatter, it decides
    and this page only records what it does.** `gofmt` indents Go with tabs; there is no
    setting and no discussion. `rustfmt` does the same for Rust. A guide that disagreed
    with them would only be a guide people have to remember to ignore.

  <a name="the-formatter-decides--run-it"></a><a name="2.2"></a>
  - [2.2](#the-formatter-decides--run-it) **Run the formatter rather than matching it by
    hand.** `gofmt -l` naming a file is the same information as a review comment, and it
    arrives before the review.

## An existing file wins

  <a name="an-existing-file-wins"></a><a name="3.1"></a>
  - [3.1](#an-existing-file-wins) **When editing, match the file you are in.** A file with
    two widths in it is worse than a file with the wrong one: the first is unreadable, the
    second is merely not our style.

  <a name="an-existing-file-wins--reformat-alone"></a><a name="3.2"></a>
  - [3.2](#an-existing-file-wins--reformat-alone) **Reformat in a commit of its own.** A
    change of substance hidden inside a reindentation cannot be reviewed, and that is
    exactly when a mistake gets through.

## Endings and trailing space

  <a name="endings"></a><a name="4.1"></a>
  - [4.1](#endings) **LF, and a newline at the end of the file.** A missing final newline
    makes the last line show as changed the next time anyone touches it.

  <a name="endings--trailing"></a><a name="4.2"></a>
  - [4.2](#endings--trailing) **No trailing whitespace**, with one exception: inside a
    Markdown paragraph two trailing spaces are a line break, so leave those alone.
