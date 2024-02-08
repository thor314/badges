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
end
```

### logo
https://shields.io/docs/logos
- they host a few icons: https://github.com/badges/shields/tree/master/logo
- find more: https://simpleicons.org/?q=github
- static link: ![](https://img.shields.io/npm/v/npm.svg?logo=npm)
- custom icon: ![](https://img.shields.io/badge/play-station-blue.svg?logo=data:image/svg%2bxml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZlcnNpb249IjEiIHdpZHRoPSI2MDAiIGhlaWdodD0iNjAwIj48cGF0aCBkPSJNMTI5IDExMWMtNTUgNC05MyA2Ni05MyA3OEwwIDM5OGMtMiA3MCAzNiA5MiA2OSA5MWgxYzc5IDAgODctNTcgMTMwLTEyOGgyMDFjNDMgNzEgNTAgMTI4IDEyOSAxMjhoMWMzMyAxIDcxLTIxIDY5LTkxbC0zNi0yMDljMC0xMi00MC03OC05OC03OGgtMTBjLTYzIDAtOTIgMzUtOTIgNDJIMjM2YzAtNy0yOS00Mi05Mi00MmgtMTV6IiBmaWxsPSIjZmZmIi8+PC9zdmc+)


![](<svg role="img" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><title>GitHub Sponsors</title><path d="M17.625 1.499c-2.32 0-4.354 1.203-5.625 3.03-1.271-1.827-3.305-3.03-5.625-3.03C3.129 1.499 0 4.253 0 8.249c0 4.275 3.068 7.847 5.828 10.227a33.14 33.14 0 0 0 5.616 3.876l.028.017.008.003-.001.003c.163.085.342.126.521.125.179.001.358-.041.521-.125l-.001-.003.008-.003.028-.017a33.14 33.14 0 0 0 5.616-3.876C20.932 16.096 24 12.524 24 8.249c0-3.996-3.129-6.75-6.375-6.75zm-.919 15.275a30.766 30.766 0 0 1-4.703 3.316l-.004-.002-.004.002a30.955 30.955 0 0 1-4.703-3.316c-2.677-2.307-5.047-5.298-5.047-8.523 0-2.754 2.121-4.5 4.125-4.5 2.06 0 3.914 1.479 4.544 3.684.143.495.596.797 1.086.796.49.001.943-.302 1.085-.796.63-2.205 2.484-3.684 4.544-3.684 2.004 0 4.125 1.746 4.125 4.5 0 3.225-2.37 6.216-5.048 8.523z"/></svg>)

## install and use
```sh
npm i -g badge-maker
badge tk-label tk-message :blue @flat > tk-badge.svg
# then put ![label](tk-badge.svg) in a readme
```
