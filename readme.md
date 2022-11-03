# Autocomplete for Bootstrap 4/5

[![NPM](https://nodei.co/npm/bootstrap5-autocomplete.png?mini=true)](https://nodei.co/npm/bootstrap5-autocomplete/)
[![Downloads](https://img.shields.io/npm/dt/bootstrap5-autocomplete.svg)](https://www.npmjs.com/package/bootstrap5-autocomplete)

## How to use

An ES6 autocomplete for your `input` using standards Bootstrap 5 (and 4) styles.

No additional CSS needed!

```js
import Autocomplete from "./autocomplete.js";
Autocomplete.init();
```

## Server side support

You can also use options provided by the server. This script expects a json response that is an array or an object with the data key containing an array.

Simply set `data-server` where your endpoint is located. It should provide an array of value/label objects. The suggestions will be populated upon init except if `data-live-server` is set, in which case, it will be populated on type. A ?query= parameter is passed along with the current value of the searchInput.

## Options

Options can be either passed to the constructor (eg: optionName) or in data-option-name format.

| Name                 | Type                                      | Description                                                  |
| -------------------- | ----------------------------------------- | ------------------------------------------------------------ |
| suggestionsThreshold | <code>Number</code>                       | Number of chars required to show suggestions                 |
| maximumItems         | <code>Number</code>                       | Maximum number of items to display                           |
| autoselectFirst      | <code>Boolean</code>                      | Always select the first item                                 |
| highlightTyped       | <code>Boolean</code>                      | Highlight matched part of the label                          |
| fullWidth            | <code>Boolean</code>                      | Match the width on the input field                           |
| labelField           | <code>String</code>                       | Key for the label                                            |
| valueField           | <code>String</code>                       | Key for the value                                            |
| items                | <code>Array</code> \| <code>Object</code> | An array of label/value objects or an object with key/values |
| datalist             | <code>String</code>                       | The id of the source datalist                                |
| server               | <code>String</code>                       | Endpoint for data provider                                   |
| serverParams         | <code>String</code>                       | Parameters to pass along to the server                       |
| liveServer           | <code>Boolean</code>                      | Should the endpoint be called each time on input             |
| noCache              | <code>Boolean</code>                      | Prevent caching by appending a timestamp                     |
| debounceTime         | <code>Boolean</code>                      | Debounce time for live server                                |
| onRenderItem         | <code>function</code>                     | Callback function that returns the label                     |
| onSelectItem         | <code>function</code>                     | Callback function to call on selection                       |
| onServerResponse     | <code>function</code>                     | Callback function to process server response                 |

## Tips

- Use arrow down to show dropdown (and arrow up to hide it)
- If you have a really long list of options, a scrollbar will be used
- Access instance on a given element with Autocomplete.getInstance(myEl)

## Demo

https://codepen.io/lekoalabe/pen/MWXydNQ or see demo.html

## Browser supports

Modern browsers (edge, chrome, firefox, safari... not IE11). [Add a warning if necessary](https://github.com/lekoala/nomodule-browser-warning.js/).

## Also check out

- [Bootstrap 5 Tags](https://github.com/lekoala/bootstrap5-tags): tags input for bootstrap
- [Admini](https://github.com/lekoala/admini): the minimalistic bootstrap 5 admin panel
