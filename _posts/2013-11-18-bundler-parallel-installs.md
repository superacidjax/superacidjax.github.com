---
layout: post
title: "Bundler Parallel Installs"
description: "How to parallel bundle in Bundler 1.5"
category: "Rails"
tags : [rails, bundler, tutorial]
---
{% include JB/setup %}

The new Bundler version [1.5.0.rc.1](http://bundler.io/v1.5/whats_new.html)
is awesome. One of the cool new features is
the ability to bundle install in parallel. Which means you can speed up your
bundling by up to 60% over the previous version of bundler.

## Parallel Installs

First you need to install the new version of bundler. Since it's a pre-release,
you'll need to install it like this:

```gem install bundler --pre```

Next you'll need to use the --jobs option like this:

```bundle install -j4```

This specifies that 4 workers will be used to complete the bundle process.

To always use it this way you can run this:

```bundle config --global jobs 4```

And that's it! Happy bundling.