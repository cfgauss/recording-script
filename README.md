# README.md - `recording-script`

## To install on Mac:

0. Install `gsed`, `gawk` and `core-utils` using `brew`  (Because the tools provided by Apple are not GNU).
1. Clone the `https://github.com/mboisson/recording-script` repository, and add it to your PATH.

To use :

```
recordsession.sh git@github.com:<user>/<repo>.git <filename> [delay]
```

For example, the above .html was recorded using the command

```
recordsession.sh git@github.com:mboisson/testing.git bash_lesson 10
```

* The script pushes from the `gh-pages` branch, and creates one if it does not exist. It has been used with [Software Carpentry](http://software-carpentry.org/) event pages.
* The delay is in seconds, and there is a default delay of 60 seconds between each sync.
* This script assumes that your github is configured to use SSH keys.
* The script uses a modified version of `ansi2html.sh`, which can be obtained
  from
  [`http://github.com/pixelb/scripts/commits/master/scripts/ansi2html.sh`](`http://github.com/pixelb/scripts/commits/master/scripts/ansi2html.sh`)

OWM addendum:

For me to save keystrokes in a bash session:

0. Make a repository on GitHub. This could be the SWC repository I'm teaching
from. E.g. testScript
1. Make sure that the current directory is on the `PATH`:
```
export PATH=.:$PATH
```
2. To save keystrokes for a bash session with a 10-second delay:
```
recordsession.sh git@github.com:cfgauss/testScript.git bash_lesson 10
```
3. Type into shell as normal. The history will sync every 10 seconds.
4. Have students reference the URL: `cfgauss.github.io/testScript/bash_lesson.html`
