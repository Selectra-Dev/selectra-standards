Markdown
=

This document contains the common standards for all the [markdown](https://daringfireball.net/projects/markdown/) files we create.

# Table of contents

1. [Naming convention](#naming-convention.)

2. [Contents](#contents)

# Naming convention

- **MUST** use `UPPERCASE` file names

    > They're easier to find among other files in the directory tree.

- **MUST** use underscores (`_`) to separate words in the file name

    > This improves readability.

# Contents

- **MUST** begin document with its title - use a **single** equal sign (`=`)

    > Most of the times it's humanized file name (without underscores), but sometimes might be extended abbreviation (for example file name is `PHP.md` but the title is `PHP Hypertext Preprocessor`).

- **SHOULD** contain brief description under the title

    > It's used to indicate what reader can find in it.

- **SHOULD** contain `TOC` (_table of contents_)

    > Sometimes, document isn't typical documentation or doesn't contain more than one chapter. In such case `TOC` can be skipped.

- **MUST NOT** contain any trailing spaces

    > It might be useful to use regular expression replacement in shell by running `sed -i -r 's/\ {1,}$//' FILE.md`.

- Every sentence **MUST** be ended with comma (`.`)

- Titles and list items **MUST NOT** be ended with comma (`.`)

- **MUST** use numbers (ended with comma, for example `1.` or `1.1.`) or hyphen-minus (`-`)

    > Preferably, on the same list, they shouldn't mix.

- **MUST** end with a **single** blank line
