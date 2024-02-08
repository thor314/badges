# playing with badges from shields.io

## experiments:
### static links
static link two-tone:
![](https://img.shields.io/badge/label-message-8AFAE2)

static link one-tone (with spaces):
![](https://img.shields.io/badge/just_the%20message-8AAAE2)

### styling
![flat](media/flat.svg)
![flat-square](media/flat-square.svg)
![plastic](media/plastic.svg)
![for-the-badge](media/for-the-badge.svg)
![social](media/social.svg)

```fish
for l in flat flat-square plastic for-the-badge social
  badge $l msg :8AFAE2 @$l > $l.svg
end
```

### logo
https://shields.io/docs/logos
- they host a few icons: https://github.com/badges/shields/tree/master/logo
- find more: https://simpleicons.org/?q=github
- static link: ![](https://img.shields.io/npm/v/npm.svg?logo=npm)
- my svg logo: ![](media/hammer.svg)

- test: ![Badge](https://img.shields.io/badge/LEFT_TEXT-RIGHT_TEXT-blue?style=flat&logo=media/hammer.svg&logoColor=grey)
- test no collor: ![Badge](https://img.shields.io/badge/LEFT_TEXT-RIGHT_TEXT-blue?style=flat&logo=media/hammer.svg)

Making an svg from webp:
```fish
convert a.webp a.png
inkscape a.png --export-type=svg
```

## install and use
```sh
npm i -g badge-maker
badge tk-label tk-message :blue @flat > tk-badge.svg
# then put ![label](tk-badge.svg) in a readme
```
