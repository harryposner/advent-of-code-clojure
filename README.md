# Advent of Code Clojure template

This is a project template for solutions for [Advent of
Code](https://adventofcode.com/) in Clojure.

## Instructions

1. [Copy this
   template](https://github.com/harryposner/advent-of-code-clojure/generate) to
   make your own repo.

2. [Install Clojure and the Clojure
   CLI](https://clojure.org/guides/install_clojure).  If you have Nix, you can
   run `nix develop` to get a dev shell.

3. Get an editor with nREPL integration and paredit.  The classic choice is
   emacs with [CIDER](https://cider.mx/), but VSCode with
   [Calva](https://calva.io/) is the most beginner-friendly.  I use Neovim with
   [Conjure](https://github.com/Olical/conjure),
   [vim-sexp](https://github.com/guns/vim-sexp), [vim-sexp mappings for regular
   people](https://github.com/tpope/vim-sexp-mappings-for-regular-people), and
   [rainbow parentheses](https://github.com/HiPhish/rainbow-delimiters.nvim).

4. Start the REPL by running `clj -M:repl` in this directory.  You should see
   it print `nREPL server started on port 5555 on host localhost -
   nrepl://localhost:5555`.

5. Connect to the nREPL server from your editor.
    - CIDER: [`M-x
      cider-connect`](https://docs.cider.mx/cider/basics/up_and_running.html#connect-to-a-running-nrepl-server).
      Tell it to connect to localhost port 5555 when prompted.
    - [Calva](https://calva.io/connect/#connecting-without-jack-in): Run the
      command "Connect to a running REPL server in the project" (Ctrl + Alt +
      C, Ctrl + Alt + C) and choose deps.edn from the project type dropdown. It
      should connect here--- if it fails, you'll need to explicitly tell it to
      connect to `localhost:5555`
    - [Conjure](https://github.com/Olical/conjure/wiki/Quick-start:-Clojure):
      Open `src/advent/core.clj`.  You should see a floating window pop up that
      says `localhost:5555 (connected)`.  If you don't, you can run
      `:ConjureConnect 5555`.

6. Open `src/advent/core.clj` and run `(scaffold YEAR DAY)` for the year and
   day you want to set up.  There's an example in the comment block at the
   bottom of the file.  This is a common pattern in Clojure codebases---
   comment blocks will have snippets that you can send to the REPL.  To send a
   form from an editor buffer to the REPL, put your cursor over the form and
   use the following keyboard shortcut:
    - CIDER: `C-c C-e`
    - Calva: `Ctrl + Enter`
    - Conjure: `<localleader>ee`

   `advent.core/scaffold` will create a Clojure file at
   `src/advent/y$YEAR/day_$DAY.clj` and an empty file for example data at
   `resources/examples/$YEAR/$DAY.txt`.
