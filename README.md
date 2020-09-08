## Packages for svetlanux

It is an http exposed repository available through following links:

* [core](https://svetlanux.github.io/packages/core/) - The core packages set (all base stages built with)
* [xorg](https://svetlanux.github.io/packages/core/) - A minimal set of preinstalled packages to run `i3` with xterm
* [pkg](https://svetlanux.github.io/packages/pkg/) - Everything else

They're could be used with following settings (pkg-get.conf)

```
pkgdir          /var/lib/pkg/core|https://svetlanux.github.io/packages/core/ 
pkgdir          /var/lib/pkg/xorg|https://svetlanux.github.io/packages/xorg/ 
pkgdir          /var/lib/pkg/pkg|https://svetlanux.github.io/packages/pkg/ 
``
