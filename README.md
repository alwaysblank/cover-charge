# Cover Charge

Force people to do something (i.e. sign up for a newsletter) before they can 
access something (i.e. a page, a download, etc), *but* store a cookie to
authenticate them for future requests for 

1) that thing
2) (optionally) other, similar things

## Planning

I have a couple major goals:

- Redirection and blocking should operate without JavaScript (ideally all
server-side).
- Cookies (or other auth storage) should be set only *as-needed*, to optimize
network performance and simplicity. i.e. Set a cookie on the url of an item,
or on a "higher" url to apply to everything below it, but *don't* set a cookie
on the root domain.
- Provide the simplest possible implementation: The intent is that this package
can be transparently added to any project, and then built on top of. This means
it should be an unopinionated as possible, and provide as little styling as
possible (ideally none).
