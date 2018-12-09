# react-simple-matchmedia
React component used for matching media queries.
(It doesn't exists in DOM if media query is not matched)
Under the hood it uses browser's `window.matchMedia`.


[![](https://img.shields.io/circleci/project/github/RedSparr0w/node-csgo-parser.svg)](https://circleci.com/gh/egdbear/react-simple-matchmedia)
[![install size](https://packagephobia.now.sh/badge?p=react-simple-matchmedia)](https://packagephobia.now.sh/result?p=react-simple-matchmedia)
[![](https://img.shields.io/packagecontrol/dm/GitGutter.svg)](https://www.npmjs.com/package/react-simple-matchmedia)



### Install

```sh
$ yarn add react-simple-matchmedia
```

### Usage

[![Edit 1z02pl6xqq](https://codesandbox.io/static/img/play-codesandbox.svg)](https://codesandbox.io/s/1z02pl6xqq)


#### Pre-defined media queries:

| media | value |
| ------ | ------ |
| phone | (min-width: 320px) and (max-width: 568px) |
| tablet | (min-width : 768px) and (max-width : 1024px) |
| desktop | (min-width : 1224px) |


#### With pre-defined query:
```
import SimpleMatchMedia from 'react-simple-matchmedia'

 // somewhere in render

<SimpleMatchMedia media="phone">
  I am only able to be visible and rendered in DOM on phone screen!
</SimpleMatchMedia>
```
#### With custom query:

```
<SimpleMatchMedia media="(min-width: 200px) and (max-width: 600px)">
  I am only able to be visible and rendered in DOM on screen with query of (min-width: 200px) and (max-width: 600px)!
</SimpleMatchMedia>
```


#### With render prop:

```
<SimpleMatchMedia media="(min-width: 600px)">
    {matched =>
      matched ? (
        I am matching (min-width: 600px)
      ) : (
        "Warning. I am not maching (min-width: 600px)"
      )
    }
</SimpleMatchMedia>
```

###

Enjoy and have fun!
