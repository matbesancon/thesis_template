# LaTeX template for cotutelle (double PhD programs)

This is my template for a PhD thesis written for a cotutelle.
Since universities have various and conflicting requirements, I adapted
the initial template from Polytechnique Montreal to be able to build
two documents, one for Polytechnique Montréal and one for Centrale Lille.

The initial readme (mostly in French) from Polytechnique Montréal is also available LISEZMOI.txt.

## Building

The template works on Linux with latexmk or the provided Makefile with the make command.
It should work on other platforms with your favourite toolchain.
If you are using [Atom](https://atom.io), adding
```
% !TEX root = Document.tex
```
at the beginning of a file to be able to compile Document.tex on save.

## Important variable settings

Most variables are defined in `0-Definitions_Etudiant.tex`.
Two important ones are set in `Document.tex`, the thesis language (French or English)
and the School. If the school is set as `centrale`:
- `pagegarde_centrale.tex` is the first page;
- the abstracts will appear at the end of the thesis on a single page in a compact version (single paragraph).

If the school is set to anything else, the template used will be Polytechnique Montreal:
- `Pagegarde.tex` will be used as first page and second page, with the jury defined with the custom commands;
- The abstract will appear after the second page, with each abstract on its own new page in an extended version.

## The abstracts situation

Because Centrale Lille required abstracts in a compact way and Polytechnique in
a more extended style, I defined a command `\clinebreak` which is a line break
and new paragraph when building with `school = polytechnique`  and is equivalent
to doing nothing when building with `school = centrale`.

## Licensing

The project is MPL-licensed as the template from Polytechnique Montréal.

Good luck with the thesis writing, you got this.
