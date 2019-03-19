# Another very simple sample project structure to manage a Purescript web app

## Tools used

- [`spago`][spago]
- [`modd`][modd]
- [`devd`][devd]
- [`sass`][sass]


## Description

Although `spago` has just released a new `--watch` feature, the combination of `modd`and `devd` provides a more flexible solution.

The basic `modd` configuration provided in this projects takes care of the following actions:

 - run `spago install` whenever the `spago.dhall` file changes
 - run `spago bundle …` when any `.purs` files change
 - copy `html` resources into `target` folder whenever they change
 - process `scss` files whenever they changes
 - run `devd` and trigger a live-reload of the connected browsers whenever some of the source files is changed (the live-reload is actually triggered by changes into the `target` folder, that is caused by the processing of some files in the `src` folder).

The current solution still lacks an option to do the final packaging of all the resources when ready to release a new version of the app, but I'll think to this once I have written some actual Purescript code worth sharing. :)


[modd]: https://github.com/cortesi/modd
[devd]: https://github.com/cortesi/devd
[spago]: https://github.com/spacchetti/spago
[sass]: https://sass-lang.com/install
