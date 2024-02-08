# playing with badges from shields.io

## experiments:
### static links
static link two-tone:
![](https://img.shields.io/badge/label-message-8AFAE2)

static link one-tone (with spaces):
![](https://img.shields.io/badge/just_the%20message-8AAAE2)

### styling
![flat](flat.svg)
![flat-square](flat-square.svg)
![plastic](plastic.svg)
![for-the-badge](for-the-badge.svg)
![social](social.svg)

```fish
for l in flat flat-square plastic for-the-badge social
  badge $l msg :8AFAE2 @$l > $l.svg

```

## install and use
```sh
npm i -g badge-maker
badge tk-label tk-message :blue @flat > tk-badge.svg
# then put ![label](tk-badge.svg) in a readme
```
