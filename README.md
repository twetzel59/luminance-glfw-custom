# luminance-glfw

## Legal Notice

This repository is free and open source software. It is a **derivative work not promoted or endorsed by its original author.**

## What this is

*NOTE*: This is almost entirely the work of [phaazon](https://github.com/phaazon), not me.
This is a *partial fork* of: https://github.com/phaazon/luminance-rs.

Originally, I had forked ``luminance-glfw`` when it was its own crate. phaazon later reorganized the structure of the ``luminance-rs`` repository to be a ``workspace`` containing ``luminance-glfw`` as one of its library crates. I've downloaded the files I needed from that crate within the workspace.

## So what is this even for, then?

I want to use ``luminance-rs`` for a game. However, ``luminance-rs`` is lightweight and lacks a few features that my game will need. Some of those features include:
* **Direct inputs:** Events are great for resizes, text input, and mouse clicks. But, for real-time input I need to check the immediate state of the keys.
* **Window control:** I need to be able to dynamically show/hide the cursor*, or dynamically switch between fullscreen and windowed modes.

*I opened [an issue](https://github.com/phaazon/luminance-rs/issues/124) about this.

This crate will contain an escape hatch to GLFW, which will allow me to accomplish what I need for now. If ``luminance-glfw`` eventually adds the features I need, I'll switch back to the stock version. That said, my goals are potentially different from the normal use case of ``luminance-rs``, so it may be more appropriate to maintain my own windowing wrapper anyway.
