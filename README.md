# npm-sum
Show brief summary of package information registered on npm.

``` shell
$ npm i -g npm-sum
```

## Why and What
`npm view`  (or `show`, `info`, `v`) outputs huge raw JSON which contains all information of the package,
but, for a human, it's not easy to read and find what one wants to know.

``` shell
$ npm view npm
{
  "name": "npm",
  "description": "a package manager for JavaScript",
  "dist-tags": {
    "latest": "4.0.2",
    "next": "4.0.3",
    "latest-2": "2.15.11",
    "v3.x-latest": "3.10.9",
    "3.x-latest": "3.10.9",
    "3.x-next": "3.10.10",
    "v3.x-next": "3.10.10",
    "next-2": "2.15.11",
    "latest-1": "1.4.29",
    "lts": "2.15.11",
    "latest-3": "3.10.10",
    "next-3": "3.10.10"
  },
  "versions": [
    "1.1.25",
    "1.1.70",
    "1.1.71",
    "1.2.19",
    "1.2.20",
    "1.2.21",
    ... (more than 1000 lines)
}
```

`npm-sum` outputs a summary of the information which includes only the most important ones (as I think).

``` shell
$ npm-sum npm
  Name        : npm
  Version     : 4.0.2 (2016-11-4 11:38:17)
  Homepage    : https://docs.npmjs.com/
  Author      : Isaac Z. Schlueter <i@izs.me> (http://blog.izs.me)
  License     : Artistic-2.0
  Description : a package manager for JavaScript
  Keywords    : install, modules, package manager, package.json
  Tags        :
    3.x-latest  : 3.10.9 (2016-10-7 13:38:58)
    3.x-next    : 3.10.10 (2016-11-5 10:18:12)
    latest      : 4.0.2 (2016-11-4 11:38:17)
    latest-1    : 1.4.29 (2015-10-30 10:52:42)
    latest-2    : 2.15.11 (2016-9-9 11:52:01)
    latest-3    : 3.10.10 (2016-11-5 10:18:12)
    lts         : 2.15.11 (2016-9-9 11:52:01)
    next        : 4.0.3 (2016-11-18 08:28:08)
    next-2      : 2.15.11 (2016-9-9 11:52:01)
    next-3      : 3.10.10 (2016-11-5 10:18:12)
    v3.x-latest : 3.10.9 (2016-10-7 13:38:58)
    v3.x-next   : 3.10.10 (2016-11-5 10:18:12)
  Binaries    : npm
```

## How to use
Just like `npm view`.

```
$ npm-sum [<@scope>/]<name>[@<version>]
```

It executes `npm` as a child process to fetch package information from the registry, and summarizes it into a human readable format.

## License
[MIT License](http://opensource.org/licenses/mit-license.php)

## Author
Susisu ([GitHub](https://github.com/susisu), [Twitter](https://twitter.com/susisu2413))
