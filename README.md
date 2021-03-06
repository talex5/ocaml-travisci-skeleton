## Travis CI skeleton for OCaml projects

1. Create an `opam` file at the root of your project. If you use opam
   1.2, you can simply do `opam pin add PKG .` -- this will open an
   editor and propose you a template.

2. Copy `.travis.yml` at the root of your project.

3. Enable Travis runs on
   `https://travis-ci.org/profile/<YOURGITHUBID>` (sign in with your
   Github account and click on `+` on top of the left pane).

4. (optional) If you want to support multiple OCaml versions, update
   `.travis.yml` to add some of the following lines (by default, the
    file contains only the line with `OCAML_VERSION=latest`):

    ````
  - OCAML_VERSION=3.12
  - OCAML_VERSION=4.00
  - OCAML_VERSION=4.01
  - OCAML_VERSION=4.02
  - OCAML_VERSION=latest
    ````

5. (optional) Set `PACKAGE=<name of your package>`. By default, the script will use `my-package` as package name, which might not be what you want if your tests consist of installing reverse dependencies.
