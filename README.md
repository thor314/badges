# playing with badges from shields.io
My faves:
- ![](https://img.shields.io/badge/made_by-cryptograthor-pink?style=for_the_badge&logo=tina&logoColor=pink)
- ![](https://img.shields.io/badge/made_by-cryptograthor-pink?style=flat&logo=tina&logoColor=pink)
- ![](https://img.shields.io/badge/made_by-cryptograthor-hotpink?style=flat&logo=stackblitz&logoColor=hotpink)

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
- svg - undertale: ![](https://img.shields.io/badge/just-msg-blue?style=flat&logo=undertale)

> Any custom logo can be passed in a URL parameter by base64 encoding it.
now try to include it in a badge: nah, my svg's are too huge, just re-use one of these:
- undertale: ![](https://img.shields.io/badge/just-msg-blue?style=flat&logo=undertale)
- rust![](https://img.shields.io/badge/just-msg-blue?style=flat&logo=rust)
- toml ![](https://img.shields.io/badge/just-msg-blue?style=flat&logo=toml)
- tina ![](https://img.shields.io/badge/just-msg-blue?style=flat&logo=tina)
- gamejolt ![](https://img.shields.io/badge/just-msg-blue?style=flat&logo=gamejolt)
- lighting ![](https://img.shields.io/badge/just-msg-blue?style=flat&logo=lightning)
- stackblitz ![](https://img.shields.io/badge/just-msg-blue?style=flat&logo=stackblitz)
- etcd ![](https://img.shields.io/badge/just-msg-blue?style=flat&logo=etcd)
- ethereum ![](https://img.shields.io/badge/just-msg-blue?style=flat&logo=ethereum)
- org ![](https://img.shields.io/badge/just-msg-blue?style=flat&logo=org)

styling
- tina ![](https://img.shields.io/badge/just-msg-blue?style=flat-square&logo=tina)
- tina ![](https://img.shields.io/badge/just-msg-blue?style=plastic&logo=tina)
- tina ![](https://img.shields.io/badge/just-msg-blue?style=flat-square&logo=tina&logoColor=grey)
- tina ![](https://img.shields.io/badge/just-msg-blue?style=flat-square&logo=tina&logoColor=pink)

fails:
- test: ![Badge](https://img.shields.io/badge/LEFT_TEXT-RIGHT_TEXT-blue?style=flat&logo=./media/hammer.svg&logoColor=grey)
- test no color: ![Badge](https://img.shields.io/badge/LEFT_TEXT-RIGHT_TEXT-blue?style=flat&logo=./media/hammer.svg)
- test: ![Badge](https://img.shields.io/badge/LEFT_TEXT-RIGHT_TEXT-blue?style=flat&logo=https://github.com/thor314/badges/media/hammer.svg&logoColor=grey)
- test: ![Badge](https://img.shields.io/badge/LEFT_TEXT-RIGHT_TEXT-blue?style=flat&logo=https://github.com/thor314/badges/media/hammer.svg)

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
