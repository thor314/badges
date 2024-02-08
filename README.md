# playing with badges from shields.io
My faves:
- ![](https://img.shields.io/badge/made_by-cryptograthor-pink?style=for-the-badge&logo=tina&logoColor=pink)
- ![](https://img.shields.io/badge/made_by-cryptograthor-pink?style=flat&logo=tina&logoColor=pink)
- ![](https://img.shields.io/badge/made_by-cryptograthor-hotpink?style=flat&logo=stackblitz&logoColor=hotpink)
- ![](https://img.shields.io/badge/made_by-cryptograthor-hotpink?style=flat&logo=undertale&logoColor=hotpink)
- ![](https://img.shields.io/badge/made_by_cryptograthor-white?style=flat&logo=undertale&logoColor=hotpink)
- ![](https://img.shields.io/badge/made_by_cryptograthor-grey?style=flat&logo=undertale&logoColor=hotpink)
- ![](https://img.shields.io/badge/made_by_cryptograthor-grey?style=flat&logo=undertale&logoColor=hotpink)
- ![](https://img.shields.io/badge/made_by_cryptograthor-black?style=flat&logo=undertale&logoColor=hotpink)

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

## couldn't get my own logos to render unfortunately

their example has a reasonably short svg:
- https://img.shields.io/badge/play-station-blue.svg?logo=data:image/svg%2bxml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZlcnNpb249IjEiIHdpZHRoPSI2MDAiIGhlaWdodD0iNjAwIj48cGF0aCBkPSJNMTI5IDExMWMtNTUgNC05MyA2Ni05MyA3OEwwIDM5OGMtMiA3MCAzNiA5MiA2OSA5MWgxYzc5IDAgODctNTcgMTMwLTEyOGgyMDFjNDMgNzEgNTAgMTI4IDEyOSAxMjhoMWMzMyAxIDcxLTIxIDY5LTkxbC0zNi0yMDljMC0xMi00MC03OC05OC03OGgtMTBjLTYzIDAtOTIgMzUtOTIgNDJIMjM2YzAtNy0yOS00Mi05Mi00MmgtMTV6IiBmaWxsPSIjZmZmIi8+PC9zdmc+

my hacky svg from chatGPT is huge, so that's probably a non-starter.

can we path link? nope
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
