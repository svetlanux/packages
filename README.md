
## Releases and stages

Stages - is a full-featured filesystems that could be installed on a drive.
The releases section of this repository contains stages for download.

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
```

## Security

I don't trust thirdparties, therefore I highly recommend to check `sha256` sums of all files as well as gpg signatures.
Every folder has its own `files.sum.gpg` file that you have to use for verification using:

```
gpg --verify files.sum.gpg
```

Just compare its fingerprint with this:
`746C80706C9696F326BCE993D901EF18FA491208`

Then extract it using:
```
gpg --decrypt files.sum.gpg > files.sum
```

It will override exsting `files.sum` with signed one , and then, as usual run filesystem check.

```
sha256sum -c files.sum
```

And watch the sequence of `OK`'s.
And remember - don't trust github, never, it belongs to m$.
