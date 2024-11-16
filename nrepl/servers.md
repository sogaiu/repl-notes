# Servers

## Clojure

The following are some implementations that support some nREPL ops.

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
* [nrepl-lazuli](https://gitlab.com/clj-editors/nrepl-lazuli) - nrepl
  server for ruby by mauricioszabo
  * standard ops
    * clone
    * describe
    * eval
    * interrupt
    * load-file
    * ls-sessions
  * non-standard ops
    * eval_pause
    * eval_resume
    * get_watches
    * last_exception
    * unwatch
    * update_watch_lines
    * watches_for_file
* [nrepl-server](https://github.com/borkdude/nrepl-server) -
  borkdude's prototype
  * standard ops
    * clone
    * describe
    * eval
* [ogion](https://gitlab.com/technomancy/ogion) - nrepl server for
  racket by technomancy
  * standard ops
    * clone
    * eval

## Non-Clojure

* [cl-nrepl](https://github.com/sjl/cl-nrepl)
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
* [jeejah](https://gitlab.com/technomancy/jeejah)
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
* [HyREPL](https://github.com/allison-casey/HyREPL) - no eval...
  * standard ops
    * clone
    * close
    * describe
    * ls-sessions
    * stdin
  * non-standard ops
    * client.init
* [nrepl-cljs-sci](https://github.com/viesti/nrepl-cljs-sci)
  * standard ops
    * clone
    * close
    * describe
    * eval
    * load-file
* [nrepl-ruby](https://github.com/delonnewman/nrepl-ruby)
  * standard ops
    * clone
    * describe
    * eval
* [python-nrepl](https://gitlab.com/sasanidas/python-nrepl)
  * standard ops
    * clone
    * completions
    * describe
    * eval
    * load-file
    * ls-sessions
* [R-nREPL](https://github.com/vspinu/R-nREPL)
  * standard ops
    * clone
    * close
    * describe
    * eval
    * ls-sessions
* [ruby-nrepl-server](https://github.com/chrisblatchley/ruby-nrepl-server) -
  abandoned?
  * standard ops
    * clone
    * eval

