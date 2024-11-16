# Notes on nREPL ops

## An Enumeration

The following are some (> 10) nREPL ops:

* add-middleware
* clone
* close
* completions
* describe
* eval
* interrupt
* load-file
* lookup
* ls-middleware
* ls-sessions
* stdin
* swap-middleware

## Another Attempt at an Enumeration

Being presented with the above list might not have been particularly
helpful, the following seemed a bit better:

* bare minimum
  * clone - name a bit misleading as this is also used for a new session
  * eval

* capabilities
  * describe - if capability discovery is needed

* session management
  * close - if cleanup of sessions are needed
  * ls-sessions - if reconnecting is needed

* reference
  * completions
  * lookup

* evaluation
  * interrupt - may not be practical depending on runtime characteristics
  * load-file
  * stdin - if supporting "input" from user is needed

* extension management
  * add-middleware
  * ls-middleware
  * swap-middleware

## Subsets of Ops

Based on examining [a number of server implementations](servers.md), it appears that
there exist useful subsets of the ops.

It seems possible that just implementing `clone` and `eval` might be
enough for something useful.  Might make sense to include `describe`
as well.  If any other ops are to be implemented, it seems like one
would want to have `describe` so that clients can discover what is
provided by a server.

If managing of sessions is desired (e.g. to clean up older sessions),
implementing both `close` and `ls-sessions` seems reasonable.

If editor-related functionality is desired, `completions` and/or
`lookup` seem like good things to implement.

For more evaluation-related capabilities, `load-file` and/or `stdin`
might be nice to have.  In theory, `interrupt` sounds good, but in
practice, it may be difficult for various runtimes to support this
properly.

It's unclear how useful middleware might be generally speaking, but if
that is desired in a dynamic fashion (so not pre-determined at
startup), at least `add-middleware` and `ls-middleware` seem good to
have.  For more advanced capabilities, one might also want
`swap-middleware`, but on the surface it seems like many use cases
could be covered without it (might be nice for development /
investigation?).

## Ops Naming

It seems that there are some "non-standard" op names in use.  If there
are to be extensions to nREPL, may be it would be nicer to "namespace"
op names that are not "standard" to prevent collisions or "using up"
of nice names for common use.  This seems tricky though beecause can
one really say there is a standard...

## Implementation-Independent Information

So far, haven't had much luck finding documentation that isn't tied
closely to a specific implementation.  For now, relying on the existing
implementations seems to be better than nothing.

