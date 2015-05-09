---
title: Getting started with servant
author: Alp Mestanogullari
toc: true
---

This is an introductory tutorial to the current version of *servant*, which is **0.4**. Any comment or issue can be directed to [this website's issue tracker](http://github.com/haskell-servant/haskell-servant.github.io/issues).

# Introduction

*servant* has the following guiding principles:

- concision

   This is a pretty wide-ranging principle. You should be able to get nice
   documentation for you web servers, and client libraries, without repeating
   yourself. You should not have to manualy serialize and deserialize your
   resources, but only delcare how to do those things *once per type*. If a
   bunch of your handlers take the same query parameters, you shouldn't have to
   repeat that logic for each handler, but instead just "apply" it to all of
   them at once. Your handlers shouldn't be where composition goes to die. And
   so on

- flexibility

   If we haven't thought of your use case, it should still be easily
   achievable. If you want to use templating library X, go ahead. Forms? Do
   them however you want, but without difficulty. We're not opinionated.

- separatation of concerns

   Your handlers and your HTTP logic should be separate. True to the philosphy
   at the core of HTTP and REST, with *servant* your handlers return normal
   Haskell datatypes - that's the resource. And then from a description of your
   API, *servant* handles the *presentation* (i.e., the Content-Types). But
   that's just one example.

- type safety

   Want to be sure your API meets a specification? Your compiler can check
   that for you. Links you can be sure exist? You got it.

To stick true to these principles, we do things a little differently than you
might expect. The core idea is *reifying the description of your API*. Once
reified, everything follows. We think we might be the first web framework to
reify API descriptions in an extensible way. We're pretty sure we're the first
to reify it as *types*.

To be able to write a webservice you only need to read the first two sections,
but the goal of this document being to get you started with servant, we also
cover the couple of ways you can extend servant for a great good.

# Tutorial

## [A web API as a type](/tutorial/api-type.html)
## [Serving an API](/tutorial/server.html)
## [Deriving Haskell functions to query an API](/tutorial/client.html)
## [Generating javascript functions to query an API](/tutorial/javascript.html)
## [Generating documentation for APIs](/tutorial/docs.html)

# Links, community and more

## Hackage links

- [servant](http://hackage.haskell.org/package/servant)
- [servant-server](http://hackage.haskell.org/package/servant-server)
- [servant-lucid](http://hackage.haskell.org/package/servant-lucid)
- [servant-blaze](http://hackage.haskell.org/package/servant-blaze)
- [servant-client](http://hackage.haskell.org/package/servant-client)
- [servant-docs](http://hackage.haskell.org/package/servant-docs)
- [servant-jquery](http://hackage.haskell.org/package/servant-jquery)

## Community

- [Mailing list](https://groups.google.com/forum/#!forum/haskell-servant)
- Join us on IRC: **#servant** on *irc.freenode.net*

## Github

- the servant packages: [haskell-servant/servant](https://github.com/haskell-servant/servant)
- the website (including this tutorial): [haskell-servant/haskell-servant.github.io](https://github.com/haskell-servant/haskell-servant.github.io/hakyll/tree)
- Feel free to use the issue tracker (or to send PRs!) on the website's repository to give feedback and suggestions about this tutorial

Thanks for reading!