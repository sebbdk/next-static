---
title: Why this setup?
slug: why-this-setup
author: Sebb
date: 2017-10-3 20:26 PDT
tags:
  - blog
---
## How this blog?

This blog is a static git based blog, meaning there is no database, no serverside script, and no dependencies.
The only requirement for this site is the abillity to server some files.

This keeps the blog clean, simple and secure when it is being served to the web.

Also being gitbased i, and my readers, have revisions on all my changes, since i host on github.

# That sounds dum, dont you need dynamic things?

I have those things, contrary to fx. wordpress that generates them on page-request i have all the options precompiled as static files.

This gives me the benefit of fast pageloads, and few bottlenecks, all i do is serve files.

# But surely you cannot do that with all content?

True, my intention is that things that require too much generation or cannot be precompiled are handled in javascript on the client.
The data for these features will come from 3'rd party services. 

For a blog like this i doubt i will have much of said things however.
For comments, and social interactions can all be handled bu thirdparty services that take the featues out of my hands to maintain.

# Sounds great, what is the catch?

The 'catch' is that i need to run a generator everytime i do changes, and then move the generated files onto the hosting webserver.

There are a number of libraries that help facilitate this today however.

Problably the biggest catch here is that it makes it hard for the none tecknically inclined person to maintain a blog like this.

A proper application could facilitate fixing this however.
It would be a very neat replacement for the horror that is wordpress.
In fact "someone should" make that, i see a huge earning potential here if implemented right.
Think "3'rd party server subscribtions".

## So specificly, how did you make this?

I have choosen to use 'next-static' as my blog setup for now.
Basically i write my articles in markup -which is a generic document format- and then i run a nodejs generator which converts it into html for me.
Next-static then publish directly to github pages, on demand, which is what i am using currently.

Doing that means all i have to do is some DNS magic and blog.sebb.dk is a reality.

This means that setup is really easy from a teckincal perspective. 

The keypoint here is that all my articles are in markup, so migration will always be super easy if i decide to try something else.

# final thoughts
I am still trying out this setup, and changes are bound to happen but i feel very positive towards thi setup/stack.