# Search

> A search bar with a searching result list.

----------

## Import

```javascript
import { Search } from 'mint-ui';

Vue.component(Search.name, Search);
```

## Examples

Basic usage

```html
<mt-search :value.sync="value"></mt-search>
```

Configure texts

```html
<mt-search
  :value.sync="value"
  cancel-text="取消"
  placeholder="搜索">
</mt-search>
```

Display searching result
```html
<mt-search :value.sync="value" :result.sync="result"></mt-search>
```

Custom the display of the searching result list
```html
<mt-search :value.sync="value">
  <mt-cell
    v-for="item in result"
    :title="item.title"
    :value="item.value">
  </mt-cell>
</mt-search>
```



## API

| option | description | type | acceptable values | default |
|------|-------|---------|-------|--------|
| value | search input  | String | |   |
|cancel-text | text of the cancel button | String | | '取消' |
|placeholder | place holder for the search bar  | String | | '搜索' |
| result | the searching result list | Array | | |

## Slot

| name | description |
|------|--------|
| - | custom searching result list|
