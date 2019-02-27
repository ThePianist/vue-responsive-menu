# vue-responsive-menu
Easily customizable responsive menu for VueJS 2.x

## Features

- [x] Custom logo with style options
- [x] Custom items with style options
- [ ] Background style options
- [ ] Add shadow to the menu, built-in, but optionally
- [ ] Horizontal options
- [ ] Menu slides from left or right
- [ ] Different types or menu triggers

## Setup

[npm](https://npmjs.com) or [yarn](https://yarnpkg.com) install will come soon.

```js
import VueResponsiveMenu from "@/components/VueResponsiveMenu.vue";
```
```js
export default {
  components: {
      VueResponsiveMenu
    }
}
```
```html
<vue-responsive-menu :options="menuOptions"/>
```

## Options

### Props
| Props       | Type          | Default  | Description  |
| ----------- |:--------------| ---------|--------------|
| logo.src   | String        | null | Set logo source, example: 'http://example.com/logo.png' or '@/assets/images/logo.png' |
| logo.style  | Object        | null   | The style of the logo. |
| logo.class  | String        | null   | The class of the logo. |
| items.data  | Array of Objects        | null   | The menu items. [More details](#items-data) about the objects. |
test
| items.style  | Object        | null   | The style of the menu items. |
| items.class  | String        | null   | The class of the menu items. |

### Slots
| Slot       | Description  |
| ----------- |--------------|
| items   | By default menu items are Vue routes with <a> tags, if you want to change it and create on your own, use this slot. |

---------

## items-data

### The item object
| Props       | Type          | Description  |
| ----------- |:--------------| --------------|
| id   | Number        | Must be a unique ID |
| label   | String        | The name of the menu item that will be displayed |
| to   | String        | The router path associated with the menu item |

Example:
```js
items: {
    data: [{
        id: 1,
        label: "Home",
        to: "/"
      },
      {
        id: 2,
        label: "Blog",
        to: "/blog"
      }
    }
```
