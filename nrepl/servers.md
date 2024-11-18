# Servers

The following are some implementations of nREPL servers along with
which ops appear to be implemented.

## Clojure

* [babashka.nrepl](https://github.com/babashka/babashka.nrepl) -
  babashka's nrepl server
  * standard ops
    * clone
    * close
    * describe
    * eval
    * load-file
    * ls-sessions
  * non-standard ops
    * complete
    * eldoc
    * info
    * ns-list
* [nrepl-cljs](https://github.com/djblue/nrepl-cljs) - initial nrepl
  bits (client and server) for bootstrapped cljs by djblue
  * standard ops
    * clone
    * describe
    * eval
  * non-standard ops
    * info
* [nrepl-server](https://github.com/borkdude/nrepl-server) -
  borkdude's prototype
  * standard ops
    * clone
    * describe
    * eval

## Non-Clojure

* [cl-nrepl](https://github.com/sjl/cl-nrepl) - for common lisp by sjl
  * standard ops
    * clone
    * close
    * describe
    * eval
    * load-file
    * ls-sessions
  * non-standard ops
    * arglist
    * documentation
    * macroexpand
* [jeejah](https://gitlab.com/technomancy/jeejah) - for fennel by
  technomancy
  * standard ops
    * clone
    * close
    * completions
    * describe
    * eval
    * interrupt - silently ignored
    * load-file
    * lookup
    * ls-sessions
    * stdin
  * non-standard ops
    * complete
* [HyREPL](https://github.com/allison-casey/HyREPL) - for Hy by
  allison-casey (no eval...)
  * standard ops
    * clone
    * close
    * describe
    * ls-sessions
    * stdin
  * non-standard ops
    * client.init
* [nrepl-cljs-sci](https://github.com/viesti/nrepl-cljs-sci) - for
  nodejs by viesti
  * standard ops
    * clone
    * close
    * describe
    * eval
    * load-file
* [nrepl-lazuli](https://gitlab.com/clj-editors/nrepl-lazuli) - for
  ruby by mauricioszabo
  * standard ops
    * clone
    * describe
    * eval
    * interrupt
  * non-standard ops
    * eval_pause
    * eval_resume
    * get_watches
    * last_exception
    * unwatch
    * update_watch_lines
    * watches_for_file
* [nrepl-ruby](https://github.com/delonnewman/nrepl-ruby) - for ruby
  by delonnewman
  * standard ops
    * clone
    * describe
    * eval
* [ogion](https://gitlab.com/technomancy/ogion) - for racket by
  technomancy
  * standard ops
    * clone
    * eval
* [python-nrepl](https://gitlab.com/sasanidas/python-nrepl) - for
  python by sasanidas
  * standard ops
    * clone
    * completions
    * describe
    * eval
    * load-file
    * ls-sessions
* [R-nREPL](https://github.com/vspinu/R-nREPL) - for r by vspinu
  * standard ops
    * clone
    * close
    * describe
    * eval
    * ls-sessions
* [ruby-nrepl-server](https://github.com/chrisblatchley/ruby-nrepl-server) -
  for ruby by chrisblatchley (abandoned?)
  * standard ops
    * clone
    * eval

