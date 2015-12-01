# eslint-config-bgw

This is a [sharable config][] for ESLint to allow me to keep a consistent linter
configuration between my personal projects.

It's based on, but diverges from [Facebook's ESLint configuration][fbjs], which
I helped develop. Mostly, it's stricter.

[sharable config]: http://eslint.org/docs/developer-guide/shareable-configs
[fbjs]: https://github.com/facebook/fbjs/blob/master/scripts/eslint/.eslintrc

## Adding to a project

```sh
$ npm i --save-dev eslint eslint-config-bgw
$ echo 'extends: bgw' >> .eslintrc
```

## Notes on SemVer

This project will follow Semantic Versioning. To quote the [specification]:

1. MAJOR version when you make incompatible API changes,
2. MINOR version when you add functionality in a backwards-compatible manner,
   and
3. PATCH version when you make backwards-compatible bug fixes.

Because tightening the configuration (and therefore disallowing code that was
previously valid) is potentially breaking, except in the case of warnings, I
will increment the MAJOR version every time I tighten the configuration. If I
loosen the configuration, I'll increment the MINOR version.

This means that I expect the version number to grow quickly. Version numbers say
nothing about the maturity of a project.

[specification]: http://semver.org/
