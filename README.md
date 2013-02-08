Heroku buildpack: Dereference symlinks from component
=====================================================

Since heroku builds in a temporary directory and moves it to `/app` symlinks break unless you resolve them.

This buildpack will dereference all of the symlinks in `./build`, which is the default output directory of [component](https://github.com/component/component).