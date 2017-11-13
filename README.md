# ng-data-picker  <sup>[![Version Badge](http://versionbadg.es/hiyali/ng-data-picker.svg)](https://npmjs.com/package/ng-data-picker)</sup>
🏄🏼 A Data Picker for Angular 4

[![npm package](https://img.shields.io/npm/v/ng-data-picker.svg)](https://npmjs.com/package/ng-data-picker)
[![travis build](https://img.shields.io/travis/hiyali/ng-data-picker/master.svg)](https://travis-ci.org/hiyali/ng-data-picker)
[![NPM downloads](http://img.shields.io/npm/dt/ng-data-picker.svg)](https://npmjs.org/package/ng-data-picker)
![JS gzip size](http://img.badgesize.io/hiyali/ng-data-picker/gh-pages/dist/smooth-picker.js.svg?compression=gzip&label=gzip:%20JS)
![CSS gzip size](http://img.badgesize.io/hiyali/ng-data-picker/gh-pages/dist/css/style.css.svg?compression=gzip&label=gzip:%20CSS)
[![CircleCI](https://circleci.com/gh/hiyali/ng-data-picker/tree/master.svg?style=shield)](https://circleci.com/gh/hiyali/ng-data-picker/tree/master)

[![NPM Description](https://nodei.co/npm/ng-data-picker.png?downloads=true&stars=true)](https://npmjs.org/package/ng-data-picker)

> Let's more easily select some data on the touch screen device, such as time / city / gender / seat number / product / ...

## Take a look

![Screen shot](https://raw.githubusercontent.com/hiyali/ng-data-picker/gh-pages/assets/smooth-picker-screenshot.png "screenshot")

![Screen record](https://raw.githubusercontent.com/hiyali/ng-data-picker/gh-pages/assets/smooth-picker-screen-record.gif "screen record")

## Install

```shell
yarn add ng-data-picker
```

## Usage

TODO

### Quick look

```javascript
// import and use in your app.module
import { DataPickerComponent } from 'ng-data-picker'

@NgModule({
  ...
  declarations: [
    DataPickerComponent
  ]
  ...
})
// in your template
<ng-data-picker [data]="data" [change]="change" />
```

## props

| name                       | type       |  default      | explain                          |
| :------------------------- | :--------- | :------------ | :------------------------------- |
| `change`                   | `Function` | (gIndex, iIndex) => {} | Callback after data current index changed, pass two arguments, group index `gIndex` and item index `iIndex` |
| `data`                     | `Array`    | []            | SmoothPicker initial data        |
| `data[i].currentIndex`     | `Number`   | 0             | Current index of this group's list |
| `data[i].weight`             | `Number`   | 1             | Group weights in parent width `1..12` |
| `data[i].list`             | `Array`    | -             | List of the group                |
| `data[i].list[j]`          | `String` or `Object` | -   | Item in the list of group, use `value` key when it is a object item |
| `data[i].onClick`          | `Function` | -             | Click event on the middle layer of this group, pass two arguments, this group index `gIndex` and selected index `iIndex` of this group |
| `data[i].textAlign`        | `String`   | -             | `left` `center` or `right` in item block |
| `data[i].className`        | `String`   | -             | Your custom class name for this group |
| `data[i].divider`          | `Boolean`  | false         | If it is true, then `onClick` `list` `currentIndex` will be not used |
| `data[i].text`             | `String`   | -             | Just used when `divider` is true |

## Instance methods

| name                       | type       | explain                          |
| :------------------------- | :--------- | :------------------------------- |
| `setGroupData`             | `Function` | Dynamically set a group data with two arguments `(gIndex, gData)`, group index and group data (see props `data[i]`) |
| `getCurrentIndexList`      | `Function` | Return a `Array` of the groups current index list (has divider current index, and it is default to `0`) |

## Development

```shell
npm run dev # development
npm run build # build
```

## Examples

> See branch gh-pages.

## Any problem?

> Please let me know.
* [Open a new issue for this repo](https://github.com/hiyali/ng-data-picker/issues)
* [Send a Email to: hiyali920@gmail.com](mailto:hiyali920@gmail.com)

## Donate

🌚 [A github star ⍟](https://github.com/hiyali/ng-data-picker)

## License

MIT

